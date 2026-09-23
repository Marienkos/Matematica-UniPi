# Invarianza
Al cambio di base per similitudine, per Binet il determinante si annulla per l'inverso e rimane il determinante della matrice simile.

# Molteplicità algebrica e geometrica
La base di un autospazio può essere estesa a base dello spazio vettoriale, componendo una matrice associata dove sulla diagonale compaiono tanti autovalori almeno quanto la molteplicità geometrica.

# Criterio di diagonalizzabilità
$f$ diagonalizzabile $\iff$ $V$ si decompone come somma diretta degli autospazi $\iff$ la somma delle molteplicità geometriche è la dimensione di $V$. Dunque anche la somma delle molteplicità algebriche deve essere uguale.

# Criterio di simultanea diagonalizzabilità
Se esiste una base che diagonalizza entrambe le matrici associate a $f$ e $g$, allora esse commutano. D'altronde se commutano, anche $f-\lambda \text{id}$ e $g$ commutano e gli autospazi di $f$ sono $g$-invarianti. La restrizione di $g$ a ciascuno di essi è diagonalizzabile, quindi esiste una base che le diagonalizza. L'unione di queste basi diagonalizza sia $f$ che $g$.

# Criterio di triangolarizzabilità
Si induce sulla dimensione di $V$. Se il polinomio caratteristico è riducibile, ha una radice in $\mathbb{K}$ e $f$ ha un autovalore di autovettore completabile a base di $V$.

# Teorema di Hamilton - Cayley
Data una matrice $A$, vale $AA' = \det A*I$ dove $A'$ è la matrice (aggiunta) trasposta dei cofattori. Dunque data $B$ aggiunta di $A-\lambda\text{id}$ vale $(A-\lambda\text{id})B = \det(A-\lambda\text{id})*I = p_{a}(\lambda)*I$. Allora $B$ si sviluppa come potenze di $\lambda$ e il polinomio caratteristico si annulla.

# Teorema della forma canonica di Jordan
Si può decomporre $V$ in sottospazi invarianti tali che la restrizione a ciascuno di essi ha solo un autovalore, quindi $f-\lambda_{i}\text{id}$ è nilpotente. Tali sottospazi sono gli autospazi generalizzati.