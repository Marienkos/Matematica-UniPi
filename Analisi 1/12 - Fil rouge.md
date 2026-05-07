# Fil rouge del calcolo differenziale
A partire dagli assiomi di $\mathbb{R}$ si può, in ordine, dimostrare:
1. Weierstrass
2. Rolle
3. Cauchy $\to$ De L'Hôpital $\to$ Taylor
4. Lagrange $\to$ monotonia

# Teorema di Rolle
Sia $f : [a,b] \to \mathbb{R}$ tale che:
1. $f$ continua in $[a,b]$
2. $f$ derivabile in $(a,b)$
3. $f(a) = f(b)$
Allora $\exists c \in (a,b)$   $f'(c) = 0$

DIMOSTRAZIONE:
1. Per Weierstrass esistono max e min
	- Se uno dei due sta in $(a,b)$, allora è $c$
	- Se max e min sono al bordo, allora $f$ è costante

# Teorema di Cauchy
Siano $f,g : [a,b] \to \mathbb{R}$ tali che:
1. $f$ e $g$ continue in $[a,b]$
2. $f$ e $g$ derivabili in $(a,b)$
Allora $\exists c \in (a,b)$   $(f(b) - f(a))g'(c) = (g(b)-g(a))f'(c)$

Inoltre se $g'(x) \neq 0$ in tutto $(a,b)$, allora:
1. $g(b) \neq g(a)$
2. $\frac{{f(b)-f(a)}}{g(b)-g(a)} = \frac{f'(c)}{g'(c)}$

DIMOSTRAZIONE:
1. Considero $\varphi(x) := (f(b)-f(a))g(x) - (g(b)-g(a))f(x)$
2. $\varphi(a) = \varphi(b)$ per sostituzione $\implies \varphi : [a,b] \to \mathbb{R}$ verifica le ipotesi di Rolle
3. $\exists c \in (a,b)$   $\varphi'(c) = 0 \implies$ prima tesi
4. Se $g$ non verifica le ipotesi di Rolle vale la seconda tesi

# Teorema di Lagrange
Sia $f : [a,b] \to \mathbb{R}$ tale che:
1. $f$ continua in $[a,b]$
2. $f$ derivabile in $(a,b)$
Allora $\exists c \in (a,b)$   $f(b)-f(a) = f'(c)(b-a)$

DIMOSTRAZIONE: Cauchy con $g(x) = x$.

DIMOSTRAZIONE:
1. Considero $\varphi(x) = f(x) - mx-q$
2. $\varphi(a) = \varphi(b) = 0 \implies$ Rolle su $\varphi$
3. $\varphi'(c) = f'(c) - m \implies$ tesi

# De L'Hôpital
Siano $x_{0} \in \mathbb{R}, r>0, f,g : (x_{0},x_{0}+r) \to  \mathbb{R}$ tali che:
1. $f$ e $g$ sono continue e derivabili in $(x_{0},x_{0}+r)$
2. $\lim\limits_{x \to x_{0}^+} f(x) = \lim\limits_{x \to x_{0}^+} g(x) = 0$
3. $g'(x) \neq 0$   $\forall x \in (x_{0},x_{0}+r)$
Allora $g(x) \neq 0$   $\forall x \in (x_{0},x_{0}+r)$   e   $\liminf\limits_{x \to x_{0}^+} \frac{f'(x)}{g'(x)} \leq \liminf\limits_{x \to x_{0}^+} \frac{f(x)}{g(x)} \leq \limsup\limits_{x \to x_{0}^+} \frac{f(x)}{g(x)} \leq \limsup\limits_{x \to x_{0}^+} \frac{f'(x)}{g'(x)}$

