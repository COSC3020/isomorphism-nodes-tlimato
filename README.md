# Isomorphism

Prove that if two graphs $A$ and $B$ do not have the same number of nodes, they
cannot be isomorphic. I have started with the formal definition of isomorphism
below. Add your answer to this markdown file. [This
page](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/writing-mathematical-expressions)
might help with the notation for mathematical expressions.

$G_1=(V_1 , E_1)$ is isomorphic to $G_2 = (V_2, E_2)$ if there exists a
one-to-one and onto function (bijection) $f: V_1 \rightarrow V_2$ such that $(u,v)
\in E_1$ iff $(f(u),f(v)) \in E_2$.

Proof w/ Markdown Notation:
----------------------------
# Case 1: Two Isomorphic Graphs A & B are fully connected.
This is trivially true; as two isomorphic graphs $A$ and $B$ are fully connected and retain isomorphism {Definition of Isomorphism}

# Case 2: At least A or B is not fully connected, given A and B are Isomorphic Graphs.
Let's assume $A$ is not fully connected. Since A & B are isomorphic, there exists a bijection $f: V(A) \rightarrow V(B)$ such that $(u,v) \in E(A)$ if and only if $(f(u),f(v)) \in E(B)$. {Definition of Isomorphism}. 
The function $f$ is a bijection, meaning it is both injective (one-to-one) and onto. This ensures that each vertice in $A$ maps to a unique vertex in $B$ and covers all vertices in $B$. Furthermore, for any two vertices $u$ and $v$ in $A$, if $(u, v) \in E(A)$, then $(f(u), f(v))$ must be in $(E(B)$. Conversely, if $(u, v) \notin E(A)$, then $(f(u), f(v))$ must not be in $E(B)$. This preservation of adjacency and non-adjacency confirms the isomorphism.

As $A$ is not fully connected, there exists at least one pair of vertices $(u,v) \in V(A)$ such that $(u,v) \notin E(A)$, meaning they have no adjacency and thus are not connected. Therefore, their corresponding vertices $f(u), f(v) \in V(B)$ must also satisfy $(f(u), f(v)) \notin E(B)$ as the bijection $f$ preserves said relation.

Subsequently, $B$ is not fully connected as it contains at least one set of vertices, preserved by the bijection $f$, such that $f(u), f(v) \in V(B)$ AND $(f(u), f(v)) \notin E(B)$. {Definition of Isomorphism} {Definition of fully connected}


# Conclusion:
"Case 1" proves trivially that two fully connected graphs that are isomorphic retain said isomorphism. "Case 2" demonstrates that if one of the isomorphic graphs $A$ or $B$ is not fully connected, then the other must also be not fully connected due to the preservation of adjacency and non-adjacency by the bijection $f$. Therefore, the isomorphism between two graphs does NOT imply that they must be fully connected; it only requires that the connectivity pattern (what is connected to what) is preserved.

