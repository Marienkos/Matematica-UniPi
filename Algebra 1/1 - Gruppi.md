_"Vedi a non dare fastidio a nessuno, ti chiamano anormale" cit. Il Bandito del Diedrale_
# Gruppo
Un gruppo $G$ è un insieme non vuoto dotato di un'operazione $\circ : G \times G \to G$ tale che
1. $\circ$ associativa
2. $\exists$ elemento neutro
3. $\exists$ inversi sinistro e destro

Valgono unicità dell'elemento neutro, dell'inverso e la legge di cancellazione.

Sia $G$ gruppo e $H \subseteq G$ non vuoto, è sottogruppo se $(H, \circ|_{H \times H})$ gruppo.

Ogni sottogruppo di un gruppo abeliano è abeliano.

Sia $S \subseteq G$, il sottogruppo $\langle S \rangle$ di $G$ generato da $S$ è il più piccolo sottogruppo di $G$ che contiene $S$.

$\langle S \rangle$ si può costruire in due modi:
- Dall'alto, considerando $\langle S \rangle = \bigcap\limits_{H \text{ sgr } G \supseteq S} H$
- Dal basso considerando $S = \{ s_{i} : i \in I \} \subseteq G$ e aggiungendo inversi e prodotti

$\langle \emptyset \rangle = \{ e \}$.

Se $S = \{ a \}$, allora $\langle S \rangle =: \langle a \rangle$ e si dice gruppo ciclico.

Sia $G=\langle a \rangle$, allora:
- $o(a)=+\infty \implies G \cong \mathbb{Z}$
- $o(a)=n \implies G \cong \mathbb{Z}_{n}$.

Un gruppo $G$ si dice finitamente generato se $\exists S \subseteq G$   $|S| < +\infty$   $\langle S \rangle = G$.

Insiemi minimali di generatori possono non avere la stessa cardinalità.

Sia $G$ gruppo e $a \in G$, si dice ordine di $a$ il $o(a) = \{ \min \{ n \in \mathbb{N} \setminus \{ 0 \} \}$   $a^n=e\}$ se tale minimo esiste, altrimenti $o(a)=+\infty$.

Se $o(a)$ finito, vale $a^m = e \iff o(a) \mid m$.

$H < G$ si dice caratteristico se $\forall \varphi \in \text{Aut}G$   $\varphi(H) \subseteq H$.

# Quoziente
Sia $S$ insieme, $\sim$ si dice relazione di equivalenza se è riflessiva, simmetrica e transitiva.

Sia $H < G$, la relazione $\sim_{H}$ data da $g_{1} \sim_{H} g_{2} \iff g_{1}g_{2}^{-1}\in H$ è d'equivalenza.

Si definisce la classe di equivalenza di $g \in G$ come $[g] := \{ g_{1} \in G : g_{1} \sim_{H} g \}$.

$[g] = Hg := \{ hg : h \in H \}$ si definisce classe laterale destra di $g$ rispetto ad $H$.

Si definisce analogamente la classe laterale sinistra.

Siano $S$ insieme e $\sim$ relazione d'equivalenza, essa partiziona $S$.

Si definisce il quoziente $G / H := \{ \text{classi laterali destre di } G \}$.

Sia $|G|<+\infty$, allora $|G| = o(g) = o(h)[G : H]$ dove $[G:H]$ è detto indice di $H$ in $G$.

$H<G$ si dice normale in $G$ e si denota con $H \lhd G$ se $gH=Hg$.

Si definisce centro $Z(G)=\{ z \in G : zg = gz$   $\forall g \in G\}$ e vale $Z(G) \lhd G$.

$G / H$ gruppo $\iff H \lhd G \iff gHg_{1}H=gg_{1}H \land HgHg_{1} = Hgg_{1}$   $\forall g,g_{1} \in G$.

Sia $H = \langle a \rangle \lhd G$, allora ogni sottogruppo di $H$ è normale in $G$.

DIMOSTRAZIONE:
1. $S$ sottogruppo di $H \implies S = \langle a^n \rangle$
2. $ga^ng^{-1}=(gag^{-1})^n = (a^m)^n = (a^n)^m \in \langle a^n \rangle$

# Omomorfismo
$(G_{1}, \circ) \to (G_{2}, \star)$ si dice omomorfismo di gruppi se rispetta le operazioni.

Un omomorfismo bigettivo si dice isomorfismo e si denota con $\cong$.

