# Algebra su campo
Si chiama algebra su $\mathbb{K}$ uno spazio vettoriale $A$ su $\mathbb{K}$ tale che $\exists(\cdot) : A \times A \to A$ bilineare.

# Lemma 1
Siano $X$ metrico compatto, $x_{0} \in X$, $U \in I(x_{0})$ aperto e $A \subseteq C(X)$ tale che:
1. $1 \in A$
2. $A$ separa i punti di $X$, ossia $\forall x \neq y \in X$   $\exists f \in A$   $f(x) \neq f(y)$
Allora $\exists V \in I(x_{0})$   $V \subseteq U$   $\forall\varepsilon > 0$   $\exists f \in A$ tale che:
3. $0 \leq f \leq 1$
4. $f(x) < \varepsilon$   $\forall x \in V$
5. $f(x)>1 - \varepsilon$   $\forall x \in X \setminus U$

DIMOSTRAZIONE:
1. $\forall x \in X \setminus U$   $\exists g_{x} \in A$   $g_{x}(x) \neq g_{x}(x_{0})$
2. Sia $h_{x} = g_{x} - g_{x}(x_{0}) \cdot 1 \in A$, allora $h_{x}(x) \neq h_{x}(x_{0}) = 0$
3. Sia $p_{x} = \frac{h_{x}^2}{||h_{x}||_{\infty}} \in A$, allora $p_{x}(x_{0}) = 0$ e $0 \leq p_{x} \leq 1$
4. $U_{x} = \{ g \in X : p_{x}(y) > 0 \} \in I(x)$ aperto, dunque $X \setminus U$ compatto ricoperto da $U_{x}$
5. Per compattezza $\exists x_{1},\dots,x_{n} \in X \setminus U$   $X \setminus U \subseteq \bigcup\limits_{i=1}^m U_{x_{i}}$
6. Sia $p = \frac{{\sum\limits_{i = 1}^{m} p_{x_{i}}}}{m} \in A$, allora $p(x_{0})= 0$ e $0 \leq p \leq 1$
7. Per compattezza $\exists\delta = \min p(X \setminus U) > 0$, da cui $p(x)\geq \delta > 0$ e $0 < \delta \leq 1$
8. Sia $V = \left\{  x \in X : p(x) < \frac{\delta}{2}  \right\} \in I(x_{0})$, per $p(x) \geq \delta$ si ha $V \subseteq U$
9. Sia $k \in \mathbb{N}$ tale che $\frac{1}{\delta} < k \leq \frac{1}{\delta} + 1 = \frac{{\delta + 1}}{\delta} < \frac{2}{\delta}$, allora $1 < k\delta < 2$
10. Sia $q_{n}(x) = [1-p^n(x)]^{k^n} \in A$, allora $q_{n}(x_{0}) > 0$ e $0 \leq q_{n} \leq 1$
11. Per Bernoulli $kp(x) \leq k \frac{\delta}{2} < 1$, da cui $q_{n}(x)\geq 1 - k^np^n(x) \geq 1 - \left( k \frac{\delta}{2} \right)^n \to 1$
12. Se $x \in X \setminus U$ si ha $kp \geq k\delta > 1$, da cui $q_{n}(x) \leq \frac{1}{(k\delta)^n} \to 0$
13. Per $n$ grande si ha $q_{n} < \varepsilon$ su $X \setminus U$ e $q_{n}>1-\varepsilon$ su $V$, da cui $f=1-q_{n}$ soddisfa la tesi

# Lemma 2
Siano $X$ metrico compatto, $B_{1},B_{2} \subseteq X$ compatti disgiunti e $A \subseteq C(X)$ tale che:
1. $1 \in A$
2. $A$ separa i punti di $X$
Allora $\forall \varepsilon > 0$   $\exists f \in A$ tale che:
3. $0 \leq f \leq 1$
4. $f(x) < \varepsilon$   $\forall x \in B_{1}$
5. $f(x) > 1 - \varepsilon$   $\forall x \in B_{2}$

DIMOSTRAZIONE:
1. Sia $U \subseteq B_{1}$ aperto disgiunto da $B_{2}$, allora $\forall x \in B_{1}$   $\exists V_{x} \subseteq U$ intorno aperto di $x$
2. $V_{x}$ ricopre $B_{1}$ compatto, da cui $\exists x_{1},\dots,x_{m} \in B_{1}$   $B_{1} \subseteq \bigcup\limits_{i=1}^m V_{x_{i}}$
3. $\exists g_{1},\dots,g_{m} \in A$   $0 \leq g_{k} \leq 1 \land g_{i} < \frac{\varepsilon}{m}$ su $V_{x}$ e $g_{i} > 1 - \frac{\varepsilon}{m}$ su $X \setminus U$
4. Sia $g = \prod\limits_{i=1}^{m} g_{m}$, allora $0 \leq g \leq 1$ e $\forall x \in B_{1}$   $\exists x_{i}$   $x \in V_{x_{i}}$
5. $g_{i}(x) < \frac{\varepsilon}{m}$, da cui $g(x) < \frac{\varepsilon}{m}$ e $\forall x \in B_{2}$   $x \not\in\bigcup V_{x}$   e   $\forall i$   $g_{i}(x) < 1 - \frac{\varepsilon}{m}$
6. $g > \left( 1 - \frac{\varepsilon}{m} \right)^m \geq 1 - m \frac{\varepsilon}{m} = 1-\varepsilon$

