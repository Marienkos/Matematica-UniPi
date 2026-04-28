# Proposizione
Frase avente valore di verità vero o falso.

Le possibili operazioni sono: negazione, and, or, xor, implicazione

$p \implies q$ ha la stessa tabella di verità di $\neg q \implies \neg p$ e su tale principio si basa la dimostrazione per assurdo.

# Predicato
Proposizione parametrizzata tramite quantificatori.

I possibili quantificatori sono: per ogni, esiste almeno un, esiste ed è unico.

$\neg(\forall x\; P(x))$ è come dire $\exists x\; \neg P(x)$ e viceversa.

# Principio di induzione
Sia P(n) un predicato sui naturali, allora vale:
$$P(n_0) \land (P(n) \implies P(n+1)) \implies \forall n>n_0 \;P(n)$$

# Disuguaglianza di Bernoulli
Vale $(1+x)^n \geq 1+nx$