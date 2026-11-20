# Successione
Sia $X$ topologico, una successione è una funzione $x : \mathbb{N} \to X$ e si denota con $x_{n}n$.

Si dice che  $x_{n}$ converge a $\bar{x}$ e si scrive $\lim\limits_{n \to +\infty} x_{n} = \bar{x}$ se $\forall U \in I(\bar{x})$   $x_{n} \in U$ definitivamente.

# Chiusura per successioni
Sia $Y \subseteq X$, la chiusura per successioni di $Y$ è $\hat{Y} = \{ \bar{x} \in X : \exists y_{n} \in Y \text{ }\text{ }\text{ }\lim\limits_{n \to +\infty} y_{n} = \bar{x} \}$.

$Y$ si dice chiuso per successioni se $\hat{Y} = Y$.

Sia $Y \subseteq X$, allora:
1. $\hat{Y} \subseteq \overline{Y}$
2. $X$ I-numerabile $\implies \hat{Y} = \overline{Y}$

DIMOSTRAZIONE:
1. (1.)
	1. Sia $\bar{y} = \lim\limits_{n \to +\infty} y_{n}$, allora $\forall U \in I(\bar{y})$   $y_{n} \in U$ definitivamente
	2. $y_{n} \in Y \implies U \cap Y \neq \emptyset \implies \bar{y} \in \overline{Y}$
2. (2.)
	1. Sia $\bar{y} \in \overline{Y}$, per ipotesi $\exists$SFI $U_{n}$ numerabile di $\bar{y}$   $U_{n+1} \subseteq U_{n}$
	2. Per costruzione $U_{n} \cap Y \neq \emptyset$, da cui si può scegliere $y_{n} \in U_{n} \cap Y$
	3. Dato $U \in I(\bar{y})$, per definizione di SFI $\exists n_{0}$   $U_{n_{0}} \subseteq U$, da cui $U_{n}\subseteq U_{n_{0}\subseteq U}$   $\forall n \geq n_{0}$
	4. $y_{n} \in U$   $\forall n \geq n_{0}$, da cui $\lim\limits_{n \to +\infty} y_{n} = \bar{y}$

$X$ topologico si dice:
- di Fréchet - Urysohn se $\forall Y \subseteq X$   $\hat{Y} = \overline{Y}$
- sequenziale se $\forall Y \subseteq X$   $Y$ chiuso $\iff Y$ chiuso per successioni

Sia $Y \subseteq X$, allora:
1. $y \in \mathring{Y} \implies \forall x_{n} \in X$ con $\lim\limits_{n \to +\infty} x_{n} = y$ vale $x_{n} \in Y$ definitivamente
2. $X$ di Fréchet - Urysohn $\implies$ il viceversa della precedente proposizione

DIMOSTRAZIONE:
1. $y \in \mathring{Y} \implies Y \in I(Y)$, da cui $x_{n}\to y \implies x_{n} \in Y$ definitivamente
2. $X$ di Fréchet - Urysohn $\implies \hat{X \setminus Y} = \overline{X \setminus Y}$
3. $X \setminus \mathring{Y} = \overline{X \setminus Y}$, quindi sia per assurdo $y \not\in \mathring{Y}$, allora $y \in \overline{X \setminus Y} = \hat{X \setminus Y}$
4. $\exists x_{n} \in X \setminus Y$ con $\lim\limits_{n \to +\infty} x_{n} = y$ che non cade definitivamente in $Y$

# Continuità sequenziale
Siano $X,Y$ topologici, allora $f : X \to Y$ si dice sequenzialmente continua o continua per successioni se $\forall x_{n} \in X$ con $\lim\limits_{n \to +\infty} x_{n} = \bar{x}$ si ha $\lim\limits_{n \to +\infty} f(x_{n}) = f(\bar{x})$.

Siano $X,Y$ topologici e $f : X \to Y$, allora:
1. $f$ continua $\implies f$ sequenzialmente continua
2. $X$ di Fréchet - Urysohn $\implies$ ($f$ continua $\iff f$ sequenzialmente continua)

DIMOSTRAZIONE:
1. (1.)
	1. Siano $x_{n} \in X$ con $x_{n} \to \bar{x}$ e $U \in I(f(\bar{x}))$, ossia $f(\bar{x}) \in \mathring{U} \subseteq U$
	2. Per continuità $\bar{x} \in f^{-1}(\mathring{U})$ che è aperto, quindi $f^{-1}(\mathring{U}) \in I(\bar{x})$ e $x_{n} \in f^{-1}(\mathring{U})$ def.
	3. $f(x_{n}) \in \mathring{U} \subseteq U$ definitivamente, da cui $\lim\limits_{n \to +\infty} f(x_{n}) = f(\bar{x})$
2. (2.)
	1. Sia $A \subseteq Y$ aperto tale che $f^{-1}(A)$ non sia aperto, allora $\exists \bar{x} \in f^{-1}(A) \setminus f^{-1}(\mathring{A})$
	2. Per Fréchet - Urysohn e (1.), $\bar{x} \not\in f^{-1}(\mathring{A}) \implies \exists x_{n} \in X \setminus f^{-1}(A)$   $x_{n} \to \bar{x}$
	3. $x_{n} \not\in f^{-1}(A)$ definitivamente, da cui $\lim\limits_{n \to +\infty} x_{n} = \bar{x}$ ma $f(x_{n}) \not\in A$ definitivamente
	4. $\bar{x} \in f^{-1}(A) \implies f(\bar{x}) \in A$ aperto e $A \in I(f(x))$, cioè $\lim\limits_{n \to +\infty} f(x_{n}) \neq f(\bar{x})$