# Congruenza
Siano $a,b \in \mathbb{Z}$ e $m \in \mathbb{Z}^+$. Allora $a \equiv b$   $(m)$ e si dicono congrui modulo $m$ se le divisioni euclidee per $m$ danno lo stesso resto.

$a\equiv b$   $(m) \iff m | a-b$

DIMOSTRAZIONE: Osservazione sui resti.

Siano $a \equiv a'$   $(m)$ e $b\equiv b'$   $(m)$. Allora:
1. $a+b \equiv a' + b'$   $(m)$
2. $ab \equiv a'b'$   $(m)$

DIMOSTRAZIONE: Definizione di congruenza.

Si dice inverso di $a$ un numero $x$ tale che $ax \equiv 1$   $(m)$.

$\exists$ inverso di $a$ $\iff$ $(a,m)=1$.

DIMOSTRAZIONE: Bézout.

$\forall m \in \mathbb{Z}^+$   $\forall a \in \mathbb{Z} \setminus \{ 0 \}$   $\forall b_{1},b_{2} \in \mathbb{Z}$   $ab_{1}\equiv ab_{2}$   $(m)$   $\iff$   $b_{1}\equiv b_{2}$   $\left( \frac{m}{(a,m)} \right)$.

Dalle equazioni diofantee derivano le proprietà delle equazioni congruenziali.

# Piccolo teorema di Fermat
Sia $p$ primo e $a \in \mathbb{Z}$ non multiplo di $p$. Allora $a^{p-1}\equiv 1$   $(p)$.

DIMOSTRAZIONE:
1. Dato $a \not\equiv 0$   $(p)$, consideriamo i numeri $a, 2a,\dots,(p-1)a$
2. Tali numeri sono a due a due non congrui modulo $p$
3. Tali numeri sono congrui a $1,2,\dots,p-1$
4. Tramite manipolazione algebrica si ottiene la tesi

DIMOSTRAZIONE (Eulero):
1. $\binom{p}{i}i!(p-i)! = p!$ e $p | p!$ ma $p \not{|}$  $i!(p-i)!$, ossia $p | \binom{p}{i}$
2. $(1+a)^p = \sum\limits_{i=0}^{p} \binom{p}{i}a^i \equiv a^p + 1^p \equiv a^p + 1$   $(p)$
3. $a^p \equiv a$   $(p)$ per induzione

Sia $p$ primo e $a \in \mathbb{Z}$. Allora $a^p \equiv a$   $(p)$.

DIMOSTRAZIONE: Piccolo teorema di Fermat.

Sia $1<n \in \mathbb{Z}$ tale che $\exists a$   $a^n \not\equiv a$   $(n)$. Allora $n$ non è primo.

DIMOSTRAZIONE: Contronominale della proposizione precedente.

Si definisce ordine $o = \min \{ x : a^x \equiv 1 \text\}$. 