# Classical and Forward Planning

Dennis Ping
Homework 4
June 20, 2021

## Air Cargo Problem Search Results

**Air Cargo Problem 1: BFS**
```
# Actions   Expansions   Goal Tests   New Nodes
    20          43          56         178

Plan length: 6  Time elapsed in seconds: 0.0015986000000012268
```

**Air Cargo Problem 1: DFS**
```
# Actions   Expansions   Goal Tests   New Nodes
    20          21          22          84

Plan length: 20  Time elapsed in seconds: 0.0008188000000000015
```

**Air Cargo Problem 1: UCS**
```
# Actions   Expansions   Goal Tests   New Nodes
    20          60          62         240

Plan length: 6  Time elapsed in seconds: 0.0022312999999999986
```

**Air Cargo Problem 1: Greedy BFS Unmet Goals**
```
# Actions   Expansions   Goal Tests   New Nodes
    20          7           9           29

Plan length: 6  Time elapsed in seconds: 0.00039820000000000133
```

**Air Cargo Problem 1: Greedy BFS PG LevelSum**
```
# Actions   Expansions   Goal Tests   New Nodes
    20          6           8           28

Plan length: 6  Time elapsed in seconds: 0.0557566
```

**Air Cargo Problem 1: Greedy BFS PG MaxLevel**
```
# Actions   Expansions   Goal Tests   New Nodes
    20          6           8           24

Plan length: 6  Time elapsed in seconds: 0.024775599999999995
```

**Air Cargo Problem 1: Greedy BFS PG SetLevel**
```
# Actions   Expansions   Goal Tests   New Nodes
    20          6           8           28

Plan length: 6  Time elapsed in seconds: 0.2479428
```

**Air Cargo Problem 1: AStar Unmet Goals**
```
# Actions   Expansions   Goal Tests   New Nodes
    20          50          52         206

Plan length: 6  Time elapsed in seconds: 0.0021609000000000003
```

**Air Cargo Problem 1: AStar PG LeveSum**
```
# Actions   Expansions   Goal Tests   New Nodes
    20          28          30         122

Plan length: 6  Time elapsed in seconds: 0.1356994
```

**Air Cargo Problem 1: AStar PG MaxLevel**
```
# Actions   Expansions   Goal Tests   New Nodes
    20          43          45         180

Plan length: 6  Time elapsed in seconds: 0.0870322
```

**Air Cargo Problem 1: ASar PG SetLevel**
```
# Actions   Expansions   Goal Tests   New Nodes
    20          33          35         138

Plan length: 6  Time elapsed in seconds: 0.6307035
```

## Air Cargo Problem 2 Search Results:

**Air Cargo Problem 2: BFS**
```
# Actions   Expansions   Goal Tests   New Nodes
    72         3343        4609       30503

Plan length: 9  Time elapsed in seconds: 0.4001556
```

**Air Cargo Problem 2: DFS**
```
# Actions   Expansions   Goal Tests   New Nodes
    72         624         625         5602

Plan length: 619  Time elapsed in seconds: 0.5118424
```

**Air Cargo Problem 2: UCS**
```
# Actions   Expansions   Goal Tests   New Nodes
    72         5154        5156       46618

Plan length: 9  Time elapsed in seconds: 0.6597519
```

**Air Cargo Problem 2: Greedy BFS Unmet Goals**
```
# Actions   Expansions   Goal Tests   New Nodes
    72          17          19         170

Plan length: 9  Time elapsed in seconds: 0.004145500000000003
```

**Air Cargo Problem 2: Greedy BFS PG LevelSum**
```
# Actions   Expansions   Goal Tests   New Nodes
    72          9           11          86

Plan length: 9  Time elapsed in seconds: 1.2496456999999999
```

**Air Cargo Problem 2: Greedy BFS PG MaxLevel**
```
# Actions   Expansions   Goal Tests   New Nodes
    72          27          29         249

Plan length: 9  Time elapsed in seconds: 1.1254385
```

**Air Cargo Problem 2: Greedy BFS PG SetLevel**
```
# Actions   Expansions   Goal Tests   New Nodes
    72          9           11          84

Plan length: 9  Time elapsed in seconds: 5.687038
```

**Air Cargo Problem 2: AStar Unmet Goals**
```
# Actions   Expansions   Goal Tests   New Nodes
    72         2467        2469       22522

Plan length: 9  Time elapsed in seconds: 0.4604009
```

**Air Cargo Problem 2: AStar PG LevelSum**
```
# Actions   Expansions   Goal Tests   New Nodes
    72         357         359         3426

Plan length: 9  Time elapsed in seconds: 37.755327199999996
```

**Air Cargo Problem 2: AStar PG MaxLevel**
```
# Actions   Expansions   Goal Tests   New Nodes
    72         2887        2889       26594

Plan length: 9  Time elapsed in seconds: 104.7466914
```

**Air Cargo Problem 2: AStar PG SetLevel**
```
# Actions   Expansions   Goal Tests   New Nodes
    72         1037        1039        9605

Plan length: 9  Time elapsed in seconds: 435.4820243
```

## Search Analysis

1. In a very restricted domain, all the Greedy BFS algorithms would be appropriate. Specifically, the Greedy BFS LevelSum algorithm is very fast and expands a low amount of layers in order to find the goals for both Air Cargo Problem 1 and 2.  
This is probably because the nature of a narrow domain quickly guides the greedy BFS algorithm to the goals. The algorithm has a low chance of expanding a bad nodes.

2. 