>Sea $(X, \mathcal{T})$ espacio topológico
Si $V \in \mathcal{U}^{x_1}$, y $W \in \mathcal{U}^{x_2}$, entonces si $p = (x_1, x_2) \in X \times X$ se tiene que
$$
V\times W \in \mathcal{U}^p_{X\times X}
$$

Por ser $V$ y $W$ entornos de $x_1$, y $x_2$ respectivamente, existen
$\mathcal{O}_{x_1}$, $\mathcal{O}_{x_2}$ abiertos tal que $x_1 \in \mathcal{O_{x_1}} \subset V$ y $x_2 \in \mathcal{O_{x_2}} \subset W$.


Por tanto $\mathcal{O}_{x_1} \times \mathcal{O}_{x_2} \in \mathcal{T}\times \mathcal{T}$ tal que

$p \in \mathcal{O}_{x_1}\times \mathcal{O}_{x_2} \subset V\times W$


Luego $V\times W \in \mathcal{U}_{X\times X}^p$


>  Probar que un espacio $(X, \mathcal{T})$ es Haussdorf si y sólo si la diagonal:
$$
\Delta = \{(x,x) \in X\times X: x \in X\}
$$
es un subconjunto cerrado de $(X\times X, \mathcal{T}\times\mathcal{T})$


$\Rightarrow$

Sea $p \in (X\times X)\setminus \Delta$, entonces las coordenadas de $p=(x_1, x_2)$ son distintas, $x_1 \neq x_2$. Como $(X, \mathcal{T})$ es Haussdorf, existen $V \in \mathcal{U}^{x_1}$, $W \in \mathcal{U}^{x_2}$ tal que $V \cap W = \emptyset$.

Veamos que $V \times W \subset (X\times X)\setminus \Delta$.

Sea $q = (q_1, q_2) \in V \times W \subset X\times X$. Supongamos que $q \in \Delta$ y lleguemos a contradicción. Si $q = (q', q') \in V\times W$, entonces $q' \in V \cap W$, pero esta interseccion es vacía luego $q \notin \Delta$

Por tanto, existe $V\times W$, entorno de $p$ en $X\times X$ tal que
$p \in V \times W \subset (X\times X) \setminus \Delta$.

Luego $(X\times X) \setminus \Delta \in \mathcal{U}_{X\times X}^p \forall p\in X \times X$, lo cual es equivalente a que $(X\times X) \setminus \Delta \in \mathcal{T}$, lo cual es equivalente a que $\Delta \in \mathcal{C}_{\mathcal{T\times T}}$ como se quería

$\Leftarrow$

Volviendo desde atrás, vemos que existe $V'$  entorno de $p$ en $X\times X$ tal que
$p \in V' \subset (X\times X) \setminus \Delta$.
Por tanto 
