# Spazio topologico
Siano $X$ insieme e $\tau \subseteq \mathscr{P}(X)$ detto topologia contenente elementi detti aperti, si definisce lo spazio topologico la tupla $(X,\tau)$ tale che:
1. $X,\emptyset \in \tau$
2. $A_{1},A_{2} \in \tau \implies A_{1} \cap A_{2} \in \tau$
3. $\{ A_{i} \} \in \tau \implies \bigcup\limits_{i \in I} A_{i} \in \tau$

Siano $(X,d)$ spazio metrico e $\tau = \{ A \subseteq X : A \text{ aperto} \} \subseteq \mathscr{P}(X)$, allora $(X,d)$ topologico.

$C \subseteq X$ si dice chiuso se $X \setminus C$ aperto.

La definizione di spazio topologico si può dare con i chiusi sostituendo $\cup \longleftrightarrow \cap$.

Sia $(X,\tau)$ topologico, si dice metrizzabile se esiste una distanza che induce $\tau$.

$X$ metrizzabile $\implies \forall x_{0} \in X$   $\{ x_{0} \}$ chiuso.

DIMOSTRAZIONE:
1. Sia $d$ che induce $\tau$, allora $X \setminus \{ x_{0} \}$ aperto
2. Sia $y \in X \setminus \{ x_{0} \}$, allora $B(y,d(x_{0},y)) \subseteq X \setminus \{ x_{0} \}$
3. $x_{0} \not\in B(y,d(x_{0},y))$ poiché $d(x_{0},y) \geq d(x_{0},y)$

# Continuità
Siano $X,Y$ topologici, allora $f : X \to Y$ si dice continua se $\forall A \subseteq Y$ aperto   $f^{-1}(A) \subseteq X$ aperto.

Siano $X,Y,Z$ topologici, $f : X \to Y$ e $g : Y \to Z$, allora:
1. $\text{id}_{X} : X \to X$ continua
2. $f,g$ continue $\implies g \circ f : X \to Z$ continua

DIMOSTRAZIONE:
1. Ovvio
2. $(g \circ f)^{-1}(A) = f^{-1}(g^{-1}(A))$, poi doppia continuità

Un omeomorfismo è una funzione continua e invertibile con inversa continua.

# Confronto tra topologie
Siano $\tau_{1}, \tau_{2}$ topologie su $X$, si dice che $\tau_{1}$ è meno fine di $\tau_{2}$ se $\tau_{1} \subseteq \tau_{2}$.

$\tau_{1}$ meno fine di $\tau_{2} \iff \text{id} : (X,\tau_{2}) \to (X,\tau_{1})$ continua.

Siano $d_{1},d_{2}$ distanze su $X$ che inducono $\tau_{1},\tau_{2}$, se $\exists k > 0$   $d_{1} \leq kd_{2}$, allora $\tau_{1} \subseteq \tau_{2}$.

DIMOSTRAZIONE: Ragionamenti sull'apertura della palla con $d_{1}$ e $d_{2}$.

$d_{1} \leq kd_{2} \land d_{2} \leq hd_{1} \implies \tau_{1} = \tau_{2}$ e si dicono topologicamente equivalenti.

Su $\mathbb{R}^n$ le topologie indotte da $||\cdot||_{1}$, $||\cdot||_{2}$ e $||\cdot||_{\infty}$ sono topologicamente equivalenti.

DIMOSTRAZIONE: Ragionamenti sulle norme.

# Intorno
Siano $(X,\tau)$ topologico e $x_{0} \in X$, si dice intorno di $x_{0}$ un certo $U \subseteq X$ tale che $\exists A$ aperto di $\tau$ per cui $x_{0} \in A \subseteq U$.

L'insieme degli intorni di $x_{0}$ si denota con $I(x_{0})$.

Valgono:
- $U \in I(x_{0}) \land U \subseteq V \implies V \in I(x_{0})$
- $U \in I(x_{0}) \land V \in I(x_{0}) \implies U \cap V \in I(x_{0})$

$A \subseteq X$ aperto $\iff A$ intorno di ogni suo punto.

DIMOSTRAZIONE:
- ($\implies$) $A$ aperto e $x_{0} \in A \implies x_{0} \in A \subseteq A \implies A$ intorno di $x_{0}$
- ($\impliedby$) $\forall x_{0} \in A$   $\exists B_{x_{0}}$ aperto di $X$   $x_{0} \in B_{x_{0}} \subseteq A \implies A = \bigcup\limits_{x_{0} \in A} B_{x_{0}}$ aperto

Siano $X,Y$ topologici e $f : X \to Y$, allora $f$ si dice continua in $x_{0} \in X$ se:
- $\forall W \in I(f(x_{0}))$   $\exists U \in I (x_{0})$   $f(U) \subseteq W$

$f : X \to Y$ continua $\iff \forall x_{0} \in X$   $f$ continua in $x_{0}$.

