# Serie numeriche
Data una successione $a_{n}$ si definisce la somma parziale come $S_{n}=\sum\limits_{k=0}^{n} a_k$

Una serie è $\sum\limits_{n=0}^{\infty} a_n = \lim\limits_{n \to +\infty} S_{n}$ e può essere:
- $l \in \mathbb{R}$ e si dice che la serie converge a $l$
- $+\infty$ e si dice che la serie diverge a $+\infty$
- $-\infty$ e si dice che la serie diverge a $-\infty$
- non esistente e si dice che la serie è indeterminata

Siano $a_{n}$ e $\hat{a}_{n}$ due successioni tali che $a_{n} = \hat{a}_{n}$ definitivamente. Allora le serie hanno lo stesso comportamento.

DIMOSTRAZIONE: Hp $\implies$ $S_{n} - \hat{S}_{n}$ costante $\implies$$\lim\limits_{n \to +\infty} S_{n}$ si comporta come $\lim\limits_{n \to +\infty} \hat{S}_{n}$

Una serie $\sum\limits_{n=0}^{\infty} a_n$ si dice telescopica se $a_{n} = b_{n+1}-b_{n}$ o viceversa.

Valgono:
- $\sum\limits_{n=0}^{\infty} (a_{n} + b_{n}) = \sum\limits_{n=0}^{\infty} a_n+\sum\limits_{n=0}^{\infty} b_{n}$ tranne nei punti problematici
- $\sum\limits_{n=0}^{\infty} \lambda a_{n} = \lambda \sum\limits_{n=0}^{\infty} a_n$

# Condizione necessaria
$\sum\limits_{n=0}^{\infty} a_n$ converge $\implies$ $a_{n} \to 0$

DIMOSTRAZIONE: Sia $S_{n} \to l \in \mathbb{R}$. Allora $a_{n} = S_{n} - S_{n-1} \to l-l=0$

Se $a_{n} \geq 0$, la serie converge o diverge a $+\infty$

DIMOSTRAZIONE: $S_{n}$ è definitivamente debolmente crescente, dunque tende a $l\in \mathbb{R}$ o $+\infty$

# Confronto a 2 per serie
Sia $0 \leq a_{n} \leq b_{n}$ definitivamente, allora valgono:
- $\sum\limits_{n=0}^{\infty} a_n = +\infty \implies \sum\limits_{n=0}^{\infty} b_{n} = +\infty$
- $\sum\limits_{n=0}^{\infty} b_{n}$ converge $\implies$ $\sum\limits_{n=0}^{\infty} a_n$ converge

DIMOSTRAZIONE: Siano $S^a_{n}$ e $S^b_{n}$ le due somme parziali. Hp $\implies$ $S^a_{n} \leq S^b_{n}$   $\forall n \in \mathbb{N}$
- $S^a_{n} \to +\infty \implies S^b_{n} \to +\infty$
- $S^b_{n} \to l\in \mathbb{R} \implies S^a_{n} \to l_{1}\in \mathbb{R}$

# Criterio della radice e/o rapporto
Sia $a_{n}\geq 0$ definitivamente e $\sqrt[n]{a_{n}} \to l$
- $l>1 \implies$ la serie diverge
- $l<1 \implies$ la serie converge

Sia $a_{n}>0$ definitivamente e $\frac{a_{n+1}}{a_{n}} \to l$. Valgono le implicazioni precedenti.

DIMOSTRAZIONE (Esempio con la radice):
- $l>1 \implies a_{n} \to +\infty \implies$ manca la condizione necessaria
- $l<1 \implies a_{n} \to 0$
	1. $\sqrt[n]{a_{n}} \leq \frac{{l+1}}{2}$ definitivamente, cioè $a_{n} \leq (\frac{{l+1}}{2})^n = b_{n}$
	2. $b_{n}$ è geometrica con parametro $\in (0,1)$ $\implies \sum\limits_{n=0}^{\infty} b_{n}$ converge
	3. La serie converge per confronto con $\sum\limits_{n=0}^{\infty} b_{n}$

# Criterio del confronto asintotico
Siano $a_{n}$ e $b_{n}$ due successioni tali che:
1. $a_{n} \geq 0$ definitivamente
2. $b_{n}>0$ definitivamente
3. $\exists \lim\limits_{x \to +\infty} \frac{a_{n}}{b_{n}}=l \in \mathbb{R}^+$
Allora le due serie hanno lo stesso comportamento.

DIMOSTRAZIONE:
1. (3.) $\implies \frac{l}{4} \leq \frac{a_{n}}{b_{n}} \leq 4l$ definitivamente
2. Per due posso moltiplicare per  $b_{n}$. Dunque $\frac{l}{4}b_{n} \leq a_{n} \leq 4lb_{n}$
3. La tesi segue dal confronto

