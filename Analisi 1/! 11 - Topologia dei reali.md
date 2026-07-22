# Linguaggio topologico in uno spazio metrico
Sia $A \subseteq \mathbb{R}$ un sottoinsieme, $x_{0} \in \mathbb{R}$ e dato un certo $r$, sia $i_{x_0,r} = (x_{0}-r,x_{0}+r)$. Allora $x_{0}$ si dice:
- interno ad $A$ se $\exists r > 0$   $i_{x_{0},r} \subseteq A$
- aderente ad $A$ se $\forall r > 0$   $i_{x_{0},r} \cap A \neq \emptyset$
- di frontiera o sul bordo di $A$ se aderente ad $A$ e a $\mathbb{R} \setminus A$
- isolato in $A$ se $\exists r>0$   $i_{x_{0},r} \cap A = \{ x_{0} \}$
- di accumulazione per $A$ se $\forall r>0$   $(i_{x_{0},r} \cap A) \setminus \{ x_{0} \} \neq \emptyset$

Sia $A \subseteq \mathbb{R}$, allora siano:
- $\text{Int}(A)$ o $\mathring{A}$ l'insieme dei punti interni ad $A$
- $\text{Clos}(A)$ o $\bar{A}$ l'insieme dei punti aderenti ad $A$
- $\partial A$ l'insieme dei punti di frontiera di $A$
- $\text{Isol}(A)$ l'insieme dei punti isolati in $A$
- $D(A)$ l'insieme dei punti di accumulazione per $A$

$A$ si dice:
- aperto se $A = \text{Int}(A)$
- chiuso se $A = \text{Clos}(A)$

Valgono:
1. $\text{Int}(A) \subseteq A \subseteq \text{Clos}(A)$
2. $\partial A \subseteq \text{Clos}(A)$
3. $\text{Clos}(A) = \text{Int}(A) \cup \partial A$ con unione disgiunta
4. $\text{Clos}(A) = \text{Isol}(A) \cup D(A)$ con unione disgiunta

~={cyan}DIMOSTRAZIONE=~: Definizioni.

Valgono su intersezioni e unioni finite:
1. Se $A$ e $B$ sono aperti, allora $A \cap B$ e $A \cup B$ sono aperti
2. Se $A$ e $B$ sono chiusi, allora $A \cap B$ e $A \cup B$ sono chiusi

~={cyan}DIMOSTRAZIONE=~ ($A \cap B$ aperto):
1. $A$ aperto $\implies \forall x_{0}\in A$   $\exists r_{A}$   $(x_{0}-r_{A}, x_{0}+r_{A})\subseteq A$
2. $B$ aperto $\implies \forall x_{0} \in B$   $\exists r_{B}$   $(x_{0}-r_{B},x_{0}+r_{B}) \subseteq B$
3. Se $x_{0}\in A \cap B$ basta usare $r := \min\{ r_{A},r_{B} \}$ e vale $(x_{0}-r,x_{0}+r) \subseteq A \cap B$ 

Valgono:
1. L'unione di infiniti aperti è aperta
2. L'intersezione di infiniti chiusi è chiusa

# Caratterizzazione con le successioni
Sia $A \subseteq \mathbb{R}$ e $x_{0} \in \mathbb{R}$. Allora:
1. $x_{0} \in \text{Int}(A) \iff \forall \{ x_{n} \} \subseteq \mathbb{R}$   $[x_{n} \to x_{0} \implies x_{n} \in A \text{ definitivamente}]$
2. $x_{0} \in \text{Clos}(A) \iff \exists \{ x_{n} \} \subseteq A$   $x_{n} \to x_{0}$
3. $x_{0} \in \partial A \iff x_{0} \in \text{Clos}(A) \land x_{0} \in \text{Clos}(\mathbb{R} \setminus A)$
4. $x_{0} \in \text{Isol}(A) \iff \forall \{ x_{n} \} \subseteq A$   $[x_{n} \to x_{0} \implies x_{n} = x_{0} \text{ definitivamente}]$
5. $x_{0} \in D(A) \iff \exists \{ x_{n} \} \subseteq A \setminus \{ x_{0} \}$   $x_{n}\to x_{0}$

~={cyan}DIMOSTRAZIONE=~: Definizione di limite.

# Linguaggio topologico relativo
Sia $A \subseteq B \subseteq \mathbb{R}$. Allora si dice, relativamente a $B$:
- $x_{0}$ interno ad $A$, ossia $x_{0} \in \text{Int}_{B}(A)$, se $\exists r>0$   $i_{x_{0},r} \cap B \subseteq A$
- $A$ aperto se $A = \text{Int}_{B}(A)$

La definizione si può estendere al resto del linguaggio.

