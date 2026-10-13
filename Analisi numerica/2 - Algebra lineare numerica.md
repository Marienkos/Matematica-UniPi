# Teoremi di Gershgorin
Sia $A \in \mathbb{C}^{n\times n}$ e $\lambda$ un suo autovalore. Se $x_{h}$ è una coordinata di modulo massimo di un autovettore $v$ relativo a $\lambda$, allora $\lambda \in K_{h}$.

DIMOSTRAZIONE: Si pone $Av = \lambda v$ e si sostituiscono i prodotti tra matrici.

Se esistono famiglie di cerchi Gershgorin disgiunte, l'unione dei cerchi di ogni famiglia contiene esattamente tanti autovalori quanti i cerchi nella famiglia.

DIMOSTRAZIONE:
1. Si pone $A(t)=D + t(A - D)$
2. $A(0)=D$ e $A(1) = A$
3. $A(t)$ continuo in $t$
4. Gli autovalori di $A(t)$ al variare di $t$ non possono uscire dai cerchi di Gershgorin

Una matrice si dice irriducibile se non esiste una base nella quale è triangolare a blocchi.

$A$ irriducibile $\iff$ grafo associato ad $A$ fortemente connesso.

DIMOSTRAZIONE: Permutazioni e grafi.

Sia $\lambda$ un autovalore di $A$ tale che $\lambda \in K_{i} \implies \lambda \in \partial K_{i}$. Allora $A$ irriducibile $\implies \lambda \in \bigcap\limits_{i \in I} \partial K_{i}$.

DIMOSTRAZIONE: Teorema precedente.

Gli ovali di Cassini sono delle estensioni più forti dei cerchi di Gershgorin.

# Forma normale di Schur
$\forall A\in \mathbb{C}^{n\times n}$   $\exists T$ triangolare superiore   $\exists U$ unitaria   $U^H AU = T$.

DIMOSTRAZIONE: Induzione sulla taglia di $A$.

$T \in \mathbb{R}^{n\times n}$ si dice quasi triangolare se è triangolare con numeri reali o blocchi $2\times 2$ con coppie di autovalori complessi coniugati.

$\forall A \in \mathbb{R}^{n\times n}$   $\exists T$ quasi triangolare superiore   $\exists Q$ ortogonale   $Q^T A Q = T$.g 

# Norma matriciale
Una norma matriciale è una funzione $||\cdot|| : \mathbb{C}^{n\times n} \to \mathbb{R}$ tale che:
1. $||A|| \geq 0$
2. $||A|| = 0 \iff A = 0$
3. $||\lambda A||=|\lambda| \, ||A||$
4. $||A+B|| \leq ||A|| + ||B||$
5. $||AB||\leq ||A|| \cdot ||B||$

La norma di Frobenius $||A||_{F}= \text{tr}(A^HA)^{1/2}$ è una norma matriciale.

Siano $||\cdot||$ norma su $\mathbb{C}^n$ e $S = \{ x \in \mathbb{C}^n : ||x||=1 \}$, allora:
1. $\forall A \in \mathbb{C}^{n\times n}$   $\exists \max\limits_{x \in S} ||Ax||$
2. $||\cdot||$ induce la norma matriciale $||A||=\max\limits_{||x||=1}||Ax||$

La norma precedente equivale a $||A||=\max\limits_{x \in \mathbb{C}^n \setminus \{ 0 \}} \frac{||Ax||}{||x||}$.

In questo corso si indicherà con NMI la norma matriciale indotta.

Si definisce il raggio spettrale $\rho(A)=\max\{ |\lambda| : Ax=\lambda x \}$.

Siano $x \in \mathbb{C}^n$ e $A \in \mathbb{C}^{n\times n}$, allora:
- $||x||_{1}$ induce $||A||_{1} = \max\limits_{j = 1,\dots,n} \sum\limits_{i=1}^{n} |a_{ij}|$
- $||x||_{\infty}$ induce $||A||_{\infty} = \max\limits_{i = 1,\dots,n} \sum\limits_{j=1}^{n} |a_{ij}|$
- $||x||_{2}$ induce $||A||_{2} = \rho(A^HA)^{1/2}$

DIMOSTRAZIONE (Norma 1):
1. $||x||_{1} = \sum\limits_{i=1}^{n} |x_{i}|$
2. $||Ax||_{1}=\sum\limits_{i=1}^{n} \left | \sum\limits_{j=1}^{n} a_{ij}x_{j}\right| \leq \sum\limits_{i=1}^{n} \sum\limits_{j=1}^{n} |a_{ij}|\cdot |x_{j}| \leq \sum\limits_{j=1}^{n} |x_{j}| \sum\limits_{i=1}^{n} |a_{ij}| \leq 1 \cdot \max\limits_{h} \sum\limits_{i=1}^{n} |a_{ih}|$
3. Sia $x \in \mathbb{R}^n_{+}$ tale che $||Ax||_{1} = \max\limits_{h} \sum\limits_{i=1}^{n} |a_{ih}|$
4. Sia $l$ tale che $\sum\limits_{i=1}^{n} |a_{il}| = \max\limits_{h} \sum\limits_{i=1}^{n} |a_{ih}|$
5. $x = e_{l} \implies ||Ax||_{1}$ come definita

