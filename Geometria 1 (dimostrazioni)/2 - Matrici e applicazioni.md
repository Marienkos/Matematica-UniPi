# Formula delle dimensioni
Considero la base del nucleo e la estendo a base di $V$ con $k$ vettori, che sono base dell'immagine per combinazione lineare.

# Teorema di Rouché - Capelli
Un sistema lineare $A\underline{x} = \underline{b}$ è risolubile $\iff \underline{b} \in \text{Span}A \iff \text{Span}(A|\underline{b}) = \text{Span}A$.

# Algoritmo di Gauss
Le 3 operazioni lasciano invariate sia le soluzioni che lo span delle righe, verificato tramite loro applicazione sulle combinazioni lineari.

# Restrizione come bigezione da $\mathcal{L}(V,W)$ a $W^\mathscr{B}$
Dato un vettore $\underline{v}$ esiste un'unica espressione in coordinate rispetto alla base $\mathscr{B}$, dunque l'applicazione $f$ è univocamente determinata dalla sua restrizione $\mathscr{B}$. Viceversa, si definisce $f$ come proiezione e si verifica che è lineare.

# Algoritmo di Zassenhaus
Siano $U,W \subseteq V$ e $\pi$ la proiezione sulla prima componente. Sia $H = U\times U + W \times 0$. Allora $\pi(H) = U + W$ e $\text{Ker}(\pi|_{H}) = H \cap (0 \times V) = 0 \times (U \cap W)$. Ne consegue che le prime righe sono una base di $U + W$ e le ultime sono una base di $U \cap W$.

# Formula del cambio di base
Date due basi $\mathscr{B} = \{ v_{i} \}$ e $\mathscr{B}'$, un'applicazione $f$ è univocamente determinata dalla sua applicazione a $v_{i}$. Passando alle coordinate si ottiene una combinazione lineare rappresentata da una matrice avente come colonne proprio $[f(v_{i})]_{\mathscr{B}'}$.