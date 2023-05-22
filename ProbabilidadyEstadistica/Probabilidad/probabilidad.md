## Probabilidad

**Principio de inclusión-exclusión**

$$
P\left( \bigcup_{i=1}^n A_i \right) =
\sum_{k=1}^n (-1)^{k+1}
\left(
  \sum_{1 \leq i_1 \leq \ldots i_k \leq n } |A_{i_1}
  \cap \ldots \cap A_{i_k}|
\right) = \\
= \sum_{i=1}^n P(A_i) - \sum_{i<j}^n P(A_i \cap A_j ) +
\sum_{i<j<k}^n P(A_i \cap A_j \cap A_k) + \ldots  +
(-1)^{n-1} P\left(\bigcap_{i=1}^n A_i\right)
$$

**Demostración**

Procedemos por inducción:

Para $n=2$:

$$
P(A_1 \cup A_2) = P(A_1) + P(A_2) - P(A_1 \cap A_2)
$$

Supongamos la proposición cierta para $n-1$ y demostrémosla para $n$:

$$
P\left( \bigcup_{i=1}^n A_i \right) =
 P\left( A_n \cup \bigcup_{i=1}^{n-1} A_i \right) =
  P\left(\bigcup_{i=1}^{n-1} A_i \right) + P(A_n)
  -P\left( A_n \cap \bigcup_{i=1}^{n-1} A_i
  \right) = \\
= \sum_{i=1}^{n-1} P(A_i) - \sum_{i<j}^{n-1} P(A_i \cap A_j ) + \ldots  +
(-1)^{n-2} P\left(\bigcap_{i=1}^{n-1} A_i\right) + P(A_n) 
-P\left( A_n \cap \bigcup_{i=1}^{n-1} A_i\right) = \\
= \sum_{i=1}^n P(A_i) - \sum_{i<j}^{n-1} P(A_i \cap A_j ) + \ldots  +
(-1)^{n-2} P\left(\bigcap_{i=1}^{n-1} A_i\right)
-P\left( \bigcup_{i=1}^{n-1} A_i \cap  A_n\right) = \\

= \sum_{i=1}^n P(A_i) - \sum_{i<j}^{n-1} P(A_i \cap A_j ) + \ldots  +
(-1)^{n-2} P\left(\bigcap_{i=1}^{n-1} A_i\right) \\
- \sum_{i=1}^{n-1} P(A_i \cap A_n) + \sum_{i<j}^{n-1} P(A_i \cap A_j \cap A_n ) + \ldots  +
(-1)^{n-1} P\left(\bigcap_{i=1}^{n-1} A_i \cap A_n \right) =\\
= \sum_{i=1}^n P(A_i) - \sum_{i<j}^n P(A_i \cap A_j ) +
\sum_{i<j<k}^n P(A_i \cap A_j \cap A_k) + \ldots  +
(-1)^{n-1} P\left(\bigcap_{i=1}^n A_i\right)
$$

Donde se ha usado que

$$
\sum_{1 \le i_1 \lt \ldots \lt i_k \leq n}^{n-1}
 P(A_{i_1}\cap \ldots \cap A_{i_k}) +
\sum_{1 \le i_1 \lt \ldots \lt i_k \leq n}^{n-1}
 P(A_{i_1}\cap \ldots \cap A_{i_{k-1}} \cap A_n)
 = \sum_{1 \le i_1 \lt \ldots \lt i_k \leq n}^n
 P(A_{i_1}\cap \ldots \cap A_{i_k})
