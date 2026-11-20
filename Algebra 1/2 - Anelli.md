# Anello
Un anello $A$ è un insieme non vuoto dotato di due operazioni $+,\cdot : A \times A \to A$ tale che:
- $(A,+)$ gruppo abeliano
- $\cdot$ associativa
- $+$ e $\cdot$ distributive

$A$ anello si dice:
- commutativo se $\cdot$ commutativa
- unitario se esiste un elemento neutro per $\cdot$
- corpo se $(A\setminus \{ 0 \}, \cdot)$ gruppo
- campo se $(A\setminus \{ 0 \}, \cdot)$ gruppo abeliano
- dominio se $ab = 0 \implies a = 0 \lor b = 0$

~={yellow}Il corso farà riferimento da ora a $(A,+,\cdot)$ anello commutativo unitario.=~

$a \in A$ si dice:
- invertibile se $\exists b \in A$   $ab = 1$
- $0$-divisore dello $0$ se $\exists b \in A$   $b \neq 0$   $ab = 0$
- nilpotente se $\exists n \in \mathbb{N}$   $a^n = 0$

Si definiscono:
- $A^* = \{ a \in A : a \text{ invertibile} \}$
- $D(A) = \{ a \in A : a\text{ } 0\text{-divisore} \}$
- $N(A) = \{ a \in A : a \text{ nilpotente} \}$

$A$ campo $\iff A^* = A \setminus \{ 0 \}$.

$A$ dominio $\iff D(A) = \{ 0 \} \iff$ vale la legge di cancellazione.

# Sottoanello
$B \subseteq A$ si dice sottoanello di $A$ se $(B,+,\cdot)$ anello.

$B \subseteq A$ sottoanello $\iff \exists1_{B} \in B$$   $\land$   $\forall b_{1},b_{2} \in B$   $b_{1}+b_{2},b_{1}b_{2} \in B$.

# Ideale
$I \subseteq A$ si dice ideale di $A$ se $(I,+) < (A,+)$ e $\forall a \in A$   $\forall i \in I$   $ai \in I$.

$I$ ideale si dice:
- proprio se $I \neq A$
- banale se $I = \{ 0 \}$ o $I = A$
- massimale se, dato $J$ ideale, $I \subseteq J \subseteq A \implies J = I \lor J = A$

$I$ proprio $\iff 1 \not\in I \iff A^* \cap I = \emptyset$.

$A$ campo $\iff$ gli ideali di $A$ sono banali.

Sia $S \subseteq A$, si definisce $(S) = \left\{  \sum\limits_{i = 1}^{n} a_{i}s_{i} : a_{i} \in A, s_{i} \in S  \right\}$ ideale generato da $S$.

$S \subseteq A$ si dice insieme di generatori di $I$ se $I = (S)$ e $I$ si dice:
- finitamente generato se $|S| < \infty$
- principale se $|S| = 1$

Un anello i cui ideali sono tutti principali è detto PIR.

Un dominio PIR è detto PID.

$(S)$ si può costruire sia dall'alto che dal basso.

# Lemma di Zorn
Sia $(\Sigma, \leq)$ poset tale che ogni catena in $\Sigma$ è superiormente limitata, allora $\Sigma$ possiede elementi massimali.

# Ideale massimale
$A$ possiede un ideale massimale.

DIMOSTRAZIONE: Lemma di Zorn.

$I \subseteq A$ ideale proprio $\implies I \subseteq$ ideale massimale.

DIMOSTRAZIONE:
1. Sia $I$ ideale proprio e $\Sigma_{I} = \{ J \subsetneq A : I \subseteq J \}$
2. Per Zorn ogni catena in $\Sigma_{I}$ ammette maggiorante in $\Sigma_{I}$
3. Siano $J_{0}$ massimale in $\Sigma_{I}$ e $J_{1} \subseteq A$ ideale con $J_{0} \subseteq J_{1}$
4. Se $J_{0} \subsetneq J_{1}$, allora $J_{1} \not\in \Sigma_{I}$, cioè $J_{1} = A$

$a \in A \setminus A^* \implies a \in$ ideale massimale.

DIMOSTRAZIONE: Proposizione precedente con l'ideale generato da $a$.

# Omomorfismo
Siano $A,B$ anelli, $\varphi : A \to B$ si dice omomorfismo di anelli se:
1. $\varphi(a_{1}+a_{2})=\varphi(a_{1})+\varphi(a_{2})$
2. $\varphi(a_{1}a_{2})=\varphi(a_{1})\varphi(a_{2})$
3. $\varphi(1_{A})=1_{B}$

Sia $I\subseteq A$ ideale, allora $(A/ I, +)$ è un gruppo con $\bar{a} \in A / I$ denotato con $a + I$.

Sia $(\cdot) : A / I \times A / I \to A / I$ data da $(\bar{a},\bar{b}) \mapsto \overline{ab}$, allora $(A/I, +, \cdot)$ è un anello.

