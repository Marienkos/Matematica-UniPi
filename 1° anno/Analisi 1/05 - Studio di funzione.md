# Teorema di esistenza degli zeri
Sia $[a,b] \subseteq \mathbb{R}$ un intervallo, e sia $f : [a,b] \to \mathbb{R}$ tale che:
1. $f$ è continua in $[a,b]$
2. $f(a)f(b) < 0$
Allora $\exists c \in(a,b)$   $f(c) = 0$

~={red}DIMOSTRAZIONE=~:
1. wlog $f(a) < 0$ e $f(b)>0$
2. $c := \inf \{ x \in [a,b]:f(x)>0 \} \neq \emptyset$
3. $f(c) = 0$ per assurdo usando la continuità.

~={cyan}DIMOSTRAZIONE=~:
1. wlog $f(a) < 0$ e $f(b)>0$
2. $c := \inf \{ x \in [a,b]:f(x)>0 \} \neq \emptyset$
3. $\forall x \in [a,c)$   $f(x) \leq 0$   di conseguenza   $f(c) = \lim\limits_{x \to c^-} f(x)\leq 0$
4. Per caratterizzazione di inf $\exists x \in [c,c+\delta]$   $f(x)>0$
5. Per confronto a 3 con $x_{n}$ si ha $x_{n} \to c$
6. Per la continuità $f(c) = \lim\limits_{n \to +\infty} f(x_{n})\geq 0$

# Teorema dei valori intermedi
Sia $[a,b] \subseteq \mathbb{R}$ e $f : [a,b] \to \mathbb{R}$ continua e $\lambda \in \mathbb{R}$ tali che $f(a) <\lambda$ e $f(b) > \lambda$. Allora $\exists c \in (a,b)$   $f(c) = \lambda$

~={pink}DIMOSTRAZIONE=~: Teorema di esistenza degli zeri applicato a $g(x) = f(x) - \lambda$

Sia $A \subseteq \mathbb{R}$ non vuoto e connesso e $f : A \to \mathbb{R}$ continua. Allora $f$ assume in $A$ tutti i valori tra $\inf f$ e $\sup f$.

~={cyan}DIMOSTRAZIONE=~:
1. Sia $\inf \leq \lambda \leq \sup$
2. Per caratterizzazione $\exists a,b \in A$   $f(a) < \lambda < f(b)$
3. Teorema dei valori intermedi in $[a,b] \subseteq A$ per convessità

# Teorema di Lagrange
Sia $f : [a,b] \to \mathbb{R}$ tale che:
1. $f$ continua in $[a,b]$
2. $f$ derivabile in $(a,b)$
Allora $\exists c \in (a,b)$   $f(b)-f(a) = (b-a)f'(c)$

# Teoremi di monotonia
Sia $x_{0} \in \mathbb{R}$, $r>0$, $f : (x_{0}-r,x_{0}+r) \to \mathbb{R}$ tale che $f'(x)>0$. Allora $\exists\delta \in(0,r)$ tale che:
- $f(x) > f(x_{0})$   $\forall x \in (x_{0},x_{0}+\delta)$
- $f(x) < f(x_{0})$   $\forall x \in (x_{0}-\delta,x_{0})$

~={pink}DIMOSTRAZIONE=~: Definizione di derivata.

Sia $f : (a,b)\to \mathbb{R}$ derivabile in $(a,b)$. Valgono in tutto $(a,b)$:
1. $f'(x)\geq 0 \implies f$ debolmente crescente
2. $f'(x)>0 \implies f$ strettamente crescente
3. $f$ crescente $\implies f'(x) \geq 0$

~={pink}DIMOSTRAZIONE=~: Lagrange

Sia $f: (a,b)\to \mathbb{R}$ derivabile ovunque tale che:
1. $f'(x)\geq 0$   $\forall x \in (a,b)$
2. $f'(x)$ non è nulla in un intero intervallo (annullamento sporadico)
Allora $f$ è strettamente crescente in $(a,b)$

~={red}DIMOSTRAZIONE=~: $f$ crescente, se fosse strettamente esisterebbe un tratto in cui $f'(x)=0$

# Teorema di Weierstrass
Il massimo (max) di una funzione è il massimo valore assunto in un punto, detto punto di massimo. Al contrario si parla di minimo (min) e punto di minimo.

Sia $[a,b] \subseteq \mathbb{R}$ e $f : [a,b] \to \mathbb{R}$ continua. Allora max e min esistono.

~={red}DIMOSTRAZIONE=~:
1. $\exists I = \inf \{ f(x):x \in [a,b] \}$
2. $x_{0} = \inf \{ x \in [a,b] : \inf \{ f(t) : t \in [a,x] \} = I \}$
3. $f(x_{0})\geq I$ in quanto $I$ è l'inf
4. Supponiamo $f(x_{0}) > I$
	- $x_{0} = a \implies x_{0}$ non inf per continuità $\implies$ assurdo
	- $x_{0} > a \implies$ assurdo
5. $f(x_{0}) = I$

