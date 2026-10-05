# Funzione a più variabili
Sia $f : \mathbb{R}^n \to \mathbb{R}^m$, allora $f$ si dice:
- scalare se $m = 1$
- curva se $n = 1$
- campo vettoriale se $m=n$

Dato $y \in \mathbb{R}^m$ si dice insieme di livello la preimmagine $f^{-1}(\{ y \})\subseteq \mathbb{R}^n$.

Ogni funzione quadratica è riconducibile a una conica dal grafico paraboloide o a sella.

Le funzioni radiali hanno grafico $S_{r}=\left\{  \sum\limits_{k=1}^{n} x_{k}^2=r^2  \right\}$, ossia una sfera di raggio $r$.

# Metrica
Sia $X$ insieme, una distanza o metrica è una funzione $d : X \times X \to \mathbb{R}$ tale che:
1. $d(x,y)\geq 0$
2. $d(x,y) = 0 \iff x = y$
3. $d(x,y) = d(y,x)$
4. $d(x,z) \leq d(x,y) + d(y,z)$

$(X,d)$ è detto spazio metrico.

Siano $(X, d_{1})$ e $(X,d_{2})$ spazi metrici, le metriche si dicono equivalenti se:
- $\exists C,\tilde{C} > 0$   $\forall x,y \in X$   $Cd_{2}(x,y)\leq d_{1}(x,y) \leq \tilde{C}d_{2}(x,y)$.

Sia $(X,d)$ spazio metrico, $\{ x_{n} \}_{n \in \mathbb{N}} \subseteq X$, $\bar{x} \in X$, si dice che $x_{n}$ tende a $x$ e si scrive $x_{n}\to x$ se $d(x_{n},x)\to {0}$.

# Norma
Sia $V$ spazio vettoriale, una norma è una funzione $||\cdot|| : V \to \mathbb{R}$ tale che:
1. $||v|| \geq 0$
2. $||v|| = 0 \iff v = 0$
3. $||\lambda v||=|\lambda| \, ||v||$
4. $||v+w|| \leq ||v|| + ||w||$

$(V, ||\cdot||)$ è detto spazio normato.

In uno spazio normato, una norma induce una metrica $d(v,w) := ||v-w||$.

Siano $(V, ||\cdot||_{1})$ e $(V, ||\cdot||_{2})$ spazi normati, le norme si dicono equivalenti se:
- $\exists C,\tilde{C} > 0$   $\forall v \in V$   $C||v||_{2} \leq ||v||_{1} \leq \tilde{C}||v||_{2}$.

# Prodotto scalare
Sia $V$ spazio vettoriale, un prodotto scalare è una funzione $\langle\cdot, \cdot \rangle : V \times V \to \mathbb{R}$ tale che:
1. $\langle v,v \rangle \geq 0$
2. $\langle v, v \rangle = 0 \iff v = 0$
3. $\langle v, w \rangle = \langle v, w \rangle$
4. $\langle \lambda u + \mu v, w \rangle = \lambda \langle u, w \rangle + \mu \langle v, w \rangle$

$(V, \langle \cdot, \cdot \rangle)$ è detto spazio euclideo.

In uno spazio euclideo, un prodotto scalare induce una norma $||v|| := \sqrt{ \langle v, v \rangle }$ e una distanza come prima, dette euclidee.

In uno spazio euclideo valgono Young e Cauchy - Schwarz.

# Topologia degli spazi metrici
Sia $(X,d)$ spazio metrico, allora si definisce la palla $B_{r}(x_{0})=\{ x \in X : d(x,x_{0})< r \}$.

Sia $(X, d)$ spazio metrico, allora $A \subseteq X$ si dice:
- aperto se $\forall x \in A$   $\exists r > 0$   $B_{r}(x)\subseteq A$
- chiuso se $X \setminus A$ aperto

Sia $A \subseteq X$, allora $x \in X$ si dice:
- interno ad $A$ se $\exists r > 0$   $B_{r}(x) \subseteq A$
- aderente ad $A$ se $\forall r > 0$   $B_{r}(x) \cap A \neq \emptyset$
- di frontiera o sul bordo di $A$ se aderente ad $A$ e a $\mathbb{R} \setminus A$
- isolato in $A$ se $\exists r>0$   $B_{r}(x) \cap A = \{ x \}$
- di accumulazione di $A$ se $\forall r>0$   $(B_{r}(x) \cap A) \setminus \{ x \} \neq \emptyset$

Il resto della terminologia segue come per $\mathbb{R}$.

$B_{r}(x)$ aperta.

$A \subseteq X$ si dice chiuso sequenzialmente se $\forall a_{n} \in A$   $a_{n}\to a \in X \implies a \in A$.

$A$ chiuso $\iff$ chiuso sequenzialmente.

