# Avverbi
Un predicato $P(n)$ su $\mathbb N$ vale:
- definitivamente se    $\exists n_0 \in \mathbb N$   $\forall n \geq n_0$   $P(n)$
- frequentemente se   $\forall n_0 \in \mathbb N$   $\exists n \geq n_0$   $P(n)$

Per estensione in questi appunti si utilizzerà sui predicati $P(x)$ definiti su $D \subseteq\mathbb{R}$:
- definitivamente se   $\exists k \in \mathbb{R}$   $\forall x \in D \cap [k,+\infty)$   $P(x)$
- definitivamente a sinistra se   $\exists k \in \mathbb{R}$   $\forall x \in D \cap (-\infty,k]$   $P(x)$

# Successione
Funzione $f : \mathbb N \to \mathbb R$ definita definitivamente.

# Limite di una successione
Data una successione $a_n$, il limite $\lim\limits_{n \to \infty} a_n$ è:
- $+\infty$ se   $\forall M \in \mathbb R$   $a_n \geq M$   definitivamente
- $-\infty$ se   $\forall M \in \mathbb R$   $a_n \leq M$   definitivamente
- $l \in \mathbb R$ se   $\forall \varepsilon \in \mathbb R$   $|a_n - l| \leq \varepsilon$   definitivamente

Se il limite è
- $+\infty$ allora la successione è limitata dal basso
- $-\infty$ allora la successione è limitata dall'alto
- $l \in \mathbb R$ allora la successione è limitata dall'alto e dal basso

# Confronto a 2
Siano $a_n$ e $b_n$ due successioni tali che $a_n \leq b_n$ definitivamente. Allora:
- $a_n \to +\infty \implies b_n \to +\infty$
- $b_n \to -\infty \implies a_n \to -\infty$

~={orange}DIMOSTRAZIONE:=~
1. Per ipotesi valgono $a_n \leq b_n$ da $n_0$
2. Per il limite vale $\forall M \in \mathbb R$   $a_n \geq M$  da $n_1$
3. Ponendo $n_2 = \max\{n_0, n_1\}$ vale $b_n \geq M$ da $n_2$

# Confronto a 3
Siano $a_n$, $b_n$, e $c_n$ tre successioni tali che:

1. $a_n \leq b_n \leq c_n$ definitivamente
2. $a_n \to l \in \mathbb R$
3. $c_n \to l$
Allora anche $b_n \to l$.

~={orange}DIMOSTRAZIONE=~:
1. Per (2.) si ha $l-\varepsilon \leq a_{n} \leq l+\varepsilon$ definitivamente da $n_{a}$
2. Per (3.) si ha $l-\varepsilon \leq c_{n} \leq l + \varepsilon$ definitivamente da $n_{c}$
3. Per (1.) si ha $a_n \leq b_n \leq c_n$ definitivamente da $n_{b}$
4. $l-\varepsilon \leq b_{n}\leq l + \varepsilon$ definitivamente da $\max\{ n_{a},n_{b},n_{c} \}$

# Teorema delle successioni monotone
Sia $a_{n}$ una successione debolmente crescente. Allora $a_{n} \to \sup\{ a_{n} :n \in \mathbb{N} \}$.

~={orange}DIMOSTRAZIONE=~:
- Sia $l = +\infty$
	1. Considero $M$
	2. Poiché $\sup = +\infty$, per caratterizzazione $\exists n_{0}\in \mathbb{N}$   $a_{n_{0}}\geq M$
	3. Per monotonia $a_{n}\geq a_{n_{0}} \geq M$ definitivamente
- Sia $l \in \mathbb{R}$
	1. Considero $\varepsilon$
	2. Per caratterizzazione $\exists n_{0} \in \mathbb{N}$   $a_{n_{0}}\geq l - \varepsilon$
	3. Per monotonia $a_{n}\geq a_{n_{0}} \geq l - \varepsilon$ definitivamente
	4. Vale $a_{n} \leq l \leq l+\varepsilon$ in quanto $l$ è un maggiorante

# Numero di Nepero
La successione $e_n = (1 + \frac 1 n)^n$ ha limite, detto numero di Nepero e indicato con $e$. Inoltre $2 < e < 3$.

