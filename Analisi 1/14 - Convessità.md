# Funzione convessa
Siano $x,y \in \mathbb{R}$. Una combinazione convessa di $x$ e $y$ è $\lambda x+(1-\lambda)y$ con $\lambda \in [0,1]$.

Al variare di $\lambda$ le combinazioni convesse di $x$ e $y$ descrivono il segmento di estremi $x$ e $y$.

~={cyan}DIMOSTRAZIONE=~:
1. Supponiamo wlog $x < y$
2. $\lambda x + (1-\lambda)y \leq \lambda y + (1-\lambda)y = y$
3. $\lambda x + (1-\lambda)y \geq \lambda x + (1-\lambda)x = x$
4. $x \leq z \leq y \implies \exists \lambda \in[0,1]$   $z = \lambda x + (1-\lambda)y \implies \lambda = \frac{{y-z}}{y-x}$

Un sottoinsieme $C \subseteq \mathbb{R}$ si dice convesso se $\forall x,y \in C$   $\forall\lambda \in [0,1]$   $\lambda x+(1-\lambda)y \in C$.

Una funzione $f: C \to \mathbb{R}$ si dice convessa se, alternativamente:
- per ogni coppia di suoi punti, il segmento sta sopra
- $\forall x,y \in C$   $\forall\lambda \in [0,1]$   $f(\lambda x+(1-\lambda)y) \leq \lambda f(x) + (1-\lambda)f(y)$

Se vale il $<$ allora è strettamente convessa. Analogamente per concava se $-f$ è convessa.

# Lemma dei 3 rapporti incrementali
Sia $C \subseteq \mathbb{R}$ convesso e $f : C \to \mathbb{R}$. Allora $f$ convessa $\iff$ $\forall a<b<c \in C$   $r_{b}^{a} f \leq r_{c}^{a} f \leq r_{c}^{b} f$

~={pink}DIMOSTRAZIONE=~: Espansione e definizione di convessità.

# Lemma dei 2 rapporti incrementali
Sia $C \subseteq \mathbb{R}$ convesso e $f : C \to \mathbb{R}$. Allora $f$ convessa $\iff$ $\forall a<b<c \in C$   $r_{b}^{a} f \leq r_{c}^{b} f$

~={pink}DIMOSTRAZIONE=~: Espansione e definizione di convessità.

# Convessità e derivata prima
Sia $C \subseteq \mathbb{R}$ convesso aperto e $f : C \to \mathbb{R}$ derivabile. Valgono:
1. $f$ convessa $\iff$ $f'$ debolmente crescente
2. $f$ strettamente convessa $\iff$ $f'$ strettamente crescente

~={pink}DIMOSTRAZIONE=~: Lemmi dei 3 e 2 rapporti incrementali.

# Convessità e derivata seconda
Sia $C \subseteq \mathbb{R}$ convesso aperto e $f : C \to \mathbb{R}$ derivabile almeno due volte. Valgono:
1. $f$ convessa $\iff$ $f''\geq 0$ in $C$
2. $f$ strettamente convessa $\impliedby$ $f''>0$ in $C$

~={pink}DIMOSTRAZIONE=~: Teorema precedente e monotonia.

# Convessità e continuità
Sia $C \subseteq \mathbb{R}$ convesso e $f : C \to \mathbb{R}$ convessa. Valgono:
1. $f$ continua in $\text{Int}(C)$
2. $f$ localmente Lipschitziana in $\text{Int}(C)$

~={pink}DIMOSTRAZIONE=~: Monotonia e definizione di Lipschitzianità.

# Derivate di funzioni convesse
Sia $f : A \to \mathbb{R}$ e $x_{0} \in \text{Int}(A)$. Poniamo:
- $f'_{+}(x_{0}) := \lim\limits_{h \to 0^+} r_{x_{0}+h}^{x_{0}} f$
- $f'_{-}(x_{0}) := \lim\limits_{h \to 0^-} r_{x_{0}+h}^{x_{0}} f$

