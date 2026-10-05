# Linguaggio formale
Si definisce alfabeto un insieme di simboli.

Sia $A$ alfabeto, si dice $A$-linguaggio un insieme di stringhe in $A$.

Si definisce linguaggio del primo ordine una terna $(R,F,ar)$ con:
- $R$ insieme dei simboli di relazione
- $F$ insieme dei simboli di funzione
- arietà $ar : R \cup F \to \mathbb{N}$

# Termini e formule
Siano $L = (R,F,ar)$ linguaggio del primo ordine e $\text{Var} = \{ x_{i} \}_{i \in \mathbb{N}}$, si dice $L$-termine una stringa $\alpha$ nell'alfabeto $F \cup \text{Var} \cup \{ (, ), , \}$ tale che vale una tra:
- $\alpha \in \text{Var}$
- $\alpha = f(t_{1},\dots,t_{n})$ con $f \in F$, $n = ar(f)$ e $t_{i}$ $L$-termine

Un simbolo di funzione 0-ario si dice costante.

Un simbolo di relazione 0-ario si dice costante proposizionale.