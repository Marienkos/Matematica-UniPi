# Funzione a più variabili
Una funzione $f(x_{1},\dots,x_{n})$ è detta a $n$ variabili.

Siano $\Omega \subseteq \mathbb{R}^n$ e $f : \Omega \to \mathbb{R}$. Si definisce $\frac{\partial f}{\partial x_{i}} = \lim\limits_{\Delta x_{i} \to 0} \frac{f(x_{1},\dots, x_{i} + \Delta x_{i}, \dots, x_{n}) - f(x_{1},\dots,x_{n})}{\Delta x_{i}}$ e si dice derivata parziale di $f$ rispetto a $x_{i}$.

# Teorema di Schwarz
$f(x,y,z)$ ammette derivata parziale seconda continua $\implies$ $\frac{\partial ^2f}{\partial x \partial y} = \frac{\partial^2f}{\partial y \partial x}$.

# Differenziale esatto
Una forma differenziale $A(x,y,z)dx + B(x,y,z)dy + C(x,y,z)dz$ si dice esatta o totale se, dato $D \subseteq \mathbb{R}^3$, esiste $Q : D \to \mathbb{R}$ detta potenziale tale che:
- $dQ \equiv \frac{\partial Q}{\partial x}dx + \frac{\partial Q}{\partial y}dy + \frac{\partial Q}{\partial z}dz = Adx + Bdy + Cdz$

# Lavoro
Sia $\vec{f}(\vec{r})$ una forza, allora si definisce lavoro della forza $L_{\gamma(A,B)} =  \int_{\gamma} \vec{f} \cdot \, d\vec{r}$

# Teorema delle forze vive o dell'energia cinetica
Sia l'energia cinetica $K = \frac{1}{2}mv^2$, allora $L_{\gamma(A,B)} = \Delta K$.

DIMOSTRAZIONE: Secondo principio della dinamica Newtoniana.

# Forza conservativa
Una forza si dice conservativa se il suo lavoro non dipende da $\gamma$.

Si definisce il gradiente $\vec{\nabla} \equiv \hat{i}\frac{\partial}{\partial x} + \hat{j}\frac{\partial}{\partial y} + \hat{h}\frac{\partial}{\partial z}$.

Si definisce il rotore di un vettore $\vec{\nabla} \times \vec{f} = \det(^t(\hat{i}, \partial, f))$.

Sono equivalenti le seguenti affermazioni:
1. $f$ conservativa
2. $dL$ esatto
3. $\exists U$ energia potenziale tale che $dL = -dU$
4. $\forall\gamma$ linea chiusa   $\oint_{\gamma}\vec{f}\cdot d\vec{r} = 0$
5. $\vec{f} = -\vec{\nabla}U$
6. $\vec{\nabla} \times \vec{f} = 0$

La forza peso è conservativa con $U(z) = mgz$.

La forza elastica è conservativa con $U(x) = \frac{1}{2}kx^2$.

# Teorema di conservazione dell'energia meccanica
Si definisce l'energia meccanica $E = K + U$. Valgono:
- $\Delta E = L_{\gamma}$ delle forze non conservativa
- $f$ conservativa $\implies E$ costante