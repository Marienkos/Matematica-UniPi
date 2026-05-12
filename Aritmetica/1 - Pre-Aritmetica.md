# Coefficiente binomiale
Si definisce coefficiente binomiale $\binom{n}{k}$ il numero di sottoinsiemi di $\{ 1,\dots,n \}$ con $k$ elementi.

$\binom{n}{k} = \binom{n}{n-k}$

DIMOSTRAZIONE: A ogni sottoinsieme corrisponde il complementare.

$\forall n \in \mathbb{N}$   $x$ variabile   $(1+x)^n=\sum\limits_{k=0}^{n} \binom{n}{k}x^k$

DIMOSTRAZIONE: Per ottenere $x^k$ bisogna scegliere $k$ volte la $x$ dagli $n$ binomi.

$\binom{n}{k}=\frac{n!}{k!(n-k)!}$

DIMOSTRAZIONE: Combinatoria.

$\binom{n}{k}=\binom{n-1}{k-1}+\binom{n-1}{k}$ e da tale formula deriva il triangolo di Tartaglia.

DIMOSTRAZIONE: Considero un elemento e divido le combinazioni in base al suo contenimento.

# Principio di induzione ed equivalenti
Sia $P(n)$ un predicato su $\mathbb N$. Se valgono:
1. $P(n_0)$
2. $P(n) \implies P(n+1)$
Allora $\forall n>n_0$ vale $P(n)$ per induzione.

Sia $P(n)$ un predicato su $\mathbb{N}$. Se valgono:
1. $P(n_{0})$
2. $P(n_{0}) \land \dots \land P(n) \implies P(n+1)$
Allora $\forall n>n_0$ vale $P(n)$ per induzione forte.

Ogni sottoinsieme non vuoto di $\mathbb{N}$ ammette minimo. Tale affermazione è nota come principio del minimo o assioma del buon ordinamento.

L'induzione, l'induzione forte e il principio del minimo sono equivalenti.

DIMOSTRAZIONE: Si rifanno alla struttura di $\mathbb{N}$ e si può facilmente dimostrare uno con l'altro.

# Successione di Fibonacci
Sia la successione di Fibonacci la successione di numeri naturali definita come:
1. $F_{0}=0$
2. $F_{1}=1$
3. $F_{n+2}=F_{n+1}+F_{n}$   $\forall n \in \mathbb{N}$

Esiste una formula chiusa, in particolare $F_{n}=\frac{1}{\sqrt{ 5 }}\left( \frac{1+\sqrt{ 5 }}{2} \right)^n - \frac{1}{\sqrt{ 5 }}\left( \frac{1-\sqrt{ 5 }}{2} \right)^n$.

DIMOSTRAZIONE: Si veda la risoluzione di successioni per ricorrenza in Analisi 1.