DIMOSTRAZIONE:
- ($\implies$)
	1. Siano $x_{0} \in X$ e $W \in I(f(x_{0}))$
	2. $\exists A \subseteq Y$ aperto   $f(x_{0}) \in A \subseteq W$
	3. $x_{0} \in f^{-1}(A) \subseteq f^{-1}(W)$ e $f^{-1}(A)$ aperto in $X$ per continuità di $f$
	4. $f^{-1}(W) \in I(x_{0})$ e $f(f^{-1}(W)) \subseteq W$ da cui $f$ continua in $x_{0}$
- ($\impliedby$)
	1. Siano $A \subseteq Y$ aperto e $x_{0} \in f^{-1}(A)$
	2. Per apertura di $A$ e continuità di $f$, $\exists U \in I(x_{0})$   $f(U) \subseteq A$
	3. Per definizione $f(U) \subseteq A \implies U \subseteq f^{-1}(A) \implies x_{0} \in U \implies f^{-1}(A) \in I(x_{0})$

# Insiemi rilevanti
Sia da ora in poi $B \subseteq X$ topologico.

Si dice parte interna di $B$ il più grande aperto di $X$ contenuto in $B$ e si denota con $\mathring{B}$.

Si dice chiusura di $B$ il più piccolo chiuso di $X$ che contiene $B$ e si denota con $\overline B$.

Valgono:
1. $\mathring{B} = \bigcup\limits_{A \subseteq B \text{ aperto}} A$.
2. $\overline B = \bigcap\limits_{C \subseteq B \text{ chiuso}} C$.
3. $\mathring{B} \subseteq B \subseteq \overline B$
4. $X \setminus \mathring{B} = \overline {X \setminus B}$
5. $U \in I(x_{0}) \iff x_{0} \in \mathring{U}$

$x_{0} \in X$ si dice:
- aderente a $B$ se $\forall U\in I(x_{0})$   $U \cap B \neq \emptyset$.
- di accumulazione per $B$ se $\forall U \in I(x_{0})$   $(U \cap B) \setminus \{ x_{0} \} \neq \emptyset$
- punto isolato di $B$ se $x_{0} \in B$ e $\exists U \in I(x_{0})$   $U \cap B = \{ x_{0} \}$

$x_{0}$ aderente a $B \iff x_{0}$ di accumulazione per $B$ $\lor$ $x_{0}$ punto isolato per $B$.

$\overline B = \{ x_{0} \in X : x_{0} \text{ aderente a }B \}$.

DIMOSTRAZIONE: $x_{0} \in \mathring{X \setminus B} \iff \exists U \in I(x_{0})$   $U \subseteq X \setminus B \iff \exists U \in I(x_{0})$   $U \cap B \neq \emptyset$.

Sia $Y \subseteq X$ topologico, $Y$ si dice denso se $\overline Y = X$.

Sia $Y \subseteq X$ topologico, la frontiera di $Y$ è $\partial Y = \overline Y \setminus \mathring{Y}$.

# Topologia generata
Siano $\tau_{i}$ topologie su $X$, allora $\tau = \bigcap\limits_{i \in I} \tau_{i}$ è una topologia su $X$.

Siano $\tau_{i}$ topologie su $X$, esiste la topologia più fine tra le topologie meno fini di ogni $\tau_{i}$ ed è $\tau$.

Sia $S \subseteq \mathscr P(X)$, esiste la topologia meno fine che contiene $S$ e si dice topologia generata da $S$.

# Base
Sia $\tau$ topologia su $X$, si dice base di $\tau$ un $\mathscr{B} \subseteq \tau$ tale che $\forall A \in \tau$   $\exists \mathscr{B}' \subseteq \mathscr{B}$   $A = \bigcup\limits_{B \in \mathscr{B}'} B$.

$\mathscr{B}$ base di $\tau \iff \mathscr{B} \subseteq \tau$   $\land$   $($ $\forall A \in \tau$   $\forall x_{0} \in A$   $\exists B \in \mathscr{B}$   $x_{0} \in B \subseteq A$ $)$.

DIMOSTRAZIONE: Verifiche di inclusioni.

Siano $(X,d)$ metrico, $\Omega \subseteq (0,+\infty)$ tale che $0$ di accumulazione per $\Omega$ e $Z \subseteq X$ denso, allora:
- $\mathscr{B} = \{ B(x_{0},R),x_{0} \in Z,R \in \Omega \}$ base di $X$

DIMOSTRAZIONE:
1. $\mathscr{B} \subseteq \tau$ ovviamente
2. $A$ aperto $\implies \exists R > 0$   $B(\bar{x},R) \subseteq A$
3. $0$ di accumulazione $\implies \exists\varepsilon \in \Omega$   $0 < \varepsilon < \frac{R}{e}$
4. $Z$ denso $\implies B(\bar{x},R) \cap Z \neq \emptyset \implies \exists x_{0} \in Z$   $d(\bar{x},x_{0}) < \varepsilon$
5. $\bar{x} \in B(x_{0},\varepsilon) \implies d(x_{0},x) < \varepsilon \implies d(\bar{x},x) \leq d(\bar{x},x_{0}) + d(x_{0},x) < \varepsilon + \varepsilon = 2\varepsilon = R$
6. $x \in B(\bar{x},R) \subseteq A$

