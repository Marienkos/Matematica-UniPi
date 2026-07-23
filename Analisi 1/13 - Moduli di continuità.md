# Uniforme continuità
Sia $A \subseteq \mathbb{R}$ e $f : A \to \mathbb{R}$. Si dice $f$ continua in $A$ se:
- $\forall \varepsilon>0$   $\forall x \in A$   $\exists\delta>0$   $\forall y \in A$   $|x-y|\leq\delta \implies |f(x)-f(y)|\leq \varepsilon$

Sia $A \subseteq \mathbb{R}$ e $f : A \to \mathbb{R}$. Si dice $f$ uniformemente continua (UC) in $A$ se:
- $\forall \varepsilon>0$   $\exists\delta>0$   $\forall x \in A$   $\forall y \in A$   $|x-y|\leq\delta \implies |f(x)-f(y)|\leq \varepsilon$

La continuità è topologica (locale), mentre l'uniforme continuità è metrica (globale).

$f$ Lipschitziana in $A$ $\implies$ $f$ UC in $A$

~={green}DIMOSTRAZIONE=~:
1. Per Lipschizianità $|f(x)-f(y)|\leq L|x-y|$
2. Sia $\varepsilon>0$, considero $\delta := \frac{\varepsilon}{L}$
3. $|f(x)-f(y)|\leq L|x-y|\leq L \frac{\varepsilon}{L} \leq \varepsilon$

Valgono:
- $f$ e $g$ UC in $A$ $\implies f+g$ UC in $A$
- $f$ UC in $A$ e $\lambda \in \mathbb{R}$ $\implies$ $\lambda f$ UC in $A$
- $f$ e $g$ UC e limitate in $A$ $\implies$ $fg$ UC in $A$
- $f$ UC in $A$ e $B \subseteq A$ $\implies$$f$ UC in $B$
- $a<b<c$, $f$ UC in $[a,b]$ e $f$ UC in $[b,c]$ $\implies$ $f$ UC in $[a,c]$

~={green}DIMOSTRAZIONE=~:
- Uso $\delta_{1}$ e $\delta_{2}$  per avere la definizione con $f$ e $g$ e $\frac{1}{2}\varepsilon$
- Sia $\varepsilon>0$, trovo $\delta$ tale che $|x-y| \leq \delta \implies |f(x)-f(y)|\leq \frac{\varepsilon}{|\lambda|}$
- Sia $\varepsilon>0$, trovo $\delta$ tale che $|f(x)-f(y)|\leq \frac{1}{2}\varepsilon {\frac{1}{M_{g}}}$ e così con $g$
- Ovvio
- Considero $\delta$ che garantisce $\frac{\varepsilon}{2}$ nei due sottointervalli

Sia $A \subseteq \mathbb{R}$ e $f : A \to \mathbb{R}$ UC. Sia $\{ x_{n} \} \subseteq A$ di Cauchy. Allora $\{ f(x_{n}) \}$ di Cauchy.

~={pink}DIMOSTRAZIONE=~:
1. Considero $\varepsilon>0$ e trovo $\delta$ in quanto $f$ è UC
2. Applico la definizione di successione di Cauchy a $x_{n}$
3. Di conseguenza $|f(x_{n})-f(x_{m})|\leq \varepsilon$

# Teorema di estensione
Sia $f : A \to \mathbb{R}$ UC. Allora $\exists!\hat{f} : \text{Clos}(A) \to \mathbb{R}$ UC tale che $\hat{f}(x) = f(x)$ in tutto $A$.

~={cyan}DIMOSTRAZIONE=~:
1. Considero $x \in \text{Clos}(A)$
2. $\exists \{ x_{n} \} \subseteq A$   $x_{n} \to x$   ossia $x_{n}$ di Cauchy
3. $\{ f(x_{n}) \}$ di Cauchy, pongo $\hat{f}(x) := \lim\limits_{n \to +\infty} f(x_{n})$
4. La definizione precedente è ben posta
5. $\hat{f}$ estende $f$
6. $\hat{f}$ UC usando $\hat{\delta} \in (0,\delta)$ e passando al limite

# Teorema di Heine - Cantor
Sia $f : A \to \mathbb{R}$ tale che:
1. $f$ continua in $A$
2. $A$ compatto
Allora $f$ UC in $A$

