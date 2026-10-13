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

# Teorema di Dini
Sia $f_{k} \in C^0([a,b])$ monotona in $k$ tale che $f_{k}\to f \in C^0([a,b])$. Allora $f_{k} {}^{\longrightarrow}_{\longrightarrow} f$.

DIMOSTRAZIONE:
1. $g_{k} := f - f_{k}$ continua, decrescente, $g_{k}\to 0$ puntualmente
2. $g_{k}\geq 0$ poiché $\forall x \in [a,b]$   $g_{k}(x) = f(x)-f_{k}(x) = \lim\limits_{h \to +\infty} [f_{h}(x)-f_{k}(x)] \geq 0$ per $h\geq k$
3. Fissato $\varepsilon > 0$, si definisce $U_{k} := \{ x \in [a,b] : g_{k}(x)\leq\varepsilon \}$
4. $\forall x \in [a,b]$   $\exists k(x)$   $x \in U_{k(x)}$   poiché $g_{k(x)}\to 0$
5. $\bigcup\limits_{x \in [a,b]} U_{k(x)} = [a,b]$ e $[a,b]$ compatto, per cui $\exists$ sottoricoprimento finito $U_{k_{1}},\dots,U_{k_{n}}$
6. $\bigcup\limits_{k_{i} = k_{1},\dots,k_{N}} U_{k_{i}} = U_{k_{N}}$ poiché $U_{k} \subseteq U_{k+1} \subseteq \dots$
7. $[a,b]  = U_{k_{N}} = \{ g_{k(N)} < \varepsilon \}$

Sia $f_{k} : [a,b] \to \mathbb{R}$ crescente in $[a,b]$ tale che $f_{k}\to f \in C^0([a,b])$. Allora $f_{k} {}^{\longrightarrow}_{\longrightarrow} f$.

DIMOSTRAZIONE:
1. Fissato $\varepsilon > 0$, si considera $x \in [a,b]$
2. $[a,b] := \bigcup\limits_{i=0,\dots,N} [x_{i},x_{i+1}]$ tale che $x_{i+1}-x_{i} < \delta$
3. $\forall x \in [a,b]$   $\exists i=0,\dots,N$   $x \in [x_{i},x_{i+1}]$
4. $|f_{k}(x)-f(x)| \leq |f_{k}(x) - f_{k}(x_{i})| + |f_{k}(x_{i}) - f(x_{i})| + |f(x_{i}) - f(x)|$
5. Sia $\bar{k}$ il $k$ tale da garantire la convergenza uniforme di $f_{k}(x_{i})$
6. $|f_{k}(x_{i})-f(x_{i})|<\varepsilon$ se $k \geq \max\limits_{i=0,\dots,N}\{ \bar{k}(\varepsilon,x_{i}) \}$
7. $|f(x_{i})-f(x)|<\varepsilon$ per uniforme continuità
8. $f_{k}(x)-f(x) = [f_{k}(x)-f_{k}(x_{i+1})] + [f_{k}(x_{i+1}) - f(x_{i+1})]+[f(x_{i+1}) - f(x)] < 2\varepsilon$
9. $f_{k}(x)-f(x) = [f_{k}(x)-f_{k}(x_{i})] + [f_{k}(x_{i}) - f(x_{i})] + [f(x_{i})-f(x)] > -2\varepsilon$
10. $|f_{k}(x)-f(x)| < 2\varepsilon$

# Scambio limite - integrale
Siano $f_{n},f : [a,b] \to X$ limitate e Riemann integrabili su $[a,b]$ con $f_{n} {}^{\longrightarrow}_{\longrightarrow} f$. Allora:
1. $\lim\limits_{n \to +\infty} \int_{a}^{b} f_{n}(x) \, dx = \int_{a}^{b} f(x) \, dx$.
2. $\forall c \in [a,b]$   $F_{k}(x) = \int_{c}^{x} f_{k}(t) \, dt$   $F(x)=\int_{c}^{x} f(t) \, dt$   $F_{k} {}^{\longrightarrow}_{\longrightarrow}F$

DIMOSTRAZIONE:
1. $f_{n}, f$ Riemann integrabili $\implies f_{n}-f, |f_{n}-f|$ Riemann integrabili
2. $\left|\int_{a}^{b} f_{n}(x) \, dx - \int_{a}^{b} f(x) \, dx\right| \leq \int_{a}^{b} |f_{n}(x)-f(x)| \, dx \leq \int_{a}^{b} \sup\limits_{t \in [a,b]}|f_{n}(t)-f(t)| \, dx$
3. Il termine sopra si riduce a $\sup\limits_{t \in [a,b]}|f_{n}(t)-f(t)|\int_{a}^{b} 1 \, dx \to 0$
4. $||F_{k}-F||_{\infty} = \sup\limits_{x \in [a,b]}\left|\int_{c}^{x}f_{k}(t)-f(t)  \, dt\right| \leq \sup\limits_{x \in [a.b]}|x-c| \cdot ||f_{k}-f||_{\infty} \leq (b-a)||f_{k}-f||_{\infty}\to {0}$

