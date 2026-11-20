# Topologia di sottospazio
Siano $X$ topologico e $Y \subseteq X$, la topologia di sottospazio che $Y$ eredita da $X$ è la topologia meno fine che renda $Y \hookrightarrow X$ continua.

La definizione è ben posta.

DIMOSTRAZIONE:
1. $\Omega = \{ \tau \text{ topologia} : (Y,\tau) \hookrightarrow X \text{ continua} \} \neq \emptyset$
2. L'intersezione delle topologie in $\Omega$ è una topologia

Sia $Y \subseteq X$, allora $A \subseteq Y$ aperto $\iff \exists B \subseteq X$ aperto   $A = Y \cap B$.

DIMOSTRAZIONE:
1. Sia $\tau = \{ A \subseteq Y : \exists B\subseteq X \text{ aperto }\text{ }\text{ }A = Y \cap B \}$
2. $\emptyset = Y \cap \emptyset$ e $Y = Y \cap X$
3. $A_{1},A_{2} \in \tau \implies \exists B_{1},B_{2} \subseteq X$ aperti   $A_{i} = Y \cap B_{i} \implies A_{1} \cap A_{2} = Y \cap (B_{1} \cap B_{2}) \in \tau$
4. $A_{i} \in \tau$   $\forall i \in I \implies \bigcup\limits_{i \in I} A_{i} \in \tau$ come al punto precedente
5. $\tau$ è una topologia
6. Sia $\tau'$ topologia su $Y$, allora $i : (Y,\tau') \hookrightarrow X$ continua $\iff \forall B \subseteq X$ aperto   $i^{-1}(B) = Y \cap B$ aperto in $\tau' \iff \tau \subseteq \tau'$
7. $\tau$ è la topologia più fine che rende $i$ continua`hookrightarrow`

$C \subseteq Y$ chiuso in $Y \iff \exists D \subseteq X$ chiuso in $X$   $C = Y \cap D$.

DIMOSTRAZIONE: Passaggio al complemento.

$A \subseteq Y$ aperto in $X \implies A$ aperto in $Y$.

DIMOSTRAZIONE: $A = Y \cap A$.

Valgono:
1. un aperto di un aperto è aperto
2. un chiuso di un chiuso è chiuso

DIMOSTRAZIONE:
1. $Y$ aperto e $A \subseteq Y$ aperto in $Y \implies \exists B \subseteq X$ aperto   $A = Y \cap B \implies A$ aperto in $X$
2. Come prima

Siano $Z \subseteq Y \subseteq X$, la topologia indotta da $X$ su $Z$ coincide con la topologia indotta da $Y$ su $Z$.

DIMOSTRAZIONE:
1. Siano $\tau_{1}$ da $X$ su $Z$ e $\tau_{2}$ da $Y$ su $Z$
2. $(Z, \tau_{2}) \hookrightarrow Y \hookrightarrow X$ da cui $\tau_{1} < \tau_{2}$
3. Sia $A \in \tau_{2}$, allora $\exists B$ aperto in $Y$   $A = Z \cap B$
4. Per definizione $\exists \Omega$ aperto in $X$   $B = Y \cap \Omega$
5. $A = Z \cap B = Z \cap Y \cap \Omega = Z \cap \Omega$ aperto per $\tau_{1}$ e $\tau_{2}$, da cui $\tau_{1} = \tau_{2}$

Siano $(X,d)$ metrico e $Y \subseteq X$, allora la topologia di sottospazio di $Y$ è indotta da $d|_{Y}$.

DIMOSTRAZIONE:
1. $i : (Y, d|_{Y}) \hookrightarrow (X,d)$ 1-Lipschitz, quindi continua
2. La topologia indotta su $Y$ da $d|_{Y}$ è più fine della topologia di sottospazio
3. --- dimostrazione da continuare ---

Siano $Y \subseteq X$, $x_{0} \in Y$ e $\mathscr{U}$ SFI di $x_{0}$ in $X$, allora $\mathscr{U}_{Y} = \{ Y \cap U : U \in \mathscr{U} \}$ SFI di $x_{0}$ in $Y$.

