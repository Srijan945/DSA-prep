# Bellman–Ford Algorithm

## Overview
Bellman–Ford computes shortest paths from a single source vertex to all other vertices in a weighted directed graph. It supports negative edge weights and can detect negative-weight cycles reachable from the source.

## When to use
- Graphs with negative edge weights (Dijkstra cannot handle negative weights).
- Need detection of negative-weight cycles.

## Algorithm (high level)
1. Initialize distances: dist[source] = 0, all others = +∞.
2. Relax all edges V−1 times (V = number of vertices).
3. Optionally, run one more relaxation pass: if any distance improves, a negative-weight cycle exists.

## Complexity
- Time: O(V * E)
- Space: O(V + E) (depending on representation)

## Java implementation

The implementation below uses an edge-list representation. It relaxes all edges V-1 times and reports distances or a negative cycle.

```java
// filepath: /Users/srijansaini/Desktop/DSA-prep/bellman-ford.md (Java snippet)
import java.util.Arrays;

public class BellmanFord {
    static class Edge {
        int u, v;
        int w;
        Edge(int u, int v, int w) { this.u = u; this.v = v; this.w = w; }
    }

    int V; // number of vertices
    Edge[] edges;

    public BellmanFord(int V, Edge[] edges) {
        this.V = V;
        this.edges = edges;
    }

    // Returns distances array or null if a negative-weight cycle is detected.
    public long[] shortestPaths(int src) {
        long INF = Long.MAX_VALUE / 4;
        long[] dist = new long[V];
        Arrays.fill(dist, INF);
        dist[src] = 0;

        // Relax edges V-1 times
        for (int i = 0; i < V - 1; i++) {
            boolean updated = false;
            for (Edge e : edges) {
                if (dist[e.u] != INF && dist[e.u] + e.w < dist[e.v]) {
                    dist[e.v] = dist[e.u] + e.w;
                    updated = true;
                }
            }
            if (!updated) break; // early exit if no changes
        }

        // Check for negative-weight cycles
        for (Edge e : edges) {
            if (dist[e.u] != INF && dist[e.u] + e.w < dist[e.v]) {
                return null; // negative cycle detected
            }
        }
        return dist;
    }

    // Example usage
    public static void main(String[] args) {
        // Graph:
        // 0 -> 1 (5), 0 -> 2 (4)
        // 1 -> 3 (3), 2 -> 1 (6), 3 -> 2 (-10)
        Edge[] edges = new Edge[] {
            new Edge(0, 1, 5),
            new Edge(0, 2, 4),
            new Edge(1, 3, 3),
            new Edge(2, 1, 6),
            new Edge(3, 2, -10)
        };
        int V = 4;
        BellmanFord bf = new BellmanFord(V, edges);
        long[] dist = bf.shortestPaths(0);
        if (dist == null) {
            System.out.println("Graph contains a negative-weight cycle reachable from source.");
        } else {
            for (int i = 0; i < V; i++) {
                System.out.printf("dist[%d] = %s%n", i, dist[i] == Long.MAX_VALUE / 4 ? "INF" : Long.toString(dist[i]));
            }
        }
    }
}
```

## Notes
- Use long for distances if weights or path sums may exceed int.
- For dense graphs, other representations (adjacency matrix) may be used; edge list is simple and direct for Bellman–Ford.
