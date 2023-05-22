---
title: "Actividad Evaluable 1"
author: [Ricardo Ruiz Fernández de Alba]
date: "06-06-21"
subject: "Probabilidad"
subtitle: "Propiedades función de probabilidad"
---

# Función de probabilidad

Se denota por $(\Omega, \mathcal{A},P)$ el espacio probabilístico base. Se considera la siguiente definición de medida de probabilidad:

**Definición 1.**  $P : \mathcal{A} \rightarrow[0,1]$ es una función de probabilidad si satisface los siguientes tres axiomas:

**A1.** $P(A) \geq 0, \quad \forall A \in \mathcal{A}$

**A2.** $P(\Omega) = 1$

**A3.** Para cualquier secuencia $\{A_n\}_{n \in \mathbb{N}} \subseteq \mathcal{A}$ de sucesos disjuntos
$$
P\left(\bigcup_{n\in \mathbb{N}}A_n\right) = \sum_{n \in \mathbb{N}} P(A_n)
$$

# Propiedades

**Demostrar, a partir de la definición anterior, las siguientes propiedades:**

- a) $P(\emptyset) = 0$

Basta considerar la secuencia de sucesos imposibles $\{ A_n \}_{n \in \mathbb{N}}$ con $A_n = \emptyset \quad \forall n \in \mathbb{N}$. Es claro que son disjuntos, luego usando **A3**

$$
P\left(\bigcup_{n \in \mathbb{N}} \emptyset \right) = \sum_{n \in \mathbb{N}} P(\emptyset)
$$

Observamos que **A1** garantiza la convergencia de la serie $\sum_{n \in \mathbb{N}} P(\emptyset)$ lo cual, de nuevo por **A1** se da si y sólo si $P(\emptyset) = 0$. $\square$

**Nota**: Asumiendo aditividad finita la prueba se deduce con mayor facilidad:
$$
P(\emptyset) = P(\emptyset \cup \emptyset) = P(\emptyset)+ P(\emptyset) 
$$

- b) Aditividad finita para sucesos disjuntos .
Sean $A_1, A_2, \dots, A_N \in \mathcal{A}$ un número finito de sucesos disjuntos, entonces
$$
P\left(\bigcup_{n=1}^N A_n \right) = \sum_{n=1}^N P(A_n)
$$

**Dem.**

Basta considerar la secuencia extendida $\{A_n\}_{n \in \mathbb{N}}$ tal que 
$A_n = \emptyset \quad \forall n > N$ 

Aplicando **A3** (aditividad contable).
$$
P\left(\bigcup_{n \in \mathbb{N}} A_n \right) = \sum_{n \in \mathbb{N}} P(A_n)
$$

Que en este caso, es equivalente a 

$$
P\left(\bigcup_{n=1}^N A_n\right) = \sum_{n=1}^N P(A_n) + \sum_{n=N+1}^\infty P(\emptyset) =  \sum_{n \in \mathbb{N}}^N P(A_n)
$$

utilizando que $P(\emptyset) = 0.$ $\square$

- c) Probabilidad del suceso complementario. Para cada suceso $A \in \mathcal{A}$
$$
P(A^c) = 1 - P(A)
$$

**Dem.**
Aplicando la aditividad finita para $A$ y su complementario $A^c$, que son disjuntos, se tiene:

$$
1 = P(\Omega) = P(A \cup A^c) = P(A) + P(A^c) \\
P(A^c) = 1 - P(A)
$$

Donde se ha utilizado **A2.** $\square$

**Nota:** sin considerar la aditividad finita es necesario extender la secuencia con vacíos. Por eso, se ha alterado el orden del enunciado.

- d) Probabilidad de la diferencia y monotonía. Sea $B \subseteq A \in \mathcal{A}$, entonces
$$
P(A −B) = P(A) −P(B)
$$ y $P(B) \leq P(A)$

**Dem.**

Consideramos los sucesos disjuntos $B$ y $A-B$, cuya unión es $A$ y aplicamos aditividad finita

$$
P(A) = P(B \cup (A-B)) = P(B) + P(A-B)
$$

Como $P(A-B) \geq 0$ por **A1**, deducimos $P(B) \leq P(A)$. 
Y despejando,

$$
P(A-B) = P(A) - P(B)
$$

$\square$

**Nota:** Se obtiene como caso particular la probabilidad del complementario.
$$
P(B^c) = P(\Omega - B) = P(\Omega) - P(B) = 1 - P(B)
$$