Sia $C \subseteq \mathbb{R}$ convesso e $f : C \to \mathbb{R}$ convessa. Valgono:
1. $\forall x_{0} \in \text{Int}(C)$   $\exists f'_{+}(x_{0}),f'_{-}(x_{0})$
2. $f'_{-}(x_{0})\leq f'_{+}(x_{0})$
3. $x \mapsto f'_{+}(x)$ e $x \mapsto f'_{-}(x)$ debolmente crescenti
4. $f'_{+}(x)$ continua a destra, $f'_{-}(x)$ continua a sinistra

~={pink}DIMOSTRAZIONE=~:
1. Osservazione sui rapporti incrementali
2. Osservazione sui rapporti incrementali
3. Monotonia delle derivate
4. Definizione di continuità

# Lemma dei 2/3 rapporti incrementali
Sia $C \subseteq \mathbb{R}$ convesso e $f : C \to \mathbb{R}$. Sono equivalenti:
- $f$ convessa
- $r_{b}^{a} f \leq r_{c}^{a} f$
- $r_{c}^{a} f \leq r_{c}^{b} f$
- $r_{b}^{a} f \leq r_{c}^{b} f$

~={pink}DIMOSTRAZIONE=~: Lemmi precedenti.

# Convessità e punti di min
Sia $x_{0} \in \text{Int}(C)$ un punto di min per $f$ convessa. Allora $x_{0}$ punto di min $\iff$ $f'_{-}(x_{0}) \leq 0 \leq f'_{+}(x_{0})$

~={pink}DIMOSTRAZIONE=~: Definizioni.

# Convessità e retta tangente
Sia $f : C \to \mathbb{R}$ convessa, $x_{0} \in \text{Int}(C)$ e $m \in [f'_{-}(x_{0}),f'_{+}(x_{0})]$. Allora $f(x) \geq f(x_{0}) + m(x-x_{0})$

~={pink}DIMOSTRAZIONE=~: Rapporto incrementale.

# Osservazioni su intersezioni convesse
Siano $f$ e $g$ due funzioni convesse. Allora $m(x):=\max \{ f(x),g(x) \}$ è convesso.

~={cyan}DIMOSTRAZIONE=~: $m(\lambda x + (1-\lambda)y)$
1. $= f(\lambda x + (1-\lambda)y) \impliedby$ wlog
2. $\leq \lambda f(x) + (1-\lambda)f(y) \impliedby$ convessità di $f$
3. $\leq \lambda m(x) + (1-\lambda)m(y) \impliedby f \leq m \land \lambda,1-\lambda\geq 0$

Sia $\{ f_{i}(x) \}_{i\in I}$ una famiglia di funzioni convesse. Allora $S(x):= \sup \{ f_{i}(x) : i \in I\}$ è convesso.

~={cyan}DIMOSTRAZIONE=~: $\forall i \in I$   $f_{i}(\lambda x + (1-\lambda )y) \leq \lambda S(x) + (1-\lambda)S(y)$ e faccio il sup.

In $\mathbb{R}^2$ valgono:
1. $f$ convessa $\iff$ sopragrafico convesso
2. Il sopragrafico dell'intersezione è l'intersezione dei sopragrafici
3. L'intersezione di convessi è convessa

# Disuguaglianza di Jensen
Sia $C \subseteq \mathbb{R}$ convesso e $f : C \to \mathbb{R}$ convessa. Sia $n\geq 2$ intero. Siano $x_{1},\dots,x_{n} \in C$. Siano $\lambda_{1},\dots,\lambda_{n}$ numeri $\geq 0$ tali che $\lambda_{1}+\dots+\lambda_{n} = 1$. Allora $f(\lambda_{1}x_{1}+\dots+\lambda_{n}x_{n}) \leq \lambda_{1}f(x_{1})+\dots+\lambda_{n}f(x_{n})$

~={yellow}DIMOSTRAZIONE=~: Induzione su $n$.

~={pink}DIMOSTRAZIONE=~: Applico la retta tangente.

# Disuguaglianza di Young
Siano $a$ e $b$ reali positivi. Siano $p$ e $q$ reali $>1$ tali che $\frac{1}{p} + \frac{1}{q} = 1$. Allora $ab \leq \frac{1}{p}a^p+\frac{1}{q}b^q$.

