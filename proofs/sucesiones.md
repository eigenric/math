## Sucesiones

**Toda sucesión convergente es acotada**


**El límite de las diferencias de los términos de una sucesión convergente respecto a su límite es cero**

Sea $\{x_n\}$ una sucesión convergente a $x$, entonces:


$$
  \lim \{x_n - x\} = 0 \Longleftrightarrow \lim \{x_n\} = x
$$

**Demostración**


Para los dos casos, por def de convergencia, $\forall \varepsilon > 0$, existe un
natural $m$, tal que a partir del término $m$ en adelante:

$$
||x_n - x|| = |x_n - x| \lt \varepsilon
$$

<br>

**Una sucesión es convergente si y sólo si se acumula en un entorno de x**

Sea $\{x_n\}$ una sucesión de números reales:

  $$
  \{x_n \} \rightarrow x \Longleftrightarrow
  x_n \in ]x - \varepsilon, x+ \varepsilon ]
  \quad \forall \varepsilon > 0
  $$

**Demostración**

Por def

$\forall \varepsilon > 0, \exists m \in \mathbb{N}:
\forall n \geq m$

$$
| x_n -x | \lt \varepsilon \quad \Longleftrightarrow
$$

Luego

$$
\left.\begin{array}{l}
x_n - x \lt \varepsilon \\
x - x_n \lt \varepsilon \Rightarrow x_n - x \gt -\varepsilon
\end{array}\right\} \Longleftrightarrow

-\varepsilon \lt x_n - x \lt \varepsilon \quad
$$
Y sumando x

$$
x-\varepsilon \lt x_n \lt x + \varepsilon \Longleftrightarrow x_n \in ]x-\varepsilon, x+\varepsilon[
$$
Como se quería demostrar

<br>

**El producto de una sucesión convergente a cero por una sucesión
acotada es una sucesión convergente a 0**

Sea $\{x_n\} \rightarrow 0$, e $\{y_n\}$ acotada.
Sea $c > |y_n| \quad \forall n \in \mathbb{N}$. Dado $\varepsilon > 0$,
existe un número natural $m$ tal que para todo $n \geq m$ se verifica
$|x_n|< \frac{\varepsilon}{c}$.
Deducimos que para todo $n \geq m$, se verifica que

$$
|x_n y_n| = |x_n||y_n| \lt \frac{\varepsilon}{c} c = \varepsilon
$$

lo que prueba que $\{x_n y_n\} \rightarrow 0$

**El límite de la sucesión de los términos opuestos de una sucesión
convergente es el opuesto de su límite**

Sea $\{y_n\}$ una sucesión convergente tal que $\{y_n\} \rightarrow y$.

Entonces:

$$
\{-y_n\} \rightarrow  - y
$$

**Demostración**

Por la convergencia de $\{y_n\}$, tenemos que dado un $\varepsilon \gt 0$,
existirá un $m \in \mathbb{N}$, tal que todo término de la sucesión
a partir de $m$ en adelante:


$$y-\varepsilon \lt y_n \lt y + \varepsilon$$

Multiplicando por $-1$
$$-y+\varepsilon \gt -y_n \gt -y - \varepsilon$$
$$ -y-\varepsilon \lt -y_n \lt -y + \varepsilon$$

lo cual prueba que $\{-y_n\} \rightarrow -y$


**La sucesión suma dos sucesiones convergente es convergente y su
límite es la suma de los límites de las sucesiones.**

Sean $\{x_n\} \rightarrow x$ e $\{y_n\} \rightarrow y$, entonces

$$\{x_n + y_n\} \rightarrow x+y$$

**Demostración**

Dado $\varepsilon \gt 0$

Por la convergencia de $\{x_n\}$, existe
un $m\in\mathbb{N}$ tal que para todo término de la sucesión
partir de $m$ en adelante:

$$x-\frac{\varepsilon}{2} \lt x_n \lt x + \frac{\varepsilon}{2}$$


Por la convergencia de $\{y_n\}$, existe
un $m'\in\mathbb{N}$ tal que para todo término de la sucesión
a partir de $m'$ en adelante:

$$y-\frac{\varepsilon}{2} \lt y_n \lt y + \frac{\varepsilon}{2}$$

Luego sea $p=\max\{m, m'\}$, entonces para todo $p \geq n$, se
verifican las dos ecuaciones anteriores.

Sumándolas, se obtiene:

$$
x+y-\varepsilon \lt x_n + y_n \lt x + y + \varepsilon  \\
$$

Luego, hemos llegado a que la sucesión $\{x_n + y_n\}$ converge y se verifican que
$$
\{x_n + y_n\} \rightarrow x+y
$$

**Corolario**

**La sucesión resta de dos sucesiones convergentes es convergente y
su límite es la resta de los límites de las sucesiones**

Como si $\{y_n\} \rightarrow y \Rightarrow \{-y_n\} \rightarrow -y$ ,
se verifica que

$$
\{x_n - y_n\} \rightarrow x - y
$$

**El producto de dos sucesiones convergentes es convergente, y
su límite es el producto de los límites**


Sean $\{x_n\} \rightarrow x$ e $\{y_n\} \rightarrow y$, entonces

$$\{x_ny_n\} \rightarrow xy$$

**Demostración**
