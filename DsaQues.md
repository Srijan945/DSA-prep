## LeetCode practice — Questions mapped to the 6-week plan

### Week 1 — Foundations + Patterns (pick 20; focus on templates & from-memory coding)

| Topic | Problem | LC # | Status | Practice Link | Important / Revise | Notes |
|---|---|---:|:---:|---|:---:|---|
| Sliding window | Longest Substring Without Repeating Characters | 3 | [x] Done | https://leetcode.com/problems/longest-substring-without-repeating-characters/ | [ ] | revisit O(n) template HashMap |
| Sliding window | Minimum Window Substring | 76 | [x] Done | https://leetcode.com/problems/minimum-window-substring/ | [ ] | O(n+m) solution Freq Array |
| Sliding window | Sliding Window Maximum | 239 | [x] Done | https://leetcode.com/problems/sliding-window-maximum/ | [ ] | use deque |
| Sliding window | Minimum Size Subarray Sum | 209 | [x] Done | https://leetcode.com/problems/minimum-size-subarray-sum/ | [ ] | two-pointer shrinking window |
| Sliding window | Subarray Product Less Than K | 713 | [x] Done | https://leetcode.com/problems/subarray-product-less-than-k/ | [ ] | handle product and left pointer |
| Prefix / Suffix | Product of Array Except Self | 238 | [x] Done | https://leetcode.com/problems/product-of-array-except-self/ | [ ] | Create prefix and suffix product array |
| Prefix / Suffix | Subarray Sum Equals K | 560 | [x] Done | https://leetcode.com/problems/subarray-sum-equals-k/ | [ ] | Hash Table but check zero condition |
| Prefix / Suffix | Maximum Size Subarray Sum Equals k | 325 | [O] | https://leetcode.com/problems/maximum-size-subarray-sum-equals-k/ | [ ] | Premium leetcode |
| Binary search / search patterns | Binary Search | 704 | [x] Done | https://leetcode.com/problems/binary-search/ | [ ] | |
| Binary search / search patterns | Search in Rotated Sorted Array | 33 | [ ] | https://leetcode.com/problems/search-in-rotated-sorted-array/ | [ ] | |
| Two-pointer | Two Sum II - Input array is sorted | 167 | [x] Done | https://leetcode.com/problems/two-sum-ii-input-array-is-sorted/ | [ ] | O(n) TC O(1) SC |
| Two-pointer | 3Sum | 15 | [x] Done | https://leetcode.com/problems/3sum/ | [ ] | |
| Two-pointer | Container With Most Water | 11 | [x] Done | https://leetcode.com/problems/container-with-most-water/ | [ ] | |
| Two-pointer | Trapping Rain Water | 42 | [x] Done | https://leetcode.com/problems/trapping-rain-water/ | [ ] | good for learning see again |
| Two-pointer | Remove Duplicates from Sorted Array | 26 | [x] Done | https://leetcode.com/problems/remove-duplicates-from-sorted-array/ | [ ] | |
| Two-pointer | Merge Sorted Array | 88 | [ ] | https://leetcode.com/problems/merge-sorted-array/ | [ ] | |
| Two-pointer | Valid Palindrome | 125 | [x] Done | https://leetcode.com/problems/valid-palindrome/ | [ ] | |

### Week 2 — Graphs (BFS/DFS, topo, Dijkstra, 0-1 BFS, grid BFS)

