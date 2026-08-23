# Gruppo
Un gruppo $G$ è un insieme non vuoto dotato di un'operazione binaria con:
1. associatività: $\forall a,b,c  \in G$   $(ab)c=a(bc)$
2. esistenza di un elemento neutro: $\exists e\in G$   $\forall g \in G$   $eg = ge = g$
3. esistenza di un inverso rispetto all'operazione: $\forall g \in G$   $\exists g^{-1}\in G$   $gg^{-1}=g^{-1}g=e$

Se l'operazione è commutativa, il gruppo si dice commutativo o abeliano.

Dato un gruppo $G$ valgono:
1. $\exists!e\in G$
2. $\forall a \in G$   $\exists!a^{-1}\in G$
3. $\forall a \in G$   $(a^{-1})^{-1}=a$
4. $\forall a,b \in G$   $(ab)^{-1}=b^{-1}a^{-1}$
5. $\forall a,b,c \in G$   $axb=c$ ha un'unica soluzione $x = a^{-1}c b^{-1}$

DIMOSTRAZIONE:
1. Siano $e$ e $e'$ elementi neutri. Allora $e=e e' =e'$.
2. Siano $h$ e $k$ inversi di $a$. Allora $h = he = h(ak) = (ha)k = ek = k$.
3. Sia $g$ che $(g^{-1})^{-1}$ sono inversi di $g^{-1}$. Per unicità i due coincidono.
4. Si verifica che $b^{-1} a^{-1}$ è un inverso di $ab$.
5. Deriva dalle altre proprietà.

Un insieme $H \subseteq G$ si dice sottogruppo di $G$ e si denota $H < G$ se:
1. $e \in H$
2. $a,b \in H \implies ab \in H$
3. $a \in H \implies a^{-1} \in H$

Il centro $Z(G) = \{ g\in G : gh=hg$   $\forall h \in G \}$ è un sottogruppo di $G$.

# Gruppo simmetrico
Dato $n \in \mathbb{Z}^+$, si dice permutazione una funzione bigettiva da $\{ 1,\dots,n \}$ in se stesso.

Si chiama gruppo simmetrico e si denota con $S_{n}$ l'insieme delle permutazioni di $\{ 1,\dots n \}$.

$S_{n}$ ha $n!$ elementi.

DIMOSTRAZIONE: Calcolo combinatorio.

$S_{n}$ è un gruppo con la composizione di permutazioni.

DIMOSTRAZIONE: Verifiche.

Dato $a$, si dice ciclo un insieme di elementi tale che:
- ogni elemento è $\sigma$ applicata al precedente
- il primo elemento $a$ coincide con $\sigma$ applicata all'ultimo elemento

Esistono 2 notazioni per $S_{n}$:
- notazione ad array, cioè ponendo in due righe $n$ e $\sigma(n)$
- notazione a cicli disgiunti, cioè scrivendo i cicli separati da parentesi senza ripetizioni

# Laterale di un sottogruppo
Dati $H < G$, si dice laterale sinistro di $H$ l'insieme $gH = \{ gh : h \in H \}$ con $g \in G$.

L'insieme dei laterali sinistri si indica con $G / H$ e la sua cardinalità è detta indice di $H$ in $G$.

Ogni elemento $w \in G$ è contenuto in uno e un solo laterale sinistro $wH$.

DIMOSTRAZIONE: $w \in \gamma H \implies \exists h_{1} \in H$   $w = \gamma h_{1} \implies \gamma H = wH$.

I laterali $gH$ e $bH$ coincidono $\iff b \in gH$.

DIMOSTRAZIONE:
- ($\impliedby$) Per il teorema precedente $b \in gH \land b \in bH \implies gH = bH$
- ($\implies$) Se $bH = gH$ gli elementi coincidono.

# Teorema di Lagrange
Sia $G$ gruppo finito e $H < G$. Allora $|H|$ divide $|G|$.

DIMOSTRAZIONE:
1. $G$ è l'unione disgiunta di un numero finito di laterali sinistri di $H$
2. Gli elementi $gh$ al variare di $h \in H$ sono tutti diversi
3. $|gH| = |H|$

# Gruppo ciclico
Dato $a \in G$ l'insieme $\langle a \rangle = \{ a^i : i \in \mathbb{Z}\}$ è detto sottogruppo ciclico generato da $a$. 