DIMOSTRAZIONE:
1. Siano $A$ chiuso e $a_{k} \in A$ convergente a $a \in X$
2. $\forall \varepsilon > 0$   $\exists K \in \mathbb{N}$   $\forall k > K$   $d(a_{k},a) < \varepsilon$
3. $a_{k} \in B_{\varepsilon}(a)$, dunque $a \in A$

# Continuità
Siano $X$ e $Y$ spazi metrici, allora $f : X \to Y$ si dice sequenzialmente continua in $x \in X$ se:
- $\forall x_{n}\to x \in X$   $f(x_{n})\to f(x) \in Y$

Siano $X$ e $Y$ spazi metrici, allora $f:X \to Y$ si dice continua in $x \in X$ se:
- $\forall\varepsilon > 0$   $\exists \delta> 0$   $\forall y \in X$   $d(x,y)<\delta\implies d(f(x),f(y))<\varepsilon$

Siano $X$ e $Y$ spazi metrici, allora $f:X\to Y$ si dice topologicamente continua se:
- $\forall A$ aperto in $Y$   $f^{-1}(A)$ aperto in $X$

$f$ sequenzialmente continua $\iff f$ continua $\iff f$ topologicamente continua.

DIMOSTRAZIONE (sequenzialmente continua $\implies$ continua):
1. Per assurdo $f$ sequenzialmente continua ma non continua in $x$
2. $\exists \varepsilon > 0$   $\forall \delta =\frac{1}{k}$   $\exists y_{k}$   $d(y_{k},x) < \frac{1}{k} \land d(f(y_{k}),f(x)) \geq \varepsilon$
3. $y_{k} \to x$ e $f(y_{k})\to f(x)$, assurdo col punto precedente

DIMOSTRAZIONE (Resto delle implicazioni): Definizioni.

Siano $X$, $Y$ e $Z$ spazi metrici, $f : X \to Y$ e $g : Y \to Z$ continue, allora $g \circ f$ continua.

DIMOSTRAZIONE: Continuità sequenziale.

# Compattezza sequenziale
Sia $X$ spazio metrico, si dice limitato se esiste una palla che lo contiene.

Sia $X$ spazio metrico, si dice sequenzialmente compatto se $\forall x_{k} \in X$   $\exists x_{k_{j}}\to x \in X$.

Sia $K \in \mathbb{R}^n$ chiuso e limitato, allora $K$ sequenzialmente compatto.

DIMOSTRAZIONE:
1. Sia $x_{k} \in K$, allora per limitatezza $|x_{k}-y|<r$   $\forall k$
2. Dato $R = r + |y|$, per disuguaglianza triangolare $|x_{k}|<R$
3. Date $(x_{k})_{i}$ coordinate, per Bolzano - Weierstrass $(x_{k})_{1}$ ha un'estratta convergente
4. Ogni componente converge a $p_{i} \in \mathbb{R}$ e $x_{k} \to p \in \mathbb{R}^n$
5. Per chiusura $p \in K$ e $K$ sequenzialmente compatto

Sia $X$ spazio metrico e $A \subseteq X$ sequenzialmente compatto, allora $A$ chiuso e limitato.

DIMOSTRAZIONE: Diretta con la chiusura, assurdo con la limitatezza.

# Teorema di Weierstrass
Funzioni continue tra spazi metrici mandano sequenzialmente compatti in altri.

DIMOSTRAZIONE:
1. Sia $y_{k} \in f(K)$, allora $\exists x_{k} \in K$   $f(x_{k})=y_{k}$
2. Per compattezza $\exists x_{k_{j}}\to x$
3. Per continuità $y_{k_{j}}=f(x_{k_{j}})\to f(x) \in f(K)$

# Uniforme continuità
Siano $X$ e $Y$ spazi metrici, allora $f : X \to Y$ si dice uniformemente continua se:
- $\forall \varepsilon>0$   $\exists\delta>0$   $d(x,x')<\delta\implies d(f(x),f(x'))<\varepsilon$

# Teorema di Heine - Cantor
Siano $X$ spazio metrico sequenzialmente compatto, $Y$ spazio metrico e $f : X \to Y$ continua. Allora $f$ uniformemente continua.

DIMOSTRAZIONE:
1. Per assurdo $f$ continua non uniformemente
2. $\exists\varepsilon > 0$   $\forall \delta>0$   $\exists x,y \in X$   $d(x,y) < \delta \land d(f(x),f(y))\geq \varepsilon$
3. Fissato $\varepsilon$ si usa $\delta = \frac{1}{k}$ e si ha contraddizione con le definizioni

