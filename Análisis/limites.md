## Límite funcional

### Punto de Acumulación

**Definición**

Se dice que $\alpha \in \mathbb{R}$ es un punto de acumulación de $A$ si
existe una sucesión de puntos de $A \setminus \{\alpha\}$ que
convergente a  $\alpha$. El conjunto de todos los puntos de acumulación de $A$ se denota por $A'$

Simbólicamente:

$$
\alpha \in A' \Longleftrightarrow
\exists \{x_n\}
\left\{\begin{array}{l}
 x_n \in A \setminus \{\alpha\} \quad \forall n \in \mathbb{N} \\
 \{x_n\} \rightarrow \alpha
\end{array}\right.
$$

**Proposición**

$\alpha$ es punto de acumulación de $A$ sii hay puntos de
$A \setminus \{\alpha\}$ en un entorno de $\alpha$.


$$
\alpha \in A' \Longleftrightarrow
\quad ]\alpha-\delta, \alpha+\delta[ \space \cap \space (A \setminus \{\alpha\}) \neq \emptyset
\quad \forall \delta > 0
$$

**Demostración**

$\Rightarrow$

Por def. de punto de acumulación, existe una sucesión de puntos
de $A \setminus \{\alpha\}$ que converge a $\alpha$. Luego esta sucesión
se acumula en un entorno de $\alpha$

$$
x_n \in ]\alpha-\delta, \alpha+\delta[ \quad \forall \delta > 0
$$

Y como la sucesión es de puntos de $A \setminus \{\alpha\}$,
se verifica

$$
\quad ]\alpha-\delta, \alpha+\delta[ \space \cap \space (A \setminus \{\alpha\}) \neq \emptyset
\quad \forall \delta > 0
$$

$\Leftarrow$

Tomando $\delta = \frac{1}{n} \quad \forall n \in \mathbb{N}$.
Existirá $x_n \in A$ tal que $0 < |x_n - \alpha | < \frac{1}{n}$.
Por tanto, existe una sucesión de puntos de  puntos de $A \setminus \{\alpha\}$ que converge a $\alpha$.

### Concepto de límite.

Sea $f: A \rightarrow \mathbb{R}$


Dado $\alpha \in A'$, se dice que $f$ tiene límite en el punto $\alpha$
cuando existe $L \in \mathbb{R}$, tal que para cualquier sucesión de puntos de $A$ distintos de $\alpha$ que converja a $\alpha$, se
tiene que la sucesión de las imágenes converge a $L$

$$
\lim_{x\to\alpha} f(x) = L \Longleftrightarrow
[\space x_n \in A \setminus \{\alpha\} \space \forall n \in \mathbb{N},
\{x_n\} \rightarrow \alpha
\Longrightarrow  \{f(x_n)\} \rightarrow L \space]
$$

### Álgebra de límites

**Proposición**

El límite de la suma de funciones con límites cuando $x$ tiende
a $\alpha$ es la suma de esos límites.

$$
\lim_{x\to\alpha} f(x) + g(x) = \lim_{x\to\alpha} f(x) + \lim_{x\to\alpha} g(x)
$$

**Demostración**

Sean $f: A \rightarrow \mathbb{R}$, $\quad g: B \rightarrow \mathbb{R}$,
con límites $L$ y $L'$ cuando $x$ tiende a $\alpha$

Sea $\{x_n\}$ una sucesión de puntos de $A$ distintos de $\alpha$ que
converja a $\alpha$, entonces por def. de límite, se tiene que

$$\{f(x_n)\} \rightarrow \lim_{x\to\alpha} f(x)$$

$$\{g(x_n)\} \rightarrow \lim_{x\to\alpha} g(x)$$

Y como el límite de la suma de sucesiones convergentes es la suma
de sus límites:

$$\{f(x_n) + g(x_n)\} \rightarrow \lim_{x\to\alpha} f(x) + \lim_{x\to\alpha} g(x)$$

**Proposición**

El límite del opuesto de una función con límite cuando $x$ tiende
a $\alpha$ es el opuesto de su límite.

$$
\lim_{x\to\alpha} -f(x) = -\lim_{x_\to\alpha} f(x)
$$

**Demostración**

Sea $\{x_n\}$ una sucesión de puntos de $A$ distintos de $\alpha$,
entonces por def. de límite:

$$\{f(x_n)\} \rightarrow \lim_{x\to\alpha} f(x)$$
Y como el límite de la sucesión de opuestos de una sucesión
convergente es el opuesto de su límite:


$$\{-f(x_n)\} \rightarrow -\lim_{x\to\alpha} f(x)$$


**Corolario**

$$
\lim_{x\to\alpha} (f(x) - g(x)) =
\lim_{x\to\alpha} f(x) + \lim_{x\to\alpha}-g(x) = \\
\lim_{x\to\alpha} f(x) - \lim_{x\to\alpha} g(x)

$$