~={yellow}DIMOSTRAZIONE=~:
1. Per induzione $e_{n}\geq e_{n-1}$, alla fine si usa Bernoulli
2. $e_{n} = \left( 1 + \frac{1}{n} \right)^n = \sum\limits_{k=0}^{n} \binom{n}{k} \frac{1}{n^k} = 1 + \sum\limits_{k=1}^{n} \binom{n}{k} \frac{1}{n^k} \leq 1 + \sum\limits_{k=1}^{n} \frac{1}{k!} \leq 1 + \sum\limits_{k=1}^{n} \frac{1}{2^{k-1}} = 3 - \frac{1}{2^{n-1}}< 3$ 

# Retta reale estesa
Si definisce $\overline{\mathbb{R}} = \mathbb{R} \cup \{ +\infty, -\infty \}$

Siano $a_{n} \to l_{1} \in \overline{\mathbb{R}}$ e $b_{n} \to l_{2} \in \overline{\mathbb{R}}$ due successioni, valgono:
- $a_{n} \pm b_{n} = l_{1} \pm l_{2}$
- $a_{n} b_{n} = l_{1} l_{2}$
- $\frac{a_{n}}{b_{n}} = \frac{l_{1}}{l_{2}}$

# Criterio della radice
Sia $a_{n}$ una successione definitivamente $\geq 0$ tale che $\sqrt[n]{a_{n}} \to l \in \overline{\mathbb{R}}^+$
- $l>1 \implies a_{n} \to +\infty$
- $l<1 \implies a_{n} \to 0$

~={orange}DIMOSTRAZIONE=~:
- Sia $l>1$
	1. $\sqrt[n]{a_{n}}\geq \frac{{l+1}}{2}$ definitivamente
	2. $a_{n} \geq (\frac{{l+1}}{2})^n \to +\infty$
- Sia $l < 1$
	1. $\sqrt[n]{a_{n}} \leq \frac{{l+1}}{2}$ definitivamente
	2. $0 \leq a_{n} \leq (\frac{{l+1}}{2})^n \to 0$

# Criterio del rapporto
Sia $a_n$ una successione definitivamente $>0$ tale che $\frac{a_{n+1}}{a_{n}}\to l \in \overline{\mathbb{R}}^+$. Valgono le implicazioni precedenti.

~={orange}DIMOSTRAZIONE=~:
- Sia $l>1$
	1. Definitivamente per $n_{0}$ si ha $\frac{a_{n+1}}{a_{n}}\geq \frac{{l+1}}{2}$
	2. $a_{n_{0}+1}\geq \frac{{l+1}}{2}a_{n_{0}}$
	3. Per induzione $a_{n_{0}+k}\geq (\frac{{l+1}}{2})^ka_{n_{0}}$
	4. $a_{n} \geq (\frac{{l+1}}{2})^{n-n_{0}}a_{n_{0}} \to +\infty$
- Sia $l<1$: come prima $0 \leq a_{n} \leq \left( \frac{{l+1}}{2} \right)^n \left( \frac{2}{l+1} \right)^{n_{0}}a_{n_{0}} \to 0$

# Criterio rapporto $\to$ radice
Sia $a_{n}$ una successione definitivamente $>0$. Vale $\frac{a_{n+1}}{a_{n}} \to l \in \overline{\mathbb{R}}^+ \implies \sqrt[n]{a_{n}} \to l$

~={orange}DIMOSTRAZIONE=~:
1. Definitivamente per $n_{0}$ si ha $l- \frac{\varepsilon}{2} \leq \frac{a_{n+1}}{a_{n}} \leq l+ \frac{\varepsilon}{2}$
2. Per induzione $\left( l - \frac{\varepsilon}{2} \right)^n\left( l- \frac{\varepsilon}{2} \right)^{-n_{0}}a_{n_{0}} \leq a_{n} \leq \left( l + \frac{\varepsilon}{2} \right)^n\left( l + \frac{\varepsilon}{2} \right)^{-n_{0}}a_{n_{0}}$
3. Facendo la radice $n$-esima e i limiti si ha $l-\varepsilon \leq \sqrt[n]{a_{n}} \leq l + \varepsilon$

# Intorno
Dati $x_{0}, \delta$ e $D \subseteq \mathbb{R}$, si dice intorno chiuso di $x_{0}$ in $D$ l'insieme $D \cap [x_{0}-\delta,x_{0}+\delta]\setminus \{ x_{0} \}$ e si indica con $I_{x_{0},\delta}$.

