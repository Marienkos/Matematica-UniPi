# Corpo rigido
Un corpo è detto rigido se indeformabile.

Un corpo rigido possiede 6 gradi di libertà e il suo moto è determinato dalle equazioni cardinali della meccanica dei sistemi di punti materiali.

Per fare ciò bisogna ricavare $\vec{R}$ e $\vec{\omega}$.

# Momento d'inerzia
Si definisce il momento d'inerzia $I = \sum\limits_{i=1}^{n} m_{i}\delta_{i}^2$.

Il momento angolare possiede una componente perpendicolare e $\vec{L} = I\vec{\omega} + I_{\perp}$.

Passando al continuo $I = \int r^2 \, dm = \int r^2\delta(\vec{r}) \, dV$.

# Teorema di Huygens - Steiner
Siano:
1. $I_{\text{CM}}$ momento d'inerzia rispetto a un asse passante per il centro di massa
2. $I$ momento d'inerzia rispetto a un'asse parallelo a distanza $d$
Allora $I = I_{\text{CM}} + Md^2$.

# Esempi di momenti d'inerzia
Nel caso di un disco omogeneo, cilindro pieno o anello sottile, vale $I= \frac{1}{2}MR^2$.

Nel caso di una barra sottile omogenea, vale $I = \frac{1}{3}Ml^2$.

Nel caso di un cilindro cavo, vale $I = \frac{1}{2}M(R_{1}^2+R_{2}^2)$.

Nel caso di una sfera omogenea, vale $I = \frac{2}{5}MR^2$.

# Dinamica rigida attorno a un asse fisso
Sia $\vec{\omega}(t) = \omega(t)\hat{k}$. Allora si definisce il momento angolare assiale $L_{z}\equiv \vec{L} \cdot \hat{k}$.

Dalle leggi cardinali si evince l'equazione del moto $\tau_{z}=I \ddot{\theta}$.

# Pendolo fisico
Un pendolo fisico o composto è un corpo rigido vincolato a ruotare, senza attrito, attorno a un asse fisso orizzontale non passante per il centro di massa.

Valgono:
- $\tau_{z} = -Mgd\sin \theta$
- $\omega\equiv \sqrt{ \frac{Md}{I}g }$
- $\ddot{\theta}+\omega^{2}\sin \theta=0$
- per piccole oscillazioni $\ddot{\theta}+\omega^{2}\theta = 0$
- $\theta(t)=\theta \sin(\omega t+\phi)$
- lunghezza ridotta $l^* \equiv \frac{I}{Md}$
- $T = 2\pi \sqrt{ \frac{l^*}{g}}$

In termini di Huygens - Steiner si ha $l^* = \frac{I_{\text{CM}}}{Md}+d$.

Se si prende un asse passante per $P_{1}$ distante $d_{1}$ dal centro di massa parallelo all'asse $z$, il periodo non cambia se $l^* \equiv l^*(P) = l^*(P_{1}) \equiv l_{1}^*$.

Il periodo minimo è $T_{\text{min}} = 2\pi \sqrt{ \frac{2}{g}\sqrt{ \frac{I_{\text{CM}}}{M} } }$.

# Lavoro ed energia
Vale $K = \frac{1}{2}MV^2 + \frac{1}{2}I_{\text{CM}}\omega^2$.

Le forze interne compiono lavoro nullo, da cui in un modo rototraslazionale, l'infinitesimo lavoro è $dL = \vec{F} \cdot dR + \tau_{\Omega} \cdot \vec{\omega}dt$.

# Ruota
Sia una ruota con punto di tangenza $p^*$. Si dice puro rotolamento il moto $v^*= 0$.

In puro rotolamento valgono:
- $\vec{V} = -\omega R\hat{i}$
- $K = \frac{3}{4}MR^2$

# Moto su piano scabro
Sia un blocco su un piano scabro. Allora il tempo d'arresto è $t^* = \frac{v_{0}}{\mu_{1}g}$.

Una ruota in puro rotolamento non ha forza d'attrito statico compiente lavoro. Invece l'attrito dinamico compie $L = \Delta E = -\frac{1}{6}Mv_{0}^2$.

Col cilindro similmente:
- $E_{0} = \frac{1}{4}MR^2\omega_{0}^2$
- $E = \frac{1}{12}MR^2\omega^2$
- $L = \Delta E = \frac{1}{6}MR^2\omega_{0}^2$