| Topic | Problem | LC # | Status | Practice Link | Important / Revise | Notes |
|---|---|---:|:---:|---|:---:|---|
| Grid BFS / islands | Number of Islands | 200 | [ ] | https://leetcode.com/problems/number-of-islands/ | [ ] | |
| Shortest path / BFS | Word Ladder | 127 | [ ] | https://leetcode.com/problems/word-ladder/ | [ ] | |
| Grid shortest distances | Shortest Distance from All Buildings | 317 | [ ] | https://leetcode.com/problems/shortest-distance-from-all-buildings/ | [ ] | multi-source BFS |
| Graph DP / DFS | Longest Increasing Path in a Matrix | 329 | [ ] | https://leetcode.com/problems/longest-increasing-path-in-a-matrix/ | [ ] | DFS + memo |
| Graph clone | Clone Graph | 133 | [ ] | https://leetcode.com/problems/clone-graph/ | [ ] | BFS/DFS + map |
| Connected components | Number of Connected Components in an Undirected Graph | 323 | [ ] | https://leetcode.com/problems/number-of-connected-components-in-an-undirected-graph/ | [ ] | DSU / DFS |
| Graph coloring | Is Graph Bipartite? | 785 | [ ] | https://leetcode.com/problems/is-graph-bipartite/ | [ ] | BFS coloring |
| Topological sort | Course Schedule | 207 | [ ] | https://leetcode.com/problems/course-schedule/ | [ ] | detect cycle |
| Topological + order | Course Schedule II | 210 | [ ] | https://leetcode.com/problems/course-schedule-ii/ | [ ] | produce ordering |
| Shortest path (Dijkstra) | Network Delay Time | 743 | [ ] | https://leetcode.com/problems/network-delay-time/ | [ ] | Dijkstra |
| Shortest path variants | Cheapest Flights Within K Stops | 787 | [ ] | https://leetcode.com/problems/cheapest-flights-within-k-stops/ | [ ] | BFS / Dijkstra / Bellman-Ford |
| 0-1 BFS style | 01 Matrix | 542 | [ ] | https://leetcode.com/problems/01-matrix/ | [ ] | multi-source BFS |

### Week 3 — DP Basics (1D DP, Grid DP, Knapsack, LIS)

| Topic | Problem | LC # | Status | Practice Link | Important / Revise | Notes |
|---|---|---:|:---:|---|:---:|---|
| 1D DP | Climbing Stairs | 70 | [ ] | https://leetcode.com/problems/climbing-stairs/ | [ ] | simple rec->iter |
| 1D DP | Fibonacci Number | 509 | [ ] | https://leetcode.com/problems/fibonacci-number/ | [ ] | memo/iter |
| 1D DP | Maximum Subarray | 53 | [ ] | https://leetcode.com/problems/maximum-subarray/ | [ ] | Kadane |
| 1D DP | House Robber | 198 | [ ] | https://leetcode.com/problems/house-robber/ | [ ] | DP rolling |
| 1D DP | House Robber II | 213 | [ ] | https://leetcode.com/problems/house-robber-ii/ | [ ] | circular case |
| Grid DP | Unique Paths | 62 | [ ] | https://leetcode.com/problems/unique-paths/ | [ ] | combinatorics/DP |
| Grid DP | Unique Paths II | 63 | [ ] | https://leetcode.com/problems/unique-paths-ii/ | [ ] | obstacles |
| Grid DP | Minimum Path Sum | 64 | [ ] | https://leetcode.com/problems/minimum-path-sum/ | [ ] | DP |
| Grid DP | Maximal Square | 221 | [ ] | https://leetcode.com/problems/maximal-square/ | [ ] | DP |
| Knapsack | Partition Equal Subset Sum | 416 | [ ] | https://leetcode.com/problems/partition-equal-subset-sum/ | [ ] | subset-sum DP |
| Knapsack | Coin Change | 322 | [ ] | https://leetcode.com/problems/coin-change/ | [ ] | unbounded knapsack |
| Knapsack | Target Sum | 494 | [ ] | https://leetcode.com/problems/target-sum/ | [ ] | transform to subset-sum |
| LIS | Longest Increasing Subsequence | 300 | [ ] | https://leetcode.com/problems/longest-increasing-subsequence/ | [ ] | DP / patience |
| LIS variant | Russian Doll Envelopes | 354 | [ ] | https://leetcode.com/problems/russian-doll-envelopes/ | [ ] | LIS + sort |
| DP classic | Word Break | 139 | [ ] | https://leetcode.com/problems/word-break/ | [ ] | DP / trie |
| DP classic | Decode Ways | 91 | [ ] | https://leetcode.com/problems/decode-ways/ | [ ] | DP |
| DP classic | Edit Distance | 72 | [ ] | https://leetcode.com/problems/edit-distance/ | [ ] | 2D DP |
| DP hard | Super Egg Drop | 887 | [ ] | https://leetcode.com/problems/super-egg-drop/ | [ ] | optimized DP |
| String DP | Longest Palindromic Substring | 5 | [ ] | https://leetcode.com/problems/longest-palindromic-substring/ | [ ] | expand / DP |

### Week 4 — Advanced Data Structures (Segment Tree, Fenwick, DSU, Heaps)