L'ordine di un elemento si definisce analogamente all'aritmetica modulare.

In un gruppo finito $G$ ogni elemento $x$ ha ordine finito che divide $|G|$.

DIMOSTRAZIONE: $o(x)$ è la cardinalità di $\langle x \rangle$, che è un sottogruppo di $G$.

$x^{|G|} = e$

DIMOSTRAZIONE: $x^{|G|} = x^{ko(x)} = (x^{o(x)})^k = e^k = e$.

In un gruppo ciclico $G$ con $n$ elementi ci sono esattamente $\phi(n)$ generatori.

DIMOSTRAZIONE:
1. Sia $g$ generatore di $G$, gli elementi di $G$ sono nella forma $g^i$
2. Sia $d=o(g^i)$, per Lagrange $d \, | \, n$
3. $(g^i)^d=e$, ossia $g^{di}=e$ per cui $n \, | \, di$
4. Se $(i,n)=1$ allora $n \, | \, d$ e $n=d$, altrimenti $g^i$ non è un generatore 

Sia $G$ gruppo ciclico e $H < G$, allora $H$ è ciclico.

DIMOSTRAZIONE:
1. Sia $g$ generatore di $G$ e $k$ il minimo intero positivo tale che $g^k \in H$
2. Sia $g^a \in H$, per divisione euclidea $\exists q,r \in \mathbb{Z}$   $a = qk+r$   $0 \leq r < k$
3. $(g^k)^{-q} g^{qk+r} = (g^k)^{-q} (g^k)^q g^r = g^r \in H$ poiché $H < G$
4. Essendo $k$ minimo, $r = 0$ e $g^a \in \langle g^k \rangle$

Sia $G$ gruppo ciclico con $n$ elementi. Allora $\forall d \, | \, n$   $\exists!H < G$   $|H| = d$.

DIMOSTRAZIONE: Osservazioni sui gruppi ciclici.

# Omomorfismo
Dati $G_{1}$ e $G_{2}$ gruppi, $f:G_{1} \to G_{2}$ si dice omomorfismo se $\forall g,h \in G_{1}$   $f(gh) = f(g)f(h)$.

Sia $f$ omomorfismo. Allora $f(e_{G_{1}})=e_{G_{2}}$ e $f(g^{-1})=f(g)^{-1}$.

DIMOSTRAZIONE: $f(e_{G_{1}})=f(e_{G_{1}}e_{G_{1}})=f(e_{G_{1}})f(e_{G_{1}})$ e simile per l'inverso.

Un omomorfismo tra $G_{1}$ e $G_{2}$ bigettivo è detto isomorfismo e i due gruppi isomorfi $G_{1} \cong G_{2}$.

Siano $G_{1},G_{2}$ gruppi e $\alpha$ omomorfismo. Sia $g \in G$ tale che $o(g)=n$. Allora $o(\alpha(g)) \, | \, n$.

DIMOSTRAZIONE: $\alpha$ è omomorfismo, quindi $\alpha(g^k)=\alpha(g)^k$, da cui $\alpha(g)^n = e_{G_{2}}$.

Dati $G_{1},G_{2}$ gruppi e un omomorfismo $f$, si dice nucleo $\text{Ker}f=\{ g \in G_{1} : f(g)=e_{G_{2}}\}$.

Similmente si dice immagine $\text{Imm}f = \{ f(g) : g \in G_{1} \}$.

Valgono $\text{Ker}f < G_{1}$ e $\text{Imm}f < G_{2}$.

$f$ iniettivo $\iff$ nucleo banale.

DIMOSTRAZIONE:
- ($\implies$) Per assurdo $f(x)=f(e_{G_{1}}) \implies f$ non iniettivo
- ($\impliedby$) Per assurdo sugli inversi.

# Sottogruppo normale
Sia $G$ gruppo e $g \in G$. Si dice coniugio rispetto a $g$ la funzione $C_{g}(h) = ghg^{-1}$.

Il coniugio è un automorfismo.

DIMOSTRAZIONE: Esiste l'inversa.

Si dice orbita rispetto al coniugio di $\gamma$ l'insieme $\text{Orb}(\gamma) = \{ C_{g}(\gamma) : g \in G \}$.

