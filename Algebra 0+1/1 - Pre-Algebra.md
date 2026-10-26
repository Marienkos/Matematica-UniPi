# Relazione
Sia $A$ insieme, si dice relazione binaria un $\mathfrak{R} \subseteq A\times A$.

Sia $(a,b) \in \mathfrak{R}$, si dice che $a$ è in relazione con $b$ e si scrive $aRb$.

$\mathfrak{R}$ relazione binaria su $A$ si dice:
- totale se $\forall a,b \in A$   $a\mathfrak{R}b \lor b\mathfrak{R}a$
- riflessiva se $\forall a \in A$   $a\mathfrak{R}a$
- simmetrica se $\forall a,b \in A$   $a\mathfrak{R}b \implies b\mathfrak{R} a$
- antisimmetrica se $\forall a,b \in A$   $a\mathfrak{R}b \land b\mathfrak{R}a \implies a=b$
- transitiva se $\forall a,b,c \in A$   $a\mathfrak{R}b\land b\mathfrak{R}c \implies a\mathfrak{R}c$

$\mathfrak{R}$ relazione binaria su $A$ si dice relazione di equivalenza se riflessiva, simmetrica e transitiva.

Siano $\mathfrak{R}$ di equivalenza su $A$ e $a \in A$, si dice classe di equivalenza l'insieme di tutti gli elementi di $A$ equivalenti ad $a$ rispetto a $\mathfrak{R}$ e si denota con $[a]_{\mathfrak{R}}$.

Sia $A$ insieme, $P = \{ \text{sottoinsiemi non vuoti di A} \}$ si dice partizione se:
1. $\bigcup\limits_{p_{i} \in P} p_{i} = A$
2. $\forall p_{1},p_{2} \in P$   $p_{1} \neq p_{2} \implies p_{1} \cap p_{2} = \emptyset$

Siano $A$ insieme e $\mathfrak{R}$ di equivalenza su $A$, l'insieme $\bigcup\limits_{a \in A} [a]_{\mathfrak{R}}$ partiziona $A$.

DIMOSTRAZIONE: Verifica.

Sia $\mathfrak{R}$ di equivalenza su $A$, l'insieme delle classi di equivalenza si dice insieme quoziente di $A$ rispetto a $\mathfrak{R}$ e si denota con $A / \mathfrak{R}$.

Sia $\mathfrak{R}$ di equivalenza su $A$, si definisce insieme di rappresentanti $R$ per $\mathfrak{R}$ tale che:
- $\forall C \in A / \mathfrak{R}$   $|R \cap C| = 1$.

$\mathfrak{R}$ relazione binaria su $A$ si dice relazione di ordine se riflessiva, antisimmetrica e transitiva.

# Funzione