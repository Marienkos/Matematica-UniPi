# Base come insieme linearmente indipendente massimale
Sia $\mathscr{B} \subseteq V$  linearmente indipendente massimale. Allora $\underline{v} \in V \setminus \mathscr{B} \implies \underline{v} \in \text{Span}\mathscr{B}$ dunque $\mathscr{B}$ genera $V$ ed è per definizione una base.

# Base come insieme di generatori minimale
Sia $\mathscr{B} \subseteq V$ di generatori minimale. Se non fosse linearmente indipendente $\underline{v} \in \mathscr{B} \implies \underline{v} \in \text{Span}(\mathscr{B}\setminus \underline{v})$, ma allora essi lo genererebbero e $\mathscr{B}$ non sarebbe un insieme di generatori minimale. Dunque per assurdo $\mathscr{B}$ è linearmente indipendente ed è per definizione una base.

# Esistenza della base in spazi finitamente generati
Uno spazio vettoriale $V$ è generato da $V$. Se esistono sottoinsiemi che generano $V$, il minimale di essi è la base. Altrimenti $V$ è la base.

# Algoritmo di scambio
Siano $A$ e $B$ insiemi linearmente indipendenti con $B \subseteq \text{Span}A$. Sia $B' \subseteq A$ di cardinalità uguale a quella di $B$. L'insieme $A' = (A \setminus B') \cup B$ è linearmente indipendente e preserva lo span di $A$. Infatti ci si può ridurre al caso della sostituzione un vettore alla volta, che mantiene lo span in quanto combinazione lineare degli altri vettori.

# Uguale cardinalità delle basi
Grazie all'algoritmo di scambio si ottiene, date due basi $\mathscr{B}$ e $\mathscr{B}'$ nei ruoli di $A$ e $B$, che $\#\mathscr{B} \leq \#\mathscr{B}'$. Per simmetria si ha che $\#\mathscr{B} = \#\mathscr{B}'$.

# Somma come span dell'unione delle basi
Siano $A$ e $B$ di basi $\mathscr{B}$ e $\mathscr{B}'$. L'insieme $A + B$ è dato dalle combinazioni lineari dei vettori di $A$ e $B$, a loro volta combinazioni lineari di $\mathscr{B}$ e $\mathscr{B}'$. L'insieme $\mathscr{B} \cup \mathscr{B}'$ dunque genera $A + B$.

# Formula di Grassmann
Siano $A$ e $B$ di basi $\mathscr{B}$ e $\mathscr{B}'$. La base di $A+B$ è $\mathscr{B} \cup \mathscr{B}'$, di cardinalità pari alla somma delle cardinalità di $\mathscr{B}$ e $\mathscr{B}'$ meno i vettori presenti nell'intersezione, contati una volta.