Sia $H < G$, si dice normale se $\forall g \in G$   $C_{g}(H) \subseteq H$ e si denota con $H \lhd G$.

Se $G$ è abeliano, ogni suo sottogruppo è normale.

DIMOSTRAZIONE: $C_{g}(h) = ghg^{-1} = gg^{-1}h = eh=h$.

Sia $f : G_{1} \to G_{2}$ omomorfismo, allora $\text{Ker}f \lhd G_{1}$.

DIMOSTRAZIONE: Il coniugio manda nell'identità.

Si può usare l'uguaglianza nella definizione di sottogruppo normale.

Sia $\sigma \in S_{n}$ e $m_{i}$ il numero di cicli di $\sigma$ di lunghezza $i$. Allora $|\text{Orb}(\sigma)|=\frac{n!}{1^{m_{1}}\dots n^{m_{n}}m_{1}!\dots m_{n}!}$.

DIMOSTRAZIONE: Calcolo combinatorio.

Sia $\sigma \in S_{n}$ con $n\geq 2$ e esprimibile come prodotto di $k$ e $k'$ trasposizioni, allora $k \equiv k'$   $(2)$.

DIMOSTRAZIONE: Da espandere.

$\sigma$ è pari se esprimibile come prodotto di un numero pari di trasposizioni, altrimenti dispari.

L'insieme delle permutazioni pari $A_{n}$ è detto gruppo alterno e valgono:
1. $A_{n} \lhd S_{n}$
2. $|A_{n}| = \frac{n!}{2}$

DIMOSTRAZIONE: Si considera la funzione segno.

# Centralizzatore
Sia $G$ gruppo e $\gamma \in G$. Si dice centralizzatore di $\gamma$ l'insieme $C(\gamma)=\{ g\in G : g\gamma=\gamma g \}$.

$C(\gamma) < G$.

DIMOSTRAZIONE: Verifica.

$G / C(\gamma) \cong \text{Orb}(\gamma)$.

DIMOSTRAZIONE: Si considera $f:gC(\gamma) \mapsto g\gamma g^{-1}$, si verifica la bigettività.

$|\text{Orb}(\gamma)|=\frac{|G|}{|C(\gamma)|}$.

DIMOSTRAZIONE: Isomorfismo precedente.

# Primo teorema di omomorfismo
Sia $H \lhd G$, allora $G / H$ è un gruppo, detto quoziente, col prodotto $g_{1}Hg_{2}H=g_{1}g_{2}H$.

Dati $G_{1},G_{2}$ gruppi e $f$ omomorfismo tra essi, vale $G_{1} / \text{Ker}f \cong \text{Imm}f$.

DIMOSTRAZIONE:
1. Il quoziente è ben definito poiché $\text{Ker}f \lhd G_{1}$
2. $\text{Imm}f < G_{2} \implies \text{Imm}f$ gruppo
3. Sia $\bar{f} : G_{1} / \text{Ker}f \to \text{Imm}f$ definita come $\bar{f}(g_{1}\text{Ker}f) = f(g_{1})$
4. $\bar{f}$ è ben definito ed è un omomorfismo bigettivo, dunque un isomorfismo

Sia $H \lhd G$, la funzione $\pi_{H} : G_{1} \to G_{1} / H$ data da $\pi(g)=gH$, detta proiezione al quoziente, è un omomorfismo surgettivo e $\text{Ker}\pi = H$.

DIMOSTRAZIONE: Primo teorema di omomorfismo.

# Gruppo diedrale
Sia $P_{n}$ poligono regolare di $n$ lati in $\mathbb{R}^2$ con $n\geq 3$ con baricentro nell'origine. Sia $D_{n}$ l'insieme delle isometrie che mandano $P_{n}$ in se stesso. $D_{n}$ è un gruppo, detto diedrale, con la composizione di funzioni.

Sia $\rho$ la rotazione rispetto all'origine di $\frac{2\pi}{n}$ e $r$ la riflessione rispetto a una retta passante per il centro e il punto medio di un lato. Vale $r\rho r = \rho^{-1}$.

$|D_{n}|=2n$ e $D_{n}$ è isomorfo a un sottogruppo di $S_{n}$.