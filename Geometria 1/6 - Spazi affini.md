# Spazio affine
Sia $V$ spazio vettoriale su $\mathbb{K}$. Uno spazio affine $E$ associato a $V$ è un $V$-insieme omogeneo principale.

Si dice spazio affine standard $E=\mathbb{K}^n=V$, dove $V$ agisce su $E$ tramite traslazioni, ossia dato un punto $P = \underline{u}$ e un vettore $\underline{v}$, vale $\underline{v}.P = P + \underline{v} = \underline{u} + v$ semplicemente transitiva.

Per analogia si usa la notazione $\underline{v}.P = P+\underline{v}$.

Definiamo la dimensione di $E$ come la dimensione di $V$.

Quando $Q = P + \underline{v}$ usiamo la notazione $\underline{v} = Q - P$ come unico vettore da $P$ a $Q$.

Le seguenti applicazioni sono bigettive:
- $P \mapsto P+\underline{v} : E \to E$ con $\underline{v}$ fissato
- $\underline{v} \mapsto O+\underline{v} : V \to E$ con $O$ fissato
- $P \mapsto P-O : E \to V$ con $O$ fissato

Valgono:
- $\forall P$   $P-P=\underline{0}$
- $\forall P,Q$   $P-Q = -(Q-P)$
- $\forall P_{1},P_{2},P_{3}$   $(P_{3}-P_{1})+(P_{1}-P_{2}) = P_{3}-P_{2}$

# Combinazione affine
Siano $P_{1},\dots,P_{k} \in E$ e $\lambda_{1},\dots ,\lambda_{k} \in \mathbb{K}$. Passiamo da $O$ a $O'$:
1. $P = O + \sum\limits_{i=1}^{k} \lambda_{i}(P_{i}-O)$
2. $P' = O' + \sum\limits_{i=1}^{k} \lambda_{i}(P_{i}-O')$
Vale $P=P' \iff O'-O = (O'-O)\sum\limits_{i=1}^{k} \lambda_{i} \iff \sum\limits_{i=1}^{k} \lambda_{i} = 1$

Si dice combinazione affine $\sum\limits_{i=1}^{k} \lambda_{i}P_{i}$ con $\sum\limits_{i=1}^{k} \lambda_{i} = 1$.

Le combinazioni convesse di Analisi sono le combinazioni affini di $\mathbb{R}^2$.

# Sottospazio affine
Un sottoinsieme $D \subseteq E$ si dice sottospazio affine se chiuso per combinazioni affini.

Sia $E$ spazio affine su $V$. Allora:
1. dati $W \subseteq V$ e $P_{0} \in E$, vale $P_{0} + W$ sottospazio affine su $W$
2. dato $D \subseteq E$ sottospazio affine, $D$ è della forma $P_{0}$ per $W = \{ Q-P : P,Q \in D\}$

Il sottospazio $W$ associato a $D$ si dice direzione di $D$.

Il sottospazio affine $D \subseteq E$ generato da un sottoinsieme $S \subseteq E$ è l'insieme delle combinazioni affini dei punti di $S$ e si denota $D = \text{Aff}(S)$.

$\text{Aff}(S)$ è il più piccolo sottospazio affine che contiene $S$.

Nello spazio standard $\mathscr{A}_{n}(\mathbb{K})$ una combinazione affine in $E$ definisce $\underline{w} = \underline{v}_{0} + \sum\limits_{i=1}^{n} \lambda_{i}(\underline{w}_{i}-\underline{v}_{0})$.

Sia $E$ affine su $V$ di dimensione $n$ su $\mathbb{K}$, allora $\forall O \in E$ con $\mathscr{B}$ base di $V$, si ha la bigezione $\varphi_{O,\mathscr{B}} : E \to \mathscr{A}_{n}(\mathbb{K}) : 0+\underline{v} \mapsto [\underline{v}]_{B}$.

Due sottospazi affini con la stessa direzione sono detti paralleli.

Due sottospazi affini paralleli o coincidono o hanno intersezione vuota.

Si dice iperpiano affine un sottospazio affine di dimensione $n-1$.

# Indipendenza affine
$P_{1},\dots,P_{k} \in E$ si dicono affinemente indipendenti se la loro combinazione affine è unica.

Le seguenti proposizioni sono equivalenti:
- $P_{1},\dots,P_{k}$ affinemente indipendenti
- $\forall i=1,\dots,k$   $j \neq j$   $P_{j}-P_{i}$ linearmente indipendenti
- $\exists i \in \{ 1,\dots,k \}$   $j \neq i$   $P_{j}-P_{i}$ linearmente indipendenti

DIMOSTRAZIONE: Passaggio alla differenza.

Le seguenti due proposizioni sono equivalenti:
- $\underline{w}_{1},\dots,\underline{w}_{k} \in \mathscr{A}_{n}(\mathbb{K})$ affinemente indipendenti
- $\hat{w}_{1}=\binom{\underline{w}_{1}}{1},\dots,\hat{w}_{k}=\binom{\underline{w}_{k}}{1}$ linearmente indipendenti