# Successione di Cauchy
Sia $(X,d)$ spazio metrico e $x_{k} \in X$. Allora $x_{k}$ si dice successione di Cauchy se:
- $\forall \varepsilon > 0$   $\exists n \in \mathbb{N}$   $\forall j > n$   $\forall k > n$   $d(x_{j},x_{k})<\varepsilon$

La proprietà delle successioni di Cauchy è equivalente a $\lim\limits_{k \to +\infty} \sup\limits_{{j \geq k}}d(x_{j},x_{k})=0$.

Sia $(X,d)$ spazio metrico e $x_{k} \in X$ convergente, allora è di Cauchy.

DIMOSTRAZIONE: Definizione e disuguaglianza triangolare.

# Completezza
$(X,d)$ spazio metrico si dice completo se ogni successione di Cauchy converge.

Uno spazio vettoriale normato si dice di Banach se completo come spazio metrico.

Uno spazio di Banach si dice di Hilbert se la norma è euclidea.

Successione di Cauchy $\implies$ limitata.

DIMOSTRAZIONE:
1. Sia $x_{k}$ di Cauchy, fissato $\varepsilon$ esiste $N$ per cui $\forall k>N$   $d(x_{k},x_{N+1})<\varepsilon$
2. Sia $R$ il massimo delle distanze con $d(x_{0},x_{N+1})+\varepsilon$, si ha $d(x_{0},x_{k})<R$
3. $x_{k} \in B_{R}(x_{0})$ dunque la successione è limitata

Sia $x_{k}$ di Cauchy, allora $x_{k_{j}}$ converge $\implies x_{k}$ converge.

DIMOSTRAZIONE: La distanza è infinitesima dal punto di convergenza.

$\mathbb{R}$ completo.

DIMOSTRAZIONE:
1. $x_{k}$ di Cauchy limitata
2. Per Bolzano - Weierstrass $x_{k}$ ha un'estratta convergente
3. Per il teorema precedente $x_{k}$ converge

$\mathbb{R}^n$ e $\mathbb{C}$ completi.

DIMOSTRAZIONE: $x_{k} \in \mathbb{R}^n$ converge se ogni componente converge, $\mathbb{C} \cong \mathbb{R}^2$.

Ogni spazio metrico sequenzialmente compatto è completo.

DIMOSTRAZIONE: Per compattezza ogni successione ha un'estratta convergente.

SIa $(X,d)$ spazio metrico e $A \subseteq X$ chiuso. Allora:
1. $X$ sequenzialmente compatto $\implies A$ sequenzialmente compatto
2. $X$ completo $\implies A$ completo

DIMOSTRAZIONE: Definizioni di Cauchy, compattezza, chiusura e completezza.

# Teorema di estensione
Siano $X$ e $Y$ spazi metrici, $Y$ completo, $A \subseteq X$, $f : A \to Y$ uniformemente continua, allora:
1. $\exists! \tilde{f} : \bar{A} \to Y$   $\forall x \in A$   $\tilde{f}(x)=f(x)$
2. $\tilde{f}$ uniformemente continua

DIMOSTRAZIONE:
1. $f$ manda successioni di Cauchy in successioni di Cauchy
2. $\forall x \in \bar{A}$   $\exists a_{n} \in A$   $a_{n} \to x$
3. $a_{n} \to a \implies a_{n}$ di Cauchy in quanto convergente
4. $f(a_{n})$ di Cauchy convergente in $Y$ per completezza
5. $f(a_{n})\to l$, dunque sia $\tilde{f}(x)=l$
6. $\tilde{f}$ uniformemente continua per costruzione

# Lipschitzianità
Siano $X$ e $Y$ spazi metrici e $f : X \to Y$ tale che $\forall x,y \in X$   $d(f(x),f(y))\leq Ld(x,y)$. Allora $f$ si dice $L$-lipschitziana.

$f$ si dice lipschitziana se $\exists L\geq 0$   $f$ $L$-lipschitziana.

$f$ lipschitziana $\implies f$ sequenzialmente continua.

DIMOSTRAZIONE: $d(x_{k},x) \to 0 \implies Ld(f(x_{k}),f(x))\to 0$.

# Teorema di Banach - Caccioppoli
Sia $X$ spazio metrico completo non vuoto e $f : X \to X$ lipschitziana con $L < 1$, anche detta contrazione. Allora $\exists! x \in X$   $f(x)=x$.

DIMOSTRAZIONE:
1. Sia $p \in X$ e si definisce $x_{k} \in X$ come la ricorrenza $x_{0}=p$, $x_{k+1} = f(x_{k})$
2. $f$ lipschitziana, quindi per induzione $d(x_{m+1}, x_{m})\leq L^md(x_{1},x_{0})$
3. Per disuguaglianza triangolare e serie geometria $x_{k}$ è di Cauchy
4. Per continuità $f$ ha un punto fisso, unico per assurdo