~={red}DIMOSTRAZIONE=~ (Compattezza per successioni):
1. Supponiamo $\exists \varepsilon_{0}> 0$   $\forall\delta>0$   $\exists x,y \in A$   $|x-y| \leq \delta \land |f(x)-f(y)| > \varepsilon_{0}$
2. Considero $\delta = \frac{1}{n}$ o qualsiasi cosa tenda a $0$
3. $|x_{n} - y_{n}|\leq \frac{1}{n} \land |f(x_{n}) - f(y_{n})|> \varepsilon_{0}$
4. Per compattezza per successioni $\exists x_{n_{k}}\to x_{\infty}$
5. Per confronto $x_{n_{k}} - \frac{1}{n_{k}} \leq y_{n_{k}} \leq x_{n_{k}} + \frac{1}{n_{k}}$ da cui $y_{n_{k}} \to x_{\infty}$
6. $|f(x_{n_{k}}) - f(y_{n_{k}})|>\varepsilon_{0}$ e passando al limite $0 > \varepsilon_{0}$ 

~={cyan}DIMOSTRAZIONE=~ (Compattezza per ricoprimenti):
1. Per continuità $\forall x \in A$   $\exists\delta(x,\varepsilon)>0$   $\forall y \in A$   $|x-y|\leq\delta \implies |f(x)-f(y)| \leq \frac{\varepsilon}{2}$
2. Siano $y_{1},y_{2} \in [x-\delta, x+\delta] \cap A$
3. $|f(y_{1})-f(y_{2})| \leq |f(y_{1}) - f(x)| + |f(y_{2})-f(x)|\leq \frac{\varepsilon}{2} + \frac{\varepsilon}{2} = \varepsilon$
4. $u_{x} = (x-\delta(x), x + \delta(x))$ ricoprimento aperto di $A \implies$ ammette sottoricoprimento finito
5. Considero il raggio magico del ricoprimento

# Teorema asintotico
Sia $a \in \mathbb{R}$ e $f : [a,+\infty) \to \mathbb{R}$ tale che:
1. $f$ continua
2. $\exists \lim\limits_{x \to +\infty} f(x) \in \mathbb{R}$
Allora $f$ UC in $[a,+\infty)$

~={pink}DIMOSTRAZIONE=~: Heine - Cantor.

Siano $f,g : [a,+\infty) \to \mathbb{R}$ tali che:
1. $f$ continua
2. g UC
3. $f(x)-g(x)\to 0$ per $x \to +\infty$
Allora $f$ UC in $[a,+\infty)$

~={pink}DIMOSTRAZIONE=~: $f(x) = g(x) + [f(x) - g(x)]$, ossia $f$ = UC + UC = UC.

# Teorema di sublinearità
Sia $a \in \mathbb{R}$ e $f : [a,+\infty) \to \mathbb{R}$ UC. Allora $f$ sublineare, cioè $\exists A,B$   $\forall x\geq a$   $f(x) \leq A(x-a) + B$

~={cyan}DIMOSTRAZIONE=~:
1. Per uniforme continuità con $\varepsilon=1$ trovo $\delta$ tale che $|x-y|\leq \delta \implies |f(x)-f(y)|\leq 1$
2. Per induzione su $k$ vale la tesi con $A:=\frac{1}{\delta}$ e $B:= \max\{ f(x) : x \in [a, a+\delta] \}$

$f : [a,+\infty) \to \mathbb{R}$ UC $\implies f(x) = O(x)$ per $x \to +\infty$

~={cyan}DIMOSTRAZIONE=~:
1. $|f(x)| \leq Ax+B$
2. $\limsup\limits_{x \to +\infty} \frac{|f(x)|}{x} \leq \limsup\limits_{x \to +\infty} \frac{{Ax+B}}{x} = A$

# Hölderianità
Sia $A \subseteq \mathbb{R}$ e $f : A \to \mathbb{R}$. Sia $a \in (0,1]$. Si dice $f$ $a$-Hölderiana in $A$ se:
- $\exists H \in \mathbb{R}$   $\forall x,y \in A$   $|f(x)-f(y)|\leq H|x-y|^a$

$f$ $a$-Hölderiana con $a>1$ $\implies$ $f$ costante

~={pink}DIMOSTRAZIONE=~: $f'(x) = 0$