# Continuità
Sia $A \subseteq \mathbb{R}$ e $f : A \to \mathbb{R}$. Sia $x_{0} \in  A$. Allora $f$ è continua in $x_{0}$ se:
1. ($\varepsilon / \delta$) $\forall \varepsilon>0$   $\exists \delta>0$   $\forall x \in i_{x_{0},\delta} \cap A$   $f(x) \in i_{f(x_{0}), \varepsilon}$
2. (Successioni) $\forall \{ x_{n} \} \subseteq A$   $[x_{n}\to x_{0} \implies f(x_{n}) \to f(x_{0})]$
3. (Limiti) $x_{0} \in \text{Isol}(A) \lor [x_{0} \in D(A) \land \lim\limits_{x \to x_{0}} f(x) = f(x_{0})]$
4. (Aperti) $\forall U \subseteq \mathbb{R}$ aperto con $f(x_{0}) \in U$ vale $x_{0} \in \text{Int}_{A}(f^{-1}(U))$

~={cyan}DIMOSTRAZIONE=~: Definizioni.

Se $f$ e $g$ sono continue, allora $g \circ f$ è continua.

~={cyan}DIMOSTRAZIONE=~: $x_{n} \to x_{0} \implies f(x_{n}) \to f(x_{0}) \implies g(f(x_{n})) \to g(f(x_{0}))$ per continuità.

# Teorema di Bolzano - Weierstrass
Sia $\{ x_{n} \} \subseteq \mathbb{R}$ una successione limitata. Allora $\exists \{ n_{k} \} \subseteq \mathbb{N}$   $x_{n_{k}}\to L \in \mathbb{R}$

~={cyan}DIMOSTRAZIONE=~: $L := \limsup\limits_{n \to +\infty} x_{n} \in [-M,M]$ da cui $L \in \mathbb{R}$ e inoltre $L = \text{maxlim } x_{n}$

# Compattezza
Si dice ricoprimento aperto una famiglia $\{ u_{i} \}_{i \in I}$ di aperti di $\mathbb{R}$ tale che $A \subseteq \bigcup\limits_{i \in I} u_{i}$

Un suo sottoricoprimento viene detto finito se $\exists J \subseteq I$ finito per cui $A \subseteq \bigcup\limits_{i \in J} u_{i}$

Sia $A \subseteq \mathbb{R}$, allora $A$ si dice compatto:
- se limitato e chiuso
- per successioni se $\forall \{ x_{n} \} \subseteq A$   $\exists \{ n_{k} \} \subseteq \mathbb{N}$ crescente   $\exists x_{\infty} \in A$   $x_{n_{k}}\to x_{\infty}$
- per ricoprimenti se ogni ricoprimento aperto di $A$ ammette un sottoricoprimento finito

Sia $A \subseteq \mathbb{R}$ non vuoto e $L := \sup A \in \mathbb{R} \cup \{ +\infty \}$. Allora $\exists \{ a_{n} \} \subseteq A$   $a_{n} \to L$.

~={green}DIMOSTRAZIONE=~:
- Se $L = +\infty$, si usa la caratterizzazione
- Se $L < +\infty$
	1. $a \leq L$   $\forall a \in A$
	2. $\forall \varepsilon > 0$   $\exists a \in A$   $a \geq L - \varepsilon$
	3. Uso $\varepsilon = \frac{1}{n}$ e trovo $a_{n}$ tale che $L - \frac{1}{n} \leq a_{n} \leq L$
	4. Per carabinieri $a_{n} \to L$

Sia $A \subseteq \mathbb{R}$ compatto e non vuoto. Allora ammette max e min.

~={cyan}DIMOSTRAZIONE=~:
1. $L := \sup A \in \mathbb{R}$ poiché $A$ limitato
2. $L \in \text{Clos}(A)$ poiché $\forall r>0$   $\exists a \in A$   $L-r \leq a \leq L \leq L+r$ per cui $L \in A$

Sia $A \subseteq \mathbb{R}$ compatto per ricoprimenti e $f: A \to \mathbb{R}$ continua. Allora $f(A)$ è compatto per ricoprimenti.

~={cyan}DIMOSTRAZIONE=~:
1. $f(A) \subseteq \bigcup\limits_{i \in I} V_{i}$
2. Pongo $u_{i}:= f^{-1}(V_{i})$ e osservo che sono aperti in $A$ e ricoprono $A$
3. $A$ è compatto per ricoprimenti, per cui esiste un sottoricoprimento finito
4. $y \in f(A)$, prendo $x \in A$   $y = f(x)$ e $k \in u_{i_{k}}$ per cui $y \in f(u_{i_{k}}) = V_{i_{k}}$

