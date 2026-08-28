# Anello euclideo
Un dominio $D$ si dice anello euclideo se $\exists g : D \setminus \{ 0 \} \to \mathbb{N}$, detta grado, tale che:
1. $\forall a,b \in D$   $a,b \neq 0$   $g(a) \leq g(ab)$
2. $\forall a,b \in D$   $b \neq 0$   $\exists q,r \in D$   $a = qb+r$   $r = 0 \lor g(r) < g(b)$

Sia $D$ euclideo e $a,b \neq 0$. Allora $b \mid a \land a \nmid b \implies g(b) < g(a)$.

DIMOSTRAZIONE: $a \nmid b \implies b = aq + r \land r \neq 0 \land g(r) < g(a) \implies r = b(1-cq) \implies g(r) \geq g(b)$.

Sia $D$ euclideo. Allora:
1. $\forall b \in D$   $g(1) \leq g(b)$
2. $g(b) = g(1) \iff b \in D^*$

DIMOSTRAZIONE:
- ($\implies$) $g(b)=g(1) \land a \in D \implies a =qb+r \land g(r) < g(b) \implies r = 0 \implies D = (b)$
- ($\impliedby$) $b \in D^* \implies (b) = D \implies g(b) = g(1)$

Un dominio si dice PID o a ideali principali se tutti i suoi ideali sono principali.

Sia $D$ euclideo, allora è PID.

DIMOSTRAZIONE: Sia $I$ ideale, è banale oppure si usa la divisione euclidea e l'assorbimento.

Sia $D$ euclideo e $a,b \in D$ non nulli. Un MCD di $a$ e $b$ è $d \in D$ tale che:
1. $d \mid a \land d \mid b$
2. $\forall c \in D$   $c \mid a \land c \mid b \implies c \mid d$

Sia $D$ euclideo e $a,b \in D$ non nulli. Sia $d$ generatore di $(a,b)$, allora $d$ è un MCD di $a$ e $b$.

Si può estendere Bézout agli anelli euclidei.

# Elemento primo e irriducibile
Sia $D$ dominio e $\pi \in D \setminus (\{ 0 \} \cup D^*)$. Allora $\pi$ si dice irriducibile se $\pi=\gamma \delta \implies \gamma \in D^* \lor \delta \in D^*$.

Sia $D$ dominio e $\pi \in D \setminus (\{ 0 \} \cup D^*)$. Allora $\pi$ si dice primo se $\pi \mid \gamma \delta \implies \pi \mid \gamma \lor \pi \mid \delta$.

Sia $D$ dominio, allora $\pi \in D$ primo $\implies \pi$ irriducibile.

DIMOSTRAZIONE: Definizioni.

Sia $D$ euclideo, allora $\pi \in D$ irriducibile $\implies \pi$ primo.

DIMOSTRAZIONE: Definizioni.

In un anello euclideo la fattorizzazione in prodotto di irriducibili esiste ed è unica.

DIMOSTRAZIONE: Definizioni e funzione grado.

# Intero di Gauss
Un intero di Gauss è un elemento dell'insieme $\mathbb{Z}[i] = \{ a+bi : a,b \in \mathbb{Z} \}$.

$\mathbb{Z}[i]$ è un anello euclideo.

DIMOSTRAZIONE: $\mathbb{Z}[i]$ è un dominio e come grado si sceglie $g$ tale che $g(a+ib)=a^2+b^2$.

Sia $p \in \mathbb{Z}$ primo dispari riducibile in $\mathbb{Z}[i]$, allora è somma di due quadrati in $\mathbb{Z}$.

DIMOSTRAZIONE: Ragionamento sull'invertibilità.

Sia $p \in \mathbb{Z}$ primo tale che $p \equiv 1$   $(4)$. Allora $x^2 \equiv -1$   $(p)$ ammette soluzione in $\mathbb{Z}$.

DIMOSTRAZIONE: Teorema di Wilson.

Sia $p \in \mathbb{Z}$ primo tale che $p \equiv 3$   $(4)$. Allora non è somma di due quadrati in $\mathbb{Z}$.

DIMOSTRAZIONE: Assurdo con la congruenza.

Sia $p \in \mathbb{Z}$ primo tale che $p \equiv 3$   $(4)$. Allora $p$ è irriducibile in $\mathbb{Z}[i]$.

DIMOSTRAZIONE: Lemmi precedenti.

Tutti e soli gli irriducibili di $\mathbb{Z}[i]$ sono, a meno di associati:
- $p \in\mathbb{Z}$ primi tali che $p \equiv 3$   $(4)$
- $z \in \mathbb{Z}[i]$ tali che $g(z) \in \mathbb{Z}$ primo

DIMOSTRAZIONE: Lemmi e teoremi precedenti.

# Irriducibilità in un anello di polinomi
Da scrivere interamente - work in progress.