DIMOSTRAZIONE:
1. $g(x) \neq 0$
	1. Estendo $g$ a $\hat{g} : [x_{0},x_{0}+r) \to \mathbb{R}$ con $\hat{g}(x_{0})=0$
	2. $\hat{g}$ è continua
	3. Supponiamo $\exists y_{0} \in (x_{0},x_{0}+r)$   $g(y_{0}) = 0$
	4. $\hat{g}$ verifica le ipotesi di Rolle in $[x_{0},y_{0}]$
	5. $\exists c \in (x_{0},y_{0})$   $\hat{g}'(c) = 0$, ma $\hat{g}'(c) = g'(c) \neq 0 \implies$ assurdo
2. Vale la quadrupla disuguaglianza
	1. Se il limsup a destra è $+\infty$ è banale, altrimenti è $L \in \mathbb{R}$
	2. Per caratterizzazione, $\forall \varepsilon>0$   $\exists \delta \in (0,r)$   $\forall x \in (x_{0},x_{0}+\delta)$   $\frac{f'(x)}{g'(x)}\leq L+\varepsilon$
	3. Si estendono $f$ e $g$ a $\hat{f}$ e $\hat{g}$ definite come sopra
	4. $\frac{f(x)}{g(x)} = \frac{\hat{f}(x)}{\hat{g}(x)} = \frac{{\hat{f}(x)-\hat{f}(x_{0})}}{\hat{g}(x)-\hat{g}(x_{0})} =\frac{f'(c)}{g'(c)} \leq L + \varepsilon$ per Cauchy in $[x_{0},x]$
	5. $\limsup\limits_{x \to x_{0}^+} \frac{f(x)}{g(x)} \leq L+\varepsilon$   $\forall \varepsilon > 0 \implies \limsup\limits_{x \to x_{0}^+} \frac{f(x)}{g(x)} \leq L$

Vale anche per limiti nella forma $\frac{*}{\infty}$

DIMOSTRAZIONE:
1. Sia come prima $\frac{f'(x)}{g'(x)} \leq L+\varepsilon$
2. $\frac{f(x)}{g(x)} = \frac{{f(x)-f(x_{0}+\delta) + f(x_{0}+\delta)}}{g(x)}$
3. $\frac{{f(x)-f(x_{0}+\delta)}}{g(x)-g(x_{0}+\delta)} = \frac{f'(c)}{g'(c)} \leq L + \varepsilon \implies f(x) - f(x_{0}+\delta) \leq (L+\varepsilon)(g(x)-g(x_{0}+\delta))$
4. $\frac{f(x)}{g(x)} \leq \frac{{(L+\varepsilon)(g(x)-g(x_{0}+\delta))+f(x_{0}+\delta)}}{g(x)} \leq L+\varepsilon + \frac{{-(L+\varepsilon)g(x_{0}+\delta)+f(x_{0}+\delta)}}{g(x)} \to L+\varepsilon$
5. Si fa il limsup a entrambi i membri

# Dimostrazione comune di Taylor
$P_{n}(x)$ è l'unico polinomio di grado $\leq n$ tale $P_{n}^{(k)}(0) = f^{(k)}(0)$ per $k$ naturali in $[0,n]$.

$[x^k]^{(i)} = \frac{k!}{(k-i)!}x^{k-i}$

DIMOSTRAZIONE: Induzione su $i$.

Sia $Q(x) = a_{0} + \dots + a_{n}x^n$. Allora $Q^{(i)}(0) = a_{i}i$

DIMOSTRAZIONE: Derivata del monomio e della somma.

Sia $P_{n}(x)$ il polinomio di Taylor di $f$. Allora $P_{n}^{(i)}(0) = i!\frac{f^{(i)}(0)}{i!} = f^{(i)}(0)$

Sia $\varphi(x) = f(x) - P_{n}(x)$. Vale $\varphi^{(k)}(0) = 0$

# Finale di Taylor - Peano
Sia $\varphi : (-r,r) \to \mathbb{R}$ tale che:
1. $\varphi$ derivabile $(n-1)$ volte in $(-r,r)$
2. $\varphi$ derivabile $n$ volte in $0$
3. $\varphi^{(k)}(0) = 0$
Allora $\varphi(x) = o(x^n)$ per $x\to 0$