| Topic | Problem | LC # | Status | Practice Link | Important / Revise | Notes |
|---|---|---:|:---:|---|:---:|---|
| Segment Tree | Range Sum Query - Mutable | 307 | [ ] | https://leetcode.com/problems/range-sum-query-mutable/ | [ ] | segtree/BIT |
| Segment Tree 2D | Range Sum Query 2D - Mutable | 308 | [ ] | https://leetcode.com/problems/range-sum-query-2d-mutable/ | [ ] | 2D BIT/SegTree |
| Range sums | Count of Range Sum | 327 | [ ] | https://leetcode.com/problems/count-of-range-sum/ | [ ] | divide & conquer / BIT |
| Fenwick / order-stat | Count of Smaller Numbers After Self | 315 | [ ] | https://leetcode.com/problems/count-of-smaller-numbers-after-self/ | [ ] | BIT / merge sort |
| DSU | Accounts Merge | 721 | [ ] | https://leetcode.com/problems/accounts-merge/ | [ ] | DSU + map |
| DSU / graph | Number of Provinces | 547 | [ ] | https://leetcode.com/problems/number-of-provinces/ | [ ] | DSU / BFS |
| DSU / cycle | Redundant Connection | 684 | [ ] | https://leetcode.com/problems/redundant-connection/ | [ ] | DSU |
| Heap / median | Find Median from Data Stream | 295 | [ ] | https://leetcode.com/problems/find-median-from-data-stream/ | [ ] | two heaps |
| Heap / median | Sliding Window Median | 480 | [ ] | https://leetcode.com/problems/sliding-window-median/ | [ ] | balanced heaps |
| KNN / heap | K Closest Points to Origin | 973 | [ ] | https://leetcode.com/problems/k-closest-points-to-origin/ | [ ] | heap / quickselect |
| Skyline / heap | The Skyline Problem | 218 | [ ] | https://leetcode.com/problems/the-skyline-problem/ | [ ] | sweep line + heap |

### Week 5 — Advanced Graphs (MST, Bridges/Articulation, Bellman-Ford)

| Topic | Problem | LC # | Status | Practice Link | Important / Revise | Notes |
|---|---|---:|:---:|---|:---:|---|
| MST / min connect | Min Cost to Connect All Points | 1584 | [ ] | https://leetcode.com/problems/min-cost-to-connect-all-points/ | [ ] | Kruskal / Prim |
| Bridges / critical | Critical Connections in a Network | 1192 | [ ] | https://leetcode.com/problems/critical-connections-in-a-network/ | [ ] | Tarjan bridges |
| Cycle / DSU | Redundant Connection | 684 | [ ] | https://leetcode.com/problems/redundant-connection/ | [ ] | DSU (also Week 4) |
| Shortest path (negative edges) | Cheapest Flights Within K Stops | 787 | [ ] | https://leetcode.com/problems/cheapest-flights-within-k-stops/ | [ ] | Bellman-Ford style |
| Shortest path (Dijkstra) | Network Delay Time | 743 | [ ] | https://leetcode.com/problems/network-delay-time/ | [ ] | Dijkstra |
| Advanced graph practice | (extra advanced) | — | [ ] |  | [ ] | Tarjan / Kosaraju / Prim |

### Week 6 — Mixed + Revision (AtCoder DP subset, contests, review)

| Topic | Problem | LC # | Status | Practice Link | Important / Revise | Notes |
|---|---|---:|:---:|---|:---:|---|
| AtCoder DP subset | AtCoder DP practice | n/a | [ ] |  | [ ] | map problems to LC equivalents |
| Timed contests | LeetCode Weekly/Biweekly | n/a | [ ] |  | [ ] | attempt 2 contests/week |
| Hard practice | Shortest Palindrome | 214 | [ ] | https://leetcode.com/problems/shortest-palindrome/ | [ ] | string algorithms |
| Hard practice | Median of Two Sorted Arrays | 4 | [ ] | https://leetcode.com/problems/median-of-two-sorted-arrays/ | [ ] | binary search on partitions |
| Hard practice | Serialize and Deserialize Binary Tree | 297 | [ ] | https://leetcode.com/problems/serialize-and-deserialize-binary-tree/ | [ ] | tree traversal |

Notes & tips
- Target counts per week: Week1 ≥20, Week2 15–20, Week3 ≈20, Week4 ≈15, Week5 ≈15, Week6 mixed/contests.
- For each problem: write template + solve from memory at least once per weekend.
- Keep a Mistakes Log: record patterns, pitfalls, and one-line corrective notes.

Happy practicing — use this map as a checklist and adapt problem selection to your weak areas.