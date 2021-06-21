# Classical and Forward Planning

Dennis Ping  
Homework 4  
June 20, 2021  

## Purpose  

Analyze the 11 search algorithms on four air cargo problems. Three algorithms are uninformed and eight algorithms use heuristics.

## Air Cargo Problem 1 Results 

| Search Algorithm        | Actions | Expansions | Goal Tests | New Nodes | Plan Length | Time Elapsed |
| ----------------------- | ------- | ---------- | ---------- | --------- | ----------- | ------------ |
| BFS                     | 20      | 43         | 56         | 178       | 6           | 0.001599     |
| DFS                     | 20      | 21         | 22         | 84        | 20          | 0.000819     |
| UCS                     | 20      | 60         | 62         | 240       | 6           | 0.002231     |
| Greedy Best Unmet Goals | 20      | 7          | 9          | 29        | 6           | 0.000398     |
| Greedy Best PG LevelSum | 20      | 6          | 8          | 28        | 6           | 0.055757     |
| Greedy Best PG MaxLevel | 20      | 6          | 8          | 24        | 6           | 0.024776     |
| Greedy Best PG SetLevel | 20      | 6          | 8          | 28        | 6           | 0.247943     |
| A\* Unmet Goals         | 20      | 50         | 52         | 206       | 6           | 0.002161     |
| A\* PG LevelSum         | 20      | 28         | 30         | 122       | 6           | 0.135699     |
| A\* PG MaxLevel         | 20      | 43         | 45         | 180       | 6           | 0.087032     |
| A\* PG SetLevel         | 20      | 33         | 35         | 138       | 6           | 0.630704     |

## Air Cargo Problem 2 Results

| Search Algorithm        | Actions | Expansions | Goal Tests | New Nodes | Plan Length | Time Elapsed |
| ----------------------- | ------- | ---------- | ---------- | --------- | ----------- | ------------ |
| BFS                     | 72      | 3343       | 4609       | 30503     | 9           | 0.400156     |
| DFS                     | 72      | 624        | 625        | 5602      | 619         | 0.511842     |
| UCS                     | 72      | 5154       | 5156       | 44618     | 9           | 0.659752     |
| Greedy Best Unmet Goals | 72      | 17         | 19         | 170       | 9           | 0.004146     |
| Greedy Best PG LevelSum | 72      | 9          | 11         | 86        | 9           | 1.249646     |
| Greedy Best PG MaxLevel | 72      | 27         | 29         | 249       | 9           | 1.125439     |
| Greedy Best PG SetLevel | 72      | 9          | 11         | 84        | 9           | 5.687038     |
| A\* Unmet Goals         | 72      | 2467       | 2469       | 22522     | 9           | 0.460401     |
| A\* PG LevelSum         | 72      | 357        | 359        | 3426      | 9           | 37.755327    |
| A\* PG MaxLevel         | 72      | 2887       | 2889       | 26594     | 9           | 104.746691   |
| A\* PG SetLevel         | 72      | 1037       | 1039       | 9605      | 9           | 435.482024   |

## Air Cargo Problem 3 Results

| Search Algorithm        | Actions | Expansions | Goal Tests | New Nodes | Plan Length | Time Elapsed |
| ----------------------- | ------- | ---------- | ---------- | --------- | ----------- | ------------ |
| BFS                     | 88      | 14663      | 18098      | 129625    | 12          | 2.070329     |
| Greedy Best Unmet Goals | 88      | 25         | 27         | 230       | 15          | 0.007416     |
| Greedy Best PG LevelSum | 88      | 14         | 16         | 126       | 14          | 3.202100     |
| Greedy Best PG MaxLevel | 88      | 21         | 23         | 195       | 13          | 1.596612     |
| Greedy Best PG SetLevel | 88      | 35         | 37         | 345       | 17          | 28.072230    |
| A\* Unmet Goals         | 88      | 7388       | 7390       | 65711     | 12          | 1.663320     |
| A\* PG LevelSum         | 88      | 369        | 371        | 3403      | 12          | 63.058872    |
| A\* PG MaxLevel         | 88      | 9580       | 9682       | 86312     | 12          | 593.564430   |
| A\* PG SetLevel         | 88      | 3423       | 3425       | 31596     | 12          | 1907.285749  |


## Air Cargo Problem 4 Results

| Search Algorithm        | Actions | Expansions | Goal Tests | New Nodes | Plan Length | Time Elapsed |
| ----------------------- | ------- | ---------- | ---------- | --------- | ----------- | ------------ |
| BFS                     | 104     | 99736      | 114953     | 944130    | 14          | 18.403836    |
| Greedy Best Unmet Goals | 104     | 29         | 31         | 280       | 18          | 0.011811     |
| Greedy Best PG LevelSum | 104     | 17         | 19         | 165       | 17          | 5.977597     |
| Greedy Best PG MaxLevel | 104     | 56         | 58         | 580       | 17          | 4.928934     |
| Greedy Best PG SetLevel | 104     | 107        | 109        | 1164      | 23          | 122.802205   |
| A\* Unmet Goals         | 104     | 34330      | 34332      | 328509    | 14          | 10.420136    |
| A\* PG LevelSum         | 104     | 1208       | 1210       | 12210     | 15          | 381.441892   |
| A\* PG MaxLevel         |         |            |            |           |             | Too Long     |
| A\* PG SetLevel         |         |            |            |           |             | Too Long     |

*A\* MaxLevel and A\* SetLevel were omitted due to extremely long computation time. This is allowed per the project instructions.*

## Search Analysis

1. In a very restricted domain (Air Cargo Problems 1 and 2), the **BFS algorithm** and **all the Greedy algorithms** could be appropriate. Specifically, the **Greedy Best First Unmet Goals** algorithm is very fast and expands a low amount of layers in order to find the goals. This is probably because the nature of a narrow domain quickly guides the greedy algorithm to the goals. There is no room for the algorithm to accidentally expand a poor layer.

2. For a very large domain (Air Cargo Problems 3 and 4), you want a sufficiently low path length and an acceptable computation time. The **BFS algorithm** still finds the optimal path very quickly, but at the great cost of expanding every possible layer. The **A\* Unmet Goals** algorithm is just a smarter BFS algorithm that chases unmet goals. Therefore, it expands fewer layers, doesn't require much computation power, finds the optimal path, and is very fast. I believe **A\* Unmet Goals** is the best algorithm for a large domain given a narrow time window.

3. For finding only optimal paths, it is best to use a very comprehensive search algorithm such **A\* Unmet Goals**, **A\* LevelSum**, **A\* MaxLevel**, or **A\* SetLevel** because they will all find the optimal plan length. However, the expansion count and computation time differs greatly among the 4 algorithms. The simpler **A\* Unmet Goals** algorithm seems to yield a very attractive expansion count and computation time.