~={green}DIMOSTRAZIONE=~: $f(x) = \log x$ è concava e strettamente crescente.

Vale anche a 3.

~={pink}DIMOSTRAZIONE=~: Jensen a 3 per il logaritmo.

# Cauchy - Schwarz
$a_{1}b_{1}+\dots+a_{n}b_{n} \leq [a_{1}^2+\dots+a_{n}^2]^{1/2} [b_{1}^2+\dots+b_{n}^2]^{1/2}$

~={pink}DIMOSTRAZIONE=~: Prodotto scalare con vettori di componenti $a_{i}$ e $b_{i}$.

# Disuguaglianza di Hölder
$a_{1}b_{1}+\dots+a_{n}b_{n} \leq [a_{1}^p+\dots+a_{n}^p]^{1/p} [b_{1}^q+\dots+b_{n}^q]^{1/q}$

~={cyan}DIMOSTRAZIONE=~:
1. Disuguaglianza omogenea, dunque studiata wlog con somme $=1$
2. Su ogni prodotto si usa la disuguaglianza di Young

Vale anche a più di due specie.

# Media p-esima
Sia $M_{p}(a_{1},\dots,a_{n}) = \left[ \frac{{a_{1}^p+\dots+a_{n}^p}}{n} \right]^{1/p}$ detta media $p$-esima. Per definizione $M_{0}$ è la media geometrica e $M_{1}$ è la media aritmetica.

Valgono:
1. $p \mapsto M_{p}$ è crescente
2. $\lim\limits_{p \to +\infty} M_{p} = \max$
3. $\lim\limits_{p \to -\infty} M_{p} = \min$
4. $\lim\limits_{p \to 0} M_{p} =$ media geometrica

~={cyan}DIMOSTRAZIONE=~: Studio con il logaritmo.

# Massimo e minimo
Sia $f : [a,b] \to \mathbb{R}$ convessa. Allora:
1. max esiste
2. $\exists x_{0} \in (a,b)$   $x_{0}$ punto di min $\implies f'_{-}(x_{0})\leq0 \leq f'_{+}(x_{0})$
3. almeno uno degli estremi è punto di max

~={cyan}DIMOSTRAZIONE=~:
1. Max è agli estremi
	- Se $f(a) = f(b) = c$, allora per convessità $f(x)\leq c$, per cui $a$ e $b$ punti di max
	- Se $f(a) \neq f(b)$, allora $\max \{ f(a),f(b) \}$ è il max ed è unico
2. $f(x) \leq r(x)$ dove $r(x)$ congiunge gli estremi, per cui $\limsup\limits_{x \to a^+}f(x)\leq \limsup\limits_{x \to a^+} r(x) = f(a)$
3. $f$ SCS ed esiste minimo

# Lemma della sotto-sotto
Sia $\{ x_{n} \} \subseteq \mathbb{R}$ e supponiamo $\exists l \in \overline{\mathbb{R}}$ tale che $\forall x_{n_{k}}$   $\exists x_{n_{k_{i}}}\to l$. Allora $x_{n} \to l$.

~={red}DIMOSTRAZIONE=~ (Caso limite reale): Assurdo.

# Proprietà delle funzioni inverse
Siano $A,B \subseteq \mathbb{R}$ e $f: A \to B$ bigettive. Sia $g : B \to A$ la sua inversa. $f$ monotona $\implies g$ monotona.

~={cyan}DIMOSTRAZIONE=~ (Caso $f$ debolmente crescente):
1. $f$ strettamente crescente per iniettività
2. $g$ strettamente crescente per assurdo

Siano $A$ compatto e $f : A \to B$ invertibile e continua. Allora $g$ continua.

~={cyan}DIMOSTRAZIONE=~:
1. Considero $b \in B$ e $a = g(b)$
2. Pongo $x_{n} = g(y_{n})$. Per compattezza $\exists x_{n_{k_{i}}} \to x_{\infty}$
3. Per continuità $f(x_{n_{k_{i}}}) \to f(x_{\infty})$ e $b = f(x_{\infty})$
4. Applicando $g$ vale $g(b) = g(f(x_{\infty}))$