Valgono:
- $f$ e $g$ $a$-Hölderiane $\implies$ $f\pm g$ $a$-Hölderiana
- $f$ $a$-Hölderiana $\implies$ $\lambda f$ $a$-Hölderiana
- $f$ e $g$ $a$-Hölderiane e limitate in $A$ $\implies$ $fg$ $a$-Hölderiana
- $f$ $a$-Hölderiana e limitata in $A$ e $b\leq a$ $\implies$ $f$ $b$-Hölderiana
- $f$ $a$-Hölderiana e $g$ $b$-Hölderiana $\implies$ $g \circ f$ $ab$-Hölderiana

~={pink}DIMOSTRAZIONE=~: Definizioni.

# Criterio di Hölderianità
Sia $f : A \to \mathbb{R}$ continua, $|f|^{1/a}$ Lipschitziana e $A$ connesso. Allora $f$ $a$-Hölderiana in $A$.

~={cyan}DIMOSTRAZIONE=~:
1. $|f(x)-f(y)| = |(f(x)^{1/a})^a - (f(y)^{1/a})^a| \leq H|f(x)^{1/a}-f(y)^{1/a}|^a \leq HL^a|x-y|^a$
2. Divisione in casi per fixare i problemi di segno

# Moduli di continuità
Data $f$, vale: Lipschitziana e limitata $\implies$ $a$-Hölderiana $\implies$ UC $\implies$ continua

Si usa la seguente notazione:
- $C^0$ per le funzioni continue
- $C^1$ per le funzioni derivabili
- $C^{0,a}$ per le funzioni $a$-Hölderiane
- $C^{k,a}$ per le funzioni derivabili $k$ volte la cui $k$-esima derivata è $a$-Hölderiana
- $C^{0,1}$ per le funzioni Lipschitziane

Sia $f : A \to \mathbb{R}$. Se $|f(x)-f(y)|\leq \omega(|x-y|)$ con $\omega : [0,+\infty) \to [0,+\infty)$ allora si dice $f$ $\omega$-continua, si denota con $f \in C^{0,\omega}$ e si parla di modulo di continuità.

# Integrabilità
Sia $f : [a,b] \to \mathbb{R}$ continua. Allora $f$ integrabile in $[a,b]$.

~={green}DIMOSTRAZIONE=~:
1. Sia $\delta>0$, per Heine - Cantor $\exists\delta>0$   $|x-y|\leq\delta \implies |f(x)-f(y)|\leq \frac{\varepsilon}{b-a}$
2. Costruisco step function $\varphi_{\varepsilon}$ e $\psi_{\varepsilon}$ partizionando in intervalli $\leq\delta$
3. Per Weierstrass in ogni intervallo posso porre $\varphi_{\varepsilon},\psi_{\varepsilon} = \min, \max$
4. In ogni intervallo $\int_{a}^{b} (\psi_{\varepsilon}-\varphi_{\varepsilon}) \, dx \leq \frac{\varepsilon}{b-a}(b-a)=\varepsilon$

Se so che $f$ è $a$-Hölderiana, ho una stima dell'errore nell'approssimare un integrale.

Sia $f : [a,+\infty) \to \mathbb{R}$ tale che $\int_{a}^{+\infty} f(x) \, dx$ converge. Allora $\liminf\limits_{x \to +\infty} f(x)\leq 0 \leq \limsup\limits_{x \to +\infty} f(x)$.

~={red}DIMOSTRAZIONE=~:
1. Supponiamo $\liminf\limits_{x \to +\infty} f(x) = l > 0$
2. $\exists A>a$   $\forall x\geq A$   $f(x)\geq \frac{l}{2}$
3. $\int_{a}^{B} f(x) \, dx = \int_{a}^{A} f(x) \, dx + \int_{A}^{B} f(x) \, dx \geq \int_{a}^{A} f(x) \, dx + \frac{l}{2}(B-A)$
4. Per $B \to +\infty$ si ha $\int_{a}^{+\infty} f(x) \, dx = +\infty$ che è assurdo.

Sia $f : [a,+\infty) \to \mathbb{R}$ UC tale che $\int_{a}^{+\infty} f(x) \, dx$ converge. Allora $\lim\limits_{x \to +\infty} f(x) = 0$.

~={green}DIMOSTRAZIONE=~:
1. Supponiamo $\limsup\limits_{x \to +\infty} f(x) = L >0$
2. Per caratterizzazione $\exists x_{n} \to +\infty$   $f(x_{n}) \geq \frac{L}{2}$
3. Uso UC con $\varepsilon = \frac{L}{4}$ e passo all'integrale.