I punti di max e min fanno parte di una delle seguenti categorie:
- stazionari interni: $x \in (a,b)$   $f'(x)=0$
- singolari interni: $x \in (a,b)$   $f'(x)$ non esiste
- bordo: $a$ e $b$

# Varianti di Weierstrass
Sia $f : \mathbb{R} \to \mathbb{R}$ continua e periodica. Allora max e min esistono.

~={pink}DIMOSTRAZIONE=~: Weierstrass ristretto a un periodo.

Sia $f : \mathbb{R} \to \mathbb{R}$ continua e $\lim\limits_{x \to +\infty} f(x) = \lim\limits_{x \to -\infty} f(x) = +\infty$. Allora esiste min.

~={pink}DIMOSTRAZIONE=~: Weierstrass su un intervallo, maggiore a destra e sinistra.

Sia $f : (0,+\infty) \to \mathbb{R}$ continua e $\lim\limits_{x \to 0^+} f(x) = \lim\limits_{x \to +\infty} f(x) = +\infty$. Allora esiste min.

~={pink}DIMOSTRAZIONE=~: Come prima.

Sia $D \subseteq \mathbb{R}$ non vuoto e $f: D\to \mathbb{R}$ continua.
Se $\exists[a,b]\in D$   $\inf \{ f(x): x \in [a,b] \} = \inf \{ f(x): x \in D \}$ allora il min in $[a,b]$ lo è in $D$.

# Studio locale
$x_{0}$ è detto punto di min locale se $\exists \delta>0$ tale che:
- $f(x) > f(x_{0})$   $\forall x \in (x_{0},x_{0}+\delta)$
- $f(x) > f(x_{0})$   $\forall x \in (x_{0}-\delta,x_{0})$

$x_{0}$ è detto punto di flesso a tangente orizzontale discendente se $\exists \delta>0$ tale che:
- $f(x) < f(x_{0})$   $\forall x \in (x_{0},x_{0}+\delta)$
- $f(x) > f(x_{0})$   $\forall x \in (x_{0}-\delta,x_{0})$

Sia $f'(x_{0}) = f''(x_{0}) =\dots=f^{(k-1)}(x_{0}) = 0 \neq f^{(k)}(x_{0})$. Vale:
- $k$ pari e $f^{(k)}(x_{0}) > 0 \implies x_{0}$ min locale
- $k$ pari e $f^{(k)}(x_{0}) < 0 \implies x_{0}$ max locale
- $k$ dispari e $f^{(k)}(x_{0}) > 0 \implies x_{0}$ flesso a tangente orizzontale ascendente
- $k$ dispari e $f^{(k)}(x_{0}) < 0 \implies x_{0}$ flesso a tangente orizzontale discendente

~={pink}DIMOSTRAZIONE=~: Taylor.

# Studio globale
L'ordine di uno studio è il seguente:
1. Simmetrie
2. Definizione e continuità
3. Limiti
4. Zeri e segno
5. Derivata prima e monotonia
6. Punti di max e min
7. Asintoti
8. Derivata seconda e convessità
9. Lipschitzianità

# Asintoti
Una retta $x = x_{0}$ è asintoto verticale se $\lim\limits_{x \to x_{0}} f(x) = \pm\infty$ e/o $\lim\limits_{x \to x_{0}^-} f(x) = \pm\infty$

Una retta $y = y_{0}$ è asintoto orizzontale se $\lim\limits_{x \to \pm\infty} f(x)=y_{0}$

Una retta $y=ax+b$ è asintoto obliquo se $f(x) = ax + b + o(1)$

# Convessità
Sia $D \subseteq \mathbb{R}$ un insieme convesso non banale e $f : D \to \mathbb{R}$.
Allora $f$ si dice convessa (secondo la definizione geometrica) in $D$ se per ogni coppia di punti A e B, il segmento AB sta sopra il grafico. Al contrario è detta concava.

Supponiamo inoltre che esista $f''$ in tutto $D$. Allora in $D$:
- $f$ debolmente convessa $\iff$ $f''(x)\geq0$
- $f$ strettamente convessa $\impliedby$ $f''(x)>0$
- $f''(x)\geq0$ con annullamento sporadico $\implies$ $f$ strettamente convessa

# Lipschitzianità
Una funzione $f : D \to \mathbb{R}$ con $D \subseteq \mathbb{R}$ si dice Lipschitziana in $D$ se $\exists L\in \mathbb{R}$   $|f(y)-f(x)|\leq L|y-x|$

La più piccola $L$ si chiama costante di Lipschitz ed è il $\sup \left\{  \frac{{|f(y)-f(x)|}}{|y-x|}:x \in D,y \in D, x \neq y  \right\}$

$f$ Lipschitziana $\implies$ $f$ continua

~={pink}DIMOSTRAZIONE=~: Definizione di continuità

Sia $D \subseteq \mathbb{R}$ un insieme convesso e $f$ derivabile in $D$. Allora:
- $f$ è Lipschitziana in $D$ $\iff$ $f'$ è limitata in $D$
- $L = \sup \{ |f'(x)| : x \in D \}$

~={pink}DIMOSTRAZIONE=~:
- ($\impliedby$) Lagrange
- ($\implies$) Definizione di derivata