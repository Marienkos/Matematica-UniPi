# Integrale proprio
Sia $[a,b]$ un intervallo limitato, detto zona d'integrazione, e $f : [a,b] \to \mathbb{R}$ una funzione limitata, detta funzione integranda. Allora si può calcolare l'integrale proprio, la cui notazione è $\int_{a}^{b} f(x) \, dx$

Sia $D \subseteq \mathbb{R}$ un insieme limitato e $f : D \to \mathbb{R}$ una funzione limitata. Allora la notazione è $\int_{D} f(x) \, dx$

Valgono, per definizione:
- $\int_{a}^{a} f(x) \, dx = 0$
- $\int_{a}^{b} f(x) \, dx = -\int_{b}^{a} f(x) \, dx$

Si nota che l'integrale indica geometricamente l'area con segno del sottografico.

# Integrale di Darboux (inclusiva)
Sia $f(x) = \lambda$ in tutto $[a,b]$. Allora $\int_{a}^{b} f(x) \, dx = \lambda(b-a)$

La funzione caratteristica di un intervallo è la funzione che vale 1 nell'intervallo, 0 fuori.

Una step function è una combinazione lineare di funzioni caratteristiche.

Sia $f(x)$ step function, ossia valgono:
1. esista una suddivisione $a=x_{0}<x_{1}<\dots<x_{n}=b$ di $[a,b]$
2. $\exists\lambda_{1},\dots,\lambda_{n}$   $f(x) = \lambda_{i}$   $\forall x \in (x_{i-1}, x_{i})$
Allora $\int_{a}^{b} f(x) \, dx = \sum\limits_{i=1}^{n} \lambda_{i}(x_{i}-x_{i-1})$

Valgono:
- se due combinazioni lineari di funzioni caratteristiche danno la stessa step function, allora l'integrale è lo stesso
- siano $f(x)$ e $g(x)$ step function, allora vale $f(x) \geq g(x)$   $\forall x \in[a,b] \implies \int_{a}^{b} f(x) \, dx \geq \int_{a}^{b} g(x) \, dx$

Sia $f : [a,b] \to \mathbb{R}$ limitata, si definiscono:
- integrale superiore $I^+(f) = \inf \left\{  \int_{a}^{b} \psi(x) \, dx : \psi \text{ step function}, \psi(x) \geq f(x) \, \forall x \in [a,b]  \right\}$
- integrale inferiore $I^-(f) = \sup \left\{  \int_{a}^{b} \psi(x) \, dx : \psi \text{ step function}, \psi(x) \leq f(x) \, \forall x \in [a,b]  \right\}$

Vale $I^+(f) \leq I^-(f)$

DIMOSTRAZIONE: somme inferiori $\psi^-$ $\leq$ somme superiori $\psi^+$

Se $I^-(f) = I^+(f)$, allora $f$ è detta integrabile secondo Riemann.

# Criterio di integrabilità
$f:[a,b] \to \mathbb{R}$ è integrabile $\iff$ $\forall \varepsilon>0$   $\exists \varphi,\psi$ step function tali che:
- $\varphi(x)\leq f(x)\leq \psi(x)$   $\forall x \in[a,b]$
- $\int_{a}^{b} (\psi(x)-\varphi(x)) \, dx \leq \varepsilon$

DIMOSTRAZIONE: Caratterizzazione di inf e sup.

Almeno le seguenti funzioni sono integrabili:
- monotone
- continue
- continue tranne in un numero finito di punti

DIMOSTRAZIONE (Monotone):
1. Supponiamo:
	- $f$ debolmente crescente
	- $[a,b]$ diviso in parti uguali lunghi $\frac{{b-a}}{n}$
	- $\psi(x) = f(x_{i})$   $\forall x \in (x_{i-1}, x_{i})$
	- $\varphi(x) = f(x_{i-1})$   $\forall x \in (x_{i-1}, x_{i})$
2. Per crescenza $\varphi(x) \leq f(x) \leq \psi(x)$   $\forall x \in [a,b]$
3. $\int_{a}^{b} (\psi(x)-\varphi(x)) \, dx = \sum\limits_{i=1}^{n} \left( \frac{{b-a}}{n} \right)(f(x_{i})-f(x_{i-1})) = \frac{{b-a}}{n}(f(b)-f(a))$
4. Fissato $\varepsilon$, con $n$ grande l'integrale diventa $\leq \varepsilon$

# Integrale di Darboux (ortodossa)
Sia $f : \mathbb{R}\to \mathbb{R}$ limitata e nulla fuori da un intervallo $[a,b]$. Sia $x_{0}<\dots<x_{n}$ una partizione $P$.

