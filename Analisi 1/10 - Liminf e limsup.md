# Presentazione via lim sup
Sia ${a_{n}}$ una successione. Se:
- $\sup a_{n} = +\infty$, allora per definizione $\limsup\limits_{n \to +\infty} a_{n} = +\infty$
- $\sup a_{n} < +\infty$, allora
	1. Sia $S_{n} := \sup \{ a_{k} : k \geq n \} \in \mathbb{R}$
	2. Per definizione $\limsup\limits_{n \to +\infty} a_n = \lim\limits_{n \to +\infty} S_n \in \mathbb{R} \cup \{ +\infty \}$

Il liminf è definito analogamente con $-\infty$ e $I_{n}$ come versione con $\leq$ di $S_{n}$.

Liminf e limsup esistono sempre.

~={cyan}DIMOSTRAZIONE=~:
- Nei casi banali è vero
- Nei casi non banali si ha sempre $I_{n} \leq S_{n}$ e si passa al limite

# Caratterizzazione
$\limsup\limits_{n \to +\infty} a_n = +\infty \iff \forall M \in \mathbb{R}$   $a_{n} \geq M$   frequentemente

~={cyan}DIMOSTRAZIONE=~:
- ($\implies$) Per assurdo $\exists M \in \mathbb{R}$   $a_{n} \geq M$ finite volte $\implies$ $a_{n} \leq M$ definitivamente $\implies a_{n}$ limitata
- ($\impliedby$) Dall'ipotesi $\sup a_{n} = +\infty \implies \limsup\limits_{n \to +\infty} a_n = +\infty$ per definizione

$\limsup\limits_{n \to +\infty} a_n = L \in \mathbb{R} \iff \forall \varepsilon>0$:
1. $a_{n}\leq L+\varepsilon$ definitivamente
2. $a_{n} \geq L - \varepsilon$ frequentemente

~={orange}DIMOSTRAZIONE=~:
1. Per ipotesi $S_{n} \to L$, ossia $|S_{n} - L| \leq \varepsilon$ definitivamente
2. $S_{n} \leq L+\varepsilon$ definitivamente $\implies$ $a_{n} \leq L+\varepsilon$ definitivamente
3. Se $a_{n} \geq L - \varepsilon$ finite volte $\implies$ $S_{n} \leq L - \varepsilon$ definitivamente $\implies$ $\lim\limits_{n \to +\infty} S_{n} \leq L-\varepsilon$

$\limsup\limits_{n \to +\infty} a_n = -\infty \iff \forall M \in \mathbb{R}$   $a_{n} \geq M$   definitivamente $\iff$ $\lim\limits_{n \to +\infty} a_{n} = -\infty$

~={orange}DIMOSTRAZIONE=~: $S_{n} \to -\infty \implies S_{n} \leq M$ definitivamente $\implies a_{n} \leq M$ definitivamente

Il liminf è caratterizzato analogamente.

Sia $a_{n}$ una successione e $m \in \overline{\mathbb{R}}$. Vale $\liminf\limits_{n \to +\infty} a_n = \limsup\limits_{n \to +\infty} a_n = m \iff a_{n} \to m$

~={orange}DIMOSTRAZIONE=~:
- ($\implies$)
	- Se $m = \pm \infty$  il limite è banale
	- Se $m \in \mathbb{R}$, per caratterizzazione  $l - \varepsilon \leq a_{n} \leq l + \varepsilon$ per un definitivamente comune
- ($\impliedby$) Si considera la caratterizzazione nei vari casi

# Presentazione via maggioranti
Sia $a_{n}$ una successione. Se:
- $a_{n}$ non ammette maggioranti, allora $\limsup\limits_{n \to +\infty} a_n = +\infty$
- $a_{n}$ ammette maggioranti, allora $\limsup\limits_{n \to +\infty} a_n = \inf \{ M \in \mathbb{R} : a_{n} \leq M \text{ definitivamente} \}$

Il liminf è definito analogamente con $-\infty$ e i minoranti.

# Confronto a 2
Siano $a_{n}$ e $b_{n}$ due successioni. Se $a_{n} \leq b_{n}$ definitivamente, allora:
1. $\liminf\limits_{n \to +\infty} a_n \leq \liminf\limits_{n \to +\infty} b_{n}$
2. $\limsup\limits_{n \to +\infty} a_n \leq \limsup\limits_{n \to +\infty} b_{n}$

~={cyan}DIMOSTRAZIONE=~: Confronto coi limiti di $S_{n}^a$, $S_{n}^b$, $I_{n}^a$ e $I_{n}^b$.

# Confronto a 3
Siano $a_{n} \leq b_{n} \leq c_{n}$ definitivamente. Allora $\liminf\limits_{n \to +\infty} a_n \leq \liminf\limits_{n \to +\infty} b_{n} \leq \limsup\limits_{n \to +\infty} b_{n} \leq \limsup\limits_{n \to +\infty} c_{n}$

~={pink}DIMOSTRAZIONE=~: Definizione e confronto.

# Teorema delle sottosuccessioni
Sia $a_{n}$ una successione e $a_{n_{k}}$ una sua sottosuccessione.
Allora $\liminf\limits_{n \to +\infty} a_n \leq \liminf\limits_{n \to +\infty} a_{n_{k}} \leq \limsup\limits_{n \to +\infty} a_{n_{k}} \leq \limsup\limits_{n \to +\infty} a_n$

~={pink}DIMOSTRAZIONE=~: Definizione e presentazione per maggioranti.

# Presentazione via maxlim
Si pongono $\text{maxlim } a_n$ e $\text{minlim } a_n$ come il massimo e minimo limite possibile per una sottosuccessione di $a_{n}$ in $\overline{\mathbb{R}}$.

