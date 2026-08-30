# Estensione semplice
Siano $E$ campo e $A$ suo sottoanello, si dice sottocampo se $\forall a \in A$ non nullo, $a^{-1}\in A$.

Siano $K \subseteq L$ campi con $\alpha \in L$, si indica con $K(\alpha)$ il minimo sottocampo di $L$ che contiene $K$ e $\alpha$ e si dice che è un'estensione semplice di $K$.

Dato l'omomorfismo di valutazione $\psi : K[x] \to L$ dato da $\psi(f(x))=f(\alpha)$, si indica con $K[\alpha]$ la sua immagine.

$\exists f(x) \in K[x]$   $\text{Ker}\psi = (f(x))$.

DIMOSTRAZIONE: $\text{Ker}\psi$ è un ideale principale poiché $K[x]$ è euclideo.

$\text{Ker}\psi = \{ 0 \} \implies \not\exists f(x) \in K[x]$ non nullo   $f(\alpha)=0 \implies \alpha$ si dice trascendente su $K$.

$\text{Ker}\psi = (f(x)) \neq \{ 0 \} \implies \alpha$ si dice algebrico su $K$ e $f(x)$ è detto polinomio minimo di $\alpha$ su $K$.

$\alpha$ algebrico $\implies K[\alpha] = K(\alpha)$.

Siano $K \subseteq L$ campi, $f(x) \in K[x]$ irriducibile, $\alpha,\beta \in L$ sue radici distinte, allora $\exists \theta : K[\alpha] \to K[\beta]$ tale che $\theta(\alpha)=\beta$ e $\theta|_{K} = \text{id}$.

DIMOSTRAZIONE: Osservazioni sul nucleo di $\theta$.

# Grado di un'estensione
Dati $F \subseteq K$ campi, il gradodi $K$ su $F$ è $[K : F] = \dim K$ come spazio vettoriale su $F$.

Sia $L$ estensione finita di $K$ estensione finita di $F$, allora $[L : F] = [L : K][K : F]$.

DIMOSTRAZIONE: Esibizione di basi.

Sia $L$ estensione finita di $F$ e $F \subseteq K \subseteq L$, allora $[L:F] = [L : K][K : F]$.

DIMOSTRAZIONE: Teorema precedente.

# Campo di spezzamento
Sia $L$ campo e $f(x) \in L[x]$ di grado $n>0$. Allora $f(x)$ ha al più $n$ radici con molteplicità in $L$.

DIMOSTRAZIONE: Già precedentemente fatta.

Sia $K$ campo e $f(x) \in K[x]$ di grado $n\geq 0$. Allora esistono $E \subseteq K$ campo e $e_{1},\dots e_{n} \in E$ tali che $f(x)=\lambda(x-e_{1})\dots(x-e_{n}) \in E[x]$ con $\lambda \in E$ costante.

DIMOSTRAZIONE: Induzione.

Siano $K \subseteq L$ campi e $f(x) \in K[x]$ tale che $f(x)$ si fattorizza completamente in $L$ come prodotto di fattori lineari, allora si dice campo di spezzamento di $f(x)$ su $K$ il più piccolo campo $E \subseteq L$ tale che $K \subseteq E$ e $f(x)$ ha tutte le radici in $E$.

Il campo di spezzamento esiste ed è unico.

DIMOSTRAZIONE: Definizioni.

# Caratteristica
Sia $F$ campo, allora valgono:
1. $\exists!\phi : \mathbb{Z} \to F$ omomorfismo
2. $\text{Ker}\phi = (d)$ e $d$ si dice caratteristica del campo
3. $d = 0 \lor d$ primo

Sia $L$ campo finito, allora non può essere di caratteristica $0$ e $[L : \mathbb{Z}_{p}]$ è finito.

Sia $L$ campo finito, allora $|L|=p^n$ per qualche $p$ primo e $n\in \mathbb{Z}^+$.

# Omomorfismo di Frobenius
Sia $p$ primo e $K$ campo di caratteristica $p$, allora la funzione $\mathscr{F} : K \to K$ data da $\mathscr{F}(a)=a^p$ è un omomorfismo iniettivo ed è detta omomorfismo di Frobenius.

DIMOSTRAZIONE: Omomorfismo e piccolo teorema di Fermat.

Sia $K$ campo e $\psi : K \to K$ omomorfismo. Allora $\text{Fix}_{\psi}$ sottocampo di $K$.

DIMOSTRAZIONE: Vale la definizione di campo ed è un sottoanello.


# Campi di cardinalità $p^n$
$\forall p$ primo   $\forall n \in \mathbb{Z}^*$   $\exists K$ campo   $|K|=p^n$.

DIMOSTRAZIONE:
1. $\exists E$ estensione di $\mathbb{Z}_{p}$ dove $x^{p^n} - x$ ha tutte le radici
2. $[E : \mathbb{Z}_{p}]$ finito
3. Sia $R$ campo di spezzamento di $x^{p^n}-x$ in $E$
4. $R$ ha caratteristica $p$ e $[R : \mathbb{Z}_{p}]$ finito in quanto sottocampo
5. Sia $L = \{ r \in R : \mathscr{F}^nr = r \}$
6. $L$ sottocampo di $R$ con elementi radici
7. $|L|=p^n$

$\forall p$ primo   $\forall n \in \mathbb{Z}^+$   $\exists f(x) \in\mathbb{Z}_{p}[x]$ irriducibile   $\text{deg}f(x)=n$.

DIMOSTRAZIONE:
1. Sia $K$ campo con $p^n$ elementi e $\alpha$ un generatore di $K^*$
2. $\mathbb{Z}_{p}(\alpha)=K$ in quanto sottoinsieme che contiene $0$ e $\alpha$, quindi $[K : \mathbb{Z}_{p}]=n$
3. Sia $f(x)$ polinomio minimo di $\alpha$, vale $\mathbb{Z}_{p}(\alpha) \cong \mathbb{Z}_{p}[x] / (f(x))$ da cui $\text{deg}f(x)=n$

# Polinomi irriducibili e campi di spezzamento
Dato $f(x) \in \mathbb{Z}_{p}[x]$ irriducibile di grado $n$, un suo campo di spezzamento su $\mathbb{Z}_{p}[x]$ è $K = \mathbb{Z}_{p}[x] / (f(x))$.

DIMOSTRAZIONE: Ragionamento sulle radici di $f(x)$ in $K$.

# Miscellanea
Sia $p$ primo e $n \in \mathbb{Z}^+$, allora $x^{p^n}-x$ è il prodotto di tutti i polinomi monici irriducibili in $\mathbb{Z}_{p}[x]$ di grado $d$ divisore di $n$.

$K,H$ campi finiti, vale $|K|=|H|\implies K \cong H$.