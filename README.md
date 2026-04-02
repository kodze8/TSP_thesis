#  Explaining the Traveling Salesman Problem

The challenge focuses on the Travelling Salesman Problem (TSP), a classical and computationally
hard combinatorial optimization problem. In the TSP, a salesman must visit a set of cities exactly once
and return to the starting city, while minimizing the total travel distance (or cost). As the number of
cities increases, the number of possible tours grows factorially, making exact solution methods
infeasible for larger instances. This makes the TSP a canonical benchmark for sophisticated heuristic
and metaheuristic optimization techniques.

To address this complexity, a wide range of (meta)heuristics and machine learning inspired algorithms
have been developed, such as evolutionary algorithms and simulated annealing. These methods do not
guarantee finding the global optimum, but they aim to produce high‑quality solutions within a
reasonable computational time. In this project, students will implement such a solving technique and
apply it to TSP instances, with the objective of obtaining solutions that are as good as possible.

A central aspect of the challenge is not only to solve the TSP, but also to explain how the obtained
solutions arise from the algorithm’s search process. The chosen solving technique can be viewed as a
search algorithm that explores many candidate tours before termination. By systematically logging
these intermediate solutions, we can analyze the behavior of the algorithm and derive several
explanation techniques, including:

- Contrastive explanations: By comparing solutions with and without specific edges, we can
quantify how certain choices affect the objective value. For example: “When this edge is
included, we observe on average an increase of the objective by x,” providing insight into
which edges tend to help or harm solution quality.

- Edge importance and frequency analysis: Using the search log, we can measure how often
each edge appears in high‑quality tours and how its presence correlates with tour cost. Edges
that frequently occur in the best solutions, or that are associated with lower average costs
when included, can be highlighted as particularly important. This yields a global view of
which connections the algorithm consistently relies on, and can be visualized by emphasizing
these edges in the underlying graph.


- Diverse near‑optimal solutions: Instead of presenting only a single “best” tour, the algorithm
can provide a set of distinct tours that are all within a certain range (e.g., y%) of the best
solution found. This diversity helps to illustrate the structure of the solution space and shows
alternative routes that are nearly as good, which can be relevant in practice when additional
constraints or preferences are considered.


By combining advanced optimization methods with these explanation techniques, the challenge aims
to deepen students’ understanding of both heuristic search for hard combinatorial problems and
interpretable, transparent solution methods, demonstrating how complex algorithmic decisions can be
analyzed and communicated in an understandable way.


### Expected Outcome:
The main outcome of this project is a working prototype that both solves and explains instances of the
Travelling Salesman Problem (TSP).

### From a technical perspective, the student will:
- Implement and tune a (meta)heuristic search algorithm (e.g. simulated annealing, evolutionary
algorithm) to find high‑quality TSP tours within reasonable computation time.
- Design and implement a logging mechanism that records the intermediate solutions explored
during the search, together with their objective values and relevant algorithmic decisions.

### From an explainability perspective, the student will:
- Develop contrastive explanation techniques that highlight how the inclusion or exclusion of
specific edges affects the objective value (e.g. “when this edge is used, the tour cost increases
on average by x”).
- Perform edge importance and frequency analysis, identifying which edges appear frequently
in high‑quality tours and how they correlate with good solutions, potentially visualized on the
underlying graph.
- Generate a set of diverse near‑optimal solutions, i.e. multiple distinct tours within a predefined
percentage of the best solution found, to illustrate alternative high‑quality routes.


### From a scientific and educational perspective, the project should result in:
- A written thesis that clearly describes the algorithm, the logging and explanation methods, and
an empirical evaluation on benchmark TSP instances.
-  A critical reflection on the strengths and limitations of the chosen heuristic and the proposed
explanation techniques, including suggestions for future extensions.
