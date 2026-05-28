# Velocità
La cinematica è lo studio dei moti dei corpi.

Data l'origine $O$ e un punto $P \equiv (x,y,z) \in \gamma$ traiettoria, si definiscono:
- il vettore posizione $\vec{r} = \overline{OP}$
- la legge oraria $\vec{r} = \vec{r}(t)$
- la velocità media $\vec{v}_{m}(t, t+\Delta t) = \frac{\Delta \vec{r}}{\Delta t}$
- la velocità istantanea $\vec{v} = \frac{d\vec{r}}{dt} = \dot{\vec{r}}$

Dati due punti $\Omega, P$ su $\gamma$ si definisce l'ascissa curvilinea $\mathscr{s}$ tale che $|\mathscr{s}|$ è la lunghezza dell'arco tra $\Omega$ e $P$.

Si definisce velocità scalare $v_{s} = \dot{\mathscr{s}}$.

Sia $\hat{\tau} = \frac{d\vec{r}}{d\mathscr{s}}$. Allora $\vec{v}=v_{s}\hat{\tau}$.

# Accelerazione
Si definisce accelerazione $\vec{a}=\dot{\vec{v}}$ e accelerazione scalare $a_{s} = \dot{v}_{s}$.

La quantità $\frac{d\hat{\tau}}{d\mathscr{s}}$ caratterizza la curva ed è perpendicolare a $\hat{\tau}$.

$\frac{d\hat{\tau}}{d\mathscr{s}} = \frac{1}{\rho}\hat{n}$, dove $\rho$ è il raggio del cerchio osculatore, ossia il raggio della circonferenza che meglio approssima la curva localmente.

Si definiscono l'accelerazione:
- tangenziale $a_{s}\hat{\tau}$
- centripeta $\frac{v^2}{\rho}\hat{n}$

# Moto rettilineo
Se uniforme $\vec{v}$ costante e vale $\vec{r}(t) = \vec{v}t+\vec{r}_{0}$.

Se uniformemente accelerato $\vec{a}$ costante e valgono:
- $\vec{v}(t) = \vec{a}t + \vec{v}_{0}$
- $\vec{r}(t) = \frac{1}{2}\vec{a}t^2 + \vec{v}_{0}t + \vec{r}_{0}$
- $\Delta \vec{v}^2 = 2\vec{a}\Delta \vec{r}$

Un corpo in caduta libera da un'altezza $h$ è uniformemente accelerato da $g$:
- tempo di caduta $\tau_{c} = \sqrt{ \frac{2h}{g} }$
- velocità finale $v_{y} = -\sqrt{ 2gh }$
- tempo di salita $\tau_{s} = \frac{v_{0}}{g}$
- quota massima $h_{\text{max}} = -\frac{1}{2}g\tau^2+v_{0}\tau+h_{0}$

# Moto parabolico
Il moto è uniforme in $x$ e uniformemente accelerato in $y$. Dato $\alpha$ l'angolo iniziale:
- ascissa di quota massima $x_{\text{max}} = \frac{v_{0}^2}{2g}\sin 2\alpha$
- quota massima $h_{\text{max}} = \frac{(v_{0}\sin\alpha)^2}{2g}$
- tempo di salita $\tau_{s} = \frac{v_{0}\sin\alpha}{g}$
- tempo di volo $\tau_{v} = \frac{2v_{0}\sin\alpha}{g}$
- gittata $R = \frac{v_{0}^2\sin2\alpha}{g}$

# Moto circolare
Sia $\gamma$ una circonferenza di raggio $R$. Allora
- $\hat{r}(t) = \cos\theta(t)\hat{i} + \sin\theta(t)\hat{j}$
- $\vec{r} = R\hat{r}$
- $\mathscr{s}=R\theta$
- velocità angolare $\vec{\omega} = \dot{\theta}\hat{k}$
- $v_{s} = R\omega$
- $\vec{v} = v_{s}\hat{\tau}$

Se uniforme $\omega$ costante e valgono:
- $\theta(t) = \omega t + \theta_{0}$
- periodo $T = \frac{2\pi}{|\omega|}$
- frequenza $f = \frac{1}{T}$
- $\vec{a} = -\omega^2\vec{r}$