# Spazio proiettivo
Siano $\mathbb{K}$ campo e $V$ spazio vettoriale su $\mathbb{K}$. Lo spazio proiettivo associato a $V$ è $\mathbb{P}(V)=\frac{{V \setminus \{ 0 \}}}{\sim}$ dove $v \sim w$ se $\exists \lambda \in \mathbb{K}^* = \mathbb{K} \setminus \{ 0 \}$   $w = \lambda v$.

$\sim$ è una relazione di equivalenza.

$\mathbb{P}(V) \cong V$ e l'isomorfismo $[v] \mapsto \text{Span}(v)$ è ben definito.

La dimensione di $\mathbb{P}(V)$ è definita come $\dim\mathbb{P}(V)=\dim_{\mathbb{K}}V-1$.

Se $V = \mathbb{K}^n$ si definisce lo spazio proiettivo standard $\mathbb{P}(\mathbb{K}^n)=\mathbb{P}^{n-1}(\mathbb{K})$.

Nel corso si considereranno spazi a dimensione finita.

# Trasformazione proiettiva
Siano $\mathbb{P}(V)$ e $\mathbb{P}(W)$ spazi proiettivi su $\mathbb{K}$, si dice trasformazione proiettiva una funzione $f : \mathbb{P}(V) \to \mathbb{P}(W)$ tale che $\exists \varphi : V \to W$ lineare   $\forall v \in V$   $f([v]) = [\varphi(w)]$.

Nel caso precedente si dice che $f$ è indotta da $\varphi$, o $\varphi$ rappresenta $f$, e si scrive $f = [\varphi]$.

Se $\varphi$ induce una trasformazione proiettiva, allora $\varphi$ è iniettiva.

DIMOSTRAZIONE: $f([v]) = [\varphi(v)]=[0]$ non ha senso nello spazio proiettivo.

Se $\varphi$ è iniettiva, allora induce una trasformazione proiettiva.

DIMOSTRAZIONE: La trasformazione come prima è ben posta.

Le trasformazioni proiettive sono iniettive.

DIMOSTRAZIONE:
1. Siano $[v]$ e $[w]$ tali che $f([v])=f([w])$
2. $\varphi$ rappresenta $f \implies [\varphi(v)]=[\varphi(w)] \implies \exists \lambda \neq 0$   $\varphi(w)=\lambda\varphi(v)=\varphi(\lambda v)$
3. Per iniettività di $\varphi$ vale $w = \lambda v$, ossia $[w]=[v]$ in $\mathbb{P}(V)$

Sia $f : \mathbb{P}(V) \to \mathbb{P}(W)$ trasformazione proiettiva, sono equivalenti:
1. $f$ surgettiva
2. $f$ bigettiva
3. $\dim\mathbb{P}(V) = \dim \mathbb{P}(W)$
4. $f$ invertibile e $f^{-1} : \mathbb{P}(W) \to \mathbb{P}(V)$ trasformazione proiettiva

DIMOSTRAZIONE:
- ($1 \iff 2$) $f$ è sempre iniettiva
- ($2 \implies 3$)  Sia $f = [\varphi]$
	1. $0 \in \mathrm{Im}\varphi$
	2. $w \in W \setminus \{ 0 \} \implies [w] \in \mathbb{P}(W)$
	3. Per bigettività di $f$ vale $\exists v \in V \setminus \{ 0 \}$   $[\varphi(v)]=f([v])=[w]$
	4. $w \in \mathrm{Im}\varphi$ da cui $\varphi$ suriettiva
- ($3 \implies 4$) Sia $f = [\varphi]$
	1. $\varphi$ iniettiva
	2. $\dim_{\mathbb{K}}V=\dim\mathbb{P}(V)+1=\dim\mathbb{P}(W)+1=\dim_{\mathbb{K}}W$
	3. $\varphi$ isomorfismo
	4. $[\varphi^{-1}]$ trasformazione proiettiva indotta è inversa di $f$
- ($4 \implies 1$) $f$ invertibile $\implies f$ surgettiva

# Proiettività
Una proiettività di $\mathbb{P}(V)$ è una trasformazione proiettiva da $\mathbb{P}(V)$ in se stesso.

L'identità $\text{id} : \mathbb{P}(V) \to \mathbb{P}(V)$ è una proiettività.

DIMOSTRAZIONE: $\text{id}_{\mathbb{P}(V)}=[\text{id}_{V}]$.

Siano $f=[\varphi]$ e $g=[\psi]$ proiettività di $\mathbb{P}(V)$, allora $g \circ f=[\psi \circ \varphi]$ è una proiettività di $\mathbb{P}(V)$.

DIMOSTRAZIONE: $g(f([v]))=g([\varphi(v)])=[\psi(\varphi(v))]=[(\psi \circ \varphi)(v)]$.

Un isomorfismo tra spazi proiettivi si dice isomorfismo proiettivo.

