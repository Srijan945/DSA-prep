# Dijkstra's Algorithm — Summary, Use-cases and Optimal Java Code

## What it solves
Finds shortest paths from a single source to all nodes in a weighted graph with non-negative edge weights.

## Common use-cases
- Shortest path in road networks (GPS, routing).
- Network latency minimization (e.g., packet routing, Network Delay Time).
- Resource-cost minimization where costs are non-negative.
- As a subroutine in problems transforming weights or optimizing maximum-edge along path (minimax).
- Counting or enumerating shortest paths (with slight modification).

## Complexity
- Time: O((V + E) log V) using adjacency lists + binary heap (priority queue), often simplified to O(E log V).
- Space: O(V + E) for the graph + O(V) for distances and heap.

## Optimal Java implementation (adjacency list + min-heap)
- Uses List<List<int[]>> for graph where int[]{to, weight}.
- Distances stored in long[] to avoid overflow for sums.

```java
// Example usage is shown in comments below.
import java.util.*;

public class Dijkstra {
    // Returns distances from src to all nodes (0..n-1). Unreachable distances = Long.MAX_VALUE.
    public static long[] dijkstra(int n, List<List<int[]>> adj, int src) {
        long[] dist = new long[n];
        Arrays.fill(dist, Long.MAX_VALUE);
        dist[src] = 0L;

        PriorityQueue<long[]> pq = new PriorityQueue<>(Comparator.comparingLong(a -> a[0]));
        pq.add(new long[]{0L, src}); // {distance, node}

        while (!pq.isEmpty()) {
            long[] cur = pq.poll();
            long d = cur[0];
            int u = (int) cur[1];
            if (d != dist[u]) continue; // stale entry

            for (int[] e : adj.get(u)) {
                int v = e[0];
                int w = e[1];
                long nd = d + w;
                if (nd < dist[v]) {
                    dist[v] = nd;
                    pq.add(new long[]{nd, v});
                }
            }
        }
        return dist;
    }

    // Example to build graph:
    // int n = number_of_nodes;
    // List<List<int[]>> adj = new ArrayList<>();
    // for (int i = 0; i < n; ++i) adj.add(new ArrayList<>());
    // // add directed edge u->v with weight w:
    // adj.get(u).add(new int[]{v, w});
    // long[] dist = dijkstra(n, adj, source);
    // if (dist[target] == Long.MAX_VALUE) -> unreachable
}
```

Notes:
- Use long for distances if weights or path sums can exceed Integer.MAX_VALUE.
- For dense graphs, other implementations (e.g., Fibonacci heap theoretical improvement) exist but are rarely used in practice.

## 5 LeetCode problems where Dijkstra or its variants apply
- 743. Network Delay Time — compute time for signal to reach all nodes (classic Dijkstra).
- 787. Cheapest Flights Within K Stops — can use Dijkstra with state (node, stops) or modified relaxations.
- 1631. Path With Minimum Effort — apply Dijkstra minimizing the maximum edge on path (minimax Dijkstra).
- 778. Swim in Rising Water — Dijkstra (minimize maximum height along path) or binary search + BFS.
- 1976. Number of Ways to Arrive at Destination — run Dijkstra to get shortest distances and count ways in the relax step.

Each of the above can be solved by adapting Dijkstra (change state, cost aggregation, or maintain extra info like counts).