Si definiscono:
- $S_{DO}^+(f,P) := \sum\limits_{i=1}^{n} (x_{i}-x_{i-1})\sup \{ f(t) : t \in [x_{i-1},x_{i}] \}$
- $S_{DO}^-(f,P) := \sum\limits_{i=1}^{n} (x_{i}-x_{i-1})\inf \{ f(t) : t \in [x_{i-1},x_{i}] \}$
- $I_{DO}^+(f) := \inf \{ S_{DO}^+(f,P) : P \text{ partizione} \}$
- $I_{DO}^-(f) := \sup \{ S_{DO}^-(f,P) : P \text{ partizione} \}$

# Integrale di Riemann
Si dice diametro di una partizione $P$ il numero $\text{diam}(P) := \text{max}\{ x_{i}-x_{i-1} : i = 1,\dots,n \}$.

Si dice partizione taggata e si indica con $(P,T)$ una partizione e una scelta di punti $T=(t_{1},\dots,t_{n})$ con $t_{i} \in [x_{i-1},x_{i}]$.

Data $(P,T)$ si dice somma di Riemann $S_{R}(P,T) := \sum\limits_{i=1}^{n} (x_{i}-x_{i-1})f(t_{i})$.

Si dice $f$ integrabile secondo Riemann se:
- $\exists I \in \mathbb{R}$   $\forall\varepsilon >0$   $\exists\delta>0$   $\forall(P,T)$   $\text{diam}(P)\leq\delta \implies |I-S_{R}(P,T)| \leq \varepsilon$

Sia $f : \mathbb{R} \to \mathbb{R}$ limitata e non nulla in un intervallo $[a,b]$. Allora le definizioni sono equivalenti.

DIMOSTRAZIONE (Darboux inclusiva $\iff$ Darboux ortodossa):
1. $S_{DI}^+(f) \leq S_{DO}^+(f)$ facendo inf
2. $S_{DO}^+(f) \leq S_{DI}^+(f)$ con osservazioni su partizione e altezze

DIMOSTRAZIONE (Riemann $\implies$ Darboux ortodossa):
1. Sia $I$ l'integrale di Riemann, serve $\forall \varepsilon>0$   $\exists P$   $S_{DO}^+(f,P) \leq I + \varepsilon$   $S_{DO}^-(f) \geq I - \varepsilon$
2. Per $P$ con $\text{diam}(P) \leq \delta$, vale $\forall T$   $I-\varepsilon \leq S_{R}(P,T) \leq I+\varepsilon$
3. Scegliendo opportuni $t_{i}$ si raggiunge la tesi

DIMOSTRAZIONE (Darboux inclusiva $\implies$ Riemann):
1. $\forall\varepsilon>0$   $\exists\varphi(x) \leq f(x) \leq \psi(x)$   $\int \psi(x) \, dx \leq I+\frac{1}{2}\varepsilon$   $\int \varphi(x) \, dx\geq I - \frac{1}{2}\varepsilon$
2. Assumiamo wlog $\varphi$ e $\psi$ limitate in $[-M,M]$ e definite sulla stessa partizione $Q$
3. Consideriamo $\delta \leq \text{diam}(Q)$ e $\delta = \frac{1}{(m+1)(M+1)} \frac{1}{4}\varepsilon$
4. Siano gli intervalli $[x_{i-1},x_{i}]$ detti:
	- interni ($\in Int$) se totalmente compresi in un intervallo di $Q$
	- a cavallo ($\in Cav$) se parzialmente compresi in due intervalli di $Q$
5. $S_{R}(P,T) := \sum\limits_{i=1}^{n} (x_{i}-x_{i-1})f(t_{i}) = \sum\limits_{i \in Int} (x_{i}-x_{i-1})f(t_{i}) + \sum\limits_{i \in Cav} (x_{i}-x_{i-1})f(t_{i})$
6. Allora $S_{R}(P,T) \leq \int \psi(x) \, dx - \sum\limits_{i \in Cav} \int_{x_{i-1}}^{x_{i}} \psi(x) \, dx + (m+1)\delta M \leq I+\varepsilon$