- e) Probabilidad de la unión
Sea $A, B \in \mathcal{A}$, entonces la probabilidad de la unión mediante la siguiente fórmula
$$
P(A \cup B) = P(A)+P(B)−P(A \cap B).
$$ En particular, $P(A\cup B) \leq P(A) + P(B)$

**Dem.**

Consideramos los sucesos disjuntos $A$ y $B-A$ cuya unión es $A \cup B$ y aplicamos aditividad finita

$$
P(A \cup B) = P(A \cup (B-A)) = P(A) + P(B-A)
$$

Claramente $B-A = B - (A \cap B)$ con $A \cap B \subset B$ luego

$$
P(A \cup B) = P(A)  + P(B - (A \cap B)) = P(A) + P(B) - P(A \cap B)
$$

Donde se ha aplicado la probabilidad de la diferencia. $\square$


- f) Principio de inclusión-exclusión para la unión finita de sucesos no disjuntos.
Sea $A_1, A_2, \dots, A_n \in \mathcal{A}$, entonces

$$
P\left(\bigcup_{i=1}^n A_i \right) = \sum_{i=1}^n P(A_i) - \sum_{i < j}^n P(A_i \cap A_j) + \sum_{i < j < k}^n P(A_i \cap A_j \cap A_k) + \dots  + (-1)^{n-1} P\left(\bigcap_{i=1}^n A_i \right)
$$

**Dem.**

Por inducción.

- **Caso base $n=1$:** Trivial
$$
P\left(\bigcup_{i=1}^1 A_i \right) = \sum_{i=1}^1 P(A_i) = P(A_1)
$$

- **Caso $n=2$**:

Es la fórmula de la probabilidad de la unión de dos sucesos demostrada anteriormente.

$$
P(A \cup B) = P(A) + P(B) - P(A \cap B)
$$

- **Paso inductivo**: suponiendo que el resultado es cierto para $n$, lo demotramos para $n+1$.

Considerando los sucesos disjuntos $\bigcup_{i=1}^n A_i$ y $(A_{n+1} - \bigcup_{i=1}^n A_i)$ cuya unión es $\bigcup_{i=1}^{n+1} A_i$ aplicamos aditividad finita

$$
P\left(\bigcup_{i=1}^{n+1} A_i \right) = P\left(\bigcup_{i=1}^n A_i \cup \left(A_{n+1} - \bigcup_{i=1}^n A_i\right) \right) = 
P\left(\bigcup_{i=1}^n A_i \right) + P\left(A_{n+1} - \bigcup_{i=1}^n A_i \right)
$$

En general notamos que $P(A-B) = P(A - (A \cap B)) = P(A) - P(A\cap B)$ usando la probabilidad de la diferencia. Lo aplicamos al último sumando del mimebro derecho.

$$
P\left(\bigcup_{i=1}^{n+1} A_i \right) = 
P\left(\bigcup_{i=1}^n A_i \right) + P\left(A_{n+1} - \bigcup_{i=1}^n A_i \right) =
P\left(\bigcup_{i=1}^n A_i \right) + P\left(A_{n+1} \right) - P\left(\bigcup_{i=1}^n A_i \cap A_{n+1} \right)
$$

Aplicando la hipótesis de inducción al primer y tercer sumando del segundo miembro:

$$
P\left(\bigcup_{i=1}^{n+1} A_i \right) = 
\sum_{i=1}^n P(A_i) - \sum_{i < j}^n P(A_i \cap A_j) + \dots  + (-1)^{n-1} P\left(\bigcap_{i=1}^n A_i \right) + P(A_{n+1}) \\ - \sum_{i=1}^n P(A_i \cap A_{n+1}) + \sum_{i < j}^n P(A_i \cap A_j \cap A_{n+1}) - \dots  + \\ + (-1)^{n-1}\sum_{a_1 < a_2 < ... < a_{n - 1}}^n P\left(A_{a_1} \cap \dots \cap  A_{a_{n-1}} \cap A_{n+1}\right)- (-1)^{n-1} P\left(\bigcap_{i=1}^n A_i \cap A_{n+1} \right) 
$$

Agrupamos los términos, sumando el $i$-ésimo con el $(n+i)$-ésimo.

**a) Primer término con el $(n+1)$-ésimo**

$$ \sum_{i=1}^n P(A_i) + P(A_{n+1}) = \sum_{i=1}^{n+1} P(A_i) $$

