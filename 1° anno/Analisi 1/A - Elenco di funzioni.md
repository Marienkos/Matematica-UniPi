# Funzioni elementari
Potenza: $f_k(x) = x^k$
- pari
- bigettiva su opportuni intervalli
- invertibile con la radice

Valore assoluto: $f(x) = |x|$
- pari
- vale $|x+y| \leq |x| + |y|$
- vale $\big||x| - |y|\big| \leq |x-y|$

Esponenziale: $f_a(x) = a^x$
- strettamente crescente
- bigettiva ovunque
- invertibile col logaritmo
- unica se definita con i seguenti assiomi:
	- $f_a(x+y) = f_a(x)f_a(y)$
	- $f_a(1) = a$
	- non implode in $\mathbb R$

Seno: $f(x) = \sin x$
- dispari
- periodica con periodo minimo $2\pi$
- strettamente crescente e bigettiva su opportuni intervalli
- invertibile con l'arcoseno

Coseno: $f(x) = \cos x$
- pari
- periodica con periodo minimo $2\pi$
- strettamente decrescente e bigettiva su opportuni intervalli
- invertibile con l'arcocoseno

Tangente: $f(x) = \tan x$
- dispari
- periodica con periodo minimo $\pi$
- strettamente crescente e bigettiva su opportuni intervalli
- invertibile con l'arcotangente

# Funzioni iperboliche
Seno iperbolico: $f(x) = \sinh x = \frac{{e^x - e^{-x}}}{2}$
- dispari
- strettamente crescente e bigettiva ovunque
- invertibile col settorseno iperbolico

Coseno iperbolico: $f(x) = \cosh x = \frac{{e^x + e^{-x}}}{2}$
- pari
- strettamente crescente e bigettiva sui positivi
- invertibile col settorcoseno iperbolico

Tangente iperbolica: $f(x) = \tanh x$
- dispari
- strettamente crescente e bigettiva ovunque
- invertibile con la settortangente iperbolica

# Funzioni utili
Delta di Dirac (o, come la chiamo io, delta i-j): $f(x) = \delta_{i,j}$
- $f(x) = 1$ se $i = j$
- $f(x) = 0$ se $i \neq j$

# Funzioni strane
Dato $\mathbb{R}$ spazio vettoriale su $\mathbb{Q}$, esiste una base più che numerabile $\{ v_{1},v_{2},\dots \}$. Allora ogni $x \in \mathbb{R}$ si può scrivere come $x = c_{1}v_{1} + c_{2}v_{2} + \dots$ Considero:
1. $f_{1}(x)=c_{1}v_{1}$ periodica di $v_{2}$
2. $f_{2}(x)=x-f_{1}(x)$ periodica di $v_{1}$
3. $f_1(x)+f_{2}(x)=x$