Siano $A \subseteq \mathbb{R}$ convesso e $f : A \to \mathbb{R}$ debolmente monotona. Allora $f$ continua $\iff f(A)$ convesso.

~={pink}DIMOSTRAZIONE=~:
1. ($\implies$) Teorema dei valori intermedi
2. ($\impliedby$) wlog $f$ debolmente crescente
	1. Per continuità $l = \lim\limits_{x \to x_{0}^-} f(x) < \lim\limits_{x \to x_{0}^+} f(x) = L$
	2. $f(A)$ non può contenere più di un punto in $[l,L]$ e $f(A)$ non convesso

Siano $D \subseteq \mathbb{R}$ e $f : D \to \mathbb{R}$ non monotona. Allora $\exists a<b<c \in D$ tali che vale una tra:
- $f(b) > f(a)$ e $f(b) > f(c)$
- $f(b) < f(a)$ e $f(b) < f(c)$

~={cyan}DIMOSTRAZIONE=~: Non veloce $\impliedby$ skill issue gobbiniana.

Siano $A \subseteq \mathbb{R}$ convesso e $f : A \to \mathbb{R}$ continua e invertibile. Allora $f$ strettamente monotona.

~={red}DIMOSTRAZIONE=~: Assurdo con lemma del triangolino.

Siano $A$ convesso e $f : A \to B$ invertibile e continua. Allora $g$ continua.

~={pink}DIMOSTRAZIONE=~:
1. Per il lemma precedente $f$ strettamente monotona e $B = f(A)$ convesso
2. Per la prima proprietà $g : B \to A$ strettamente monotona e $B$ convesso
3. Per il primo lemma $g$ continua $\iff g(B)$ convesso $\iff A$ convesso

# Teoremi misteriosi sulle derivate
Siano $f: A \to B$ invertibile, $x_{0} \in \text{Int}(A)$, $y_{0} = f(x_{0})$ e $\exists f'(x_{0}) \neq 0$. Allora $g'(y_{0}) = \frac{1}{f'(x_{0})}$.

~={cyan}DIMOSTRAZIONE=~: $\lim\limits_{k \to 0} r_{y_{0}+h}^{y_{0}} g = \lim\limits_{y \to y_{0}} r_{y}^{y_{0}} g = \lim\limits_{x \to x_{0}} (r_{x}^{x_{0}} f)^{-1} = \frac{1}{f'(x_{0})}$

Sia $f : A \to B$ invertibile $C^1$ tale che $f'(x)\neq 0$ in $A$. Allora $g \in C^1$ in $B$ e $g'(x) = \frac{1}{f'(g(x))}$.

~={pink}DIMOSTRAZIONE=~: Teorema precedente.

Sia $f : A \to B$ invertibile $C^k$ tale che $f'(x)\neq 0$ in $A$. Allora $g \in C^k$.

~={yellow}DIMOSTRAZIONE=~: Bootstrap (autoinduzione) con la proposizione precedente.

Siano $f,g$ funzioni. Allora $[g(f(x))]' = g'(f(x))f'(x)$.

~={cyan}DIMOSTRAZIONE=~:
1. Considero $x_{n} \to x_{0}$
2. Se $\exists x_{n_{k}}\to x_{0}$ su cui $f(x_{n_{k}})\neq f(x_{0})$ il conto col rapporto incrementale torna
3. Se $\exists x_{n_{k}}\to x_{0}$ su cui $f(x_{n_{k}})=f(x_{0})$ sempre, $f'(x_{0})=0$ e $r_{x_{n_{k}}}^{x_{0}} (g\circ f) \to 0$
# Proprietà di Darboux delle derivate
Sia $f : (x_{0}-r,x_{0}+r)\to \mathbb{R}$ derivabile ovunque. Allora $\liminf\limits_{x \to x_{0}} f'(x)\leq f'(x_{0})\leq \limsup\limits_{x \to x_{0}} f'(x)$

~={pink}DIMOSTRAZIONE=~:
1. Per Lagrange $r_{x_{0}+h}^{x_{0}} f = f'(c(h))$ con $x_{0} \leq c(h) \leq x_{0}+h$
2. Faccio liminf e limsup a destra e sinistra