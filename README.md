# Comparison of Search Algorithms


<b>Conclusions from the statistics below:</b>


GBFS vs. UCS and A*

GBFS seems to be the most space-efficient and time-efficient because on average, it enters, expands, and maintains fewer nodes than UCS and A* do. However, unlike UCS and A*, it is not optimal. Although GBFS found solutions to each of the 7 problems, 4 of the solutions have greater path costs than the corresponding solutions generated by UCS and A*. This was especially true when the path between two cities was longer and more complex. The is because even though GBFS goes down paths that have smaller immediate action costs and smaller estimated distances to the goal state, these paths may lead to a dead end or accumulate to be longer and more expensive than other routes to the goal-state. GBFS does not backtrack since it does not insert child nodes into the frontier if there is already a child node with the same state. As a consequence, GBFS does not replace child nodes in the frontier with ones that have lower path costs. 
 
 
UCS vs. A*

The uninformed search algorithm UCS is not nearly as space-efficient and time-efficient as the informed search algorithm A*, even though both are complete and optimal. UCS enters and expands around twice as many nodes as A* for this particular graph because it does not use a heuristic to guide its search. Instead, it continuously goes down paths with the smallest action cost regardless of how far away the successor state is from the goal state. This means that even if the solution has already been inserted into the frontier, UCS does not recognize it as such until it plays out all of the less expensive paths first. 

---

<b>UCS</b>

STATISTICS (entered, expanded, maintained), SOLUTION, & PATH COST PER PROBLEM: 

Run 1: (16 53 24 ((VA-RENNES VA-NANTES VA-LIMOGES VA-LYON VA-AVIGNON VA-MARSEILLE) 1384))

Run 2: (16 52 25 ((VA-AVIGNON VA-LYON VA-DIJON VA-PARIS VA-CALAIS) 1139)) 

Run 3: (17 53 25 ((VA-NANCY VA-PARIS VA-LIMOGES VA-BORDEAUX) 1133))

Run 4: (11 39 20 ((VA-DIJON VA-LYON VA-GRENOBLE) 609)) 

Run 5: (10 31 19 ((VA-LYON VA-DIJON VA-PARIS) 609))

Run 6: (14 47 22 ((VA-RENNES VA-NANTES VA-LIMOGES VA-LYON VA-GRENOBLE) 1173))

Run 7:  (17 58 26 ((VA-LYON VA-LIMOGES VA-NANTES VA-RENNES VA-BREST) 1173)) 



<br>AVERAGE STATISTICS (entered, expanded, maintained, optimal solution found): </br>

(14.428572 47.57143 23.0 1.0)

---

<b>GBFS</b>

STATISTICS (entered, expanded, maintained), SOLUTION, & PATH COST PER PROBLEM: 

Run 1: (6 23 18 ((VA-RENNES VA-PARIS VA-DIJON VA-LYON VA-AVIGNON VA-MARSEILLE) 1412))

Run 2: (4 16 13 ((VA-TOULOUSE VA-LIMOGES VA-PARIS VA-CALAIS) 1246)) 

Run 3: (4 17 14 ((VA-DIJON VA-PARIS VA-LIMOGES VA-BORDEAUX) 1264))

Run 4: (3 14 12 ((VA-DIJON VA-LYON VA-GRENOBLE) 609)) 

Run 5: (3 10 8 ((VA-LYON VA-DIJON VA-PARIS) 609))

Run 6: (5 19 15 ((VA-RENNES VA-PARIS VA-DIJON VA-LYON VA-GRENOBLE) 1201))

Run 7: (5 18 14 ((VA-LYON VA-LIMOGES VA-NANTES VA-RENNES VA-BREST) 1173))


<br>AVERAGE STATISTICS (entered, expanded, maintained, optimal solution found):</br>

(4.285714 16.714285 13.428572 0.43)

---

<b>A*</b>

STATISTICS (entered, expanded, maintained), SOLUTION, & PATH COST PER PROBLEM: 

Run 1: (12 42 25 ((VA-RENNES VA-NANTES VA-LIMOGES VA-LYON VA-AVIGNON VA-MARSEILLE) 1384))

Run 2: (7 25 18 ((VA-AVIGNON VA-LYON VA-DIJON VA-PARIS VA-CALAIS) 1139)) 

Run 3: (6 25 17 ((VA-NANCY VA-PARIS VA-LIMOGES VA-BORDEAUX) 1133))

Run 4: (3 14 12 ((VA-DIJON VA-LYON VA-GRENOBLE) 609)) 

Run 5: (3 10 8 ((VA-LYON VA-DIJON VA-PARIS) 609))

Run 6: (8 31 21 ((VA-RENNES VA-NANTES VA-LIMOGES VA-LYON VA-GRENOBLE) 1173))

Run 7: (6 21 15 ((VA-LYON VA-LIMOGES VA-NANTES VA-RENNES VA-BREST) 1173))

<br>AVERAGE STATISTICS (entered, expanded, maintained, optimal solution found): </br>

(6.428571 24.0 16.571428 1.0)




















