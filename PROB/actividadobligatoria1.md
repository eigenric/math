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

**A1.** $P(A) \geq 0 \quad \forall A \in \ ∈A$

**A2.** $P(\Omega) = 1$

**A3.** Para cualquier secuencia $\{A_n\}_{n \in \mathbb{N}} \subseteq \mathcal{A}$ de sucesos disjuntos
$$
P\left(\bigcup_{n\in \mathbb{N}}A_n\right) = \sum_{n∈\mathbb{N}} P(A_n)
$$

# Propiedades

Demostrar, a partir de la definición anterior, las siguientes propiedades:

> c) Aditividad finita para sucesos disjuntos

Basta considerar la secuencia 
$$
P\left(\bigcup_{n=1}^N A_n\right) = \sum_{n=1}^N P(A_n).
$$

> a) $P(\emptyset) = 0$

$$
P(\Omega) = P(\Omega \cup \emptyset) = P(\Omega) + P(\emptyset) \\
P(\emptyset) = 0
$$

Donde se ha utilizado **A3** con $\Omega, \emptyset \in \mathcal{A}$

> b) Probabilidad del suceso complementario: 

$$
P(\Omega) = P(A \cup A^c) = P(A) + P(A^c) = 1 \\
P(A^c) = 1 - P(A)
$$

Donde se ha utilizado que **A1** y **A3** con $A, A^c$ 

## d) Probabilidad de la diferencia y monotonía:

B ⊆A ∈A,P(A −B) = P(A) −P(B),P(B) ≤ P(A).

## e) A,B ∈A,P(A∪B) = P(A)+P(B)−P(A∩B).

## f) Principio de inclusión-exclusión para la unión finita de sucesos no disjuntos.

## g) Subaditividad: 

P(⋃n∈NAn) ≤∑n∈NP(An).

## h) Desigualdad de Boole: 

P(⋂n∈NAn).≥1 −∑n∈NP(Acn)