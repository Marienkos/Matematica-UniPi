# Equazione differenziale
Equazione la cui incognita è $u(t) : [a,b] \to \mathbb{R}$, quindi sia la relazione sia l'insieme di definizione. Compaiono $t$, $u(t)$ e le sue derivate.

Si dice ordine il massimo ordine di derivazione che compare nell'equazione.

Un'equazione si dice autonoma se $t$ compare solo come argomento di $u$ e derivate.

Un'equazione si dice in forma normale se è nella forma $u^{(k)} =  F(t, u, \dots, u^{(k-1)})$

Un'equazione del primo ordine si dice a variabili separabili se è nella forma $u'(t) = f(t)g(u(t))$

Un'equazione si dice lineare se è nella forma $\sum\limits_{i=0}^{k} a_{i}(t)u^{(i)}(t) = f(t)$, dove:
- $a_{i}(t) : [a,b] \to \mathbb{R}$ sono detti coefficienti
- $f(t) : [a,b] \to \mathbb{R}$ è detto termine forzante

Se in un'equazione lineare $f(t) \equiv 0$ allora si dice omogenea.

Un sistema di $k$ equazioni di ordine 1 è equivalente a un'equazione di ordine $k$ e viceversa.

Tre classi di equazioni differenziali sono facilmente studiabili:
- primo ordine a variabili separabili
- lineari a coefficienti costanti
- lineari del primo ordine

Di solito si omette la $t$ come argomento e si usa la notazione di Newton per le derivate.

# Problema di Cauchy
Sistema di un'equazione differenziale di ordine $k$ e $k$ condizioni iniziali che prescrivono il valore di $u$ e le sue prime $k-1$ derivate in uno stesso $t$.

Sia un problema di Cauchy per un'equazione di ordine $k$ in forma normale e sia il RHS (right-hand side) una funzione continua. Allora esiste almeno una soluzione.

Sia un problema di Cauchy per un'equazione di ordine $k$ in forma normale e sia il RHS una funzione di modulo di continuità superiore alla continuità. Allora la soluzione esiste ed è unica.

Il pennello di Peano è una famiglia di problemi di Cauchy con soluzione non unica.

# Equazione a variabili separabili
La procedura risolutiva è la seguente:
1. Separare le $u$ a sinistra dalle $t$ a destra
2. Integrare rispetto a $u$ a sinistra e rispetto a $t$ a destra
3. Ricavare $u$ in funzione di $t$
4. Determinare il valore di $c$
5. Verificare l'equazione col dato iniziale $u(t_{0}) = u_{0}$
6. Studiare
	1. intervallo massimale di esistenza
	2. life span
	3. tipo di morte

Si dice intervallo massimale di esistenza la parte dell'insieme di definizione di $u$ che contiene il dato iniziale.

Si dice life span nel futuro/passato il sup/inf dell'intervallo massimale di esistenza.

Detto $T$ il life span nel futuro, ci sono 3 tipi di morte:
- esistenza globale nel futuro, se $T = +\infty$
- blow up, se $T < +\infty$ e $\lim\limits_{t \to T^-} u(t) = \pm \infty$
- break down, se $T < +\infty$ e $u$ esce dalla zona in cui RHS ha senso

Di solito al break down è associato $\lim\limits_{t \to T^-} u'(t) = \pm \infty$

Dato il parametro iniziale parametrico, esiste una soglia che divide esistenza globale da blow up.

# Teorema di esistenza (variabili separabili)
Siano $f$ e $g$ funzioni continue e $g(u_{0}) = 0$. Allora la procedura porta a una soluzione.

