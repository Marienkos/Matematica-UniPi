# Disuguaglianza di Bernoulli
Vale $(1+x)^n \geq 1+nx$

DIMOSTRAZIONE: Induzione.

# Prodotto di Wallis
$W_{n} := \sum\limits_{k=1}^{n} \frac{2k}{2k-1} \frac{2k}{2k+1} \to \frac{\pi}{2}$

DIMOSTRAZIONE:
1. Dato $I_{n} := \int_{0}^{\pi} \sin^nx \, dx$ si può dimostrare $I_{n}= \frac{{n-1}}{n}I_{n-2}$
2. Pongo $\hat{R}_{n} := \frac{I_{2n+1}}{I_{2n}}$ e osservo $\hat{R}_{n}=W_{n} \frac{2}{\pi}$ per integrazione e induzione
3. Per confronto a 3 tra $\frac{2n}{2n+1}$ e $1$ si ha $\hat{R}_{n}\to 1$

# Asintotica di $I_{n}$
$I_{n} \sim \frac{\sqrt{ 2\pi }}{\sqrt{ n }}$

DIMOSTRAZIONE: Si dimostra separatamente sui pari e sui dispari.

# Formula di Stirling
Valgono $n! \sim \left( \frac{n}{e} \right)^n \sqrt{ 2\pi n }$ e $n! \geq \left( \frac{n}{e} \right) \sqrt{ 2\pi n }$

DIMOSTRAZIONE:
1. Dato $S_{n} := \frac{n^n}{e^n}\sqrt{ n } \frac{1}{n!}$ la tesi equivale a $S_{n} \to \frac{1}{\sqrt{ 2\pi }}$ e $S_{n} \leq \frac{1}{\sqrt{ 2\pi }}$
2. Dimostriamo che $S_{n} \to S_{\infty} \in (0,+\infty)$
	1. Pongo $R_{n}=\frac{S_{n+1}}{S_{n}} = \frac{1}{e}\left( 1+ \frac{1}{n} \right)^{n+ \frac 1 2}$
	2. Osservo che $S_{n}=S_{1} \prod\limits_{k=1}^{n-1} R_{k}$
	3. $\sum\limits_{k=1}^{\infty} \log R_{k}$ converge per confronto asintotico $\iff \prod\limits_{k=1}^{n-1} R_{k}$ converge
3. $S_{n}$ crescente $\iff R_{n}>1 \iff \log R_{n}>0 \iff \left( n+\frac{1}{2} \right)\log\left( 1+\frac{1}{n} \right)>0$   $\forall n$
	- Controllo che in funzione di $n$ sia decrescente
	- Considero $g(x)=\log x$ e stimo l'integrale
4. $W_{n} = \frac{[2^nn!]^4}{(2n+1)[(2n)!]^2}$ per induzione
5. Nella formula di Wallis sostituisco con $S_{n}$ e ottengo $S_{\infty}=\frac{1}{\sqrt{ 2\pi }}$

# Integrale di Gauss
$\int_{-\infty}^{+\infty} e^{-x^2} \, dx = \sqrt{ \pi }$

DIMOSTRAZIONE:
1. $1-x \leq e^{-x} \leq \frac{1}{1+x}$   $\forall x\geq 0$
2. Uso lo step precedente con $x = t^2 \geq 0$
3. Elevo alla $n$, integro e moltiplico per $\sqrt{ n }$
4. $\sqrt{ n }I_{2n+1} \leq \int_{-\sqrt{ n }}^{\sqrt{ n }} e^{-x^{2}} \, dx \leq \sqrt{ n }I_{2n-2}$

# Serie dei reciproci dei primi
Sia $P=\{ \text{numeri primi} \}$. Allora $\sum\limits_{p \in P}^{\infty} \frac{1}{p}$ diverge.

DIMOSTRAZIONE (Erdős):
1. Supponiamo converga, allora $\exists k$   $\sum\limits_{i\geq k+1} \frac{1}{p_{i}}\leq \frac{1}{2}$
2. Sia $A_{n}=\{ i \in {1,\dots,n} : i \text{ ha solo fattori in } \{ p_{1},\dots,p_{k} \} \}$
3. Sia $B_{n}=\{ i \in {1,\dots,n} : i \text{ ha solo fattori in } \{ p_{k+1},\dots \} \}$
4. $n = \#A_{n} + \#B_{n}$
5. Ogni $p_{i}^{a_{i}} \in A_{n}$ ha $a_{i} \leq \log_{p_{i}}n \leq \log_{2}n$, quindi $\# A_{n} \leq (\log_{2}n)^k$
6. $B_{n}=\bigcup\limits_{j\geq k+1}$elementi divisibili per $p_{i}$, quindi $\# B_{n} \leq \sum\limits_{i\geq k+1} \frac{n}{p_{i}} = n\sum\limits_{i\geq k+1} \frac{1}{p_{i}} \leq \frac{1}{2}$

# Irrazionalità di e
Sia $e = \sum\limits_{n=0}^{\infty} \frac{1}{n!}$. Tale numero è irrazionale.

DIMOSTRAZIONE:
1. Supponiamo $e = \frac{a}{b}$ con $a,b \in \mathbb{Z}$, vale $e = \sum\limits_{n=0}^{b} \frac{1}{n!}+\sum\limits_{n\geq b+1} \frac{1}{n!}$
2. $a(b-1)! = b!\sum\limits_{n=0}^{b} \frac{1}{n!} + b!\sum\limits_{n\geq b+1} \frac{1}{n!} \implies b!\sum\limits_{n\geq b+1} \frac{1}{n!}$ intero
3. Stimiamo la serie dall'alto con $b!\sum\limits_{n=1}^{\infty} \frac{1}{(b+n)!}=\frac{1}{b} < 1$, ossia $0<b<1$, assurdo
4. Se $b=1$, abbiamo già dimostrato che $2 < e < 3$, ossia $e \not\in \mathbb{Z}$, assurdo