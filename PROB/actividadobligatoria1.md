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
P\left(\bigcup_{n\in \mathbb{N}}A_n\right) = \sum_{n∈\mathbb{N}} P(A_n)
$$

# Propiedades

**Demostrar, a partir de la definición anterior, las siguientes propiedades:**

> a) $P(\emptyset) = 0$

Basta considerar la secuencia de sucesos imposibles $\{ A_n \}_{n \in \mathbb{N}}$ con $A_n = \emptyset \quad \forall n \in \mathbb{N}$. Es claro que son disjuntos, luego usando **A3**

$$
P\left(\bigcup_{n \in \mathbb{N}} \emptyset \right) = \sum_{n \in \mathbb{N}} P(\emptyset)
$$

Observamos que **A1** garantiza la convergencia de la serie $\sum_{n \in \mathbb{N}} P(\emptyset)$ lo cual, de nuevo por **A1** se da si y sólo si $P(\emptyset) = 0$. $\square$

**Nota**: Asumiendo aditividad finita la prueba se deduce con mayor facilidad:
$$
P(\emptyset) = P(\emptyset \cup \emptyset) = P(\emptyset)+ P(\emptyset) 
$$

> b) Aditividad finita para sucesos disjuntos .
> Sean $A_1, A_2, \dots, A_N \in \mathcal{A}$ un número finito de sucesos disjuntos, entonces
> $$
P\left(\bigcup_{n=1}^N A_n \right) = \sum_{n=1}^N P(A_n)
$$

**Dem.**
Basta considerar la secuencia extendida $\{A_n \}_{n \in \mathbb{N}}$ tal que $A_n = \emptyset \quad \forall n \gt N$. 

Aplicando **A3** (aditividad contable).
$$
P\left(\bigcup_{n \in \mathbb{N}} A_n \right) = \sum_{n \in \mathbb{N}} P(A_n)
$$

Que en este caso, es equivalente a 

$$
P\left(\bigcup_{n=1}^N A_n\right) = \sum_{n=1}^N P(A_n) + \sum_{n=N+1}^\infty P(\emptyset) =  \sum_{n \in \mathbb{N}}^N P(A_n)
$$

utilizando que $P(\emptyset) = 0.$ $\square$

> c) Probabilidad del suceso complementario. Para cada suceso $A \in \mathcal{A}$
$$
P(A^c) = 1 - P(A)
$$

**Dem.**
Aplicando la aditividad finita para $A$ y su complementario $A^c$, que son disjuntos, se tiene:

$$
1 = P(\Omega) = P(A \cup A^c) = P(A) + P(A^c) \\
$$

Donde se ha utilizado **A2.** $\square$

**Nota:** sin considerar la aditividad finita es necesario extender la secuencia con vacíos. Por eso, se ha alterado el orden del enunciado.

> d) Probabilidad de la diferencia y monotonía. Sea $B \subseteq A \in \mathcal{A}$, entonces
$$
P(A −B) = P(A) −P(B)
$$ y $P(B) \leq P(A)$

**Dem.**

Consideramos los sucesos disjuntos $B$ y $A-B$, cuya unión es $A$ y aplicamos aditividad finita

$$
P(A) = P(B \cup (A-B)) = P(B) + P(A-B)
$$

Como $P(A-B) \geq 0$ por **A1**, deducimos $P(B) \leq P(A)$. $\square$

## e) A,B ∈A,P(A∪B) = P(A)+P(B)−P(A∩B).

## f) Principio de inclusión-exclusión para la unión finita de sucesos no disjuntos.

## g) Subaditividad: 

P(⋃n∈NAn) ≤∑n∈NP(An).

## h) Desigualdad de Boole: 

P(⋂n∈NAn).≥1 −∑n∈NP(Acn)