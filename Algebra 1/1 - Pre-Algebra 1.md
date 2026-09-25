# Nozioni sui gruppi
Un gruppo $G$ è un insieme non vuoto dotato di un'operazione $\circ : G \times G \to G$ tale che
1. $\circ$ associativa
2. $\exists$ elemento neutro
3. $\exists$ inversi sinistro e destro

Valgono unicità dell'elemento neutro, dell'inverso e la legge di cancellazione.

Sia $G$ gruppo e $H \subseteq G$ non vuoto, è sottogruppo se $(H, \circ|_{H \times H})$ gruppo.

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

# Esercizi
1. $\langle \tau \rangle$ e $\langle \sigma \rangle$ sono sottogruppi di $D_{n}$, cercarne altri
2. $\langle \sigma \rangle \lhd D_{n}$
3. $o(a^n)=\frac{o(a)}{(n, o(a))}$
4. In $G_{1} \times G_{2}$ vale $o(a,b)=\text{mcm}(o(a),o(b))$