# Convergenza dominata
Siano $f_{k},f,g:(a,b) \to \mathbb{R}$ con $a,b \in \overline{\mathbb{R}}$ tali che:
1. $\forall [\alpha,\beta] \subseteq (a,b)$   $f_{k} {}^{\longrightarrow}_{\longrightarrow} f$ su $[\alpha,\beta]$
2. $f$ e $f$ localmente Riemann integrabili su $(a,b)$
3. $g$ integrabile impropriamente su $(a,b)$ con integrale convergente
4. $|f_{k}(x)|\leq g(x)$   $\forall k \in \mathbb{N}$   $\forall x \in (a,b)$
Allora $f_{k}$ e $f$ hanno integrale improprio convergente su $(a,b)$ e $\lim\limits_{k \to +\infty} \int_{a}^{b} f_{k}(x) \, dx = \int_{a}^{b} f(x) \, dx$.

DIMOSTRAZIONE:
1. $f_{k}$ integrabile impropriamente poiché $|f_{k}(x)|\leq g(x)$   $\forall x \in(a,b)$
2. $f$ ha integrale assolutamente convergente su $(a,b)$
3. $\forall \varepsilon > 0$   $\exists \alpha > a$   $\exists \beta < b$   $\int_{\beta}^{b} g(x) \, dx < \varepsilon$   $\int_{a}^{\alpha} g(x) \, dx<\varepsilon$
4. Per il teorema precedente $\left\lvert  \int_{\alpha}^{\beta} f_{k}(x) \, dx - \int_{\alpha}^{\beta} f(x) \, dx  \right\rvert \leq \varepsilon$
5. Unendo le due cose si ha la tesi

Siano:
1. $I \subseteq \mathbb{R}$ intervallo
2. $a,b \in \overline{\mathbb{R}}$
3. $f : I \times(a,b) \to \mathbb{R}$ continua
4. $g : (a,b) \to \mathbb{R}$ continua con integrale improprio convergente
5. $\forall x \in I$   $\forall t \in (a,b)$   $|f(x,t)|\leq g(t)$
Allora $\forall x \in I$   $\lim\limits_{y \to x} \int_{a}^{b} f(y,t) \, dt = \int_{a}^{b} f(x,t) \, dt$.

DIMOSTRAZIONE:
1. Wlog sia $I$ chiuso e limitato che contiene $x$
2. $f$ continua su $I \times [\alpha,\beta]$ sequenzialmente compatto
3. $f$ uniformemente continua su $I \times [\alpha,\beta]$ per Heine - Cantor
4. $\forall \varepsilon > 0$   $\exists \delta > 0$   $\forall x,y \in I$   $\forall s,t \in [\alpha,\beta]$   $\sqrt{ (x-y)^{2} + (t-s)^{2}} < \delta \implies |f(x,t)-f(y,s)|< \varepsilon$
5. $\forall \varepsilon > 0$   $x \in I \land |x-y|<\delta \implies \sup\limits_{t \in [\alpha,\beta]}|f(y,t) - f(x,t)|\leq \varepsilon \implies \lim\limits_{y \to x} \sup\limits_{t}|f(y,t),f(x,t)|=0$

# Scambio derivata - integrale
Siano:
1. $I \subseteq \mathbb{R}$ intervallo
2. $a,b \in \overline{\mathbb{R}}$
3. $f : I \times (a,b) \to \mathbb{R}$ continua
4. $\forall x \in I$   $\forall t \in (a,b)$   $f$ derivabile rispetto a $x$
5. $\frac{{\partial f}}{\partial x}$ continua su $I \times (a,b)$
6. $\forall x \in I$   $\int_{a}^{b} f(x,t) \, dt$ convergente
7. $\exists G : (a,b) \to \mathbb{R}$ localmente Riemann integrabile con integrale convergente
8. $\forall x \in I$   $\forall t \in (a,b)$   $\left\lvert  \frac{{\partial f}}{\partial x}(x,t)  \right\rvert \leq G(t)$
Allora $\forall x \in I$   $\frac{d}{dx}\int_{a}^{b} f(x,t) \, dt = \int_{a}^{b} \frac{{\partial f}}{\partial x}(x,t) \, dt$.

