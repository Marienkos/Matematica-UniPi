# Fattorizzazione
Sia $Ax + b$ sistema lineare con $A \in \mathscr{M}_{n}(\mathbb{K})$ non singolare, se $A$ è:
- triangolare inferiore, può essere risolto con sostituzione in avanti
- triangolare superiore, può essere risolto con sostituzione all'indietro
- unitaria, allora $x = A^Hb$

Se $A = BC$, allora il sistema può essere riscritto come $By = b \land Cx = y$.

Le fattorizzazioni più comuni sono:
- $A = LU$ con $L$ triangolare inferiore con diagonale 1 e $U$ triangolare superiore
- $A = PLU$ con $P$ matrice di permutazione e $L,U$ come sopra
- $A = P_{1}LUP_{2}$ con $P_{1},P_{2}$ matrici di permutazione e $L,U$ come sopra
- $A = QR$ con $Q$ unitaria e $R$ triangolare superiore

Sia $\Omega \subseteq \{ 1,\dots,n \}$, la matrice con indici in $\Omega$ è detta principale.

Sia $\Omega = \{ 1,\dots,k \}$, la matrice con indici in $\Omega$ è detta principale di testa.

$\forall k=1,\dots,n-1$   $\forall S \in \mathscr{M}_{k}(\mathbb{K})$ principale di testa di $A$   $S$ invertibile   $\implies \exists!$ fatt. $LU$ di $A$.

DIMOSTRAZIONE:
1. Caso base: se $n = 1$, allora $L = (1)$ e $A = U = (a_{1,1})$
2. Passo induttivo: sia la tesi vera per $n-1$
	1. Sia $A = LU$, allora $\left(\begin{smallmatrix} A_{n-1} & b \\ {}^tc & a_{n,n} \end{smallmatrix}\right) = \left(\begin{smallmatrix} L_{n-1} & 0 \\ {}^tx & 1 \end{smallmatrix}\right) \left(\begin{smallmatrix} U_{n-1} & y \\ 0 & u_{n,n} \end{smallmatrix}\right)$
	2. Si uguagliano i blocchi
	3. $A_{n-1}$ ha sottomatrici principali non singolari, quindi $\exists L_{n-1},U_{n-1}$   $A_{n-1}=L_{n-1}U_{n-1}$
	4. $L_{n-1}$ triangolare inferiore con diagonale $1$, da cui $\det L_{n-1}=1$ e non è singolare
	5. $\exists! y = L_{n-1}^{-1}b$ e $U_{n-1}$ non è singolare da cui $\exists!{}^tx = {}^tcU_{n-1}^{-1}$
	6. $u_{n,n}$ è univocamente determinato da $u_{n,n}=a_{n,n} - {}^txy$

Le fattorizzazioni PLU e QR esistono per qualsiasi matrice.

La fattorizzazione QR non è unica.

DIMOSTRAZIONE:
1. Sia $A=QR$ fattorizzata e $D$ matrice diagonale con modulo $1$ sulla diagonale principale
2. $D$ unitaria e diagonale superiore, da cui $A = QDD^{-1}R = \hat{Q}\hat{R}$ fattorizzata
3. Infatti $\hat{Q}$ unitaria in quanto prodotto di unitarie e $\hat{R}$ triangolare superiore

Sia $A$ invertibile, allora ha fattorizzazione QR univ^ca a meno di trasformazioni mediante matrici diagonali unitarie.

DIMOSTRAZIONE:
1. Sia $A = Q_{1}R_{1}=Q_{2}R_{2}$, per invertibilità $Q_{2}^HQ_{1}=R_{2}R_{1}^{-1}$
2. La matrice a destra è triangolare superiore unitaria, dunque diagonale

# Matrice elementare
Siano $u,v \in \mathbb{C}^n$, per questa sezione $v^Hu = \sum\limits_{i=1}^{n} \bar{v}_{i}u_{i}$ numero complesso, mentre $uv^H$ fornisce una matrice $n\times n$ di elementi $u_{i}\bar{v}_{j}$.

Si dice elementare una matrice del tipo $M = I-\sigma uv^H$ con $\sigma \in \mathbb{C}$ e $u,v \in \mathbb{C}^n$.

Valgono:
1. $M$ invertibile $\iff \sigma v^Hu \neq 1$
2. $M^{-1} = I - \tau uv^H$ con $\tau =  \frac{{-\sigma}}{1-\sigma v^Hu}$

Siano $M$ elementare e $b$ vettore, allora:
- $Mb$ costa $2n+1$ moltiplicazioni e $2n-1$ addizioni
- $Mx=b$ costa $3n+2$ moltiplicazioni, $3n-1$ addizioni e una divisione

$\forall x,y \in C^n \setminus \{ 0 \}$   $\exists M$ elementare invertibile   $Mx=y$.