DIMOSTRAZIONE: De L'Hôpital e definizione di derivata.

# Finale di Taylor - Lagrange
Sia $\varphi : (-r,r) \to \mathbb{R}$ tale che:
1. $\varphi$ derivabile $(n-1)$ volte in $(-r,r)$
2. $\varphi^{(k)}(0) = 0$
Allora $\forall x \in (-r,r)$   $\exists c \in (0,x)$   $\varphi(x) = \frac{\varphi^{(n+1)}(c)}{(n+1)!}x^{n+1}$

DIMOSTRAZIONE: Cauchy (o anche Rolle).

# Teorema di Cesàro - Stolz
Siano $a_{n}$ e $b_{n}$ due successioni tali che:
1. $a_{n} \to 0$ e $b_{n} \to 0$
2. $b_{n}$ strettamente decrescente
Allora $\liminf\limits_{n \to +\infty} \frac{{a_{n+1}-a_{n}}}{b_{n+1}-b_{n}} \leq \liminf\limits_{n \to +\infty} \frac{a_n}{b_{n}} \leq \limsup\limits_{n \to +\infty} \frac{a_n}{b_{n}} \leq \limsup\limits_{n \to +\infty} \frac{{a_{n+1}-a_{n}}}{b_{n+1}-b_{n}}$

DIMOSTRAZIONE:
1. Assumiamo $\limsup\limits_{n \to +\infty} \frac{{a_{n+1}-a_{n}}}{b_{n+1}-b_{n}} = L \in \mathbb{R}$
2. Per caratterizzazione $\forall\varepsilon>0$   $\frac{{a_{n+1}-a_{n}}}{b_{n+1}-b_{n}} \leq L+\varepsilon$ definitivamente
3. $a_{n}-a_{n+1} \leq (L+\varepsilon)(b_{n}-b_{n+1})$
4. $a_{n}-a_{m} = \sum\limits_{k=n}^{m-1} (a_{k}-a_{k+1}) \leq (L+\varepsilon)\sum\limits_{k=n}^{m-1} (b_{k}-b_{k+1}) = (L+\varepsilon)(b_{n}-b_{m})$
5. $\frac{{a_{n} - a_{m}}}{b_{n} - b_{m}} \leq L + \varepsilon$
6. Per $m \to +\infty$ si ha $\frac{a_{n}}{b_{n}} \leq L+\varepsilon \implies \limsup\limits_{n \to +\infty} \frac{a_n}{b_{n}} \leq L+\varepsilon$

Vale anche per limiti nella forma $\frac{*}{\infty}$

DIMOSTRAZIONE:
1. Come prima $\frac{{a_{n+1}-a_{n}}}{b_{n+1}-b_{n}}\leq L + \varepsilon$ definitivamente
2. $\frac{a_{n}}{b_{n}} = \frac{{a_{n}-a_{n_{0}}+a_{n_{0}}}}{b_{n}}$
3. $a_{n}-a_{n_{0}} = \sum\limits_{k=n_{0}}^{n-1} (a_{k+1}-a_{k}) \leq (L+\varepsilon)\sum\limits_{k=n_{0}}^{n-1} (b_{k+1}-b_{k}) = (L+\varepsilon)(b_{n}-b_{n_{0}})$
4. $\frac{a_{n}}{b_{n}} = \frac{{a_{n}-a_{n_{0}}+a_{n_{0}}}}{b_{n}} \leq \frac{{(L+\varepsilon)(b_{n}-b_{n_{0}})+a_{n_{0}}}}{b_{n}} = L+\varepsilon + \frac{{a_{n_{0}}-(L+\varepsilon)b_{n_{0}}}}{b_{n}} \to L+\varepsilon$
5. Si fa il limsup a entrambi i membri