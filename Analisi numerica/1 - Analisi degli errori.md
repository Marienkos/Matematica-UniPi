_"La Matematica è ovunque. PRAISE THE LORD." semicit. Grande Fabio, Emanazione n.2_

# Teorema di rappresentazione in base
Sia $B \in \mathbb{N}$ con $B\geq 2$, allora $\forall x \in \mathbb{R}^n \setminus \{ 0 \}$ esistono unici
1. $p \in \mathbb{Z}$
2. $d_{i} \in \mathbb{N}$  ,  $0 \leq d_{i} \leq B-1$  ,  $i =1,2,\dots$  ,  $d_{1} \neq 0$  ,  $d_{j} \neq B-1$ frequentemente
tali che $x = \text{sgn}(x)B^p \sum\limits_{i=1}^{\infty} d_{i}B^{-i}$

# Numero di macchina o floating point
Dati $B\geq 2$, $t \geq 1$, $m,M>0$ si dice float $\mathscr{F}(t,B,m,M)= \{ 0 \} \cup \{ \pm B^p \sum\limits_{i=1}^{t} d_{i}B^{-i}$, $-m\leq p \leq M\}$.

Si usa la notazione $\text{fl}(x)$ per indicare il troncamento di $x$ al numero di macchina.

Se $p>M$ c'è un errore di overflow, se $p < -m$ c'è un errore di underflow.

L'errore di rappresentazione è definito come $\varepsilon_{x} = \frac{{x-\tilde{x}}}{x}$.

Vale $|x-\tilde{x}|=B^p \sum\limits_{i=t+1}^{\infty} d_{i}B^{-i} =B^pB^{-t-1} \sum\limits_{i=0}^{\infty} d_{t+1+i}B^{-i}<B^{p-t}$.

Di conseguenza $|\varepsilon_{x}|\leq B^{1-t}=u$, detta precisione di macchina.

In doppia precisione $u=2^{-52}$.

# Errore di una funzione
Siano $a,b \in \mathscr{F}$, $\text{op} \in \{ +,-,\cdot, / \}$ in $\mathbb{R}$ e $[\text{op}]$ corrispondenti in $\mathscr{F}$. Allora $a[\text{op}]b = \text{fl}(a\, \text{op}\,b)$.

Siano $c=a \, \text{op} \, b$ e $\tilde{c} = a[\text{op}]b$. Allora $\varepsilon_{c}<u$ ossia $\tilde{c}=c(1+\sigma)=\frac{c}{1+\eta}$ con $|\sigma|<u$ e $|\eta|<u$.

Sia $f : \mathbb{R}^n \to \mathbb{R}$ e dato $x \in \mathbb{R}^n$ sia $\tilde{x}  = \text{fl}(x)$. Si definisce errore inerente $\varepsilon_{\text{in}}=\frac{{f(\tilde{x})-f(x)}}{f(x)}=\frac{f(\tilde{x})}{f(x)}-1$.

Sia $\varphi(\tilde{x})$ il valore calcolato. Si definisce errore algoritmico $\varepsilon_{\text{alg}}=\frac{{\varphi(\tilde{x})-f(\tilde{x})}}{f(\tilde{x})}=\frac{\varphi(\tilde{x})}{f(\tilde{x})}-1$.

Si definisce errore totale $\varepsilon_{\text{tot}}=\frac{{\varphi(\tilde{x})-f(x)}}{f(x)} = (\varepsilon_{\text{alg}}+1)(\varepsilon_{\text{in}}+1)-1 \simeq \varepsilon_{\text{in}}+\varepsilon_{\text{alg}}$.

Sia $f$ approssimabile con Taylor. Allora $\varepsilon_{\text{in}} \simeq c\varepsilon_{x}$ dove $c=\frac{xf'(x)}{f(x)}$ è detto coefficiente di amplificazione. Si estende a $\mathbb{R}^n$ con le derivate parziali.

Sia $s = x_{1} \, \text{op} \, x_{2}$, allora $\tilde{s} = \text{fl}(\tilde{x}_{1} \, \text{op} \, \tilde{x}_{2}) = (\tilde{x}_{1} \, \text{op} \, \tilde{x}_{2})(1+\delta) = (x_{1} \, \text{op} \, x_{2})(1+c_{1}\varepsilon_{1} + c_{2}\varepsilon_{2} + \delta)$.

Si estende lo stesso errore a una generica funzione.

L'errore di una singola operazione in un algoritmo è detto errore locale.

Si può analizzare l'errore all'indietro partendo dalla fine e sostituendo gli errori locali per ottenere la perturbazione necessaria per avvicinarsi al risultato.