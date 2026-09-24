# Spazio proiettivo
Siano $\mathbb{K}$ campo e $V$ spazio vettoriale su $\mathbb{K}$. Lo spazio proiettivo associato a $V$ è $\mathbb{P}(V)=\frac{{V \setminus \{ 0 \}}}{\sim}$ dove $v \sim w$ se $\exists \lambda \in \mathbb{K}^* = \mathbb{K} \setminus \{ 0 \}$   $w = \lambda v$.

$\sim$ è una relazione di equivalenza.

$\mathbb{P}(V) \cong V$ e l'isomorfismo $[v] \mapsto \text{Span}(v)$ è ben definito.

La dimensione di $\mathbb{P}(V)$ è definita come $\dim\mathbb{P}(V)=\dim_{\mathbb{K}}V-1$.

Se $V = \mathbb{K}^n$ si definisce lo spazio proiettivo standard $\mathbb{P}(\mathbb{K}^n)=\mathbb{P}^{n-1}(\mathbb{K})$.

Se $\dim\mathbb{P}(V)=1$ si dice retta proiettiva, se è $2$ si dice piano proiettivo.

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

# Proiettività
Una proiettività di $\mathbb{P}(V)$ è una trasformazione proiettiva da $\mathbb{P}(V)$ in se stesso.

L'identità $\text{id} : \mathbb{P}(V) \to \mathbb{P}(V)$ è una proiettività.

DIMOSTRAZIONE: $\text{id}_{\mathbb{P}(V)}=[\text{id}_{V}]$.

Siano $f=[\varphi]$ e $g=[\psi]$ proiettività di $\mathbb{P}(V)$, allora $g \circ f=[\psi \circ \varphi]$ è una proiettività di $\mathbb{P}(V)$.

DIMOSTRAZIONE: $g(f([v]))=g([\varphi(v)])=[\psi(\varphi(v))]=[(\psi \circ \varphi)(v)]$.

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

Un isomorfismo tra spazi proiettivi si dice isomorfismo proiettivo.

Le proiettività di $\mathbb{P}(V)$ formano un gruppo rispetto alla composizione denotato con $\mathbb{P}\text{GL}(V)$.

Sia $f=[\varphi]$ proiettività, allora $\text{Fix}f \cong \{ \text{autospazi di } \varphi \text{ di dimensione } 1 \}$.

# Sottospazio proiettivo
Un sottospazio proiettivo è un $S \subseteq \mathbb{P}(V)$ della forma $\pi(W \setminus  \{ 0 \})$ con $W$ sottospazio vettoriale di $V$.

$\pi^{-1}(S)=W \setminus \{ 0 \}$.

Per costruzione $S \cong \mathbb{P}(W)$ e $\{ \text{sottospazi vettoriali di }V \} \cong \{ \text{sottospazi proiettivi di } \mathbb{P}(V) \}$.