# Linguaggio topologico in uno spazio metrico
Sia $A \subseteq \mathbb{R}$ un sottoinsieme, $x_{0} \in \mathbb{R}$ e dato un certo $r$, sia $i_{x_0,r} = (x_{0}-r,x_{0}+r)$. Allora $x_{0}$ si dice:
- interno ad $A$ se $\exists r > 0$   $i_{x_{0},r} \subseteq A$
- aderente ad $A$ se $\forall r > 0$   $i_{x_{0},r} \cap A \neq \emptyset$
- di frontiera o sul bordo di $A$ se aderente ad $A$ e a $\mathbb{R} \setminus A$
- isolato in $A$ se $\exists r>0$   $i_{x_{0},r} \cap A = \{ x_{0} \}$
- di accumulazione per $A$ se $\forall r>0$   $(i_{x_{0},r} \cap A) \setminus \{ x_{0} \} \neq \emptyset$

Sia $A \subseteq \mathbb{R}$, allora siano:
- $\text{Int}(A)$ o $\mathring{A}$ l'insieme dei punti interni ad $A$
- $\text{Clos}(A)$ o $\bar{A}$ l'insieme dei punti aderenti ad $A$
- $\partial A$ l'insieme dei punti di frontiera di $A$
- $\text{Isol}(A)$ l'insieme dei punti isolati in $A$
- $D(A)$ l'insieme dei punti di accumulazione per $A$

$A$ si dice:
- aperto se $A = \text{Int}(A)$
- chiuso se $A = \text{Clos}(A)$

Valgono:
1. $\text{Int}(A) \subseteq A \subseteq \text{Clos}(A)$
2. $\partial A \subseteq \text{Clos}(A)$
3. $\text{Clos}(A) = \text{Int}(A) \cup \partial A$ con unione disgiunta
4. $\text{Clos}(A) = \text{Isol}(A) \cup D(A)$ con unione disgiunta

DIMOSTRAZIONE: Definizioni.

Valgono su intersezioni e unioni finite:
1. Se $A$ e $B$ sono aperti, allora $A \cap B$ e $A \cup B$ sono aperti
2. Se $A$ e $B$ sono chiusi, allora $A \cap B$ e $A \cup B$ sono chiusi

DIMOSTRAZIONE: Definizioni.

Valgono:
1. L'unione di infiniti aperti è aperta
2. L'intersezione di infiniti chiusi è chiusa

# Caratterizzazione con le successioni
Sia $A \subseteq \mathbb{R}$ e $x_{0} \in \mathbb{R}$. Allora:
1. $x_{0} \in \text{Int}(A) \iff \forall \{ x_{n} \} \subseteq \mathbb{R}$   $[x_{n} \to x_{0} \implies x_{n} \in A \text{ definitivamente}]$
2. $x_{0} \in \text{Clos}(A) \iff \exists \{ x_{n} \} \subseteq A$   $x_{n} \to x_{0}$
3. $x_{0} \in \partial A \iff x_{0} \in \text{Clos}(A) \land x_{0} \in \text{Clos}(\mathbb{R} \setminus A)$
4. $x_{0} \in \text{Isol}(A) \iff \forall \{ x_{n} \} \subseteq A$   $[x_{n} \to x_{0} \implies x_{n} = x_{0} \text{ definitivamente}]$
5. $x_{0} \in D(A) \iff \exists \{ x_{n} \} \subseteq A \setminus \{ x_{0} \}$   $x_{n}\to x_{0}$

DIMOSTRAZIONE: Definizione di limite.

# Linguaggio topologico relativo
Sia $A \subseteq B \subseteq \mathbb{R}$. Allora si dice, relativamente a $B$:
- $x_{0}$ interno ad $A$, ossia $x_{0} \in \text{Int}_{B}(A)$, se $\exists r>0$   $i_{x_{0},r} \cap B \subseteq A$
- $A$ aperto se $A = \text{Int}_{B}(A)$

La definizione si può estendere al resto del linguaggio.

# Continuità
Sia $A \subseteq \mathbb{R}$ e $f : A \to \mathbb{R}$. Sia $x_{0} \in  A$. Allora $f$ è continua in $x_{0}$ se:
1. ($\varepsilon / \delta$) $\forall \varepsilon>0$   $\exists \delta>0$   $\forall x \in i_{x_{0},\delta} \cap A$   $f(x) \in i_{f(x_{0}), \varepsilon}$
2. (Successioni) $\forall \{ x_{n} \} \subseteq A$   $[x_{n}\to x_{0} \implies f(x_{n}) \to f(x_{0})]$
3. (Limiti) $x_{0} \in \text{Isol}(A) \lor [x_{0} \in D(A) \land \lim\limits_{x \to x_{0}} f(x) = f(x_{0})]$
4. (Aperti) $\forall U \subseteq \mathbb{R}$ aperto con $f(x_{0}) \in U$ vale $x_{0} \in \text{Int}_{A}(f^{-1}(U))$

DIMOSTRAZIONE: Definizioni.

Se $f$ e $g$ sono continue, allora $g \circ f$ è continua.

DIMOSTRAZIONE: $x_{n} \to x_{0} \implies f(x_{n}) \to f(x_{0}) \implies g(f(x_{n})) \to g(f(x_{0}))$ per continuità.