# Teorema di Stone - Weierstrass
Siano $X$ metrico compatto e $A \subseteq C(X)$ tale che:
1. $1 \in A$
2. $A$ separa i punti di $X$
Allora $A$ è densa in $C(X)$ rispetto a $||\cdot||_{\infty}$, ossia $\forall\varepsilon > 0$   $\forall f \in C(X)$   $\exists g \in A$   $||f-g||_{\infty} < \varepsilon$.

DIMOSTRAZIONE:
1. Siano $f \in C(X)$, $0 < \varepsilon < \frac{1}{3}$ e $n$ tale che $(n-1)\varepsilon \geq ||f||_{\infty}$ con $f \geq 0$
2. Per $j$ da $0$ a $n$ si definiscono $A_{j} = \left\{  x \in X : f(x) \leq \left( j - \frac{1}{3} \right)\varepsilon  \right\}$ e $B_{j}$ con $\geq$
3. $A_{j} \cap B_{j} = \emptyset$ e $A_{j},B_{J}$ sono chiusi, con $\emptyset \subseteq A_{0} \subseteq \dots \subseteq A_{n} = X$ e $\emptyset = B_{n} \subseteq \dots \subseteq B_{0}$
4. Per lemma precedente $\exists g_{j} \in A$   $g_{j} \leq \frac{\varepsilon}{n}$ su $A_{j}$   $g_{j} \geq 1 - \frac{\varepsilon}{n}$ su $B_{j}$
5. Sia $g(x) = \varepsilon \sum\limits_{i=0}^{n} g_{i}(x)$, allora $\forall x \in X$   $\exists j$   $x \in A_{j} \setminus A_{j-1} \implies \left( j-\frac{4}{3} \right)\varepsilon < f(x) \leq (j-\frac{4}{3})\varepsilon$
6. $\forall i \leq j - 2$   $x \in B_{j} \implies g_{i}(x) < 1 - \frac{\varepsilon}{n}$
7. Con $g$ fino a $j-1$, si ha $g(x) \leq \varepsilon \sum\limits_{i=j}^{n} g_{i}(x) \leq j\varepsilon + \varepsilon(n-j+1) \frac{\varepsilon}{n} \leq j\varepsilon + \varepsilon^2 < \left( j+\frac{1}{3} \right)\varepsilon$
8. Similmente $g(x) > (j-\frac{4}{3})\varepsilon$ e dunque $|f(x)-g(x)| \leq \left( j+\frac{1}{3} \right)\varepsilon - \left( j-\frac{4}{3} \right)\varepsilon < 2\varepsilon$

# Norma euclidea di una funzione
Sia $f : (a,b) \to \mathbb{R}$ localmente Riemann-integrabile, si può definire $||f||_{2} = \sqrt{ \int_{a}^{b} |f(x)|^2 \, dx }$.

Si definisce $\mathcal{K}(a,b) = \{ f \text{ localmente Riemann-integrabile su }(a,b) : ||f||_{2} < +\infty \}$.

$\mathcal{K}(a,b)$ è uno spazio vettoriale.

DIMOSTRAZIONE: Verifiche sulla norma euclidea $||\cdot||_{2}$.

Sia $f \sim g \iff ||f-g||_{2} = 0$, allora $H(a,b) = \mathcal{K}(a,b) / \sim$ è uno spazio vettoriale euclideo.

DIMOSTRAZIONE: Verifiche sul prodotto scalare in $\mathcal{K}$ e $H$.

# Base Hilbertiana
Sia $V$ spazio euclideo, $e_{k} \in V$ si dice sistema ortonormale se $\langle e_{k},e_{j} \rangle = 0$ con $k \neq j$ e $\langle e_{k},e_{k} \rangle=1$.

$e_{k}$ SO in $V$ si dice base Hilbertiana se $\forall v \in V$   $\exists c_{k} \in \mathbb{R}$   $v = \sum\limits_{k=0}^{\infty} c_{k}e_{k}$.