# Lemma del raggio magico (numero di Lebesgue)
Sia $A \subseteq \mathbb{R}$ compatto per successioni e $\{ u_{i} \}_{i \in I}$ un ricoprimento aperto di A.
Allora $\exists r>0$   $\forall x \in A$   $\exists i \in I$   $[x-r,x+r] \subseteq u_{i}$

~={red}DIMOSTRAZIONE=~:
1. Supponiamo la tesi non vera, dunque $\forall r > 0$   $\exists x \in A$   $\forall i \in I$   $[x-r,x+r] \nsubseteq u_{i}$
2. Si pone $\varepsilon = \frac{1}{n}$ ma va bene qualsiasi $\varepsilon \to 0$
3. Data $\{ x_{n} \}$, per ipotesi $\exists x_{n_{k}}\to x_{\infty} \in A$
4. Sia $i_{\infty} \in I$ tale che $x_{\infty} \in u_{i_{\infty}}$, vale $\exists r_{\infty}>0$   $(x_{\infty}-r_{\infty},x_{\infty}+r_{\infty}) \subseteq u_{i_{\infty}}$
5. Per $k$ grande $x_{n_{k}} \in \left[ x_{\infty}-\frac{r_{\infty}}{2}, x_{\infty} + \frac{r_{\infty}}{2} \right]$
6. Vale $\left[ x_{n_{k}} - \frac{r_{\infty}}{2}, x_{n_{k}} + \frac{r_{\infty}}{2} \right] \subseteq u_{i_{\infty}}$ generando assurdo quando $\frac{1}{n_{k}}< \frac{r_{\infty}}{2}$

# Lemma dei distributori ($\varepsilon$-rete)
Sia $A \subseteq \mathbb{R}$ limitato e $\varepsilon>0$. Allora $\exists \{ x_{1},\dots, x_{n} \} \subseteq A$   $\forall x \in A$   $\exists i \in \{ 1,\dots,n \}$   $|x-x_{i}|\leq \varepsilon$

DIMOSTRAZIONE:
1. Considero la griglia $kr$ con $k \in \mathbb{Z}$ e gli intervalli $[kz, (k+1)z]$
2. Un numero finito di questi interseca $A$ limitato
3. In ognuna delle intersezioni non vuote prendo $x_{i}$

# Equivalenza della compattezza
In $\mathbb{R}$ le tre nozioni di compattezza sono equivalenti.

DIMOSTRAZIONE (compatto $\implies$ compatto per successioni):
1. Sia $\{ x_{n} \} \subseteq A$ una successione
2. $A$ limitato $\implies$ $\{ x_{n} \}$ limitata $\implies$ $\exists x_{n_{k}}\to x_{\infty}\in \mathbb{R}$ per Bolzano - Weierstrass
3. $x_{\infty} \in \text{Clos}(A)=A$ poiché $(x_{\infty}-r,x_{\infty}+r)$ interseca $A$

DIMOSTRAZIONE (compatto per successioni $\implies$ compatto):
1. Supponiamo $A$ non compatto. Allora $\sup A = +\infty \implies \exists x_{n} \to +\infty \implies \not\exists x_{n_{k}}\to L \in \mathbb{R}$
2. Supponiamo $A$ non chiuso. Allora $\exists x_{\infty} \in \text{Clos}(A)$   $x_{\infty} \not\in A$   ma allora $\exists x_{n} \to x_{\infty}\not\in A$

DIMOSTRAZIONE (compatto per ricoprimenti  $\implies$ compatto):
1. ($\implies$ limitato)
	1. Considero $u_{n} := (-n,n)$ con $n \in \mathbb{N}$ e $n \geq 1$
	2. $A \subseteq \bigcup\limits_{n\geq 1} u_{n} = \mathbb{R}$
	3. Per ipotesi $A \subseteq \bigcup\limits_{n\geq 1}^{n_{0}} u_{n} = (-n_{0},n_{0})$ definitivamente
2. ($\implies$ chiuso)
	1. Considero $x \in \text{Clos}(A)$
	2. Se $x \not \in A$, considero $u_{n} = \mathbb{R} \setminus \left[ x-\frac{1}{n},x+\frac{1}{n} \right]$
	3. $A \subseteq \bigcup\limits_{n\geq 1} u_{n} = \mathbb{R} \setminus \{ x \}$
	4. $A \subseteq \bigcup\limits_{n\geq 1}^{n_{0}} u_{n} = \mathbb{R} \setminus \left[ x-\frac{1}{n_{0}}, x+\frac{1}{n_{0}} \right]$ definitivamente
	5. $\left[ x-\frac{1}{2n_{0}}, x+\frac{1}{2n_{0}} \right] \cap A\neq \emptyset \implies x \in \text{Clos}(A)$

