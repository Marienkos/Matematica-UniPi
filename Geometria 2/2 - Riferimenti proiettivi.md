# Riferimento proiettivo
Sia $\mathbb{P}(V)$ uno spazio proiettivo. Dei punti $P_{i}=[v_{i}]$ con $v_{i} \in V$ si dicono indipendenti se i $v_{i}$ sono linearmente indipendenti.

$P_{1},\dots, P_{k}$ indipendenti $\iff \dim L(P_{1},\dots,P_{k})=k-1$.

Sia $\dim \mathbb{P}(V) = n$. Dei punti $P_{i}$ si dicono in posizione generale se ogni suo sottoinsieme di $h\leq n+1$ punti è indipendente.

Un riferimento proiettivo di $\mathbb{P}(V)$ con $\dim \mathbb{P}(V)=n$ è una $(n+2)$-upla ordinata di punti $\mathscr{R}=(P_{0},\dots,P_{n+1})$ in posizione generale.

I punti $P_{0},\dots,P_{n}$ sono detti fondamentali e $P_{n+1}$ è detto d'unità.

Sia $\mathscr{R}$ un riferimento proiettivo di $\mathbb{P}(V)$, si dice base normalizzata di $V$ associata a $\mathscr{R}$ una base $(v_{0},\dots,v_{n})$ di $V$ tale che $[v_{i}]=P_{i}$ e $P_{n+1}=[v_{0}+\dots+v_{n}]$.

Sia $\mathscr{R}$ un riferimento proiettivo di $\mathbb{P}(V)$, allora:
1. $\exists$ base normalizzata $(v_{0},\dots,v_{n})$ di $V$ rispetto a $\mathscr{R}$
2. $(v_{0}',\dots,v_{n}')$ base normalizzata di $V$ rispetto a $\mathscr{R} \implies \exists \lambda\neq 0$   $v_{i}' = \lambda v_{i}$

DIMOSTRAZIONE:
- (1.)
	1. $v_{0},\dots,v_{n}$ base di $V$ e $P_{n+1}:=[v_{n+1}]$
	2. $v_{n+1}=a_{0}v_{0}+\dots+a_{n}v_{n}$
	3. Per assurdo ogni $a_{i} \neq 0$, ci sarebbe una relazione di lineare dipendenza
	4. Ponendo $w_{i}=a_{i}v_{i}$ vale $(w_{0},\dots,w_{n})$ base normalizzata di $V$ rispetto a $\mathscr{R}$