DIMOSTRAZIONE:
1. $W \in I(x_{0})$ in $Y \implies x_{0} \in \mathring{W} \subseteq W$
2. $\mathring{W}$ aperto in $Y \implies \exists A$ aperto in $X$   $\mathring{W} = Y \cap A$
3. Per costruzione $x_{0} \in A$, cioè $A \in I(x_{0})$ in $X$
4. $\mathscr{U}$ SFI $\implies \exists U \in \mathscr{U}$   $x_{0} \in U \subseteq A \implies x_{0} \in Y \cap U \subseteq Y \cap A = \mathring{W} \subseteq W$

Sia $\mathscr{B}$ base di $X$, allora $\mathscr{B}_{Y} = \{ Y \cap B : B \in \mathscr{B} \}$ è una base di $Y$ò

DIMOSTRAZIONE: $A$ aperto in $Y \iff A = Y \cap \Omega$ con $\Omega$ aperto in $X \iff \exists \mathscr{B}' \subseteq \mathscr{B}$   $A = Y \cap \bigcup\limits_{B \in \mathscr{B}'} B = \bigcup\limits_{B \in \mathscr{B}'} (Y \cap B) \iff A$ unione di elementi di $\mathscr{B}_{Y}$.

Siano $X$ topologico e $Y \subseteq X$, allora:
1. $X$ I-numerabile $\implies Y$ I-numerabile
2. $X$ II-numerabile $\implies Y$ II-numerabile

DIMOSTRAZIONE: Lemmi precedenti.

Sia $X$ metrizzabile e separabile, allora ogni sottospazio di $X$ è separabile.

# Continuità in sottospazio
Siano $i : Y \hookrightarrow Z$ inclusione e $f : X \to Y$, allora $f$ continua $\iff i \circ f$ continua.

DIMOSTRAZIONE: $i \circ f$ continua $\iff \forall A$ aperto di $Z$   $(i \circ f)^{-1}(A) = f^{-1}(i^{-1}(A))$ aperto in $X \iff \forall A$ aperto di $Z$   $f^{-1}(Y \cap A)$ aperto in $X \iff \forall B$ aperto in $Y$   $f^{-1}(B)$ aperto in $X$.

Siano $f : X \to Y$ continua e $Z \subseteq X$, allora $f |_{Z}$ continua.

DIMOSTRAZIONE: $f|_{Z} = f \circ i$ composizione di funzioni continue.

# Immersione topologica
$f : X \to Y$ si dice aperta/chiusa se $f(A)$ aperto/chiuso in $Y$   $\forall A$ aperto/chiuso di $X$.

$f : X \to Y$ si dice immersione topologica se è un omeomorfismo tra $Y$ e $f(Y) \subseteq X$.

Sia $f : Y \to X$ iniettiva, allora:
1. $f$ aperta $\implies f$ immersione topologica
2. $f$ chiusa $\implies f$ immersione topologica

DIMOSTRAZIONE: Ovvio.

# Topologia prodotto
Siano $X_{i}$ insiemi, si definisce il prodotto cartesiano $\prod\limits_{i \in I} X_{i} = \left\{  f : I \to \bigcup\limits_{i \in I} X_{i} : f(i) \in X_{i} : \forall i \in I  \right\}$.

Si definisce la proiezione $i$-esima $\pi_{i} : X \to X_{i} : f \mapsto f(i)$, cioè $x \mapsto x_{i}$ in coordinate.

La topologia prodotto è la topologia meno fine che rende ogni $\pi_{i}$ continua.

Possibili prebasi della topologia prodotto su $X = \prod\limits_{i \in I} (X_{i},\tau_{i})$ sono:
- $\{ \pi_{i}^{-1}(U) : i \in I, U \in \tau_{i} \}$
- $\{ \pi_{i}^{-1}(U) : i \in I, U \in \mathscr{B}_{i} \text{ base o prebase di }\tau_{i} \}$

DIMOSTRAZIONE:
1. $\pi_{i}$ continua $\iff \pi_{i}^{-1}(U)$ aperto di $X$   $\forall U \in \tau_{i} \iff$ $\in$ insieme della tesi
2. Topologia prodotto $\iff$ topologia generata dagli insiemi, dunque dà prebase

Una base della topologia prodotto su $X$ è $\left\{  \bigcap\limits_{i_{k-} \in I} \pi_{i_{k}}^{-1}(U_{i_{k}}) : U_{i_{k}} \in \tau_{k} \right\}$.

Siano $(X,d),(Y,d')$ metrici, allora la topologia prodotto su $X \times Y$ è indotta da:
- $d_{1}((x_{1},y_{1}),(x_{2},y_{2})) = d(x_{1},x_{2}) + d'(y_{1},y_{2})$
- $d_{2}((x_{1},y_{1}),(x_{2},y_{2})) = \sqrt{ d(x_{1},x_{2})^2 + d'(y_{1},y_{2})^2 }$
- $d_{\infty}((x_{1},y_{1}),(x_{2},y_{2})) = \max\{ d(x_{1},x_{2}),d'(y_{1},y_{2}) \}$

DIMOSTRAZIONE:
1. $d_{\infty} \leq d_{2} \leq d_{1} \leq 2d_{\infty}$, per cui $d_{1},d_{2},d_{\infty}$ sono topologicamente equivalenti
2. Siano $\tau$ la topologia prodotto su $X \times Y$ e $\tau_{d}$ la topologia indotta da $d_{1},d_{2},d_{\infty}$
3. Siano $\pi_{X} : (X \times Y, d_{\infty}) \to (X,d)$ e $\pi_{Y} : (X \times Y, d_{\infty}) \to (Y,d')$
4. $\pi_{X},\pi_{Y}$ sono 1-Lipschitziane, quindi continue, quindi $\tau < \tau_{d}$
5. $B_{d_{\infty}}((x,y),R) = \{ (x',y') \in X \times Y : d(x,x') < R \land d(y,y') < R \} = B_{d}(x,R) \times B_{d'}(y,R)$
6. $B_{d_{\infty}}((x,y),R)$ prodotto di aperti, dunque aperto, dunque $\tau_{d} < \tau$

$(\mathbb{R}^m, \tau_{\text{euclidea}}) \times (\mathbb{R}^m, \tau_{\text{euclidea}}) = (\mathbb{R}^{m+n}, \tau_{\text{euclidea}})$.

DIMOSTRAZIONE: $d_{\infty}$ su $\mathbb{R}^m$ e $\mathbb{R}^n$ inducono $d_{\infty}$ su $\mathbb{R}^{m+n}$.

Siano $X_{i}$ metrizzabili e $X = \prod\limits_{i \in I} X_{i}$, allora $I$ finito $\implies X$ metrizzabile.

Siano $X$ con topologia prodotto e $f : Y \to X$, allora $f$ continua $\iff \pi_{i} \circ f$ continua.

DIMOSTRAZIONE:
- RHS $\iff \forall U$ aperto in $X_{i}$   $(\pi_{i}\circ f)^{-1}(U) = f^{-1}(\pi_{i}^{-1}(U))$ aperto in $Y \iff$ LHS

$\pi_{i}$ aperta.

Sia $\tau$ topologia di base $\prod\limits_{i \in I} U_{i}$, se $I$ è infinito $\tau$ si dice box topology.

# Topologia della convergenza puntuale
$f_{n} \to f$ in $X^D$ con la topologia prodotto $\iff f_{n} \to f$ puntualmente.

DIMOSTRAZIONE:
- ($\implies$)
	1. Sia $\lim\limits_{n \to +\infty} f_{n} = f$ in $X^D = \prod\limits_{d \in D} X_{d}$, allora $\pi_{d} : X^D \to X_{d}$ continua
	2. $\pi_{d}$ sequenzialmente continua $\implies \lim\limits_{n \to +\infty} \pi_{d}(f_{n}) = \pi_{d}(f) \implies \lim\limits_{n \to +\infty} f_{n}(d)=f(d)$
- ($\impliedby$)
	1. Siano $f_{n} \to f$ puntualmente e $U \in I(f)$, allora $U$ contiene un aperto di $W$ base
	2. $f_{n} \in W$ definitivamente, da cui la tesi