DIMOSTRAZIONE (compatto per successioni $\implies$ compatto per ricoprimenti):
1. Mi viene dato un ricoprimento $\{ u_{i} \}_{i \in I}$
2. Prendo il raggio magico $r$ del ricoprimento
3. Scelgo $x_{1},\dots,x_{n}$ distributori e $u_{i_{1}},\dots,u_{i_{n}}$ tali che $[x_{j}-r,x_{j}+r] \subseteq u_{i_{j}}$   $\forall j=1,\dots,n$
4. $\forall x \in A$   $x \in [x_{j}-r,x_{j}+r]$ e l'ultimo intervallo $\subseteq u_{i_{j}}$ per cui $u_{i_{1}},\dots,u_{i_{n}}$ ricoprono

# Weierstrass
Sia $A \subseteq \mathbb{R}$ non vuoto e $f : A \to \mathbb{R}$ tali che:
1. $f$ continua
2. $A$ compatto
Allora esistono max e min.

DIMOSTRAZIONE:
1. $S := \sup \{ f(x) : x \in A \} \in \mathbb{R} \cup \{ +\infty \}$
2. $\exists \{ y_{n} \} \subseteq f(A)$   $y_{n}\to S$ per il solito lemma
3. $y_{n}=f(x_{n})$ con $x_{n} \in A$ per definizione di immagine
4. $\{ x_{n} \} \subseteq A$, che è compatto, dunque $\exists x_{n_{k}} \to x_{\infty}$
5. $f(x_{\infty}) = \lim\limits_{k \to +\infty} f(x_{n_{k}}) = \lim\limits_{k \to +\infty} y_{n_{k}} = \lim\limits_{n \to +\infty} y_{n} = S$

Sia $A \subseteq \mathbb{R}$ compatto per successioni e $f:A\to \mathbb{R}$ continua, allora $f(A)$ compatto per successioni.

DIMOSTRAZIONE: $y_{n_{k}} = f(x_{n_{k}}) \to f(x_{\infty}) =: y_{\infty} \in f(A)$

# Semicontinuità
Sia $f : A \to \mathbb{R}$ e $x_{0} \in A$ tali che vale uno tra:
- $x_{0}$ isolato in A
- $\liminf\limits_{x \to x_{0}} f(x) \geq f(x_{0})$
Allora $f$ è detta semicontinua inferiormente (SCI).

Si definisce analogamente con limsup $\leq$ la semicontinuità superiore (SCS).

$f$ SCI e SCS $\implies$ $f$ continua

Sia $f : A \to \mathbb{R}$ tale che:
1. $f$ SCI in ogni punto di $A$
2. $A$ compatto non vuoto
Allora esiste min.

DIMOSTRAZIONE: Esiste l'inf e per il solito lemma sulle successioni è anche min.

# Successione di Cauchy
Una successione $\{ x_{n} \} \subseteq \mathbb{R}$ si dice di Cauchy se $\forall \varepsilon>0$   $|x_{n}-x_{m}|\leq\varepsilon$ definitivamente.

Le successioni con limite reale sono di Cauchy.

DIMOSTRAZIONE:
1. Sia $x_{n} \to x_{\infty} \in \mathbb{R}$
2. Per definizione di limite $\forall\varepsilon>0$   $|x_{n}-x_{\infty}|\leq \frac{1}{2}\varepsilon$ definitivamente
3. $|x_{n}-x_{m}| \leq |x_{n}-x_{\infty}| + |x_{\infty}-x_{m}| \leq \frac{1}{2}\varepsilon + \frac{1}{2}\varepsilon = \varepsilon$ definitivamente

Le successioni di Cauchy sono limitate.

DIMOSTRAZIONE: Cherry picking di $\varepsilon$.

Sia $\{ x_{n} \}\subseteq \mathbb{R}$ di Cauchy tale che $\exists x_{n_{k}}\to x_{\infty} \in \mathbb{R}$. Allora $x_{n}\to x_{\infty}$.

DIMOSTRAZIONE: Definizione di successione di Cauchy con $n_{0} = \max \{ n_{1},n_{k_{0} } \} = n_{k_{0}}$.

Le successioni di Cauchy hanno limite reale.

DIMOSTRAZIONE: Limitatezza, Bolzano - Weierstrass e tendenza della sottosuccessione.

DIMOSTRAZIONE: Limitatezza, liminf $l$ e limsup $L$.

# $\mathbb{Q}$ vs $\mathbb{R}$
Il fatto che in $\forall r \in \mathbb{R}$   $\exists n \in \mathbb{N}$   $n>r$ è detta proprietà archimedea dei numeri reali.

La convergenza delle successioni di Cauchy è detta completezza.

In un campo ordinato proprietà archimedea $\land$ completezza $\implies$ assioma di continuità.