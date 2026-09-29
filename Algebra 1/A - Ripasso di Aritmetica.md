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

Un gruppo $G$ si dice finitamente generato se $\exists S \subseteq G$   $|S| < +\infty$   $\langle S \rangle = G$.

Insiemi minimali di generatori possono non avere la stessa cardinalità.

Sia $G$ gruppo e $a \in G$, si dice ordine di $a$ il $o(a) = \{ \min \{ n \in \mathbb{N} \setminus \{ 0 \} \}$   $a^n=e\}$ se tale minimo esiste, altrimenti $o(a)=+\infty$.

Se $o(a)$ finito, vale $a^m = e \iff o(a) \mid m$.

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

# Omomorfismo
$(G_{1}, \circ) \to (G_{2}, \star)$ si dice omomorfismo di gruppi se rispetta le operazioni.

Un omomorfismo bigettivo si dice isomorfismo e si denota con $\cong$.

Sia $\varphi : G_{1} \to G_{2}$ omomorfismo. Vale $G / \text{Ker}\varphi \cong \mathrm{Im}\varphi$.

Sia $H < G$, si dice inclusione l'omomorfismo $\varphi : H \to G$ dato da $\varphi(g_{H})=g_{G}$.

Sia $H \lhd G$, si dice proiezione l'omomorfismo $\pi : G \to G / H$ dato da $\pi(g)=gH$.