# Proprietà delle funzioni integrabili
Siano $f,g : [a,b] \to \mathbb{R}$ integrabili e $\lambda \in \mathbb{R}$. Allora:
- $f+g$ integrabile e $\int_{a}^{b} [f(x)+g(x)] \, dx = \int_{a}^{b} f(x) \, dx + \int_{a}^{b} g(x) \, dx$
- $\lambda f$ integrabile e $\int_{a}^{b} \lambda f(x) \, dx = \lambda \int_{a}^{b} f(x) \, dx$
- $|f|$ integrabile e $|\int_{a}^{b} f(x) \, dx| \leq \int_{a}^{b} |f(x)| \, dx$
- $fg$ integrabile
- $\max \{ f,g \}$ e $\min \{ f,g \}$ integrabili

DIMOSTRAZIONE: Criterio di integrabilità.

# Additività rispetto alla zona d'integrazione
Sia $a<b<c$ e $f : [a,c] \to \mathbb{R}$ limitata e integrabile in $[a,b]$ e $[b,c]$. Allora:
- $f$ integrabile in $[a,c]$
- $\int_{a}^{c} f(x) \, dx = \int_{a}^{b} f(x) \, dx + \int_{b}^{c} f(x) \, dx$

DIMOSTRAZIONE:
- Step function
- Integrale con $f : \mathbb{R} \to \mathbb{R}$ limitate e nulle fuori da un intervallo

# Funzione integrale
Sia $f : [a,b] \to \mathbb{R}$ limitata e $x_{0} \in [a,b]$. Si dice funzione integrale $F(x) = \int_{x_{0}}^{x} f(t) \, dt$

$F(x_{0}) = 0$

DIMOSTRAZIONE: Integrale con estremi uguali.

$|f(x)| \leq M$   $\forall x \in[a,b] \implies F$ è $M$-Lipschitziana

DIMOSTRAZIONE:
1. Sia $I =|F(x_{2})-F(x_{1})|$
2. $I=|\int_{x_{1}}^{x_{2}} f(x) \, dx| \impliedby$ additività rispetto alla zona d'integrazione
3. $I\leq \int_{x_{1}}^{x_{2}} |f(x)| \, dx \impliedby$ proprietà del valore assoluto
4. $I\leq \int_{x_{1}}^{x_{2}} M \, dx \impliedby$ monotonia dell'integrale
5. $I= M(x_{2}-x_{1}) \impliedby$ caso banale
6. $I= M|x_{2}-x_{1}| \impliedby x_{2}\geq x_{1}$

$\int_{c}^{d} f(x) \, dx = F(d) - F(c)$

DIMOSTRAZIONE: Additività rispetto alla zona d'integrazione.

# Teorema della media integrale
Sia $f : [a,b] \to \mathbb{R}$ continua. Allora $\exists c \in [a,b]$   $\int_{a}^{b} f(x) \, dx = f(c)(b-a)$

DIMOSTRAZIONE:
- Weierstrass, monotonia dell'integrale e continuità
- Lagrange applicato a $F$

# Teorema fondamentale del calcolo integrale
Sia $f:[a,b] \to \mathbb{R}$ continua e $F$ la sua funzione integrale. Allora in tutto $[a,b]$:
- $F$ derivabile
- $F'(x) = f(x)$, ossia $F$ è una primitiva di $f$

DIMOSTRAZIONE:
1. Preso $x_{1} \in (a,b)$ si calcola $F'(x_{1})$
2. Per il teorema della media integrale si ha $\lim\limits_{h \to 0} \frac{{F(x_{1}+h)-F(x_{1})}}{h} = f(c(h))$
3. $x_{1} \leq c(h) \leq x_{1}+h \implies c(h) \to x$ per confronto a 3
4. $f(c(h)) \to f(x_{1})$ per continuità

# Calcolo con le primitive
Sia $f$ continua e $F_{1},F_{2}$ due primitive. Allora $\exists c \in \mathbb{R}$   $\forall x \in [a,b]$   $F_{1}(x) = F_{2}(x) + c$

DIMOSTRAZIONE: Lagrange con la differenza.

Siano $f,F : [a,b] \to \mathbb{R}$ tali che in tutto $[a,b]$:
1. $f$ continua
2. $F$ derivabile
3. $F'(x) = f(x)$
Allora $\int_{a}^{b} f(x) \, dx = [F(x)]_{a}^b = F(b)-F(a)$

DIMOSTRAZIONE:
1. La formula vale con tutte le funzioni integrali
2. Tutte le funzioni integrali sono primitive per il teorema fondamentale
3. La formula vale per tutte le funzioni primitive per la proposizione precedente

# Integrazione per parti
Siano $F,G : [a,b] \to \mathbb{R}$ di classe $C^1$ tali che:
- $F'(x) = f(x)$
- $G'(x) = g(x)$
Allora $\int_{a}^{b} f(x)G(x) \, dx = [F(x)G(x)]_{a}^b - \int_{a}^{b} F(x)g(x) \, dx$