Dati $x_{0}$ e $D \subseteq \mathbb{R}$, $x_{0}$ si dice punto di accumulazione di $D$ se $\forall \delta>0$   $I_{x_{0},\delta}\neq \emptyset$

# Limite di una funzione
Data una funzione $f : D \to \mathbb{R}$ con $D \subseteq \mathbb{R}$ non vuoto, si definiscono:
- $\lim\limits_{x \to +\infty}f(x)$ con $D$ non limitato superiormente
- $\lim\limits_{x \to -\infty} f(x)$ con $D$ non limitato inferiormente
- $\lim\limits_{x \to x_{0}} f(x)$ con $x_{0}$ punto di accumulazione di $D$

Si dice che $\lim\limits_{x \to +\infty} f(x)$ è:
- $+\infty$ se   $\forall M \in \mathbb{R}$   $f(x) \geq M$   definitivamente
- $-\infty$ se   $\forall M \in \mathbb{R}$   $f(x) \leq M$   definitivamente
- $l \in \mathbb{R}$ se   $\forall \varepsilon>0$   $|f(x)-l|\leq\varepsilon$   definitivamente

Si dice che $\lim\limits_{x \to -\infty} f(x)$ è:
- $+\infty$ se   $\forall M \in \mathbb{R}$   $f(x) \geq M$   definitivamente a sinistra
- $-\infty$ se   $\forall M \in \mathbb{R}$   $f(x) \leq M$   definitivamente a sinistra
- $l \in \mathbb{R}$ se   $\forall \varepsilon>0$   $|f(x)-l|\leq\varepsilon$   definitivamente a sinistra

Si dice che $\lim\limits_{x \to x_{0}} f(x)$ è:
- $+\infty$ se   $\forall M \in \mathbb{R}$   $\exists \delta>0$   $\forall x \in I_{x_{0},\delta}$   $f(x) \geq M$
- $-\infty$ se   $\forall M \in \mathbb{R}$   $\exists \delta>0$   $\forall x \in I_{x_{0},\delta}$   $f(x) \leq M$
- $l \in \mathbb{R}$ se   $\forall \varepsilon>0$   $\exists \delta>0$   $\forall x \in I_{x_{0},\delta}$   $|f(x)-l|\leq\varepsilon$

# Continuità
Una funzione $f : D \to \mathbb{R}$ con $D \subseteq \mathbb{R}$ si dice:
- continua in $x_{0}$ se $\lim\limits_{x \to x_{0}} f(x) = f(x_{0})$
- continua in $D$ se è continua in ogni punto di $D$

Tutte le funzioni ottenute da quelle elementari mediante operazioni algebriche e/o composizioni sono continue nel loro dominio di definizione.

DIMOSTRAZIONE: Definizione di limite e continuità.

# Criterio successioni $\to$ funzioni
Sia $D \subseteq \mathbb{R}$ con $\sup D = +\infty$. Sia $a_{n}$ una successione e $f:D\to \mathbb{R}$ una funzione per cui vale:
- $f(x) = a_{n}$   $\forall x \in D \cap [n,n+1)$
Allora $\lim\limits_{x \to +\infty} f(x) = \lim\limits_{n \to +\infty} a_{n}$

~={orange}DIMOSTRAZIONE=~: Il definitivamente delle successioni è simile al definitivamente delle funzioni.

# Criterio funzioni $\to$ successioni
Sia $a_{n}$ una successione e $f:D\to \mathbb{R}$ una funzione per cui valgono:
1. $a_{n} \in D \setminus \{ x_{0} \}$ definitivamente
2. $a_{n} \to x_{0} \in \overline{\mathbb{R}}$
3. $\lim\limits_{x \to x_{0}} f(x) = l \in \overline{\mathbb{R}}$
Allora $f(a_{n}) \to l$

~={orange}DIMOSTRAZIONE=~: (3.), poi (1.) e (2.) usando le definizioni.

# Sottosuccessione
Sia $n_{k}$ una in $\mathbb{N}$ tale che $n_{k} \to +\infty$. Una sottosuccessione è l'applicazione $k \mapsto a_{n_{k}}$

Sia $a_{n}$ una successione tale che $a_{n} \to l\in \overline{\mathbb{R}}$. Allora ogni sottosuccessione tende a $l$.

# Razionalizzazione
Un trucco per risolvere limiti aventi radici al numeratore è quello di razionalizzare, cioè moltiplicare per la somma/differenza ottenendo la differenza di quadrati o cubi.