Le proiettività di $\mathbb{P}(V)$ formano un gruppo rispetto alla composizione denotato con $\mathbb{P}\text{GL}(V)$.

Sia $f=[\varphi]$ proiettività, allora $\text{Fix}f \cong \{ \text{autospazi di } \varphi \text{ di dimensione } 1 \}$.

# Sottospazio proiettivo
Un sottospazio proiettivo è un $S \subseteq \mathbb{P}(V)$ della forma $\pi(W \setminus  \{ 0 \})$ con $W$ sottospazio vettoriale di $V$.

In questo corso spesso si utilizzerà la notazione $S = \mathbb{P}(W)$.

$\pi^{-1}(S)=W \setminus \{ 0 \}$.

Per costruzione $S \cong \mathbb{P}(W)$ e $\{ \text{sottospazi vettoriali di }V \} \cong \{ \text{sottospazi proiettivi di } \mathbb{P}(V) \}$.

Siano $S_{i}$ sottospazi proiettivi di $\mathbb{P}(V)$, allora $\bigcap\limits_{i \in I} S_{i}\subseteq \mathbb{P}(V)$ sottospazio proiettivo.

DIMOSTRAZIONE:
1. Siano $W_{i}\subseteq V$ sottospazi vettoriali tali che $\pi(W_{i}\setminus \{ 0 \})=S_{i}$
2. $W_{i}=\pi^{-1}(S_{i}) \cup \{ 0 \}$
3. $\bigcap\limits_{i \in I} W_{i} \subseteq V$ sottospazio vettoriale
4. $\pi\left( \bigcap\limits_{i \in I} W_{i} \setminus  \{ 0 \} \right) = \bigcap\limits_{i \in I} \pi(W_{i} \setminus \{ 0 \})=\bigcap\limits_{i \in I} S_{i}$ in quanto $\pi^{-1}\pi(W_{i} \setminus \{ 0 \}) = W_{i} \setminus \{ 0 \}$

Sia $A \subseteq \mathbb{P}(V)$, il sottospazio proiettivo di $\mathbb{P}(V)$ generato da $A$ è il più piccolo sottospazio proiettivo di $\mathbb{P}(V)$ che contiene $A$ e si denota con $L(A)$.

La definizione precedente è ben posta e $L(A) = \bigcap\limits_{S \text{ ssp }\supseteq A} S$.

Dati $S_{i}$ sottospazi proiettivi di $\mathbb{P}(V)$, si indica con $L(S_{1},\dots,S_{k})$ il generato dell'unione.

Siano $S_{1}=\mathbb{P}(W_{1})$ e $S_{2} = \mathbb{P}(W_{2})$, allora $L(S_{1},S_{2})=\mathbb{P}(W_{1}+W_{2})$.

DIMOSTRAZIONE:
1. $W_{1} \subseteq W_{1} + W_{2}$ e $W_{2} \subseteq W_{1} + W_{2}$
2. $S_{1} \subseteq \mathbb{P}(W_{1} + W_{2})$ e $S_{2} \subseteq \mathbb{P}(W_{1} + W_{2})$
3. Per minimalità $L(S_{1},S_{2}) \subseteq \mathbb{P}(W_{1}+W_{2})$
4. Sia $W \subseteq V$ il sottospazio vettoriale tale che $L(S_{1},S_{2}) = \mathbb{P}(W)$
5. $\mathbb{P}(W_{1}) = S_{1} \subseteq L(S_{1},S_{2}) = \mathbb{P}(W) \implies W_{1} \subseteq W$ e ragionamento analogo vale per $W_{2}$
6. $W_{1} + W_{2} \subseteq W$ e $\mathbb{P}(W_{1} + W_{2}) \subseteq \mathbb{P}(W)$

Un sottospazio proiettivo $S$ di $\mathbb{P}(V)$ si dice:
- punto se $\dim S = 0$
- retta se $\dim S = 1$
- piano se $\dim S = 2$
- iperpiano se $\dim S = \dim \mathbb{P}(V)-1$

# Formula di Grassmann proiettiva
Siano $S_{1}$ e $S_{2}$ sottospazi proiettivi, allora $\dim L(S_{1},S_{2}) = \dim S_{1} + \dim S_{2} - \dim(S_{1} \cap S_{2})$.

DIMOSTRAZIONE:
1. Siano $S_{1} = \mathbb{P}(W_{1})$ e $S_{2} = \mathbb{P}(W_{2})$ con $W_{1}$ e $W_{2}$ sottospazi vettoriali di $V$
2. Per Grassmann $\dim(W_{1}+W_{2})=\dim W_{1} + \dim W_{2} - \dim(W_{1} \cap W_{2})$
3. $\dim S_{1} = \dim W_{1} - 1$ e ragionamenti analoghi

$\dim S_{1} + \dim S_{2} \geq \dim \mathbb{P}(V) \implies S_{1} \cap S_{2} \neq \emptyset$.

DIMOSTRAZIONE: Grassmann.

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