DIMOSTRAZIONE:
1. Siano $x_{0} \in I$ e $g(x,t)=\frac{f(x,t)-f(x_{0},t)}{x-x_{0}}$ se $x \neq x_{0}$, altrimenti $g(x,t)=\frac{{\partial f}}{\partial x}(x,t)$
2. $\frac{d}{dx}\int_{a}^{b} f(x,t) \, dt = \lim\limits_{x \to x_{0}} \frac{\int_{a}^{b} f(x,t) \, dt - \int_{a}^{b} f(x_{0},t) \, dt}{x-x_{0}} = \lim\limits_{x \to x_{0}} \int_{a}^{b} g(x,t) \, dt$
3. $\int_{a}^{b} \frac{{\partial f}}{\partial x}(x,t) \, dt = \int_{a}^{b} g(x_{0},t) \, dt$
4. Per Lagrange $\forall x \in I$   $\forall t \in (a,b)$   $\exists x' \in I$   $|x'-x_{0}| < |x-x_{0}|$   $|g(x,t)|=\left\lvert  \frac{{\partial f}}{\partial x}(x',t)  \right\rvert\leq G(t)$
5. Se $x \neq x_{0}$ la funzione $g : I \times (a,b) \to \mathbb{R}$ è continua
6. $\forall \varepsilon > 0$   $\exists \delta > 0$   $\sqrt{ (x-x_{0})^{2} +(t-t_{0})^{2}}<\delta \implies \left\lvert  \frac{{\partial f}}{\partial x}(x,t) - \frac{{\partial f}}{\partial x}(x_{0},t_{0})  \right\rvert < \varepsilon$
7. Per Lagrange $|(x,t)-(x_{0},t_{0})|< \delta \implies |g(x,t)-g(x_{0},t_{0})| = \left\lvert   \frac{{\partial f}}{\partial x}(x',t) - \frac{{\partial f}}{\partial x}(x_{0},t_{0})  \right\rvert<\varepsilon$

# Scambio derivata - limite
Siano:
1. $I \subseteq \mathbb{R}$ intervallo
2. $f_{k} \in C^1(I)$   $f_{k}(x_{0})$ converge per almeno $x_{0} \in I$
3. $f_{k}' {}^{\longrightarrow}_{\longrightarrow} g : I \to \mathbb{R}$   $\forall [a,b] \subseteq I$
Allora
- $\exists f \in C^1(I)$   $f' = g$   $f_{k} {}^{\longrightarrow}_{\longrightarrow} f$   $\forall[a,b] \subseteq I$
- $\lim\limits_{k \to +\infty} f_{k}'(x) = f'(x) = \left[\lim\limits_{k \to +\infty} f_{k}(x)\right]'$   $\forall x \in I$

DIMOSTRAZIONE:
1. Per ipotesi $\exists y_{0} \in \mathbb{R}$   $f_{k}(x_{0}) \to y_{0}$
2. Sia $f(x)=y_{0} + \int_{x_{0}}^{x} g(t) \, dt$
3. Per continuità del limite $g$ è continua
4. Per il teorema fondamentale del calcolo integrale $f' = g$
5. Per la formula fondamentale del calcolo integrale $\int_{x_{0}}^{x} f_{k}'(t) \, dt  = f_{k}(x)-f_{k}(x_{0})$
6. $\sup\limits_{x \in [a,b]}|f_{k}(x)-f(x)| \leq |f_{k}(x_{0})-y_{0}| + (b-a)||f_{k}'-g||\to 0$

# Norma $C^1$
$C^1([a,b])$ spazio vettoriale con $||\cdot||_{C^1}$ data da $||f||_{C^1} = ||f||_{\infty}+||f'||_{\infty}$ è di Banach.

DIMOSTRAZIONE:
1. $||\cdot||_{C^1}$ è una norma
2. Sia $f_{k}$ di Cauchy, allora anche $f_{k}'$ di Cauchy poiché $||f_{k}||_{\infty}<||f_{k}||_{C^1}$ e $||f_{k}'||_{\infty} < ||f_{k}'||_{C^1}$
3. Per completezza di $C^0$ esistono $f,g \in C^0$ tali che $f_{k} {}^{\longrightarrow}_{\longrightarrow} f$ e $f_{k}' {}^{\longrightarrow}_{\longrightarrow} g$
4. Per il teorema di passaggio al limite $f \in C^1$ e $f' = g$, per cui $||f_{k}-f||_{C^1}\to 0$

L'operatore integrale $S : C^0 \to C^1$ è continuo.

L'operatore differenziale $D : C^1 \to C^0 : f \mapsto f'$ è continuo.