$\forall I \subseteq A$ ideale   $\exists\varphi$ omomorfismo di anelli   $I = \text{Ker}\varphi$.

Sia $\varphi$ omomorfismo di anelli, vale $A / \text{Ker}\varphi \cong \mathrm{Im}\varphi$ come anelli.

# Elemento primo e irriducibile
~={yellow}Il corso farà riferimento in questa sezione a $(A,+,\cdot)$ dominio.=~

$a,b \in A$ si dicono associati se $\exists u \in A^*$   $a = bu$.

$a \notin A^*$ si dice:
- primo se $a \mid bc \implies a \mid b \lor a \mid c$
- irriducibile se $a = bc \implies b \in A^* \lor c \in A^*$

Essere associati induce una relazione di equivalenza $\sim$.

DIMOSTRAZIONE: Verifiche.

Valgono:
- $a \sim b \iff (a) = (b)$
- $a \mid b \iff (b) \subseteq (a)$
- $a$ primo $\iff (a)$ ideale primo
- $\forall a \in A \setminus (A^* \setminus \{ 0 \})$   $a$ primo $\implies a$ irriducibile

DIMOSTRAZIONE: Verifiche.

Sia $A$ PID, allora $a$ irriducibile $\implies a$ primo.

# Noetherianità
In un PID ogni catena ascendente di ideali è stazionaria, cioè $I_{1} \subseteq \dots \subseteq I_{n_{0}} = I_{n_{0}+1} = \dots$

DIMOSTRAZIONE: $I = \bigcup\limits_{i} I_{i}$ è un ideale di $A \implies \exists a \in I$   $I = (a) \implies (a \in I_{n_{0}} \implies I = I_{n_{0}})$.

Un anello si dice Noetheriano se tutti gli ideali sono finitamente generati.

# Fattorizzazione
Un anello $A$ si dice a fattorizzazione unica, o UFD, se valgono:
1. Esistenza: $\forall a \in A \setminus \{ A^* \cup \{ 0 \} \}$   $\exists u \in A^*$   $\exists b_{1},\dots,b_{k}$ irriducibili   $a = ub_{1} \dots b_{k}$
2. Unicità: $a = ub_{1}\dots b_{k}=vc_{1}\dots c_{h} \implies h = k \land b_{j} \sim c_{j}$

Sia $A$ dominio che verifica Esistenza, allora $A$ UFD $\iff$ ogni irriducibile è primo.

DIMOSTRAZIONE:
- ($\implies$)
	1. Sia $a \in A$ irriducibile, $a \mid bc \implies \exists d \in A$   $ad = bc$
	2. $ad$ e $bc$ hanno la stessa fattorizzazione $\implies$ stessi irriducibili dividono i membri
	3. $a \mid ad \implies a \mid b \lor  a \mid c \implies a$ primo
- ($\impliedby$)
	1. $a = ub_{1}\dots b_{k} = vc_{1}\dots c_{h} \implies b_{1} \mid vc_{1}\dots c_{h} \implies b_{1} \mid$ uno dei fattori
	2. $b_{1} \not\mid v \implies b_{1} \mid c_{i} \implies b_{1} \sim c_{i}$ e così via per induzione

PID $\implies$ UFD.

DIMOSTRAZIONE:
1. Per il teorema precedente vale Unicità
2. Per assurdo sia $a \in A \setminus \{ A^* \cup \{ 0 \} \}$ senza fattorizzazione, da cui $a$ non irriducibile
3. $a = a_{1}b_{1}$ con $a_{1},b_{1} \not\in A^*$, da cui uno tra $a_{1}$ e $b_{1}$ non ha fattorizzazione
4. Sia $a_{1}$ senza fattorizzazione, reitero come $a$ con $a_{2}b_{2}$ e così via
5. $(a) \subsetneq (a_{1}) \subsetneq (a_{2}) \subsetneq \dots$ all'infinito, contraddicendo la Noetherianità

Euclideo $\implies$ PID.

Sia $A$ UFD, allora:
- $\gcd(a,b) = d$ se $d \mid a \land d \mid b \land (c \mid a \land c \mid b \implies c \mid d)$
- $\text{lcm}(a,b) = m$ se $a \mid m \land b \mid m \land (a \mid l \land b \mid l \implies m \mid l)$

Sia $\text{Irr}A = \{ a \in A : a \text{ irriducibile} \} / \sim$, allora:
- $a = u \prod\limits_{\pi \in \text{Irr}A} \pi^{e_{\pi,a}}$
- $b = v\prod\limits_{\pi \in \text{Irr}A} \pi^{e_{\pi,b}}$
- $\gcd(a,b) = \prod\limits_{\pi \in \text{Irr}A} \pi^{\min \{ e_{\pi,a}, e_{\pi,b} \}}$
- $\text{lcm}(a,b) = \prod\limits_{\pi \in \text{Irr}A} \pi^{\max \{ e_{\pi,a}, e_{\pi,b} \}}$