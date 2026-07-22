# Successione per ricorrenza
Data una successione $x_{n}$, una successione per ricorrenza di ordine $k$ si presenta sotto forma di un'equazione dove compaiono $x_{n}$ e i successivi $k$ termini.

La teoria delle equazioni differenziali si estende alle successioni per ricorrenza. Si può dunque parlare di successioni autonome, lineari, omogenee, e sistemi di successioni.

Solitamente è difficile trovare una formula chiusa, ma è possibile calcolare il limite e determinare l'ordine di infinito/esimo.

# Successione lineare omogenea
Successione nella forma $x_{n+k} = a_{k-1}x_{n+k-1}+\dots+a_{0}x_{n}$

Risolvere l'equazione significa determinare il nucleo di $L : \text{Succ} \to \text{Succ}$, dove $\text{Succ}$ è lo spazio vettoriale delle successioni in $\mathbb{R}$.

~={cyan}DIMOSTRAZIONE=~: $L$ è un'applicazione lineare.

Le $k$ soluzioni formano una base di uno spazio vettoriale.

La procedura risolutiva è la seguente (caso di ordine 2, ma estendibile):
1. Si passa al polinomio caratteristico, definito da $x_{n} \mapsto x^n$
2. Si guardano le radici del polinomio:
	- se sono $\lambda,\mu \in \mathbb{R}$, allora $x_{n} = a\lambda^n + b\mu^n$
	- se è $\lambda \in \mathbb{R}$ con molteplicità 2, allora $x_{n} = a\lambda^n + bn\lambda^n$
	- se sono $\rho e^{i\theta}, \rho e^{-i\theta} \in \mathbb{C}$, allora $x_{n}=a\rho^n\cos(\theta n)+b\rho^n\sin(\theta n)$
3. Si trovano $a$ e $b$ sostituendo i valori iniziali

~={cyan}DIMOSTRAZIONE=~ (Algebrica):
1. Sia $x_{n+1} = \alpha x_{n+1} + \beta x_{n}$
2. Sia $p_{n}(t) = \beta x_{n}+x_{n+1}t$ (mod $t^2-\alpha t-\beta$)
3. $tp_{n}(t) = p_{n+1}t$, da cui $p_{n}t = t^np_{0}(t)=t^n(\beta x_{0}+x_{1}t)$ in modulo
4. $p_{n}(t) = t^n(\beta x_{0}+x_{1}t) + Q_{n}(t)(t^2-\alpha t-\beta)$
5. Sostituisco a $t$ le radici $\lambda$ e $\mu$ e ottengo un sistema lineare

~={cyan}DIMOSTRAZIONE=~ (Geometrica):
1. Pongo $U_{n} = \binom{x_{n+1}}{x_{n}}$ e $M$ la matrice di elementi $(\alpha,\beta,1,0)$
2. Noto $U_{n+1} = MU_{n}$ da cui $U_{n} = M^nU_{0}$
3. Gli autovalori di $M$ sono le radici del polinomio caratteristico
4. Si diagonalizza $M$ e si calcola $M^n$

# Successioni non lineari autonome del primo ordine
Si può studiare il limite col seguente piano con la monotonia:
1. Si cercano bound per $x_{n}$
2. Si studia la monotonia di $x_{n}$
3. Si dimostra $x_{n} \to l$
4. Si trova $l$

~={cyan}DIMOSTRAZIONE=~: Lo slogan è: verticale alla funzione, orizzontale alla bisettrice.

Il piano precedente non funziona con tutte le successioni: può succedere che esse spiraleggino.

Il seguente è il piano con la distanza:
1. Si pone $d_{n}=|x_{n}-l|$
2. Si cercano bound per $x_{n}$
3. Si dimostra $d_{n+1}\leq cd_{n}$ con $c<1$ costante
4. Si dimostra $d_{n}\leq c^nd_{0}$
5. Si dimostra $d_{n}\to 0$, da cui $x_{n} \to l$

Il seguente è il piano con le sottosuccessioni:
1. Si studia la monotonia di due sottosuccessioni
2. Si trova il limite delle due sottosuccessioni
3. I due limiti coincidono per l'esistenza del limite

# Legame tra derivata e punti fissi
Sia $f : \mathbb{R} \to \mathbb{R}$ una funzione e $\alpha \in \mathbb{R}$ tali che:
1. $f \in C^1$
2. $f(\alpha)=\alpha$
3. $|f'(\alpha)|<1$
Allora $\exists r>0$   $\forall x_{0}\in[\alpha-r,\alpha+r]$   $x_{n+1} = f(x_{n}) \to l$

~={cyan}DIMOSTRAZIONE=~:
1. Per (3.) esistono $m<1$ e $r>0$ tali che $|f'(x)|\leq m$   $\forall x \in [\alpha-r,\alpha+r]$
2. Piano con la distanza usando la Lipschitzianità di $f$ in $[\alpha-r,\alpha+r]$