~={cyan}DIMOSTRAZIONE=~:
1. Sia $F$ una primitiva di $f$ e $\Gamma$ una primitiva di $\frac{1}{g}$
2. $\Gamma$ è invertibile per monotonia. Sia $u(t) = \Gamma^{-1}(F(t)+\Gamma(u_{0})-F(t_{0}))$
3. Si verifica $u(t_{0}) = \Gamma^{-1}(\Gamma(u_{0})) = u_{0}$
4. $u'(t) = \frac{F'(t)}{\Gamma'(\Gamma^{-1}(F(t)+\Gamma(u_{0})-F(t_{0})))} = f(t)g(\Gamma^{-1}(F(t)+\Gamma(u_{0})-F(t_{0}))) = f(t)g(u(t))$

# Teorema di esistenza e unicità (variabili separabili)
Siano $f$ e $g$ funzioni continue e $g(u_{0}) = 0$. Allora la procedura porta all'unica soluzione.

~={cyan}DIMOSTRAZIONE=~:
1. Sia $f : [t_{0}-\delta_{0},t_{0}+\delta_{0}] \to \mathbb{R}$ continua $\forall \delta_{0}>0$
2. Sia $g: [u_{0}-r,u_{0}+r] \to \mathbb{R}$ continua $\forall r>0$
3. Sia $u : [t_{0}-\delta_{1}, t_{0}+\delta_{1}] \to \mathbb{R}$ di classe $C^1$ e soluzione $\forall t \in [t_{0}-\delta_{1},t_{0}+\delta_{1}]$ con $0<\delta_{1}\leq\delta_{0}$
4. Per ipotesi $g(u(t)) \neq 0$ per $t=t_{0}$
5. $g(u(t)) \neq 0$   $\forall t\in [t_{0}-\delta_{1},t_{0}+\delta_{1}]$
6. Dato il tipo di equazione, vale $\frac{u'(t)}{g(u(t))} = f(t)$
7. $\forall t \in [t_{0}-\delta_{1}, t_{0}+\delta_{1}]$   $\int_{t_{0}}^{t} \frac{u'(s)}{g(u(s))} \, ds = \int_{t_{0}}^{t} f(s) \, ds$
8. Data $\Gamma$ primitiva di $g$ e $F$ primitiva di $f$, vale $\Gamma(u(t))-\Gamma(u(t_{0})) = F(t)-F(t_{0})$
9. $\Gamma(u(t)) = F(t)+\Gamma(u_{0}) - F(t_{0}) = F(t) + c$

# Equazione lineare omogenea
Se   $a_{k}(t) \neq 0$   $\forall t \in [a,b]$   la soluzione esiste su tutto $[a,b]$.

Con dati di Cauchy nulli l'unica soluzione è $u(t) \equiv 0$.

Risolvere l'equazione significa determinare il nucleo di $L : C^k([a,b]) \to C^0([a,b])$.

~={cyan}DIMOSTRAZIONE=~: $L$ è un'applicazione lineare.

Le $k$ soluzioni formano una base di uno spazio vettoriale.

~={cyan}DIMOSTRAZIONE=~:
1. Il nucleo di un'applicazione lineare è uno spazio vettoriale
2. Fissato $t_{0} \in [a,b]$ si definisce $u_{i}(t)$ la soluzione con i dati di Cauchy $u_{i}^{(j)}(t_{0}) = \delta_{i,j+1}$
3. Tutte le $u_{i}(t)$ sono generatori
4. Tutte le $u_{i}(t)$ sono linearmente indipendenti
5. Le soluzioni sono una base dello spazio e sono $k$

La procedura risolutiva è la seguente:
1. Si passa al polinomio caratteristico, definito da $u^{(k)}(t) \mapsto x^k$
2. Si guardano le $k$ radici del polinomio con molteplicità $m$
	- ogni radice $\lambda \in \mathbb{R}$ dà $t^{n}e^{\lambda t}$ per ogni $0 \leq n < m$
	- ogni coppia $\alpha\pm i\beta \in \mathbb{C}$ dà $t^ne^{\alpha t}\cos(\beta t), t^ne^{\alpha t}\sin(\beta t)$ per ogni $0 \leq n < m$

# Equazione lineare non omogenea
Sia $\bar{u}(t)$ una soluzione qualsiasi dell'equazione non omogenea e $U(t)$ la soluzione generale dell'equazione omogenea. La soluzione generale è del tipo $u(t) = \bar{u}(t) + U(t)$

Per trovare $\bar{u}(t)$ si può:
- tentare a indovinare
- usare la variazione delle costanti

Per la variazione delle costanti la procedura è la seguente (caso di ordine 2):
1. Siano $\alpha$ e $\beta$ le radici del polinomio caratteristico dell'omogenea
2. Si pone $\bar{u}(t) = a(t)e^{\alpha t} + b(t)e^{\beta t}$
3. Si calcola $\bar{u}'(t)$ e si pone che la somma dei termini derivati si annulli
4. Si deriva di nuovo e si sostituisce
5. Si ricava un sistema lineare da risolvere

# Equazione lineare di primo ordine
Sia $\dot{u} + a(t)u = b(t)$ e $A'(t) = a(t)$. La soluzione generale è $u(t) = ce^{-A(t)}+e^{-A(t)}\int e^{A(s)}b(s) \, ds$

Se ho la condizione di Cauchy $u(t_{0}) = u_{0}$, allora è $u(t) = u_{0}e^{-A(t)}+e^{-A(t)}\int_{t_{0}}^{t} e^{A(s)}b(s) \, ds$

~={cyan}DIMOSTRAZIONE=~: Derivare e sostituire.