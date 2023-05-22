# Función implícita

El teorema de la función implícita es formalmente más general que el de la inversa. En esencia son equivalentes ya que la demostración del primero se consigue fácilmente a partir del segundo. Sin enmbargo, el teorema de la función implícita está más preparado para usarlo en la práctica.

## Planteamiento

El teorema de la función inversa resuelve localmente algunos sistemas de ecuaciones.

Dada una función $f=(f_1, f_2, \dots, f_N) : A \rightarrow \mathbb{R}^N$
donde $A$ es un abierto de $\mathbb{R}^N$, consideramos el sistema de $N$ ecuaciones

$$
f_1(x_1, x_2, \dots, x_N) - y_1 = 0 \\
f_2(x_1, x_2, \dots, x_N) - y_2 = 0 \\
\dots \ \dots \ \dots \ \dots \ \dots \ \dots \\
f_N(x_1, x_2, \dots, x_N) - y_N = 0 \\
$$

en el que intervienen $2N$ variables reales $x_1, x_2, \dots x_N, y_1, \dots, y_N$ que sólo están sometidas a la condición $x = (x_1, x_2, \dots, x_N) \in A$. Escribiendo también $y=(y_1, y_2, \dots, y_N) \in \mathbb{R}^N$ el sistema anterior se resume en una sola ecuación vectorial

$$
f(x) - y = 0
$$

con dos variables vectorialews $x$ e $y$. Sus soluciones son todos los pares $(x, y) \in A \times \mathbb{R}^N$ tales que $f(x) - y = 0$. Intentamos que $x$ e $y$ tengan, en lo posible, un papel simétrico.


La soluciones son todos los pares $(x, f(x))$ con $x \in A$.

$$
\{(x, y) \in A \times \mathbb{R}^N : f(x)-y=0\} = \{(x, f(x)): x \in A\}
$$

El problema no trivial es el recíproco. Resolver la ecuación con $y$ como dato y $x$ como incógnita, es decir, expresar las soluciones en la forma $(g(y), y)$ para conveniente función $g$, o si se quiere, "despejar" $x$ como función de $y$. Claro está que esto equivale a invertir la función $f$.

Cuando $f$ es inyectiva, la respuesta es la función $g=f^{-1}$, definida en el conjunto $f(A)$. Lo podemos expresar como

$$
\{(x, y) \in A \times \mathbb{R}^N: f(x) - y = 0\} = \{(g(y), y): y \in f(A)\}
$$


