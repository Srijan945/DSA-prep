# Topological Sort

## What is Topological Sort?
Topological sort of a directed acyclic graph (DAG) is a linear ordering of its vertices such that for every directed edge u -> v, vertex u comes before v in the ordering. A topological ordering is possible only if the graph has no directed cycles (i.e., it is a DAG).

## When to use
- Scheduling tasks with dependencies (build systems, job scheduling).
- Resolving symbol or package dependencies.
- Ordering cells in spreadsheet computations with dependency graphs.
- Determining evaluation order in compiler phases (e.g., statement dependencies).

## Intuition (DFS-based)
Perform a DFS and record vertices in the order of completion (post-order). If we push each node onto a stack when its DFS finishes, the stack ends up with vertices in reverse topological order. Popping the stack yields a valid topological ordering.

Step-by-step (DFS approach):
1. Mark all vertices as unvisited.
2. For each unvisited vertex, run DFS:
   - Mark current vertex visited.
   - Recurse on all neighbors.
   - After exploring neighbors, add the vertex to a stack (or prepend to a list).
3. After DFS finishes for all vertices, popping from the stack (or using the list order) gives a topological sort.

Note: If a back edge to a currently visiting node is found, the graph contains a cycle and topological sort is impossible.

## Complexity
- Time: O(V + E) — each vertex and edge is explored once.
- Space: O(V) for visited array and stack (plus recursion stack up to O(V)).

## Example
Graph (edges):
- 5 -> 2, 5 -> 0
- 4 -> 0, 4 -> 1
- 2 -> 3
- 3 -> 1

One possible topological ordering: 5, 4, 2, 3, 1, 0
(There can be multiple valid orders.)

Manual trace (brief):
- Start DFS at 5: visit 2 -> visit 3 -> visit 1 -> finish 1, finish 3, finish 2; push 2,3,1 accordingly.
- Visit 0 later and 4 -> push in finish order; final stack pop yields the order above.

## Use cases / Applications (concise)
- Task/job scheduling with precedence constraints.
- Build systems and package installers.
- Ordering compilation tasks (module dependencies).
- Course prerequisites planning.
- Resolving dependency graphs in data pipelines.

## Java implementation (DFS)

```java
// Java example using adjacency lists
import java.util.*;

public class TopologicalSortDFS {
    // Perform topological sort on a graph with V vertices
    // adj: adjacency list where adj[u] contains all v such that u->v
    public static List<Integer> topologicalSort(int V, List<List<Integer>> adj) {
        boolean[] visited = new boolean[V];
        boolean[] onStack = new boolean[V]; // optional, for cycle detection
        Deque<Integer> stack = new ArrayDeque<>();
        for (int i = 0; i < V; i++) {
            if (!visited[i]) {
                if (!dfs(i, adj, visited, onStack, stack)) {
                    throw new IllegalArgumentException("Graph is not a DAG (contains a cycle)");
                }
            }
        }
        List<Integer> order = new ArrayList<>();
        while (!stack.isEmpty()) order.add(stack.pop());
        return order;
    }

    // returns false if a back edge (cycle) is detected
    private static boolean dfs(int u, List<List<Integer>> adj, boolean[] visited, boolean[] onStack, Deque<Integer> stack) {
        visited[u] = true;
        onStack[u] = true;
        for (int v : adj.get(u)) {
            if (!visited[v]) {
                if (!dfs(v, adj, visited, onStack, stack)) return false;
            } else if (onStack[v]) {
                // Found a back edge -> cycle
                return false;
            }
        }
        onStack[u] = false;
        stack.push(u); // push when finished (post-order)
        return true;
    }

    // Demo main
    public static void main(String[] args) {
        int V = 6;
        List<List<Integer>> adj = new ArrayList<>();
        for (int i = 0; i < V; i++) adj.add(new ArrayList<>());

        // edges: 5->2, 5->0, 4->0, 4->1, 2->3, 3->1
        adj.get(5).add(2);
        adj.get(5).add(0);
        adj.get(4).add(0);
        adj.get(4).add(1);
        adj.get(2).add(3);
        adj.get(3).add(1);

        List<Integer> topo = topologicalSort(V, adj);
        System.out.println("Topological order: " + topo);
    }
}
```

## Notes and alternatives
- Kahn's algorithm (BFS-based using indegrees) is an alternative that is iterative and can detect cycles by counting processed vertices.
- Choose DFS when recursive postorder is natural; choose Kahn's when you need an explicit indegree-driven sequence or want to avoid recursion.

## LeetCode problems using Topological Sort (5 picks)

1. 207. Course Schedule  
   - Use-case: detect if prerequisites contain a cycle. Solve by Kahn's algorithm (BFS with indegrees) or DFS cycle detection.

2. 210. Course Schedule II  
   - Use-case: return a valid ordering of courses (topological order). Use Kahn's algorithm or DFS postorder.

3. 269. Alien Dictionary  
   - Use-case: derive character ordering from sorted words. Build directed graph of precedence and run topo sort; detect cycles for invalid cases.

4. 444. Sequence Reconstruction  
   - Use-case: determine if the original sequence is the unique topological ordering given subsequences. Use indegree-based topo and check uniqueness at each step.

5. 1203. Sort Items by Groups Respecting Dependencies  
   - Use-case: two-level topological sort (items with group constraints). Perform topo on groups then topo within groups (or transform into single graph with group-nodes), detect cycles and produce combined ordering.