Sia $\varphi : G_{1} \to G_{2}$ omomorfismo. Vale $G / \text{Ker}\varphi \cong \mathrm{Im}\varphi$.

Sia $H < G$, si dice inclusione l'omomorfismo $\varphi : H \to G$ dato da $\varphi(g_{H})=g_{G}$.

Sia $H \lhd G$, si dice proiezione l'omomorfismo $\pi : G \to G / H$ dato da $\pi(g)=gH$.

Siano $H,K < G$, allora $HK < g \iff HK = KH$.

DIMOSTRAZIONE:
- ($\impliedby$) Verifica diretta
- ($\implies$) Sia $kh \in KH$ e si nota $h^{-1}k^{-1}$ e $(hk)^{-1}$, consegue $KH \subseteq HK$ e $HK \subseteq KH$

Siano $H < G$ e $N < G$. Allora:
1. $HN < G$
2. $H \cap N \lhd H$ e $N \lhd HN$
3. $H / H \cap N \cong HN / N$

DIMOSTRAZIONE:
1. Teorema precedente
2. Ovvio
3. Sia $\varphi : H \to HN / N$, si usa il primo teorema di omomorfismo

Sia $\varphi : G_{1} \to G_{2}$ omomorfismo surgettivo. Allora:
1. $H_{1} < G_{1} \implies \varphi(H_{1}) < G_{2}$
2. $\varphi^{-1}(H_{2}) < G_{1}$ e $H_{2} < G_{2}$

DIMOSTRAZIONE: Verifica diretta.

Sia $\varphi$ omomorfismo surgettivo, allora:
1. $\varphi\varphi^{-1}(H_{2})=H_{2}$
2. $\varphi |_{\varphi^{-1}(H_{2})} : \varphi^{-1}(H_{2}) \to H_{2}$ surgettivo
3. $\varphi^{-1}(H_{2}) / \text{Ker}\varphi \cong H_{2}$
4. $\varphi^{-1}\varphi(H_{1}) = H_{1} \text{Ker}\varphi$

DIMOSTRAZIONE: Verifiche e primo teorema di omomorfismo.

Sia $\varphi : G_{1} \to G_{2}$ surgettivo, allora $\exists \{ G < G_{1} : \text{Ker} \varphi \subseteq G \} \to \{ G <G_{2} \}$ bigettiva.

DIMOSTRAZIONE: Teorema precedente.

Sia $\varphi$ omomorfismo surgettivo, $H_{1} \lhd G_{1}$ e $H_{2} \lhd G_{2}$. Allora:
1. $\varphi^{-1}(H_{2}) \lhd G_{1}$
2. $\varphi(H_{1}) \lhd G_{2}$

DIMOSTRAZIONE: Verifica diretta.

Sia $N_{2} \lhd G_{2}$, allora $G_{1} / \varphi^{-1}(N_{2}) \cong G_{2} / N_{2} \cong \frac{G_{1}}{\text{Ker} \varphi} / \frac{\varphi^{-1}(N_{2})}{\text{Ker}\varphi}$.

DIMOSTRAZIONE: Primo teorema di omomorfismo su $\pi \circ \varphi$.

$\text{Aut}\mathbb{Z}_{n} \cong \mathbb{Z}_{n}^* \cong \left( \prod\limits_{p} \mathbb{Z}_{p^{n_{p}}} \right)^* \cong \prod\limits_{p} \mathbb{Z}_{p^{n_{p}}}^* \cong \prod\limits_{p} \text{Aut}\mathbb{Z}_{p^{n_{p}}}$.

Siano $H$ e $K$ gruppi finiti, allora $\text{Aut}(H \times K) \cong \text{Aut}H \times \text{Aut}K \iff H \times \{ e_{K} \}$ e $\{ e_{H} \} \times K$ caratteristici.

DIMOSTRAZIONE:
1. Osservazione preliminare
	1. Siano $\varphi \in \text{Aut}H$ e $\psi \in \text{Aut}K$, si definisce $\lambda_{\varphi,\psi} : H \times K \to H \times K : (h,k) \mapsto (\varphi(h),\psi(k))$
	2. $\lambda_{\varphi,\psi} = \text{id}_{H \times K} \iff (\varphi(h),\psi(k))=(h,k)$   $\forall h \in H$   $\forall k \in K$ $\iff \varphi = \text{id}_{H} \land \psi = \text{id}_{K}$
	3. $\text{Aut}H \times \text{Aut}K \to \text{Aut}(H \times K) : (\varphi,\psi) \mapsto \lambda_{\varphi,\psi}$ omomorfismo iniettivo
