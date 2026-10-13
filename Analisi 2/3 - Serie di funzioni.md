# Serie di funzioni
Sia $f_{k} : A \to \mathbb{R}$, allora si definisce la somma parziale $S_{n}(x) = \sum\limits_{k=0}^{n} f_{k}(x)$   $\forall x \in A$.

Si definisce la serie $\sum\limits_{k=0}^{\infty} f_{k}(x) = \lim\limits_{n \to +\infty} S_{n}(x)$ e si indica con $\sum f_{k}$.

# Convergenza uniforme
Si dice che $\sum f_{k} {}^{\longrightarrow}_{\longrightarrow} S$ se $S_{n} {}^{\longrightarrow}_{\longrightarrow} S$, cioè se $||S-S_{n}||_{\infty} = \left\lvert  \left\lvert  \sum\limits_{k=n+1}^{\infty} f_{k}  \right\rvert  \right\rvert \to 0$.

Sia $f_{k} : [a,b] \to \mathbb{R}$ continua in $[a,b] \in \mathbb{R}$. Se $\sum f_{k}$ converge, vale $\int_{a}^{b} \sum f_{k} \, dt = \sum \int_{a}^{b} f_{k} \, dt$.

DIMOSTRAZIONE:
1. $S_{n} {}^{\longrightarrow}_{\longrightarrow} S$ e per il teorema di scambio $\lim\limits_{n \to +\infty} \int_{a}^{b} S_{n}(t) \, dt = \int_{a}^{b} S(t) \, dt$
2. $\lim\limits_{n \to +\infty} \int_{a}^{b} S_{n}(t) \, dt = \lim\limits_{n \to +\infty} \int_{a}^{b} \left( \sum\limits_{k=0}^{n} f_{k}(t) \right) \, dt = \lim\limits_{n \to +\infty} \sum\limits_{k=0}^{n} \left( \int_{a}^{b} f_{k}(t) \, dt \right) = \sum\limits_{k=0}^{\infty} \int_{a}^{b} f_{k}(t) \, dt$
3. A destra $\int_{a}^{b} S(t) \, dt = \int_{a}^{b} \sum\limits_{k=0}^{\infty} f_{k}(t) \, dt$

# Serie delle derivate
Sia $f_{k} :I \to \mathbb{R}$ continua in $I$. Se valgono:
1. $f_{k} \in C^1$
2. $\sum f_k'$ converge uniformemente   $\forall[a,b] \in I$
3. $\exists x_{0} \in I$   $\sum f_{k}(x_{0})$ converge
Allora $\left( \sum f_{k}(x) \right)' = \sum f_{k}'(x)$   $\forall x \in I$.

DIMOSTRAZIONE:
1. $\exists T : I \to \mathbb{R}$   $\forall[a,b] \in I$   $S_{n}' {}^{\longrightarrow}_{\longrightarrow} T$
2. $S_{n}(x_{0})$ converge
3. Per il teorema di scambio $\exists S \in C^1$   $\forall x \in I$   $S_{n}(x) \to S(x) \land S'(x) = T(x)$
4. A sinistra $S'(x)=[\lim\limits_{n \to +\infty} S_{n}]' = \left[ \sum f_{k} \right]'$
5. A destra $T(x) = \lim\limits_{n \to +\infty} S_{n}'(x) = \lim\limits_{n \to +\infty} \left[ \sum\limits_{k=0}^{n} f_{k}(x) \right]' = \lim\limits_{n \to +\infty} f_{k}'(x) = \sum\limits_{n=0}^{\infty} f_{k}'(x)$

# Convergenza totale
Sia $f_{k} : A \to \mathbb{R}$ con $A \subseteq \mathbb{R}$. Si dice che $\sum f_{k}$ converge totalmente se $\sum ||f_{k}||_{\infty}$ converge,

Se $\sum f_{k}$ converge totalmente, allora converge uniformemente.

DIMOSTRAZIONE:
1. Fissato $x$, vale $\sum\limits_{k=0}^{\infty} |f_{k}(x)| \leq \sum\limits_{k=0}^{\infty} ||f_{n}||_{\infty} < +\infty$ e la serie converge
2. $S_{n} \to S$ e per $n \to +\infty$ vale $|S(x)-S_{n}(x)| \leq \sum\limits_{k=n+1}^{\infty} |f_{k}(x)| \leq \sum\limits_{k=n+1}^{\infty} ||f_{k}||_{\infty} \to 0$
3. $S_{n} {}^{\longrightarrow}_{\longrightarrow} S$

Sia $\sum a_{n}z^n$ con raggio di convergenza $R \in [0,+\infty]$, allora converge totalmente $\forall D_{r}$ con $r<R$.

DIMOSTRAZIONE: $\sum\limits_{k=0}^{\infty} ||a_{k}z_{k}||_{\infty} = \sum\limits_{k=0}^{\infty} |a_{k}|r^k < +\infty$ per convergenza assoluta.

$f(x)=\sum\limits_{k=0}^{\infty} a_{k}x^k$ e $g(x) = \sum\limits_{k=1}^{\infty} ka_{k}x^{k-1}$ hanno stesso raggio di convergenza e $f'(x)=g(x)$.

DIMOSTRAZIONE: Criterio della radice e convergenza uniforme.