$\mathscr{B}$ base di $\tau$ su $X \iff$ valgono:
1. $\bigcup\limits_{B \in \mathscr{B}} B = X$
2. $B_{1},B_{2} \in \mathscr{B} \implies \exists \mathscr{B}' \subseteq \mathscr{B}$   $B_{1} \cap B_{2} = \bigcup\limits_{B \in \mathscr{B}'} B$

DIMOSTRAZIONE:
- ($\implies$) Ovvio
- ($\impliedby$)
	1. Sia $\tau = \left\{  \bigcup\limits_{B \in \mathscr{B}'} B, \mathscr{B}' \subseteq \mathscr{B}  \right\}$
	2. $\emptyset \in \tau$ prendendo $\mathscr{B}' = \emptyset$
	3. $X \in \tau$ poiché $\bigcup\limits_{B \in \mathscr{B}} B = X$
	4. $A_{1},A_{2} \in \tau \implies \exists \mathscr{B}_{1} \subseteq \mathscr{B},\mathscr{B}_{2} \subseteq \mathscr{B}$   $A_{1} = \bigcup\limits_{B \in \mathscr{B}_{1}} B$   $A_{2} = \bigcup\limits_{B \in \mathscr{B}_{2}} B$
	5. $A_{1} \cap A_{2} = \left( \bigcup\limits_{B \in \mathscr{B}_{1}} B \right) \cap \left( \bigcup\limits_{B \in B_{2}} B \right) = \bigcup\limits_{\underset{ \mathscr{B}' \in \mathscr{B}:2 }{ \mathscr{B} \in \mathscr{B}_{1}}} (\mathscr{B} \cap \mathscr{B}')$
	6. Se $A_{i} = \bigcup\limits_{B \in \mathscr{B}_{i}} B$, allora $\bigcup\limits_{i \in I} A_{i} = \bigcup\limits_{i \in I} \left( \bigcup\limits_{B \in \mathscr{B}_{i}} B \right) = \bigcup\limits_{B \in \bigcup\limits_{i \in I} \mathscr{B}_{i}} B \in \tau$

# Prebase
Sia $\tau$ topologia su $X$, si dice prebase di $\tau$ un $\mathscr{P} \subseteq \tau$ di aperti tale che $\left\{  \bigcap\limits_{P_{i} \in \mathscr{P}} P_{i}  \right\}$ è base di $X$.

Sia $S \subseteq \mathscr{P}(X)$, allora la topologia generata da $S$ ha $S \cup \{ X \}$ come prebase.

DIMOSTRAZIONE: Soliti controlli sulla topologia.

Siano $X,Y$ topologici, $\mathscr{B}$ base di $Y$, $\mathscr{P}$ prebase di $Y$ e $f : X \to Y$, allora sono equivalenti:
1. $f$ continua
2. $\forall A \in \mathscr{B}$   $f^{-1}(A)$ aperto in $X$
3. $\forall A \in \mathscr{P}$   $f^{-1}(A)$ aperto in $X$

DIMOSTRAZIONE:
- ($1 \implies 2 \implies 3$) Ovvio
- ($3 \implies 1$) $f^{-1}(A)$ aperto $\forall A \in \mathscr{P} \implies f^{-1}(A)$ aperto $\forall A \in \mathscr{B} \implies f^{-1}(A)$ aperto per ogni aperto di $Y$

# Assiomi di numerabilità
Siano $X$ topologico e $x_{0} \in X$, un sistema fondamentale di intorni di $x_{0}$ è un $S \subseteq I(x_{0})$ tale che $\forall U \in I(x_{0})$   $\exists W \in S$   $W \subseteq U$.

Sia $X$ topologico, allora si dice:
- II-numerabile se ammette una base numerabile
- I-numerabile se ogni $x_{0} \in X$ ammette un SFI numerabile
- separabile se $X$ ammette un sottoinsieme denso numerabile

Sia $X$ topologico, allora valgono:
1. II-numerabile $\implies$ I-numerabile
2. II-numerabile $\implies$ separabile
3. metrico $\land$ separabile $\implies$ II-numerabile

DIMOSTRAZIONE:
1. $\mathscr{B}$ base di $X \implies S = \{ B \in \mathscr{B} : x_{0} \in B \}$ SFI di $x_{0}$, per cui $\mathscr{B}$ numerabile $\implies S$ numerabile
2. (2.)
	1. $\mathscr{B} = \{ B_{i} \}$ base numerabile di $X$
	2. $B_{i} \neq \emptyset$, dunque si sceglie $x_{i} \in B_{i}$ e si pone $Z = \{ x_{i} \}$
	3. $Z$ denso
3. $(X,d)$ metrico e $Z$ denso $\implies \left\{  B\left( x, \frac{1}{n} \right) : x \in Z, n \in \mathbb{N}, n\geq 1  \right\}$ base di $X$

# Lipschitzianità
Siano $(X,d),(Y,d')$ metrici, allora $f : (X,d) \to (Y,d')$ si dice Lipschitziana se:
- $\exists k \in \mathbb{R}$   $\forall x_{1},x_{2} \in X$   $d'(f(x_{1}),f(x_{2})) \leq kd(x_{1},x_{2})$

Lipschitziana $\implies$ continua.