DIMOSTRAZIONE:
1. $(I-\sigma uv^h)x = y$ si riscrive come $\sigma u(v^Hx)=x-y$
2. Sia $v$ non ortogonale a $x$, si pone $\sigma u = \frac{x-y}{v^Hx}$
3. Si pone l'invertibilità di $M$ con $\sigma v^Hu \neq 1$, ossia $v^H\frac{x-y}{v^Hx} \neq 1$, cioè $v^Hy \neq 0$
4. Si sceglie $v$ non ortogonale né a $x$ né a $y$

# Matrice elementare di Gauss
Una matrice elementare $M$ si dice di Gauss se $u_{1}=0$ e $v = e_{1}$.

Sia $M$ elementare di Gauss, allora $M^{-1}=I+uv^H$.

$\forall x = (x_{i}) \in \mathbb{C}^n$   $x_{1} \neq 0 \implies \exists M$ elementare di Gauss   $Mx=x_{1}e_{1}$.

DIMOSTRAZIONE: Basta porre $u_{i} = \frac{x_{i}}{x_{1}}$.

# Matrice elementare di Householder
Una matrice elementare $M$ si dice di Householder se hermitiana e unitaria.

Sia $M$ elementare di HH, allora $M = I-\beta uu^H$ con $\beta=0$ oppure $\beta=\frac{2}{u^Hu}$ e $u\neq 0$.

$\forall x \in \mathbb{C}^n \setminus \{ 0 \}$   $\exists \alpha \in \mathbb{C}$   $\exists M$ elementare di HH   $Mx = \alpha e_{1}$.

DIMOSTRAZIONE:
1. $M$ unitaria $\implies M$ lascia invariata la norma 2, quindi $|\alpha| = ||x||_{2}$
2. $M$ hermitiana $\implies x^HMx \in \mathbb{R}$   $\forall x \implies x^H\alpha e_{1} = \bar{x}_{1}\alpha \in \mathbb{R}$
3. $\alpha = \theta ||x||_{2}$ con $|\theta|=1$
4. Sia $\theta$ di valore $\pm 1$ se $x_{1} = 0$, o $\pm \frac{x_{1}}{|x_{1}|}$ se $x_{1}  \neq 0$
5. Se $x_{1} = 0$ si ha $\bar{x}_{1}\alpha=0$, altrimenti $\bar{x}_{1}\alpha=\pm |x_{1}|\cdot ||x||_{2}$
6. Da $Mx=\alpha e_{1}$ si ha $(I-\beta uu^H)x = \alpha e_{1}$ e $\beta(u^Hx)u=x-\alpha e_{1}$
7. Sia $u=x-\alpha e_{1}$, da $\beta = \frac{2}{u^Hu}$ si ricava $\beta(u^Hx)=1$
8. $u$ ha componenti di $x$ tranne la prima
9. Se $x_{1}\neq 0$, allora $u_{1}=x_{1}-\alpha=x_{1} \mp \theta ||x||_{2} = x_{1}\left( 1\mp \frac{||x||_{2}}{|x_{1}|} \right)$
10. Se $x_{1} = 0$, allora $u_{1} = -\alpha = \mp ||x||_{2}$
11. Per semplicità si scelgono i segni $-$ e vale $\beta = \frac{1}{||x||_{2}^2 + |x_{1}|\cdot ||x||_{2}}$

# Fattorizzazione con matrici elementari
QUESTI APPUNTI SONO DA DEDISCORSIVIZZARE

Sia $A_{k} = \left(_{k}a_{i}^j\right)$ con riga $i$ e colonna $j$ successione di matrici definita da:
1. $A_{1}=A$
2. $A_{k+1}=M_{k}A_{k}$ 
con $M_{k}$ elementare, $A_{k} = \left(\begin{smallmatrix} T_{k} & V_{k} \\ 0 & W_{k} \end{smallmatrix}\right)$ e $T_{k}$ triangolare con $k-1$ colonne.

Per il teorema precedente $\exists M_{1}$   $M_{1}\cdot{}_{1}a^1={}_{2}a_{1}^1e_{1}$.

Sia $A_{k}$ fissata, si può costruire $M_{k}$ con $\hat{M}_{k}$ tale che $\hat{M}_{k}\cdot w^1 = \alpha e_{1}$.

QUESTI APPUNTI SONO DA COMPLETARE

# Complemento di Schur
Sia $A = \left(\begin{smallmatrix} A_{1,1} & A_{1,2} \\ A_{2,1} & A_{2,2} \end{smallmatrix}\right)$ con $A_{1,1} \in \mathscr{M}_{k}(\mathbb{K})$ invertibile. Si dice complemento di Schur di $A_{2,2}$ in $A$ la matrice $S=A_{2,2} - A_{2,1}A_{1,1}^{-1}A_{1,2}$.

Valgono $A = \left(\begin{smallmatrix} I & 0 \\ A_{2,1}A_{1,1}^{-1} & I \end{smallmatrix}\right) \left(\begin{smallmatrix} A_{1,1} & A_{1,2} \\ 0 & S \end{smallmatrix}\right)$ e $\det A = \det A_{1,1}\det S$.

# Eliminazione Gaussiana
QUESTI APPUNTI SONO DA COMPLETARE