# Disuguaglianza di Bessel
Siano $e_{k}$ SO in $V$ e $\forall v \in V$   $c_{k} = \langle v,e_{k} \rangle$, allora valgono:
1. $\sum\limits_{k=0}^{\infty} c_{k}^{2} \leq |v|^2$
2. $\sum\limits_{k=0}^{\infty} c_{k}^{2} = |v|^{2} \iff e_{k}$ base Hilbertiana.

DIMOSTRAZIONE:
1. Dato $v \in V$, siano $c_{k} = \langle v,e_{k} \rangle$, $v_{N} = \sum\limits_{k=0}^{N} c_{k}e_{k}$ e $w_{N} = v-v_{N}$, da cui $\forall n \in \mathbb{N}$   $\langle v_{N},w_{N} \rangle = 0$
2. Per Pitagora $|v|^{2} = |v_{N}+w_{N}|^{2} = |v_{N}|^{2} + |w_{N}|^{2} \geq |v_{N}|^2 = \left\lvert  \sum\limits_{k=0}^{N} c_{k}e_{k}  \right\rvert ^{2} = \sum\limits_{k=0}^{N} c_{k}^{2}$
3. Per $N \to +\infty$ si ha la tesi (1.)
4. (2.) $\iff|w_{N}|^{2} \to 0$, da cui $e_{k}$ Hilbertiana $\iff w_{N} \to 0$

# Serie di Fourier
Sia $e_{k}$ data da $e_{0}(x) = \frac{1}{\sqrt{ 2\pi }}$, $e_{2k+1}(x) = \frac{\sin(kx)}{\sqrt{ \pi }}$ e $e_{2k}(x) = \frac{\cos(kx)}{\sqrt{ \pi }}$, formano un SO di $H(0,2\pi)$.

$f$ si dice polinomio trigonometrico se $\exists P(x,y)$ polinomio   $f(x) = P(\cos x,\sin x)$.

$f$ PT $\iff \sum\limits_{k=0}^{n} c_{k}e_{k}$.

Sia $f \in \mathcal{K}(0,2\pi)$, con $c_{k}$ e $e_{k}$ definiti come prima, allora:
- $c_{k}$ è detto coefficiente di Fourier
- $\sum\limits_{k=0}^{\infty} c_{k}e_{k}$ è detta serie di Fourier
- $f_{N} = \sum\limits_{k=0}^{n} c_{k}e_{k}$ è detto sviluppo di Fourier

$\forall f \in C^0([0,2\pi])$ con $f(0) = f(2\pi)$   $\exists g_{k} \in \mathcal{K}(0,2\pi)$ di PT   $g_{k} {}^{\longrightarrow}_{\longrightarrow} f$.

DIMOSTRAZIONE: Stone - Weierstrass ai polinomi trigonometrici.

Valgono i seguenti enunciati equivalenti:
- $\forall f \in H(a,b)$   $\forall \varepsilon > 0$   $\exists g \in C^0([a,b])$ con $g(a)=g(b)=0$   $||f-g||_{2} < \varepsilon$
- $C_{0}^0([a,b])$ sottospazio denso in $H(a,b)$

DIMOSTRAZIONE:
1. Sia $f$ limitata su $(a,b)$, si può pensare come definita su $[a,b]$ con integrale proprio
	1. Sia $M = \sup |f|([a,b])$, per integrabilità si ha $g$ interpolazione lineare di $f$
	2. $\int_{a}^{b} |f(x)-g(x)| \, dx < \frac{\varepsilon}{M}$, ma $||f||_{\infty} \leq M \implies ||g||_{\infty} \leq M \implies ||f-g||_{2} \leq 2M$
	3. $||f-g||_{2}^{2} = \int_{a}^{b} |f(x)-g(x)|^2 \, dx \leq \int_{a}^{b} ||f-g||_{\infty} \cdot |f(x)-g(x)| \, dx \leq 2M \frac{\varepsilon}{2M} = \varepsilon$
2. Sia $|f|$ integrabile in senso improprio ma non limitata
	1. $\forall \varepsilon > 0$   $\exists[\alpha,\beta] \subseteq (a,b)$   $f^{2}$ limitata $\land \int f^{2}  \, dx$ su $(a,\alpha]$ e $[\beta,b)$ minore di $\varepsilon$
	2. Sia $M = \sup |f|([\alpha,\beta])$, allora $\exists g \in C^0([\alpha,\beta])$   $|g(x)| \leq M \land \int |f-g|^2  \, dx \leq \varepsilon$
	3. Siano $\alpha' \in (a,\alpha)$ e $\beta' \in (\beta,b)$, si estende $g$ interpolando
	4. Per Cauchy - Schwarz $\int_{a}^{b} |f-g|^2 \, dx \leq 11\varepsilon$

$e_{k}$ base Hilbertiana e ogni $f \in \mathcal{K}(a,b)$ si approssima rispetto a $||\cdot||_{2}$ con gli sviluppi di Fourier.