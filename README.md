[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/AtNXzL3S)
# Isomorphism

Prove that if two graphs $A$ and $B$ do not have the same number of nodes, they
cannot be isomorphic. I have started with the formal definition of isomorphism
below. Add your answer to this markdown file. [This
page](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/writing-mathematical-expressions)
might help with the notation for mathematical expressions.

$G_1=(V_1 , E_1)$ is isomorphic to $G_2 = (V_2, E_2)$ if there exists a
one-to-one and onto function (bijection) $f: V_1 \rightarrow V_2$ such that $(u,v)
\in E_1$ iff $(f(u),f(v)) \in E_2$.


Proof w/ Mathematical Notation
-------------------------------
for this proof, I will be using proof by contradiction.

# Case 1: let $A$ & $B$ be two graphs with $m$ and $n$ number of vertices/nodes respectively, where $m = n$.
trivial. Refer to "isomorphism-connectivity-tlimato" which proves this case more explicitly with a focus on connectivity.

# Case 2: let A & B be two graphs with m & n number of vertices/nodes respectively, where $m \neq n$.
let's assume A & B are isomorphic.

By definition of isomorphism, there must exist a bijection $f: V_1 \rightarrow V_2$ such that $(u,v)
\in E_1$ if $(f(u),f(v)) \in E_2$. This bijection applies for all arbitrary u & v, with their corresponding f(u) & f(v) as outlined by the one-to-one and onto properties of a bijection.

However, if $m \neq n$, then $|V_1| \neq |V_2|$ meaning, the cardinality of A and B are not equivalent.

Furthermore, a bijection $f: V_1 \rightarrow V_2$ requires that $|V_1| = |V_2|$, given f is a function that is **both** one-to-one and onto.

**Contradiction**. For two graphs A and B to be Isomorphic there must exist a valid bijection between A and B, which is absent when $|V_1| \neq |V_2|$.

# Conclusion:
Based upon "Case 1" and "Case 2", we can conclude two graphs A & B with a different number of vertices/nodes ( $n \neq n$ ) cannot be isomorphic
