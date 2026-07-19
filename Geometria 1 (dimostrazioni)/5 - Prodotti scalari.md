# Formula del cambio di base
Vale che $M_{i,j} = \phi(\underline{v}_{i},\underline{v}_{j})$, di conseguenza $\phi(\underline{v},\underline{w}) = {}^t[\underline{v}]_{\mathscr{B}} M_{\mathscr{B}}(\phi)[\underline{w}]_{\mathscr{B}}$ e il cambio di base avviene per congruenza, ossia coniugio per trasposta anziché per l'inversa.

# Formula della dimensione dell'ortogonale
Dato l'isomorfismo $\delta : V \to V^{* *}$ si ha $\delta(W^\perp)=\text{Ann}(\alpha_{\phi}(W))$ da cui $\dim W^\perp = n - \dim\alpha_{\phi}(W) = n - (\dim W - \dim(W\cap\text{Ker}\alpha_{\phi}) = \dim V - \dim W + \dim (W \cap V^\perp)$.

# Teorema di Lagrange
È sempre possibile trovare una base ortogonale utilizzando algoritmi quali l'algoritmo di ortogonalizzazione di Gram - Schmidt.

# Teorema di Sylvester
Per Lagrange esiste una base ortogonale, decido di mettere in coda i vettori isotropi. Dividendo ogni vettore per la sua norma trovo una base ortonormale, e gli 1 sulla diagonale derivano dai vettori non isotropi, dunque sono una base dell'immagine, che per definizione è il rango della matrice associata.

# Invarianza della segnatura
Prodotti scalari uguali sono congruenti alla stessa matrice associata nella forma di Sylvester, univocamente determinata da $\iota_{+}$, $\iota_{-}$ e $_{\iota_{0}}$ dunque la segnatura è invariante.

# Teorema di rappresentazione di Riesz
Per ipotesi $\phi$ non è degenere, quindi $V^\perp=\text{Ker}(\alpha_{\phi})=\{\underline{0} \} \iff \alpha_{\phi}$ è un isomorfismo.

# Teorema spettrale
Sono necessari tre lemmi:
1. $f$ hermitiano o simmetrico $\implies$ ha tutti autovalori reali. Infatti, dati $\lambda$ autovalore dell'autovettore $\underline{v}$, vale $\phi(\underline{v},f(\underline{v})) = \phi(\underline{v}, \lambda \underline{v}) = \lambda \phi(\underline{v},\underline{v})$, ma $\phi(\underline{v},\underline{v})$ non è nullo e $\lambda \in \mathbb{R}$.
2. $f$ hermitiano o simmetrico $\implies$ autospazi relativi ad autovettori distinti sono ortogonali. Infatti dati $f(\underline{v}) = \lambda \underline{v}$ e $f(\underline{w}) = \mu \underline{w}$, vale $\lambda \phi(\underline{v},\underline{w}) = \phi(\lambda \underline{v}, \underline{w}) = \phi(f(\underline{v}), \underline{w}) = \phi(\underline{v}, f(\underline{w})) = \phi(\underline{v}, \mu \underline{w}) = \mu \phi(\underline{v}, \underline{w}) \implies \phi(\underline{v},\underline{w})=0$.
3. $f$ hermitiano o simmetrico $\implies$ se $W \subseteq V$ è $f$-invariante, allora $W^\perp$ è $f$-invariante. Infatti se $\underline{v} \in W$ e $\underline{v}' \in W^\perp$, allora $\phi(\underline{v},f(\underline{v}')) = \phi(f(\underline{v}), \underline{v}') = 0$, quindi $f(\underline{v}') \in W^\perp$ e $W^\perp$ è $f$-invariante.
Ora se $W$ si decompone come somma ortogonale degli autospazi, $W$ è $f$-invariante. Se $W \neq V$, per il terzo lemma $V$ è somma diretta ortogonale di $W$ e $W^\perp$. Ma $f|_{W^\perp}$ è hermitiano o simmetrico, quindi ha autovalori reali e ci sono autovettori in $W^\perp$, che è assurdo poiché tutti gli autovettori di $f$ sono in $W$.