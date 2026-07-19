# Esistenza e unicità
Si verifica che il determinante soddisfa le condizioni di multilinearità, alternanza e normalizzazione. Ora consideriamo una matrice $A$:
1. Se $A$ ha due righe uguali, $\det A=0$. Infatti per alternanza $\det A = -\det A$.
2. Se $A$ ha una riga nulla, $\det A = 0$.
3. Se a una riga di $A$ si somma il multiplo di un'altra, si ottiene una matrice $B$ tale che $\det B = \det A$.
4. Riducendo a scala tramite mosse di Gauss quindi si ottiene una matrice $S$ con $\det S = \pm \det A$.
5. Se $S$ è singolare, $\det A = 0$.
6. Se $S$ non è singolare, $\det A$ è il prodotto dei termini sulla diagonale principale.
Dunque il determinante è univocamente determinato.

# Criterio di invertibilità
Una matrice $A$ è invertibile $\iff \text{rk}A = n \iff \det A \neq 0$.

# Determinante della trasposta
Utilizzando il determinante come somma del segno per gli elementi della matrice, si utilizza che $\sigma \sigma^{-1}=\text{id}$. Passando alla trasposta, il determinante diventa la somma su $\sigma^{-1}$, che coincide col determinante della matrice originale.

# Sviluppo di Laplace
La funzione definita come lo sviluppo di Laplace soddisfa le condizioni di multilinearità, alternanza e normalizzazione, dunque per unicità del determinante coincide con esso.

# Teorema di Binet
Siano $A$ e $B$ matrici. Se una delle due è singolare vale ovviamente $\det AB = 0$. Ora consideriamo la funzione $\phi(A)=\frac{\det AB}{\det B}$, che soddisfa le condizioni di multilinearità, alternanza e normalizzazione, dunque per unicità del determinante coincide con esso. Allora $\phi(A)=\det A=\frac{\det AB}{\det B} \implies \det AB = \det A \det B$.

# Rango come massimo ordine di minore non nullo
Se $k$ colonne sono linearmente dipendenti, ogni minore di ordine $k$ è nullo. Altrimenti la sottomatrice delle colonne ha rango $k$. Ma il rango per righe coincide col rango per colonne, dunque esiste un minore di ordine $k$ non nullo.