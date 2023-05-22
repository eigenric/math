
# Funciones

**Proposición**

Sea $f: X \to Y$ aplicación biyectiva, con $f^{-1}: Y \to X$
Sea $\emptyset \neq A \subset Y$, entonces:
$$
f^*(A) = f^{-1}(A)
$$

**Demostracion**
Debemos probar por def que:

$$
\{x\in X: f(x) \in A\} = \{f^{-1}(a): a\in A\}
$$

$\subset$

Sea $x \in f^{*}(A)$, entonces $f(x) \in A$. Como $f$ es biyectiva, $f^{-1}(f(x))=x$. Así pues, se tiene que $x$ es imagen por $f^{-1}$ de $f(x)$, elemento de $A$.
Por tanto $x \in f^{-1}(A)$


$\supset$

Sea $x \in f^{-1}(A)$. Entonces, $\exists y \in A$ tal que $f^{-1}(y) = x$. Como $f$ es biyectiva:

$$
f(x) = f(f^{-1}(y)) = y \in A
$$

Luego, como $f(x) \in A$, se tiene que $x \in f^{*}(A)$.