- (2.)
	1. $[v_{i}']=P_{i}=[w_{i}]$ e $[v_{0}'+\dots+v_{n}']=P_{n+1}=[w_{0}+\dots+w_{n}]$
	2. $v_{i}'=\lambda_{i}w_{i}$ e $\exists \lambda \neq 0$   $v_{0}'+\dots+v_{n}' = \lambda(w_{0}+\dots+w_{n})$
	3. Dato che $(w_{0},\dots,w_{n})$ è una base, si può porre $\lambda_{i}=\lambda$

Siano $f,g : \mathbb{P}(V) \to \mathbb{P}(W)$ trasformazioni proiettive e $\varphi,\psi : V \to W$ lineari tali che $f=[\varphi]$ e $g = [\psi]$. Allora sono equivalenti:
1. $\exists \lambda \in \mathbb{K} \setminus \{ 0 \}$   $\psi = \lambda \varphi$
2. $f = g$
3. $f(P) = g(P)$   $\forall P \in \mathscr{R}$ riferimento proiettivo di $\mathbb{P}(V)$


DIMOSTRAZIONE:
- ($1 \implies 2$) Sia $\psi = \lambda\varphi$, allora $\forall P \in \mathbb{P}(V)$   $g(P)=[\psi(v)] = [\lambda\varphi(v)] = [\varphi(v)] = f(P)$
- $(2 \implies 3)$ Ovvia
- ($3 \implies 1$)
	1. Sia $\mathscr{R}$ un riferimento proiettivo tale che $f(P)=g(P)$   $\forall P \in \mathscr{R}$
	2. Sia $(v_{0},\dots,v_{n})$ una base normalizzata di $V$ rispetto a $\mathscr{R}=\{ P_{0},\dots,P_{n+1} \}$
	3. $[\varphi(v_{i})]=f(P_{i})=g(P_{i})=[\psi(v_{i})]$   $\forall i=0,\dots,n$
	4. $[\varphi(v_{0} + \dots + v_{n})] = f(P_{n+1})=g(P_{n+1})=[\psi(v_{0}+\dots+v_{n})]$
	5. $\forall i=0,\dots,n$   $\exists \lambda_{i} \in \mathbb{K} \setminus \{ 0 \}$   $\varphi(v_{i})=\lambda_{i}\varphi(v_{i})$
	6. $\exists \lambda \in \mathbb{K} \setminus \{ 0 \}$   $\psi(v_{0}+\dots+v_{n})=\lambda\varphi(v_{0}+\dots+v_{n})$
	7. $(v_{0},\dots,v_{n})$ base di $V \land \varphi$ iniettiva $\implies \varphi(v_{0}),\dots,\varphi(v_{n})$ indipendenti
	8. $\lambda_{i}=\lambda$   $\forall i = 0,\dots,n$   e   $\psi = \lambda\varphi$

Sia $N = \{ \lambda \text{Id}_{V} : \lambda \in \mathbb{K} \setminus \{ 0 \} \} \lhd \text{GL}(V)$, allora $\mathbb{P}\text{GL}(V) \cong \text{GL}(V) / N$.

DIMOSTRAZIONE:
1. Si considera $\text{GL}(V) \to \mathbb{P}\text{GL}(V)$ tale che $\varphi \mapsto [\varphi]$
2. L'omomorfismo è surgettivo per definizione di trasformazione proiettiva
3. Il nucleo è $N$ per il teorema precedente
4. La tesi segue dal primo teorema di omomorfismo

Se $V = \mathbb{K}^{n+1}$, allora $\mathbb{P}(V) = \mathbb{P}(\mathbb{K}^{n+1}) = \mathbb{P}^n(\mathbb{K})$.

Il gruppo delle proiettività di $\mathbb{P}^n(\mathbb{K})$ si indica con $\mathbb{P}\text{GL}(\mathbb{K}^{n+1})=\mathbb{P}\text{GL}_{n+1}(\mathbb{K})$.

# Teorema fondamentale delle trasformazioni proiettive
Siano $\mathbb{P}(V)$ e $\mathbb{P}(W)$ spazi proiettivi con $\dim=n$, e siano $\mathscr{R}$ e $\mathscr{R}'$ rispettivi riferimenti proiettivi.
Allora $\exists! f : \mathbb{P}(V) \to \mathbb{P}(W)$ trasformazione proiettiva che manda ordinatamente $\mathscr{R}$ in $\mathscr{R}'$.

DIMOSTRAZIONE:
1. L'unicità segue dal teorema precedente
2. Siano $(v_{0},\dots,v_{n})$ e $(w_{0},\dots,w_{n})$ basi normalizzate per $\mathscr{R}$ e $\mathscr{R}'$ rispettivamente
3. Sia $\varphi : V \to W$ unica trasformazione tale che $\varphi(v_{i})=w_{i}$   $\forall i = 0,\dots,n$
4. $f = [\varphi]$ soddisfa la tesi

# Coordinate omogenee
Un riferimento proiettivo determina un sistema di coordinate omogenee su $\mathbb{P}(V)$.

Si chiama riferimento proiettivo standard di $\mathbb{P}^n(\mathbb{K})$ dato da $P_{i}=[e_{i}]$ e $P_{n+1}=[(1,\dots,1)]$.

Si dice che il punto $[(x_{0},\dots,x_{n})] \in \mathbb{P}^n(\mathbb{K})$ ha coordinate omogenee $[x_{0},\dots,x_{n}]$ rispetto al riferimento proiettivo standard di $\mathbb{P}^n(\mathbb{K})$.

Le coordinate omogenee sono uniche a meno di riscalamento simultaneo.

Sia $\mathscr{R}=(P_{0},\dots,P_{n+1})$ riferimento proiettivo di $\mathbb{P}(V)$. Allora $\mathscr{R}$ induce coordinate omogenee su $\mathbb{P}(V)$ in due modi equivalenti:
1. sia $f$ unica trasformazione proiettiva che manda $\mathscr{R}$ nel riferimento standard, le coordinate omogenee di $P$ indotte da $\mathscr{R}$ sono $f(P)$
2. sia $(v_{0},\dots,v_{n})$ base normalizzata di $V$ rispetto a $\mathscr{R}$, dato $P=[v]$ si scrive unicamente $v = a_{0}v_{0} + \dots + a_{n}v_{n}$ e le coordinate omogenee sono $a_{i}$

DIMOSTRAZIONE (Equivalenza): Costruzione di $f$ secondo il teorema fondamentale.

# Rappresentazione di trasformazioni
Siano:
1. $f : \mathbb{P}(V) \to \mathbb{P}(W)$ trasformazione proiettiva
2. $\mathscr{R}$ e $\mathscr{R}'$ riferimenti proiettivi rispettivi
3. $\mathscr{B}$ e $\mathscr{B}'$ basi normalizzate rispettive
4. $\varphi : V \to W$ trasformazione lineare che induce $f$
5. $M$ matrice associata a $\varphi$
6. $v \in V$ tale che $[v] = P$
Allora $[f(P)]_{\mathscr{R}'}=[M[v]_{\mathscr{B}}]$.

La matrice che rappresenta $f$ è unica a meno di riscalamento.

Siano $n = \dim\mathbb{P}(V)$ e $m = \dim \mathbb{P}(W)$, allora la matrice ha taglia $(m+1) \times (n+1)$.

# Rappresentazione di sottospazi
Sia $S \subseteq \mathbb{P}(V)$ sottospazio proiettivo $S = \mathbb{P}(W)$ con $W \subseteq V$ sottospazio vettoriale. Sia $\dim \mathbb{P}(V) = n+1$ e $\dim W = k+1$. Allora $W$ si può descrivere dentro $V$ con un sistema lineare di $n-k$ equazioni indipendenti usando le coordinate indotte su $V$ da una base normalizzata rispetto a $\mathscr{R}$ fissata.

La rappresentazione $W = \{ f_{1}=\dots=f_{n-k}=0 \}$ è detta cartesiana e valgono:
1. $f_{i}$ sono lineari omogenee
2. $f_{i}$ descrivono $S$ dentro $\mathbb{P}(V)$, ossia $[v] \in S \iff [v]$ soddisfano $f_{i}$

# Prospettività
Siano:
- $\mathbb{P}(V)$ piano proiettivo
- $r,s \in \mathbb{P}(V)$ rette distinte
- $A = r \cap s$
- $O \in \mathbb{P}(V) \setminus (r \cup s)$
Allora $\pi_{O} : r \to s : P \mapsto L(O,P) \cap s$ si dice prospettività di centro $O$.

$\pi_{O}$ trasformazione proiettiva.

DIMOSTRAZIONE:
1. Si considera un riferimento dato da $A$, $B \in r$, $C \in s$, $D = O$
2. In queste coordinate $A=e_{1}$, $B=e_{2}$, $C=e_{3}$, $D = \left(\begin{smallmatrix} 1 \\ 1 \\ 1 \end{smallmatrix}\right)$
3. Sulle coordinate agisce $\pi_{O}$ come una trasformazione di matrice $\left(\begin{smallmatrix} -1 & 1 \\ 0 & 1 \end{smallmatrix}\right)$

$f$ trasformazione proiettiva è una prospettività $\iff f(A) = A$.

DIMOSTRAZIONE:
- ($\implies$) Ovvia
- ($\impliedby$)
	1. $f(A)=A$ e $B \neq A \in r$, allora $f(B) \in s \setminus \{ A \}$
	2. Per costruzione di prospettività $O \in L(B,f(B))$
	3. Sia $B' \neq A \in r$, allora $O = L(B, f(B), L(B', f(B')))$
	4. $(A, B, B')$ riferimento proiettivo di $r$ e $f = \pi_{O}$

$\pi_{O}$ è la restrizione di $\pi : \mathbb{P}(V) \setminus \{ 0 \} \to s$ detta proiezione da $O$ a $s$.

Sia $\pi = [\varphi]$, allora $\pi$ trasformazione proiettiva degenere dove $\text{Ker}\varphi \neq \{ 0 \}$.

$\varphi : V \to W$ lineare induce $[\varphi] : \mathbb{P}(V) \setminus \mathbb{P}(\text{Ker}\varphi) \to \mathbb{P}(W)$.