# Integrazione per sostituzione
Sia $G'(x) = g(x)$, allora $\int_{a}^{b} f(G(x))g(x) \, dx = \int_{G(a)}^{G(b)} f(x) \, dx$

# Integrazione delle funzioni razionali
Ogni funzione razionale $f(x)=\frac{P(x)}{Q(x)}$ ammette una primitiva combinazione lineare di funzioni razionali e funzioni di tipo $\log(ax^{2}+bx+c)$ e $\arctan(ax+b)$.

La procedura è la seguente:
1. Divisione
2. Fattorizzazione
3. Decomposizione
4. Integrazione

Se $\deg(P) \geq \deg(Q)$, si fa la divisione tra polinomi e $f(x) = A(x) + \frac{R(x)}{Q(x)}$

Ogni polinomio in $\mathbb{R}$ si può fattorizzare in polinomi in $\mathbb{R}$ di grado 1 o 2.

DIMOSTRAZIONE: Teorema fondamentale dell'algebra.

Con la decomposizione in fratti semplici, $f$ si separa in frazioni tali che, dato $Q(x) = \prod Q_{i}^{n_{i}}(x)$:
- i fattori di grado 1 abbiano costanti al numeratore
- i fattori di grado 2 abbiano polinomi di grado 1 al numeratore
- $\forall Q_{i}$ compare una frazione $\forall n\leq n_{i}$, e il denominatore è $Q_{i}^n$

Con la decomposizione di Hermite, $f$ si separa in frazioni tali che, dato $Q(x) = \prod Q_{i}^{n_{i}}(x)$:
- i fattori di grado 1 abbiano costanti al numeratore
- i fattori di grado 2 abbiano polinomi di grado 1 al numeratore
- $\forall Q_{i}$ compare una frazione, ignorata la molteplicità, il cui denominatore è $Q_{i}$
- compare $\left[ \frac{N(x)}{D(x)} \right]'$ con $\deg(N) = \deg(Q)-1$ e $D(x) = \prod Q_{i}^{n_{i}-1}(x)$

La decomposizione è unica.

DIMOSTRAZIONE: Bezout.

# Sostituzioni razionalizzanti
Se nella funzione integranda compare $n^x$, si pone $y = n^x$

Se nella funzione integranda compaiono $x$ e $\sqrt{ ax+b }$, si pone $y = \sqrt{ ax+b }$. Se le radici hanno indice diverso, si sostituisce con il minimo comune multiplo degli indici.

Se nella funzione integranda compaiono $x$ e $\sqrt{ ax^2 +bx+c }$, si può:
- porre $\sqrt{ a } x+y=\sqrt{ ax^{2}+bx+c }$
- porre $y(x-\lambda) = \sqrt{ ax^{2}+bx+c }$ se $ax^{2}+bx+c$ si fattorizza come $(x-\lambda)(x-\mu)$
- notare che ogni polinomio di grado 2 si può scrivere come $\alpha + (ax+b)^{2}$

Se nella funzione integranda compaiono funzioni trigonometriche si possono usare le formule parametriche:
- $t = \tan \frac{x}{2}$
- $\sin x = \frac{2t}{1+t^{2}}$
- $\cos x = \frac{{1-t^{2}}}{1+t^2}$

# Simmetrie
Se $f$ è pari, allora $\int_{-a}^{a} f(x) \, dx=2\int_{0}^{a} f(x) \, dx$

DIMOSTRAZIONE:
1. Sia $I =\int_{-a}^{a} f(x) \, dx$
2. $I=F(a) - F(-a) \impliedby$ primitiva di $f$ in $[-a,a]$
3. $I = 2F(a) \impliedby$ la primitiva di una funzione pari è dispari
4. $I = 2(F(a) - F(0)) \impliedby F(0) = 0 \impliedby$ ogni funzione dispari è nulla all'origine
5. $I = 2\int_{0}^{a} f(x) \, dx \impliedby$ primitiva di $f$ in $[0,a]$

Se $f$ è dispari, allora $\int_{-a}^{a} f(x) \, dx = 0$

DIMOSTRAZIONE:
1. Sia $I = \int_{-a}^{a} f(x) \, dx$
2. $I = F(a) - F(-a) \impliedby$ primitiva di $f$ in $[-a,a]$
3. $I = F(a) - F(a) = 0 \impliedby$ la primitiva di una funzione dispari è pari