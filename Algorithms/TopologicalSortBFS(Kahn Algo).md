# KHAN's Algorithm

### Kahn's Algorithm is a Breadth-First Search (BFS) based method for topological sorting a Directed Acyclic Graph (DAG). It works by iteratively finding and removing nodes with zero in-degree (no incoming edges)

```java
import java.util.*;

class Solution {
    /* Function to return the topological sorting of given graph */
    public int[] topoSort(int V, List<List<Integer>> adj) {
        // To store the result
        int[] ans = new int[V];

        // To store the In-degrees of nodes
        int[] inDegree = new int[V];

        // Calculating the In-degree of the given graph
        for (int i = 0; i < V; i++) {
            for (int it : adj.get(i)) inDegree[it]++;
        }

        // Queue to facilitate BFS
        Queue<Integer> q = new LinkedList<>();

        // Add the nodes with no in-degree to queue
        for (int i = 0; i < V; i++) {
            if (inDegree[i] == 0) q.add(i);
        }

        int index = 0; // Index to store elements in ans array

        // Until the queue is empty
        while (!q.isEmpty()) {
            // Get the node
            int node = q.poll();

            // Add it to the answer
            ans[index++] = node;

            // Traverse the neighbours
            for (int it : adj.get(node)) {
                // Decrement the in-degree
                inDegree[it]--;

                /* Add the node to queue if 
                its in-degree becomes zero */
                if (inDegree[it] == 0) q.add(it);
            }
        }

        // Return the result
        return ans;
    }
}

class Main {
    public static void main(String[] args) {
        int V = 6;
        
        // Initializing adjacency list with List<List<Integer>>
        List<List<Integer>> adj = new ArrayList<>();
        for (int i = 0; i < V; i++) {
            adj.add(new ArrayList<>());
        }

        // Adding directed edges to the graph
        adj.get(2).add(3);
        adj.get(3).add(1);
        adj.get(4).add(0);
        adj.get(4).add(1);
        adj.get(5).add(0);
        adj.get(5).add(2);

        // Creating an instance of Solution class
        Solution sol = new Solution(); 

        // Calling topoSort function
        int[] ans = sol.topoSort(V, adj);

        // Output the topological order
        System.out.println("The topological sorting of the given graph is:");
        for (int i = 0; i < V; i++) {
            System.out.print(ans[i] + " ");
        }
    }
}
```