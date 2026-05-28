# Spazio delle applicazioni lineari
Siano $V$ e $W$ spazi vettoriali su $\mathbb{K}$. Si considera $\mathcal{L}(V,W) = \{ f : V \to W : f\text{ lineare} \}$.

$\mathcal{L}(V,W)$ è uno spazio vettoriale su $\mathbb{K}$ con:
- $(f+g)(\underline{v}) = f(\underline{v})+ g(\underline{v})$
- $(\alpha f)(\underline{v})=\alpha f(\underline{v})$

Fissata una base $\mathscr{B}$ di $V$, l'applicazione $|_{\mathscr{B}} : \mathcal{L}(V,W) \to W^\mathscr{B}$ data da $f \mapsto f|_{\mathscr{B}}$ è bigettiva.

DIMOSTRAZIONE:
1. $\forall \underline{v} \in V$   $\exists!$$\underline{v}=\sum\limits_{i \in J} x_{i}\underline{v}_{i}$ con $x_{i}\neq 0$ per un numero finito di indici
2. $f(\underline{v})=f\left( \sum\limits_{i \in J} x_{i}\underline{v}_{i} \right) = \sum\limits_{i \in J} x_{i}f(\underline{v}_{i})$
3. Viceversa si definisce analogamente $f$

# Matrice associata
Siano $\mathscr{B}=\{ \underline{v}_{1},\dots,\underline{v}_{n} \}$ base di $V$, $\mathscr{B}'$ base di $W$ e $f:V\to W$ lineare. Allora si dice matrice associata nelle basi $\mathscr{B}$ e $\mathscr{B}'$ la matrice $M_{\mathscr{B}'}^\mathscr{B}(f)=[f(\underline{v})]_{\mathscr{B}'}=[[f(\underline{v}_{1})]_{\mathscr{B}'} |\dots| [f(\underline{v}_{n})]_{\mathscr{B}'}] \in \mathscr{M}_{m,n}(\mathbb{K})$.

$[f(\underline{v})]_{\mathscr{B}'} = M_{\mathscr{B}'}^\mathscr{B}(f)[\underline{v}]_{\mathscr{B}}$

L'applicazione $M_{\mathscr{B}'}^\mathscr{B} : \mathcal{L}(V,W) \to \mathscr{M}_{m,n}(\mathbb{K})$ è un isomorfismo.

DIMOSTRAZIONE: $M_{\mathscr{B}'}^\mathscr{B}$ lineare e bigettiva.

$\dim \mathcal{L}(V,W) = \dim \mathscr{M}_{m,n}(\mathbb{K}) = mn$.

Siano $V, W, Z$ spazi vettoriali di basi $\mathscr{B}, \mathscr{B}', \mathscr{B}''$. Si ha $M_{\mathscr{B}''}^\mathscr{B}(g \circ f)=M_{\mathscr{B}''}^{\mathscr{B}'}(g)M_{\mathscr{B}'}^\mathscr{B}(f)$.