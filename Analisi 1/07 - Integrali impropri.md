# Integrale improprio
Un integrale si dice improprio se c'è un problema, ossia manca almeno una tra:
- limitatezza della zona d'integrazione
- limitatezza della funzione

Sia $f$ integrabile in $[a+\varepsilon,b]$   $\forall \varepsilon>0$. Allora per definizione $\int_{a}^{b} f(x) \, dx = \lim\limits_{\varepsilon \to 0^+} \int_{a+\varepsilon}^{b} f(x) \, dx$

Sia $f$ integrabile in $[a,A]$   $\forall A>a$. Allora per definizione $\int_{a}^{+\infty} f(x) \, dx = \lim\limits_{A \to +\infty} \int_{a}^{A} f(x) \, dx$

Ogni integrale con più problemi si può spezzare in integrali monoproblema utilizzando il limite della somma. Se durante lo spezzamento, si sommano due limiti di cui uno tende a $+\infty$ e uno a $-\infty$, allora per definizione l'integrale è indeterminato.

# Criterio del confronto
Siano $f$ e $g$ due funzioni tali che $0\leq f(x) \leq g(x)$   $\forall x \in E$. Allora:
- $\int_{E} f(x) \, dx = +\infty \implies \int_{E} g(x) \, dx = +\infty$
- $\int_{E} g(x) \, dx$ converge $\implies \int_{D} f(x) \, dx$ converge

# Criterio del confronto asintotico
Siano $f$ e $g$ due funzioni e $x_{0}$ il punto del problema. Se:
1. $f(x)\geq 0$
2. $g(x) >0$
3. $\lim\limits_{x \to x_{0}} \frac{f(x)}{g(x)} = l$ con $l\neq 0$ e $l \neq +\infty$
Allora i due integrali hanno lo stesso comportamento.

~={green}DIMOSTRAZIONE=~:
1. Per $x \to x_{0}$ vale $0 < \frac{l}{2} \leq \frac{f(x)}{g(x)} \leq 2l$, ossia $\frac{1}{2}lg(x) \leq f(x) \leq 2lg(x)$
2. Se $\int g(x) \, dx$ converge, anche $\int f(x) \, dx$ converge per confronto a destra
3. Se $\int g(x) \, dx$ diverge, anche $\int f(x) \, dx$ diverge per confronto a sinistra

# Assoluta integrabilità
$\int_{E} |f(x)| \, dx$ converge $\implies \int_{E} f(x) \, dx$ converge

# Metodo dei triangolini
Si approssima in triangoli per difetto l'area del sottografico. Se l'area è $+\infty$ allora l'integrale diverge a $+\infty$.

# Criterio di Dirichlet
Sia $\int_{0}^{+\infty} f(x)g(x) \, dx$ tale che:
1. la primitiva di $f$ è limitata
2. $g \in C^1$ debolmente decrescente
3. $g \to 0$ per $x \to +\infty$
Allora l'integrale converge.

~={cyan}DIMOSTRAZIONE=~:
1. Integrando per parti $\int_{a}^{A} f(x)g(x) \, dx = [F(x)g(x)]^A_{a} - \int_{a}^{A} F(x)g'(x) \, dx$
2. $[F(x)g(x)]^A_{a} = F(A)g(A)-F(a)g(a) \to 0$ per le ipotesi
3. $\int_{a}^{A} |F(x)||g'(x)| \, dx \leq M\int_{a}^{A} |g'(x)| \, dx = -M\int_{a}^{A} g'(x) \, dx = -M(g(A) - g(a)) \to Mg(a)$
4. $\int_{a}^{+\infty} F(x)g'(x) \, dx$ assolutamente integrabile

# Confronto serie - integrali
Siano $M \in \mathbb{N}$ e $f : [M, +\infty) \to \mathbb{R}$ debolmente decrescente.
Allora per $N>M$ vale $\sum\limits_{k=M+1}^{N} f(k) \leq \int_{M}^{N} f(x) \, dx \leq \sum\limits_{k=M}^{N-1} f(k)$

~={yellow}DIMOSTRAZIONE=~: Induzione su $N$.

Siano $f$ e $M$ come prima. Allora $\int_{M}^{+\infty} f(x) \, dx$ converge $\iff \sum\limits_{k=M}^{\infty} f(k)$

~={pink}DIMOSTRAZIONE=~: Teorema precedente.