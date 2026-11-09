# Metodo di Newton
Siano $I = (\alpha,\alpha+\rho]$ e $f \in C^2(I)$ con $f(\alpha)=0$ tale che $f'(x)f''(x)>0$   $\forall x \in I$. Allora $\forall x_{0} \in I$ la successione $x_{n+1}=x_{n}-\frac{f(x_{n})}{f'(x_{n})}$ è tale che $\alpha < x_{n+1}<x_{n}$ e converge ad $\alpha$.

DIMOSTRAZIONE:
1. Wlog $f'(x)>0$, allora $f''(x)>0$ e $f(x)>0$ per ipotesi su $f(\alpha)$
2. $x_{n}$ strettamente decrescente per verifica
3. Sia $g(x)=x-\frac{f(x)}{f'(x)}$, allora $x_{n+1}-\alpha = g(x)-g(\alpha)=g'(\xi_{n})(x_{n}-\alpha)$ con $\alpha < \xi_{n} < x_{n}$
4. $g'(x)= \frac{f(x)f''(x)}{f'(x)^2}$, da cui $x \in I \implies g'(x)>0 \implies x_{n}>\alpha$

Il metodo si può estendere a $\mathbb{R}^n$ con $x_{n+1} = x_{n}-J(x_{n})^{-1}f(x_{n})$.

# Interpolazione polinomiale
Siano $f : [a,b] \to \mathbb{R} \in C([a,b])$ e nodi $a \leq x_{0} < x_{1} <\dots<x_{n} \leq b$ con $f(x_{i})$ noti. Allora $\exists c_{i},\varphi_{i}(x)$ tali che $g(x)=\sum\limits_{i=0}^{n} c_{i}\varphi_{i}(x)$ verifica $g(x_{i})=f(x_{i})$.

DIMOSTRAZIONE: $g$ è soluzione di $Vc = y$ con $V=(\varphi_{j}(x_{i}))$, $c = (c_{i})$ e $y = (f(x_{i}))$.

Siano $\varphi_{i}$ base di $\mathbb{K}_{\leq n}[x]$, allora l'interpolazione si dice polinomiale.

Si può interpolare con Vandermonde:
- $V = (x_{i}^j)$  e $\det V = \prod\limits_{i < j}(x_{i}-x_{j})$.
- $x_{i} \neq x_{j}$ con $i \neq j \implies \det V \neq 0 \implies\exists!p$ polinomio che interpola $f$

Si può interpolare con Lagrange:
- $L_{i}(x) = \frac{\prod\limits_{j = 0 \neq i} (x-x_{j})}{\prod\limits_{j=0 \neq i}(x_{i}-x_{j})}$.
- vale $L_{i}(x_{k})=\delta_{ik}$ e il polinomio è $p(x)=\sum\limits_{i=0}^{n} f(x_{i})L_{i}(x)$

# Teorema del resto di interpolazione
Siano $f \in C^{n+1}([a,b])$, $x_{i} \in [a,b]$, $p(x) \in \mathbb{K}_{\leq n}[x]$ che interpola $f$ e $r(x) = f(x)-p(x)$. Allora:
- $\forall x \in [a,b]$   $\exists \xi_{x} \in (a,b)$   $r(x)=\frac{f^{(n+1)}(\xi_{x})}{(n+1)!}\prod\limits_{i=0}^n(x-x_{i})$

DIMOSTRAZIONE:
1. Siano $y \in [a,b]$ con $y \neq x_{i}$ e $g(y)=r(y)-\prod\limits_{i=0}^{n} (y-x_{i}) \frac{r(x)}{\prod\limits_{i=0}^{n} (x-x_{i})}$
2. $g(x)=0$ e $g(x_{i})=0$, da cui $g$ ha almeno $n+2$ zeri in $[a,b]$
3. $g \in C^{n+1}$, dunque $g^{(n+1)}(x)$ ha uno zero in $(a,b)$
4. Sa $\xi_{x}$ tale che $g^{(n+1)}(\xi_{x}) = 0$, allora $g^{(n+1)}(x)=f^{(n+1)}(x)-p^{(n+1)}(x)-(n+1)! \frac{r(x)}{\prod\limits_{i=0}^{n} (x-x_{i})}$
5. $r(\xi_{x})=$ tesi