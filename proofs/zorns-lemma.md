# Prueba del Lema de Zorn

Es un Lema básico en Teoría de Conjuntos que permite probar la existencia de bases de Espacios Vectoriales, entre otros resultados de Álgebra abstracta.

## Definiciones previas

> **Def.** Se dice que $(X, \leq)$ es un **conjunto parcialmente ordenado (o poset**) cuando algunos elementos pueden ser comparados (tricotomía $\lt, = \gt)$.

> **Def.**  Se dice que $(X, \leq)$ es un **conjunto totalmente ordenado** cuando todos los elementos son comparables.

En lo siguiente $(X, \leq)$ es un conjunto parcialmente ordenado o poset.

> **Def.** Se dice que $C \subset X$ es una **cadena de $X$** cuando $(C, \leq)$ es totalmente ordenado.

> **Def.**: Se dice que $(A, \leq)$ es un conjunto **bien ordenado** cuando todo subconjunto suyo no vacío tiene mínimo. 
La clase de subconjuntos de $X$ bien ordenados se denota 
$$Well(X)$$

> **Def.** Sea $S \subset X$. Se dice que $m \in S$ es un **elemento maximal** cuando no hay elemento de $S$ (estrictamente) mayor.

*Observación:* el elemento maximal no tiene por qué ser único. No confundir con el mayor elemento. Éste es mayor que todos (y por tanto comparable) lo cual no tiene por que suceder con el elemento maximal.
En un conjunto totalmente ordenado coinciden y se denomina máximo.

> **Def.** $S \subseteq X$ es un **conjunto cerrado inferiormente** en $X$ si para cualquier $u \in S$, si $v \in X$ tal que $v \lt u$ entonces $v \in S$. 

**Observación:** Todo conjunto es cerrado inferiormente en sí mismo.


> **Def.** Si $C$ es cadena de $X$ y $x \in X$, entonces llamamos **segmento inicial** de $x$ en $C$ a los elementos de $C$ estrictamente menores que $x$.
$$
    I_c(x) = \{y \in C : y \lt x\}
$$

**Observación:** los segmentos iniciales son cerrados inferiormente.

## Teorema (Lema de Zorn). 

> **Lema de Zorn.** Si $(X, \leq)$ es poset en el que toda cadena está acotada superiormente. Entonces $(X, \leq)$ tiene un elemento maximal.

Supongamos que $(X, \leq)$ no tiene elemento maximal y lleguemos a contradicción. Sea $C$ una cadena en $X$, y por hipótesis $u \in X$ una cota superior de $C$. Como no hay elemento maximal, necesariamente existe $v \in X$ tal que $u \lt v$. Luego $C$ admite una **cota superior estricta.**

Utilizando el Axioma de Elección, existe una función $f$ que asigna a cadena $C \subset X$ bien ordenada una cota superior estricta $f(C)$.

La contradicción buscada consistirá en encontrar una cadena $U \subset X$ tal que $f(U) \in U$.

Para ello, definimos la noción de conjunto $f$-inductivo.

> **Def.** $A \in Well(S)$ es **f-inductivo** si para todo $x \in A$
$$
x = f(I_A(x))
$$

Los conjuntos f-inductivos cumplen el siguiente **lema de comparación**.

> **Lema:** Si $A, B \subset X$ son f-inductivos y $A \neq B$, entonces uno de los dos es segmento inicial del otro.

**Dem**.

Como $A \neq B$ podemos asumir sin pérdida de generalidad que $A \setminus B \neq \emptyset$.

Sea $x = \min(A \setminus B)$, probaremos que $B$ es segmento inicial de $x$ en $A$

$$I_A(x) = B$$


$\boxed{\subset}\;\;$

Sea $y \in I_A(x)$ entonces $y \in A$ tal que $y \lt x$. Como $x = \min(A \setminus B)$. Si $y \notin B$ entonces $y \in A \setminus B$ siendo menor que el mínimo. Luego $y \in B$


$\boxed{\supset}\;\;$

Supongamos $B \setminus I_A(x) \neq \emptyset$ y lleguemos a contradicción.

Sea $y = \min(B \setminus I_A(x))$.
Sea $z = \min(A \setminus I_B(y))$.

> **Lema de Cierre.** Dado cualquier $u \in I_B(y)$, si $v \in A$ y $v \lt u$ entonces:

> - $v \lt y$  (por def. de $I_B(y)$)
> - $v \in B$ 

> Luego $v \in I_B(y)$

**Dem**.
Basta ver por qué $v \in B$.
Como $u \in I_B(y)$, $u \in B$ y $u \lt y$. 
Por def. $y = \min(B \setminus I_A(x))$, luego si $u \notin I_A(x)$, entonces $u \in B \setminus I_A(x)$  siendo menor que el mínimo.
Por tanto $u \in I_A(x)$
Como $v \in A$ tal que $v \lt u$, es claro que $v \in I_A(x) \subset B$. $\square$

Con este resultado podemos probar que
$$
I_A(z) = I_B(y)
$$

- $I_A(z) \subset I_B(y)$

