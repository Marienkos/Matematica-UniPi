# Forza
La dinamica è lo studio del moto dei corpi dal punto di vista delle cause.

Le due grandezze principali sono:
- la forza, che descrive l'interazione tra i corpi, misurata in Newton
- la massa, proprietà intrinseca del corpo

Le 4 interazioni fondamentali sono:
- la gravitazionale
- l'elettro-magnetica
- la nucleare forte
- la nucleare debole

Le forze godono di additività e decrescenza come $\frac{1}{d^2}$. 

# Principi della dinamica Newtoniana
Si definisce la quantità di moto $\vec{p} = m\vec{v}$.

La dinamica gode di 3 principi elaborati da Newton:
1. $\vec{f}_{\text{ris}}=0 \implies$ stato di quiete o di moto rettilineo uniforme
2. $\vec{f} = \dot{\vec{p}}$
3. azione $\implies$ reazione

Un sistema di riferimento si dice inerziale (SRI) se vale il primo principio.

Ogni SR a velocità costante rispetto a un SRI è inerziale.

# Oscillatore armonico
Per le molle vale la legge di Hooke, ossia $\vec{f} = -kx\hat{i}$ con $k$ detta costante elastica.

Inoltre valgono:
- sia $\omega^{2} = \frac{k}{m}$, allora $\ddot{x} + \omega^{2}x=0$
- $x(t) = A\cos(\omega t + \phi)$
- $v(t) = -A\omega\sin(\omega t+\phi)$
- $T = 2\pi \sqrt{ \frac{m}{k} }$

Si può vedere il moto circolare uniforme come la composizione di due moti armonici sfasati di $-\frac{\pi}{2}$.

Si dice posizione di equilibrio un punto con velocità nulla per un tempo indefinito.

Nel caso di un pendolo semplice si hanno:
- $\mathscr s (t) = l\theta(t)$
- $\vec{a}(t) = l \ddot{\theta}\hat{\tau}+l \dot{\theta}^{2}\hat{n}$
- $T = 2\pi \sqrt{ \frac{l}{g} }$

# Vincolo e tensione
Si possono avere vincoli lisci, ossia senza attrito, o scabri con attrito.

In una macchina di Atwood, ossia un filo di massa incomprimibile attorno a un perno, si ha oltre ai vincoli anche la tensione.

Tra i vincoli scabri ci sono l'attrito statico e l'attrito dinamico.

Esiste una $f_{\min}$ tale che con $f\leq f_{\min}$ il corpo è fermo, altrimenti $f_s \leq \mu_{s}N$.

Nel caso dinamico si ha $\vec{f}_{d} = -\mu_{d}N\hat{v}$ e vale sempre $\mu_{d} \leq \mu_{s}$.

In mezzi fiscosi vale la legge di Stokes, ossia $\vec{f} = -\beta \vec{v}$ con $\beta$ coefficiente di viscosità.

In casi non limite si può ignorare l'attrito viscoso e a forza costante si può considerare il corpo di moto uniformemente accelerato.

# Impulso e momento
Si definisce l'impulso $\vec{I}(t_{1},t_{2})=\int_{t_{1}}^{t_{2}} \vec{f}(t) \, dt$.

Per il teorema dell'impulso vale $\vec{I}(t_{1},t_{2}) = \Delta \vec{p}$.

Dati $\vec{V}$ e $\vec{r} = \overline{\Omega A}$ con $\Omega,A$ punti, si definisce il momento $\vec{m}_{\Omega} = \vec{r} \times \vec{V} = rV\sin \theta$.

Si definisce momento angolare $\vec{l}_{\Omega}$ il momento della quantità di moto.

Sia $\vec{\tau}_{\Omega}$ il momento di $\vec{f}$. Per il teorema dell'impulso angolare $\int_{t_{1}}^{t_{2}} \vec{\tau}_{\Omega}(t) \, dt = \Delta \vec{l}_{\Omega}$.

# Densità
Si definisce la densità $\delta$ il rapporto tra massa $m$ e volume $V$.

In un sistema si ha la densità media $\delta(\vec{r}_{i})=\frac{\Delta m_{i}}{\Delta V}$ o nel continuo $\delta(\vec{r})=\lim\limits_{\Delta V \to 0} \frac{\Delta m}{\Delta V}$.

Si definiscono analogamente:
- densità superficiale $\sigma = \lim\limits_{\Delta S \to 0} \frac{\Delta m}{\Delta s}$
- densità lineare $\lambda = \lim\limits_{\Delta l \to 0} \frac{\Delta m}{\Delta l}$

# Sistema di punti materiali
Dati $n$ punti di massa $m_{i}$ e posizione $r_{i}$, si definisce il centro di massa $\vec{R} = \frac{\sum m_{i}r_{i}}{\sum m_{i}}$.

Sono similmente definiti velocità $\vec{V}$, quantità di moto $\vec{P}$ e momento angolare $\vec{L}$.

Si possono estendere le leggi con le equazioni cardinali:
1. $\dot{\vec{P}} = \vec{F}_{\text{esterna}}$
2. $\dot{\vec{L}}_{\Omega} = \vec{\tau}_{\Omega, \text{esterno}} - \vec{v}_{\Omega} \times M\vec{V}$

Un sistema si dice isolato se non agiscono forze esterne.

In un sistema isolato si conservano quantità di moto e momento angolare.

In un sistema continuo si estendono tutte le grandezze tramite integrali.

# Teorema di König
Energia cinetica e momento angolare di un sistema sono pari alle grandezze del centro di massa sommate alle grandezze del sistema rispetto ad esso.

# Urto
Un urto tra due corpi in un sistema isolato si dice:
- elastico, se si conserva l'energia cinetica
- anelastico, se dopo l'urto i due corpi si comportano come un solo corpo

In caso di urto anelastico si ha il sistema:
1. $v_{1} = \frac{m_{1}-m_{2}}{ m_{1}+m_{2} }v_{1_{0}} + \frac{2m_{2}}{m_{1}+m_{2} }v_{2_{0}}$
2. $v_{2} = \frac{2m_{1}}{m_{1}+m_{2}}v_{1_{0}} + \frac{m_{2}-m_{1}}{m_{1}+m_{2}}v_{2_{0}}$

# Moti relativi
Si indica con $\vec{u})_{S}$ il vettore $\vec{u}$ rispetto al sistema di riferimento $S$.

Siano $S$ inerziale e $S'$, allora per la relazione di Poisson vale $\dot{\vec{u}})_{S} = \dot{\vec{u}})_{S'} + \vec{\omega} \times \vec{u}$.

Con la relazione di Poisson si può calcolare la velocità relativa:
- la velocità di $O'$ in $S$ è $\vec{V} = \dot{\vec{R}})_{S}$
- la velocità di trascinamento è $\vec{v}_{\tau} = \vec{V} + \vec{\omega} \times (\vec{r}-\vec{R})$
- la velocità è $\vec{v}(t) = \vec{v}'(t) + \vec{v}_{\tau}(t)$

La velocità di trascinamento è la velocità dei punti solidali a $S'$ misurata in $S$.

Un moto si dice:
- traslazionale se $\vec{\omega}(t)=0$, ossia $\vec{v}_{\tau}=\vec{V}$
- di rotazione pura se $\vec{V}(t)=0$, ossia $\vec{R}(t)$ costante e $O'$ fisso in $S$

Si definisce analogamente l'accelerazione di trascinamento.

Si definisce l'accelerazione di Coriolis $\vec{a} = 2\vec{\omega} \times \vec{v}'$.