# Compattezza
Sia $X$ spazio topologico, si dice compatto se dato un ricoprimento aperto di $X$ esiste un sottoricoprimento finito.

Sia $X$ spazio metrico, si dice totalmente limitato se dato un raggio, esiste un ricoprimento finito di $X$ con palle di tale raggio.

Sia $X$ spazio metrico, allora $X$ compatto
- $\iff$ $X$ sequenzialmente compatto
- $\implies$ $X$ totalmente limitato

DIMOSTRAZIONE:
1. (compatto $\implies$ sequenzialmente compatto)
	1. Per ogni $\rho>0$ la famiglia di palle $B_{\rho}(x)$ è un ricoprimento aperto
	2. Sia $\{ x_{k} \} \in X$, si suppone per assurdo $x_{k}$ non ha estratte convergenti
	3. $\forall y \in X$   $\exists \rho$   $U_{y} = B_{\rho}(y)$ contiene un numero finito di $x_{k}$
	4. $\not\exists$ sottofamiglia che ricopre tutto $X \implies X$ non compatto
2. (sequenzialmente compatto $\implies$ totalmente limitato)
	1. Si suppone per assurdo $X$ non totalmente limitato
	2. $\exists \rho>0$   $\not\exists\{ B_{\rho}(x) \}$ finito che ricopre $X$
	3. Si può costruire una successione a distanza $> \rho$ senza estratte convergenti
3. (sequenzialmente compatto $\implies$ compatto) Numero di Lebesgue come in Analisi 1

# Convergenza uniforme
Siano $A$ insieme non vuoto e $f : A \to \mathbb{R}$, si definisce la norma uniforme $||f||_{\infty}:= \sup\limits_{x \in A} |f(x)|$.

La norma uniforme soddisfa tutte le proprietà della norma salvo che $||\cdot||_{\infty} \in [0,+\infty]$.

Siano $f,g : A \to \mathbb{R}$, la norma induce una metrica $d_{\infty}(f,g):=||f-g||_{\infty}$.

Si dice che $\{ f_{k} : A \to \mathbb{R} \}$ converge uniformemente a $f$ se $\lim\limits_{k \to \infty}d_{\infty}(f_{k},f) = 0$ e si denota con $f_{k} {}^{\longrightarrow}_{\longrightarrow} f$.

Si dice che $\{ f_{k} : A \to \mathbb{R} \}$ converge puntualmente a $f$ se $\forall x \in A$   $\lim\limits_{k \to \infty} f_{k}(x) = f(x)$ e si denota con $f_{k} \to f$.

$f_{k} {}^{\longrightarrow}_{\longrightarrow}f \implies f_{k} \to f$.

DIMOSTRAZIONE: Il limite uniforme, se esiste, coincide con quello puntuale.

Sia $A$ insieme, allora $\mathscr{B}(A)=\{ f\in \mathbb{R}^A : ||f||_{\infty}<+\infty \}$ spazio di Banach con:
- distanza $d_{\infty}$ indotta da $||\cdot||_{\infty}$
- convergenza uniforme indotta da $d_{\infty}$

DIMOSTRAZIONE:
1. $\mathscr{B}(A)$ spazio vettoriale
2. $f$ limitate $\implies ||f||_{\infty} < +\infty \implies \mathscr{B}(A)$ spazio normato
3. $|f_{k}(x)-f_{j}(x)|\leq ||f_{k}-f_{j}||_{\infty} \implies f_{k}(x)$ converge in $\mathbb{R}$
4. Sia $f = \lim f_{k}(x)$, per disuguaglianza triangolare $f  \in \mathscr{B}(A)$

Sia $X$ spazio metrico e $f_{k} : X \to \mathbb{R}$ continue che convergono uniformemente a $f : X \to \mathbb{R}$, allora $f$ continua.

DIMOSTRAZIONE:
1. Per convergenza uniforme $\forall \varepsilon > 0$   $\exists N \in \mathbb{N}$   $d_{\infty}(f_{N},f)<\varepsilon$
2. Per continuità di $f_{N}$ in corrispondenza di $\varepsilon$   $\exists\delta>0$   $d(x,x_{0})<\delta\implies |f_{N}(x)-f_{N}(x_{0})|<\varepsilon$
3. Per disuguaglianza triangolare $|f(x)-f(x_{0})| \leq 3\varepsilon$

$C^0([a,b])$ con $||\cdot||_{\infty}$ spazio di Banach.

DIMOSTRAZIONE:
1. Per Weierstrass ogni funzione continua in $[a,b]$ è limitata
2. $C^0([a,b])$ sottospazio vettoriale di $\mathscr{B}([a,b])$
3. Per il teorema precedente $C^0([a,b])$ chiuso e completo

Per il precedente teorema la norma uniforme è anche chiamata norma $C^0$.