**b) Segundo término con $(n+2)$-ésimo$**

$$-\sum_{i < j}^n P(A_i \cap A_j) - \sum_{i=1}^n P(A_i \cap A_{n+1}) = -\sum_{i < j}^{n+1} P(A_i \cap A_j)$$

**c) Tercer término con $(n+3)$-ésimo**

$$\sum_{i < j < k}^n P(A_i \cap A_j \cap A_k) + \sum_{i < j}^n P(A_i \cap A_j \cap A_{n+1}) = \sum_{i < j < k} ^{n+1} P(A_i \cap A_j \cap A_k)$$

**$\dots$**

**d) $n$-ésimo con $(2n)$-ésimo término**

$$
(-1)^{n-1}P\left(\bigcap_{i=1}^n A_i \right) + (-1)^{n-1}\sum_{a_1 < a_2 < ... < a_{n - 1}}^n P\left(A_{a_1} \cap \dots \cap  A_{a_{n-1}} \cap A_{n+1}\right) = \sum_{a_1 < a_2 < \dots a_n}^{n+1} P\left(\bigcap_{i=1}^n A_{a_i}\right)
$$


Finalmente, notamos que $-(-1)^{n-1} = (-1)^n$ y que $\bigcap_{i=1}^n A_i \cap A_{n+1} = \bigcap_{i=1}^{n+1} A_i$ en el último término luego

$$
P\left(\bigcup_{i=1}^{n+1} A_i \right) = \sum_{i=1}^{n+1} P(A_i) - \sum_{i < j}^{n+1} P(A_i \cap A_j) + \sum_{i < j < k}^{n+1} P(A_i \cap A_j \cap A_k) + \dots  + (-1)^nP\left(\bigcap_{i=1}^{n+1} A_i \right)
$$

$\square$

- g) Subaditividad: 
$$
P\left(\bigcup_{n \in \mathbb{N}} A_n\right) \leq \sum_{n \in \mathbb{N}} P(A_n).
$$

Definimos una nueva familia de sucesos:

$$
B_1 = A_1 \\
B_2 = A_2 - A_1 \\
B_3 = A_3 - (A_1 \cup A_2)
\dots \\
B_n = A_n - \bigcup_{j=1}^{n-1} A_n
$$

Observamos lo siguiente:  

$$B_i \cap B_j = \emptyset$$
$$\bigcup_{n \in \mathbb{N}} A_n = \bigcup_{n \in \mathbb{N}} B_n $$

Luego aplicamos **A3** a la unión:

$$
P\left(\bigcup_{n \in \mathbb{N}} A_i \right) = P\left(\bigcup_{n \in \mathbb{N}} B_i \right) = \sum_{n \in \mathbb{N}} P(B_i)
$$

Además, como $B_n \subset A_n \quad \forall n \in \mathbb{N}$, usamos la consecuencia de la probabilidad de la diferencia $P(B_n) \leq P(A_n)$

y tenemos que 

$$
\sum_{i=1}^n P(B_i) \leq \sum_{i=1}^n P(A_i)
$$

Luego, eventualmente en el límite:

$$
\sum_{n \in \mathbb{N}} P(B_i) \leq \sum_{n \in \mathbb{N}} P(A_i)
$$

y llegamos al resultado

$$
P\left(\bigcup_{n \in \mathbb{N}} A_n\right) \leq \sum_{n \in \mathbb{N}} P(A_n).
$$

$\square$

- h) Desigualdad de Boole: 
$$
P\left(\bigcap_{n \in \mathbb{N}} A_n \right) \geq 1 − \sum_{n \in \mathbb{N}} P(A_n^c)
$$

Usamos que $\bigcap_{n \in \mathbb{N}} A_n = \left(\bigcup_{n \in \mathbb{N}} A_n^c \right)^c$ y la probabilidad del suceso complementario

$$
P\left( \bigcap_{n \in \mathbb{N}}A_n \right) = 
P\left( \left(\bigcup_{n \in \mathbb{N}} A_n^c \right)^c \right) = 
1 - P\left( \bigcup_{n \in \mathbb{N}}A_n^c \right)
$$

Utilizando la propiedad de subadtividad

$$
  P\left(\bigcap_{n \in \mathbb{N}} A_n \right) \geq 1 − \sum_{n \in \mathbb{N}} P(A_n^c)
$$
  
$\square$