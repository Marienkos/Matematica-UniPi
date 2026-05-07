# Simboli di Landau
Sia $D \subseteq \mathbb{R}$ e $x_{0}$ un punto in cui è possibile fare il limite.
Siano le funzioni $f, g, \omega : D \to \mathbb{R}$ con $f(x) = g(x)\omega(x)$. Si dice:
- $f(x) = o(g(x))$ se $\lim\limits_{x \to x_{0}} \omega(x)=0$
- $f(x) \sim g(x)$ se $\lim\limits_{x \to x_{0}} \omega(x)=1$
- $f(x) = O(g(x))$ se $\omega(x)$ è limitata in un intorno di $x_{0}$

Sottintendendo $f(x)$, valgono:
- $o(g) \pm o(g) = o(g)$
- $\lambda o(g) = o(g)$
- $o(g)o(g) = o(g^{2})$
- $o(o(g)) = o(g)$

Inoltre per $x \to 0$ vale $f(x) = o(x^a) \implies f(x^b) = o(x^{ab})$

La definizione si può inoltre estendere alle successioni per $n \to +\infty$

Se per $x \to 0$ vale $f(x) = ax^b + o(x^b)$, allora $ax^b$ è la parte principale e $b$ l'ordine di infinitesimo.

Valgono:
- $f(x) = o(g(x)) \implies f(x) = O(g(x))$
- $f(x) \sim g(x) \implies f(x) = O(g(x))$

# Derivata
Sia $f : D \to \mathbb{R}$ con $D \subseteq \mathbb{R}$ e $x_{0}$ interno a $D$, ossia tale che $\exists r>0$   $(x_{0}-r,x_{0}+r) \subseteq D$

Si definisce rapporto incrementale $\frac{{f(x_{0}+h) -f(x_{0})}}{h}$ con $h \in (-r,r) \setminus \{ 0 \}$

$f$ si dice derivabile in $x_{0}$ se esiste $\lim\limits_{h \to 0} \frac{{f(x_{0}+h) - f(x_{0})}}{h} \in \mathbb{R}$, detto derivata di $f$ in $x_{0}$ o $f'(x_{0})$

$f$ si dice differenziabile in $x_{0}$ se esiste $\alpha\in \mathbb{R}$ tale che $f(x_{0}+h) = f(x_{0}) + \alpha h + o(h)$ per $h\to {0}$

Valgono in $\mathbb{R}$:
- $f$ derivabile in $x_{0}$ $\iff$ $f$ differenziabile in $x_{0}$
- $\alpha = f'(x_{0})$

DIMOSTRAZIONE:
- $(\implies)$ Si usa la definizione di differenziabilità
- $(\impliedby)$ Si usa la definizione di derivabilità

Valgono, sottintendendo gli argomenti:
- $(f \pm g)' = f' \pm g'$
- $(\lambda f)' = \lambda f'$
- $(fg)' = f'g + fg'$
- $\left( \frac{1}{f} \right)' = -\frac{f'}{f^{2}}$
- $\left( \frac{f}{g} \right)' = \frac{{f'g - g'f}}{g^{2}}$
- $[g(f)]' = g'(f)f$

DIMOSTRAZIONE: Definizione di derivabilità/differenziabilità.

Sia $g$ l'inversa di $f$. Sotto certe ipotesi vale $g'(x) = \frac{1}{f'(g(x))}$

# De L'Hôpital
Sia $x_{0} \in \overline{\mathbb{R}}$ e siano $f$ e $g$ due funzioni tali che:
- $\lim\limits_{x \to x_{0}} f(x)=\lim\limits_{x \to x_{0}} g(x) \in \{ 0,+\infty \}$
- $\exists \lim\limits_{x \to x_{0}} \frac{f'(x)}{g'(x)}=l\in \overline{\mathbb{R}}$
Allora $\lim\limits_{x \to x_{0}} \frac{f(x)}{g(x)} = l$

# Taylor - Peano
Sia $f$ una funzione definita in un intorno di 0 e $n$ intero positivo. Se esiste un polinomio di grado $\leq n$ tale che $f(x) = P_{n}(x) + o(x^n)$ per $x\to {0}$, allora è unico.

DIMOSTRAZIONE: Se ce ne fossero due distinti, la differenza avrebbe tutti i termini nulli passando al limite, costituendo un assurdo.

Sia $\delta > 0$ e $f : (-\delta,\delta) \to \mathbb{R}$ una funzione. Sia $n \in \mathbb{N}$. Supponiamo:
1. $f$ derivabile almeno $n-1$ volte in $(-\delta,\delta)$
2. $f$ derivabile $n$ volte in 0
Allora $P_{n}$ esiste e $P_{n}(x) = \sum\limits_{k=0}^{n} \frac{f^{(k)}(0)}{k!}x^k$

Valgono:
- $f$ pari $\implies$ sviluppo di $f$ pari
- $f$ dispari $\implies$ sviluppo di $f$ dispari

Sia $x_{0} \in \mathbb{R}$, $\delta > 0$ e $f : (-\delta,\delta) \to \mathbb{R}$ una funzione. Sia $n \in \mathbb{N}$. Supponiamo:
1. $f$ derivabile almeno $n-1$ volte in $(x_{0}-\delta,x_{0}+\delta)$
2. $f$ derivabile $n$ volte in $x_{0}$
Allora $P_{n}$ esiste e $P_{n}(h) = \sum\limits_{k=0}^{n} \frac{f^{(k)}(x_{0})}{k!}h^k$ e vale $f(x) = \sum\limits_{k=0}^{n} \frac{f^{(k)}(x_{0})}{k!}(x-x_{0})^k + o((x-x_{0})^n)$

Siano $f(x) = P_{n}(x) + o(x^n)$ e $g(x) = Q_{n}(x) + o(x^n)$. Allora valgono:
- $f(x) \pm g(x) = P_{n}(x) \pm Q_{n}(x) + o(x^n)$
- $\lambda f(x)=\lambda P_{n}(x)+o(x^n)$
- $f(x)g(x)=P_{n}(x)Q_{n}(x)+o(x^n)$
- $f(ax^b) = P_{n}(ax^b)+o(x^{bn})$ con $b>0$
- $g(f(x)) = Q_{n}(P_{n}(x)) + o(x^n)$

# Taylor - Lagrange
Sia $\delta>0$ e $f : (-\delta,\delta) \to \mathbb{R}$ una funzione. Sia $n \in \mathbb{N}$. Supponiamo:
- $f$ derivabile almeno $n+1$ volte in $(-\delta,\delta)$
Allora $\forall x \in (-\delta,\delta)$   $\exists c \in [0,x]$   $f(x) = \sum\limits_{k=0}^{n} \frac{f^{(k)}(0)}{k!}x^k + \frac{f^{(n+1)}(c)}{(n+1)!}x^{n+1}$

# Classi di regolarità
Sia $D \subseteq \mathbb{R}$ un insieme convesso aperto e $k \in \mathbb{N}$. Sia $f$ una funzione tale che:
- $f$ derivabile almeno $k$ volte in $D$
- le prime $k$ derivate di $f$ sono continue
Allora si dice che $f \in C^k(D)$

Si dice che $f \in C^\infty(D)$ se $f \in C^k(D)$ per ogni $k$.

Si dice che $f \in C^\omega(D)$, ossia è analitica, se $f \in C^\infty(D)$ e $f$ coincide con la sua serie di Taylor in $D$.