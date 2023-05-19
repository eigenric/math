# Teoría de Conjuntos

> **Prop.** $A \setminus B = \emptyset \Leftrightarrow A \subseteq B$

**Dem**

$\boxed{\Rightarrow}$

Si $x \in A$. Si $x \notin B$ entonces $x \in A \setminus B$ imposible por ser vacío. Luego $x \in B$.

$\boxed{\Leftarrow}$
No hay $x \in A$ tal que $x \notin B$


> **Prop.** $A \setminus B \neq \emptyset \Leftrightarrow A \nsubseteq B$


**Dem**
$A \nsubseteq B$ es equivalente a que exista $x \in A$ tal que $x \notin B$.


> **Lema** Si $A \neq B$, entonces podemos asumir sin pérdida de generalidad que $A \setminus B \neq \emptyset$

Es claro que $A \neq B$ equivale a que $A \nsubseteq B$ o bien $B \nsubseteq A$, luego por la proposición anterior $A \setminus B = \emptyset$ ó $B \setminus A = \emptyset$. Si se da lo segundo, intercambiamos el papel de $A$ y $B$.