Se poniamo (3.) come $\frac{a_{n}}{b_{n}} \to +\infty$ si ha $\sum\limits_{n=0}^{\infty} b_{n} = +\infty \implies \sum\limits_{n=0}^{\infty} a_n \to +\infty$

Se poniamo (3.) come $\frac{a_{n}}{b_{n}} \to 0$ si ha $\sum\limits_{n=0}^{\infty} b_{n}$ converge $\implies$ $\sum\limits_{n=0}^{\infty} a_n$ converge.

# Criterio di condensazione di Cauchy
Sia $a_{n}$ una successione tale che:
1. $a_{n} \geq 0$ definitivamente
2. $a_{n+1} \leq a_{n}$ definitivamente
3. $a_{n} \to 0$
Allora le serie di $a_{n}$ e $2^na_{2^n}$ hanno lo stesso comportamento.

DIMOSTRAZIONE:
1. Per induzione $a_{1} + \frac{1}{2}\sum\limits_{k=1}^{n} 2^ka_{2^k} \leq \sum\limits_{k=1}^{2^n} a_k \leq a_{1} + a_{2} + \sum\limits_{k=1}^{n-1} 2^ka_{2^k}$
2. La tesi segue per confronto

# Criterio di Leibniz
Sia $\sum\limits_{n=0}^{\infty} (-1)^na_n$ tale che:
1. $a_{n} \geq 0$ definitivamente
2. $a_{n+1} \leq a_{n}$ definitivamente
3. $a_{n} \to 0$
Allora la serie converge.

DIMOSTRAZIONE:
1. (2.) $\implies S_{2n+2} = S_{2n} - a_{2n+1} + a_{2n+2} \leq S_{2n}$
2. $S_{2n} \geq S_{2m+1}$   $\forall n,m \in \mathbb{N}$
3. $S_{2n}$ è debolmente decrescente e limitata inferiormente $\implies S_{2n} \to l_{1}$
4. $S_{2n+1}$ è debolmente crescente e limitata superiormente $\implies S_{2n+1} \to l_{2}$
5. $S_{2n+1} = S_{2n} - a_{2n+1} \implies l_{1} = l_{2}$
6. $S_{n} \to l_{1}=l_{2}$

# Confronto a 3 per serie
Siano $a_{n}$, $b_{n}$ e $c_{n}$ tre successioni tali che:
1. $a_{n} \leq b_{n} \leq c_{n}$ definitivamente
2. $\sum\limits_{n=0}^{\infty} a_n$ e $\sum\limits_{n=0}^{\infty} c_{n}$ convergono
Allora $\sum\limits_{n=0}^{\infty} b_{n}$ converge

DIMOSTRAZIONE:
1. $\sum\limits_{n=0}^{\infty} (c_{n}-a_{n})$ converge in quanto differenza di serie convergenti
2. $\sum\limits_{n=0}^{\infty} (b_{n}-a_{n})$ converge per confronto
3. $\sum\limits_{n=0}^{\infty} b_{n}$ converge perché somma di serie convergenti

# Criterio di assoluta convergenza
Una serie $\sum\limits_{n=0}^{\infty} a_n$ si dice assolutamente convergente se $\sum\limits_{n=0}^{\infty} |a_{n}|$ converge. Allora $\sum\limits_{n=0}^{\infty} a_n$ converge.

DIMOSTRAZIONE: $-|a_{n}| \leq a_{n} \leq |a_{n}|$, dunque $a_{n}$ converge per confronto a 3.

# Lemma delle due sottosuccessioni
Se $a_{n}$ ha due sottosuccessioni che
1. esauriscono tutti i termini
2. hanno lo stesso limite $l\in \mathbb{R}$
Allora $a_{n} \to l$

DIMOSTRAZIONE: Definitivamente comune a entrambe.

# Lemma di Abel
Siano $a_{n}$ e $b_{n}$ successioni e $0\leq m <n$.
Vale $\sum\limits_{k=m}^{n} a_{k+1}(b_{k+1}-b_{k}) = a_{n+1}b_{n+1}-a_{n}b_{m} - \sum\limits_{k=m}^{n} b_{k}(a_{k+1}-a_{k})$

DIMOSTRAZIONE: Espansione e telescopicità della serie.

# Criterio di Dirichlet
Sia $\sum\limits_{n=1}^{\infty} a_nb_{n}$ tale che:
- le somme parziali di $a_{n}$ sono limitate
- $b_{n}$ debolmente decrescente
- $b_{n}\to {0}$
Allora la serie converge.

DIMOSTRAZIONE: Lemma di Abel