Valgono:
- $\text{maxlim } a_n = \limsup\limits_{n \to +\infty} a_n$
- $\text{minlim } a_n = \liminf\limits_{n \to +\infty} a_n$

~={cyan}DIMOSTRAZIONE=~:
1. $\text{maxlim } a_n \leq \limsup\limits_{n \to +\infty} a_n$
2. Verifichiamo che ogni sottosuccessione tenda a $\text{maxlim } a_n$
	- $\limsup\limits_{n \to +\infty} a_n = -\infty \implies a_{n} \to -\infty$
	- $\limsup\limits_{n \to +\infty} a_n = +\infty \implies$ $a_{n_{k}} \to +\infty$ per caratterizzazione
	- $\limsup\limits_{n \to +\infty} a_n = L \in \mathbb{R} \implies a_{n_{k}} \to L$ per caratterizzazione

# Criterio della radice e/o rapporto
Sia $a_{n}$ una successione con $a_{n} \geq 0$ definitivamente:
- $\liminf\limits_{n \to +\infty} \sqrt[n]{ a_{n} } > 1 \implies a_{n} \to +\infty$
- $\limsup\limits_{n \to +\infty} \sqrt[n]{ a_{n} } < 1 \implies a_{n} \to 0$   e   $\sum\limits_{n=0}^{\infty} a_n$ converge

~={cyan}DIMOSTRAZIONE=~: Caratterizzazione.

Sia $a_{n}$ una successione con $a_{n} > 0$ definitivamente:
- $\liminf\limits_{n \to +\infty} \frac{a_{n+1}}{a_{n}} > 1 \implies a_{n} \to +\infty$
- $\limsup\limits_{n \to +\infty} \frac{a_{n+1}}{a_{n}}<1 \implies a_{n} \to 0$   e   $\sum\limits_{n=0}^{\infty} a_n$ converge

~={cyan}DIMOSTRAZIONE=~: Caratterizzazione.

Sia $a_{n}$ una successione con $a_{n} > 0$ definitivamente.
Allora $\liminf\limits_{n \to +\infty} \frac{a_{n+1}}{a_{n}} \leq \liminf\limits_{n \to +\infty} \sqrt[n]{ a_{n} } \leq \limsup\limits_{n \to +\infty} \sqrt[n]{ a_{n} } \leq \limsup\limits_{n \to +\infty} \frac{a_{n+1}}{a_{n}}$

~={cyan}DIMOSTRAZIONE=~: Caratterizzazione.

# Teoremi algebrici
$\liminf\limits_{n \to +\infty} a_n + \liminf\limits_{n \to +\infty} b_{n} \leq \liminf\limits_{n \to +\infty} (a_n + b_{n}) \leq \limsup\limits_{n \to +\infty} (a_n+b_{n}) \leq \limsup\limits_{n \to +\infty} a_n + \limsup\limits_{n \to +\infty} b_{n}$

~={pink}DIMOSTRAZIONE=~: Definizione con $S_{n}$ e passaggio al limite.

Se $\limsup\limits_{n \to +\infty} a_n$ esiste, allora per ogni successione $b_{n}$ valgono:
- $\limsup\limits_{n \to +\infty} (a_n+b_{n}) = \lim\limits_{n \to +\infty} a_{n} + \limsup\limits_{n \to +\infty} b_{n}$
- $\liminf\limits_{n \to +\infty} (a_n+b_{n}) = \lim\limits_{n \to +\infty} a_{n} + \liminf\limits_{n \to +\infty} b_{n}$

~={cyan}DIMOSTRAZIONE=~:
- $\leq$ segue dal caso generale
- $\geq$ basta esibire $n_{k}$ tgale che $a_{n_{k}}+b_{n_{k}} \to \lim\limits_{n \to +\infty} a_{n}+\limsup\limits_{n \to +\infty} b_{n}$

Valgono:
- $\limsup\limits_{n \to +\infty} (-a_n) = -\liminf\limits_{n \to +\infty} a_n$
- $\liminf\limits_{n \to +\infty} (-a_n) = -\limsup\limits_{n \to +\infty} a_n$

# Limsup di una funzione
Sia $f:D\to \mathbb{R}$ una funzione con $D \subseteq \mathbb{R}$ e $I_{x_{0},\delta} \neq \emptyset$   $\forall\delta>0$.
- Se $\forall \delta>0$   $\sup \{ f(x):x \in I_{x_{0},\delta} \} = +\infty$ allora per definizione $\limsup\limits_{x \to x_{0}} f(x) = +\infty$
- In caso contrario $\limsup\limits_{x \to x_{0}} f(x)=\lim\limits_{\delta \to 0^+} \sup \{ f(x) : x \in I_{x_{0},\delta} \} \in R \cup \{ -\infty \}$

Il liminf è definito analogamente.

$\limsup\limits_{x \to x_{0}} f(x) = +\infty \iff \exists x_{n} \to x_{0}$ con $x_{n} \in D$ e $x_{n} \neq x_{0}$ per ogni $n$ tale che $f(x_{n}) \to +\infty$

~={green}DIMOSTRAZIONE=~:
- ($\impliedby$) $\forall \delta>0$   $\sup \{ f(x) : x \in I_{x_{0},\delta} \} = +\infty$
- ($\implies$) Ipotesi con $\delta = \frac{1}{n}$, poi per confronto $x_{n}\to x_{0}$ e $f(x_{n}) \to +\infty$

# Dimostrazione di un limsup
L'idea è di limitare dall'alto con una disuguaglianza, dal basso con una sottosuccessione.