DIMOSTRAZIONE: (Norma infinito): Analoga alla norma 1.

DIMOSTRAZIONE: (Norma 2):
1. $||x||^2_{2} = \sum\limits_{i} |x_{i}|^2 = x^Hx$
2. $||Ax||^2_{2} = x^HA^HAx = x^HU(U^HA^HAU)U^Hx = y^HDy = \sum\limits_{i=1}^{n} |y_{i}|^2\lambda_{i} \leq 1\cdot\rho(A^HA)$
3. Sia $x \in \mathbb{C}^n$ tale che $||x||_{2}=1$ e $A^HAx = \rho(A^HA)x$
4. $||Ax||_{2} = \rho(A^HA)^{1/2}$

# Raggio spettrale
Sia $||\cdot||$ NMI, allora $\rho(A)\leq ||A||$.

DIMOSTRAZIONE: $||Ax||=||\lambda x||=|\lambda| \cdot ||x|| \leq ||A|| \cdot ||x|| \implies |\lambda| \leq ||A||$   $\forall \lambda \in  \{ n : Ax = nx \}$.

Sia $||\cdot||$ su $\mathbb{C}^n$, $A,S \in C^{n \times n}$ con $\det S \neq 0$ e $||x||_{S}:=||Sx||$, allora $||A||_{S} = ||SAS^{-1}||$.

DIMOSTRAZIONE: $||A||_{S} = \max\limits_{||x||_{S}=1} ||Ax||_{S} = \max\limits_{||Sx||=1}||SAx|| = \max\limits_{||y||=1}||SAS^{-1}y|| = ||SAS^{-1}||$.

Siano $S$ matrice tale che $\det S \neq 0$ e $||\cdot||$ vettoriale, allora $A \to ||SAS^{-1}||$ NMI.

$\forall\varepsilon > 0$   $\forall A \in \mathbb{C}^{n\times n}$   $\exists$NMI $||\cdot||$   $||A|| \leq \rho(A)+\varepsilon$.

DIMOSTRAZIONE:
1. Sia $W = \mathbb{C}^{n\times n}$ con $\det W \neq 0$ e $A = WJW^{-1}$
2. $||W^{-1}AW||_{\infty} = ||J||_{\infty} = \max\limits_{i}||J_{i}||_{\infty} \leq \max\limits_{i}(|\lambda_{i}|+1) = \rho(A)+1$
3. Sia $J_{\varepsilon} = D_{\varepsilon}^{-1}JD_{\varepsilon}$ con $D_{\varepsilon}$ matrice diagonale con $\varepsilon^0,\dots,\varepsilon^{n-1}$
4. $J_{\varepsilon}$ ha sulla diagonale $J_{1,\varepsilon}$ con $J_{k,\varepsilon}$ blocco con $\varepsilon$ anziché $1$
5. $||B|| := ||D_{\varepsilon}^{-1}W^{-1}BWD_{\varepsilon}||_{\infty}$ infatti $||A|| = ||J_{\varepsilon}||_{\infty} \leq \rho(A)+\varepsilon$

Se per gli autovalori $\lambda$ di $A$ tali che $|\lambda| = \rho(A)$ vale $\lambda \in J^1$, allora $\rho(A) = ||A||$.

DIMOSTRAZIONE: Come prima, si fissa 𝜀 piccolo tale che $|\lambda_{k}|<\rho(A) \implies ||J_{k,\varepsilon}||_{\infty}<\rho(A)$.

$\forall A \in \mathbb{C}^{n\times n}$   $\forall ||\cdot||$ matriciale   $\lim\limits_{k \to +\infty} ||A^k||^{1/k} = \rho(A)$.

DIMOSTRAZIONE:
1. $\exists \lim\limits_{k \to +\infty} ||A^k||^{1/k}=l$ per una norma opportuna, esiste per tutte
2. Per equivalenza delle norme $\exists \alpha,\beta$   $\alpha ||B|| \leq ||B||' \leq \beta ||B||$   $\forall B \in \mathbb{C}^{n\times n}$
3. $\alpha ||A^k||\leq ||A^k||' \leq \beta ||A^k||$ e al limite si equivalgono per confronto

Se $\exists ||\cdot||$ NMI tale che $||A|| < 1$, allora $\det (I+A) \neq 0$ e $||(I+A)^{-1}|| \leq \frac{1}{1 - ||A||}$.

_- - - Lezione del 12 ottobre da recuperare - - -_