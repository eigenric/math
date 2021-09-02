# Prueba del Lema de Zorn

Es un Lema básico en Teoría de Conjuntos que permite probar la existencia de bases de Espacios Vectoriales, entre otros resultados de Álgebra abstracta.

## Definiciones previas

> **Def.** Se dice que $(X, \leq)$ es un **conjunto parcialmente ordenado (o poset**) cuando algunos elementos pueden ser comparados (tricotomía $\lt, = \gt)$.

> **Def.**  Se dice que $(X, \leq)$ es un **conjunto totalmente ordenado** cuando todos los elementos son comparables.

En lo siguiente $(X, \leq)$ es un conjunto parcialmente ordenado o poset.

> **Def.** Se dice que $C \subset X$ es una **cadena de $X$** cuando $(C, \leq)$ es totalmente ordenado.

> **Def.**: 

> **Def.** Sea $S \subset X$. Se dice que $m \in S$ es un **elemento maximal** cuando no hay elemento de $S$ (estrictamente) mayor.

*Observación:* el elemento maximal no tiene por qué ser único. No confundir con el mayor elemento. Éste es mayor que todos (y por tanto comparable) lo cual no tiene por que suceder con el elemento maximal.
En un conjunto totalmente ordenado coinciden y se denomina máximo.

> **Def.** Si $C$ es cadena de $X$ y $x \in X$, entonces llamamos **segmento inicial** de $x$ en $C$ a los elementos de $C$ estrictamente menores que $x$.
$$
    I_c(x) = \{y \in C : y \lt x\}
$$

## Teorema (Lema de Zorn). 

> **Lema de Zorn.** Si $(X, \leq)$ es poset en el que toda cadena está acotada superiormente. Entonces $(X, \leq)$ tiene un elemento maximal.

Supongamos que $(X, \leq)$ no tiene elemento maximal y lleguemos a contradicción. Sea $C$ una cadena en $X$, y por hipótesis $u \in X$ una cota superior de $C$. Como no hay elemento maximal, necesariamente existe $v \in X$ tal que $u \lt v$. Luego $C$ admite una **cota superior estricta.**

Utilizando el Axioma de Elección, existe una función $f$ que asigna a cadena $C \subset X$ bien ordenada una cota superior estricta $f(C)$.

La contradicción buscada consistirá en encontrar una $U \$ tal que $f(U) \in U$.

Para ello, definimos la noción de conjunto $f$-inductivo.

> **Def.** $W \in Well(S)$.