- ($\implies$)
	1. $G$ gruppo finito $\implies \text{Aut}G$ finito
	2. La tesi vale se l'omomorfismo dell'osservazione preliminare è surgettivo
	3. $\forall \omega \in \text{Aut}(H \times K)$   $\exists \varphi \in \text{Aut}H$   $\exists\psi \in \text{Aut}K$   $\omega = \lambda_{\varphi,\psi}$
	4. $\omega(H \times \{ e_{K} \}) \subseteq (\varphi(H), \psi(e_{K}))=(H,e_{K})=H \times \{ e_{K} \}$ e analogo per $\{ e_{H} \} \times K$
- ($\impliedby$)
	1. Dato $\omega \in \text{Aut}(H \times K)$ si definisce $\varphi : H \to H : h \mapsto \pi_{H}\omega(h,e_{K})$
	2. $\varphi$ omomorfismo in quanto composizione di omomorfismi
	3. $\text{Ker}\varphi = \{ h : \varphi(h)=e_{H} \} = \pi_{H}\{ \omega(h,e_{K})=(e_{H},e_{K}) \} = \pi_{H}\{ (e_{H},e_{K}) \}=\{ e_{H} \}$
	4. $\varphi \in \text{Aut}H$
	5. Analogo per $\psi : K \to K : k \mapsto \pi_{K}\omega(e_{H},k)$
	6. $\lambda_{\varphi,\psi}=\omega$

# Approfondimento su $D_{n}$
Sia $d \mid n$, allora $\langle \sigma^{n/d} \rangle \lhd D_{n}$.

Sia $H \lhd D_{n}$ con una simmetria, allora $H \supset \langle \tau \sigma^i,\sigma^2 \rangle = D_{n}$ con $n$ pari o $D_{n/2}$ con $n$ dispari.

Sia $\sigma^{n/d} \in Z(D_{n})$, allora $\tau \sigma^{n/d}\tau = \sigma^{-n/d}$ uguali $\iff \sigma^{-n/d}=\sigma^{n/d} \iff \frac{2n}{d} \equiv 0$   $(n)$.

$Z(D_{n}) = \{ e \}$ con $n$ dispari o $\langle \sigma^{n/2} \rangle$ con $n$ pari.

$D_{n} / \langle \sigma \rangle \cong D_{n} / \langle \sigma^2,\tau \rangle \cong D_{n} / \langle \sigma^2,\tau \sigma \rangle \cong \mathbb{Z}_{2}$

DIMOSTRAZIONE: $D_{n} / H$ con $[D_{n}:H]=2$.

$D_{n} / \langle \sigma^{n/d} \rangle \cong D_{n / d}$.

Osas paraplegico come se fosse Antani$^2$.

Le mappe  $\sigma \mapsto \sigma^j$   $j \in \mathbb{Z}_{n}^*$   e   $\tau \mapsto \tau \sigma^i$   $i \in \mathbb{Z}_{n}$ sono tutti e soli gli automorfismi di $D_{n}$.

DIMOSTRAZIONE:
1. Sia $\varphi_{ij}$ che manda $\tau$ e $\sigma$ come le mappe precedenti
2. $\varphi_{ij} \circ \varphi_{rs}$ manda $\tau \mapsto \tau \sigma^i\sigma^{rj}=\tau \sigma^{i+jr}$ e $\sigma \mapsto \sigma^{js}$, quindi $\varphi_{ij} \circ \varphi_{rs} = \varphi_{i+jr,js}$
3. $\exists$ bigezione tra $\text{Aut}D_{n}$ e $\mathbb{Z}_{n} \times \mathbb{Z}_{n}^*$
4. Sia $(G,\circ) := (\mathbb{Z}_{n} \times \mathbb{Z}_{n}^*, (i,j)\circ(r,s)=(i+jr,js))$, è un gruppo
5. $\text{Aut}D_{n} \cong G$ con $\circ$

I sottogruppi caratteristici di $D_{n}$ sono tutti e soli $\langle \sigma^{n / d} \rangle$.

DIMOSTRAZIONE: Tra i sottogruppi normali, $\varphi_{i,j}(\sigma^{n/d})=\sigma^{nj / d}$ mentre $\varphi_{1,1}(\tau)=\tau \sigma \not\in \langle \sigma^2,\tau \rangle$.