Sea $u \in I_A(z)$, entonces $u \in A$ tal que $u \lt z$.
Como $z = \min(A \setminus I_B(y))$, si $u \notin I_B(y)$ entonces $u \in A \setminus I_B(y)$ siendo menor que el mínimo.
Por tanto $u \in I_B(y)$


- $I_A(z) \supset I_B(y)$

Sea $u \in I_B(y)$ entonces $u \in I_A(x)$ (por def. de $y$), luego $u \in A$ y podemos compararlo con $z$.
Es claro que $u \neq z$ por def de $z$.
Además si $z \lt u$, por el *Lema de Cierre*, se tendría que $z \in I_B(y)$ contradiciendo la def. de $z$.
Por tanto $u \lt z$. Como $u \in A$, se sigue que $u \in I_A(z)$.

Además, $z \leq x$ por ser

$$ A \setminus B \subset A \setminus I_B(y)$$

Usando **f-inductividad** de $A$ y $B$ tendríamos que 

$z = f(I_A(z)) = f(I_B(y)) = y$

Y como $y \in B$ no puede ser $z = x$ (ya que $x \notin B$ por def.).
Por tanto, $z \lt x$ y concluimos que 
$$y = z \in I_A(x)$$

en contra de la def. de $y$.

Esto implica $B \setminus I_A(x) = \emptyset$ o equivalentemente $B \subset I_A(x)$. $\square$.


> **Lema de Comparación** nLab.

**Dem**
Sean $A \neq B$ subconjuntos f-inductivos en $X$. 

Sea $I$ la unión de todos los subconjuntos cerrados inferiormente (ci) en $A$ y en $B$ (en ambos).

$$
I = \bigcup_{S \ ci \ A, B}S \subset A \cap B
$$

Sea $u \in I$ entonces existe $S_u$ cerrado inferiormente en $A$ y en $B$ tal que $u \in S_u$.
Si $v \in A \cup B$, y $v \lt u$ entonces por ser $S_u$ cerrado inferiormente en $A$ y en $B$ se sigue que $v \in S_u \subset I$.
Luego $I$ es cerrado inferiormente en $A$ y en $B$.
Además es maximal entre estos conjuntos pues cualquier $S$ c.i en $A$ y en $B$ está contenido en $I$.

Supongamos $I \subsetneq A$ y $I \subsetneq B$ y lleguemos a contradicción.

Sea $y = \min(A \setminus I)$
Sea $z = \min(B \setminus I)$

Entonces,

$$
I_A(y) = I = I_B(z)
$$

- $I_A(y) \subset I$

Sea $u \in I_A(y)$ entonces $u \lt y$. Como $y = \min(A \setminus I)$ necesariamente $u \in I$.

- $I_A(y) \supset I$

Sea $u \in I \subsetneq A$ luego puedo compararlo con $y$.
Es claro que $u \neq y$ porque $y \notin I$.
Si $y \lt u$, entonces por ser $I$ cerrado inferiormente en $A$ se tendría $y \in I$ en contra de la def. de $y$.
Necesariamete $u \lt y$. Luego $u \in I_A(y)$.

Análogo para la otra igualdad y observamos que $I$ es segmento inicial de $A$ y de $B$ (más fuerte que c.i)

Por $f$-inductividad:

$$
y = f(I) = z
$$

Así, podemos extender $I$ a un conjunto cerrado inferiormente en $A$ y en $B$.
$$
I \cup \{y\} = I \cup \{z\} = I'
$$

En efecto como $I$ ya es cerrado inferiormente basta escoger $y=z \in I'$.  Sea $u \in A \cup B$ tal que
$u \lt y = z$, necesariamente $u \in I_A(y) =  I_B(z) = I \subset I'$.

Como $y = z \notin I$, se sigue que $I \subsetneq I'$ contradiciendo la maximalidad de $I$.

Por tanto, $I = A$ o $I = B$, luego uno es segmento inicial del otro. $\square$

> **Lemma 2.6** Sea $U_\alpha$ una colección de subconjuntos de $X$, cada con un buen-orden $\leq_\alpha$, tal que para cualquier $\alpha, \beta$, uno de $U_\alpha$, $U_\beta$ (cada uno con su orden) es un segmento inicial del otro. Sea $U$ la unión $\cup_\alpha \ U_\alpha$, equipada con el orden $x \leq y$ sii por def. $x \leq_\alpha y$ en algún $U_\alpha$ que contenga a ambos. Entonces $U$ está bien ordenado por $\leq$, con cada $U_\alpha$ un segmento inicial de $U$

**Dem**

Observamos que $\leq$ está bien definido y es un orden total. Sean $x, y \in U$, entonces $x \in U_\alpha$ e $y \in U_\beta$ para ciertos $\alpha, \beta$, donde uno de $U_\alpha, U_\beta$ es segmento inicial del otro. Sin pérdida de generalidad, suponemos $U_\alpha \subset U_\beta$ entonces $x, y$ son comparables en $U_\beta$.

Sea 

Por el **Lema de Comparación** es claro que la unión $U$ de todos los conjuntos f-inductivos de $x$ es f-inductiva.

