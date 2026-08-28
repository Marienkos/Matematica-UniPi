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