# Carta affine
In $\mathbb{P}^n(\mathbb{K})$ a ogni $i = 0,\dots,n$ corrisponde un iperpiano coordinato $H_{i}=\{ x_{i}=0 \}$.

Si denota con $U_{i}=\mathbb{P}^n(\mathbb{K}) \setminus H_{i} = \{ x_{i} \neq 0 \}$.

Si definiscono:
- $i$-esima carta affine $j_{i} : \mathbb{K}^n \to U_{i} : (y_{1},\dots y_{i}) \mapsto [y_{1}, \dots, y_{i}, 1, y_{i+1},\dots,y_{n}]$
- con $x_{i} \neq 0$ l'inversa $j_{i}^{-1} : U_{i} \to \mathbb{K}^n : [x_{0},\dots,x_{n}] \mapsto \left( \frac{x_{0}}{x_{i}},\dots, \hat{\frac{x_{i}}{x_{i}}},\dots, \frac{x_{n}}{x_{i}} \right)$

$j_{i}$ e $j_{i}^{-1}$ sono ben definite e inverse l'una dell'altra.

DIMOSTRAZIONE:
1. $j_{i}$ ben definita per costruzione
2. $j_{i}^{-1}$ ben definita perché cambiando rappresentante non cambiano i rapporti
3. $j_{i}^{-1} \circ j_{i} (y_{1},\dots,y_{n}) = j_{i}^{-1}[y_{1},\dots,y_{i},1,y_{i+1},\dots,y_{n}] = (y_{1},\dots,y_{n})$
4. $j_{i}\circ j_{i}^{-1} ([x_{0},\dots,x_{n}]) = j_{i}\left( \frac{x_{0}}{x_{i}},\dots, \hat{\frac{x_{i}}{x_{i}}},\dots, \frac{x_{n}}{x_{i}} \right) = [x_{0},\dots,x_{n}]$

Fissato $i$ si può scrivere $\mathbb{P}^n(\mathbb{K})=U_{i} \cup H_{i}$, quindi si può pensare a:
- $\mathbb{P}^n(\mathbb{K})$ come ampliamento di $\mathbb{K}^n$ con punti all'infinito o impropri
- $H_{i} =\mathbb{P}^{n-1}(\mathbb{K})$ come iperpiano all'infinito o insieme delle direzioni in $\mathbb{K}^n$

Per convenzione $U_{0}$ è usato per pensare $\mathbb{K}^n$ dentro $\mathbb{P}^n(\mathbb{K})$.

# Affine $\longleftrightarrow$ proiettivo
Sia $S \subseteq \mathbb{P}^n({\mathbb{K})}$ sottospazio proiettivo non contenuto in $H_{0}$. Allora:
1. $j_{0}^{-1}(S \cap U_{0}) \subseteq \mathbb{K}^n$ sottospazio affine di $\mathbb{K}^n$ chiamato parte affine di $S$.
2. $\dim j_{0}^{-1}(S \cap U_{0}) = \dim S$.

DIMOSTRAZIONE:
1. Sottospazio affine
	1. Sia $k = \dim S$ e $y=(y_{1},\dots,y_{n}) \in \mathbb{K}^n$
	2. $S$ luogo delle soluzioni di un sistema omogeneo $Ax=0$ di rango $n-k$
	3. $y \in j_{0}^{-1}(S \cap U_{0}) \iff j_{0}(y) \in S \cap U_{0} \iff Ay = -A^0$
	4. $j_{i}^{-1}(S \cap U_{0})$ sottospazio affine di $\mathbb{K}^n$
2. Dimensione
	1. La matrice completa del sistema ha rango $n-k$
	2. $S \cap U_{0} \neq 0$ quindi per Rouché - Capelli la seconda matrice dei coefficienti ha rango $n-k$
	3. $\dim$ spazio delle soluzioni del sistema è $n-(n-k) = k$

Sia $Z \subseteq \mathbb{K}^n$ sottospazio affine non vuoto. Allora:
1. $\exists!\bar{Z} \subseteq \mathbb{P}^n(\mathbb{K})$ non contenuto in $H_{0}$ la cui parte affine è $Z$ detto chiusura proiettiva di $Z$.
2. $\dim \bar{Z} = \dim Z$.

DIMOSTRAZIONE:
1. Dimensione
	1. Sia $k = \dim Z$
	2. $Z$ è descritto da un sistema lineare non omogeneo $Ay = b$
	3. Sia $\bar{Z}$ descritto dal sistema lineare omogeneo $(-b \mid A)x = 0$
	4. Per Rouché - Capelli il rango di $(-b \mid A)$ è $n-k$
	5. $\dim\bar{Z} = k$ e la parte affine è $Z$
2. Unicità
	1. Sia $\bar{Z}' \neq \bar{Z}$ sottospazio proiettivo con parte affine $Z$
	2. $\bar{Z} \cap \bar{Z}'$ sottospazio proiettivo con $\dim(\bar{Z} \cap \bar{Z}')<k$ con parte affine $Z$
	3. Assurdo poiché $\dim Z = k$

Sia $G = \{ f \in \mathbb{P}\text{GL}_{n+1}(\mathbb{K}) : f(U_{0})=U_{0} \}$. Allora fissata $U_{0} \cong j_{0}(\mathbb{K}^n)$, la mappa $\psi : G \to \text{Aff}(\mathbb{K}^n)$ che manda $f \mapsto f |_{U_{0}}$ è un isomorfismo di gruppi.

DIMOSTRAZIONE:
1. $f(U_{0}) \subseteq U_{0}$ per costruzione di $G$, per cui $f|_{U_{0}} : U_{0} \to U_{0}$
2. $f = [\varphi]$ con $\varphi : \mathbb{K}^{n+1} \to \mathbb{K}^{n+1}$ lineare invertibile
3. Per iniettività di $f$ vale $f(U_{0})=U_{0} \iff f(H_{0}) = H_{0} \iff \varphi(W_{0}) = W_{0}$
4. Data la base canonica $\mathscr{B}$ di $\mathbb{K}^{n+1}$, ciò equivale a $\varphi(\text{Span}\mathscr{B})=\text{Span}\mathscr{B}$
5. $\varphi$ è rappresentato da $A = \left(\begin{smallmatrix} \lambda & 0 \\ b & B \end{smallmatrix}\right)$ con $B \in \mathscr{M}_{n}(\mathbb{K})$
6. Poiché $0 \neq \det A = \lambda \det B$, vale $B \in \text{GL}_{n}(\mathbb{K})$
7. Sia $\lambda =1$, allora $A = \left(\begin{smallmatrix} 1 & 0 \\ A & B \end{smallmatrix}\right)$ e si può calcolare $f|_{U_{0}}$ come $j_{0}^{-1}\circ f \circ j_{0}(x)$ con $x \in \mathbb{K}^n$
8. $j_{0}^{-1}\circ f \circ j_{0}(x) = j_{0}^{-1} \circ f([1,x_{1},\dots,x_{n}]) = j_{0}^{-1}([\varphi \left(\begin{smallmatrix} 1 \\ x \end{smallmatrix}\right)]) = j_{0}^{-1}([\left(\begin{smallmatrix} 1 & 0 \\ b & B \end{smallmatrix}\right) \left(\begin{smallmatrix} 1 \\ x \end{smallmatrix}\right)]) = Bx+b$
9. $f|_{U_{0}}$ è nella forma $Bx+b$ e dunque affinità
10. $\psi$ omomorfismo in quanto la restrizione commuta con la composizione
11. $\psi$ surgettiva per i calcoli precedenti
12. $\psi$ iniettiva per ragionamenti sull'identità

# Dualità
Dato $\mathbb{P}(V)$ si definisce il suo proiettivo duale $\mathbb{P}(V)^* := \mathbb{P}(V^*)$.

$\exists \mathbb{P}(V^*) \longleftrightarrow \{ \text{iperpiani di }\mathbb{P}(V) \}$ bigettiva

DIMOSTRAZIONE:
1. $[\varphi] \in \mathbb{P}(V^*) \implies \varphi \neq 0 \implies \text{Ker}\varphi$ iperpiano di $V \implies \mathbb{P}(\text{Ker}\varphi)$ iperpiano di $\mathbb{P}(V)$
2. Ogni iperpiano di $V$ è nucleo di un funzionale non nullo

Sia $[a_{0},\dots,a_{n}] \in \mathbb{P}^n(\mathbb{K}^*)$, gli corrisponde l'iperpiano $\{ a_{0}x_{0}+\dots+a_{n}x_{n}=0 \} \subseteq \mathbb{P}^n(\mathbb{K})$.

DIMOSTRAZIONE: Passaggio a $V$ e $V^*$.

Si definisce $\delta_{k} : \{ k\text{-sottospazi proiettivi di }\mathbb{P}(V) \} \to \{ n-k-1\text{-sottospazi proiettivi di }\mathbb{P}(V)^* \}$ data da $\mathbb{P}(W) \mapsto \mathbb{P}(\text{Ann}W)$.

DIMOSTRAZIONE: $\dim\mathbb{P}(W) = k \implies \dim W = k+1 \implies \dim \text{Ann}W = n-k$.

$\delta_{n-1}$ associa iperpiani di $\mathbb{P}(V)$ ai singoletti $\{ P \}$ di $\mathbb{P}(V)^*$.

$\delta_{k}$ bigettiva   $\forall k = -1, 0, \dots, n$.

DIMOSTRAZIONE: $\text{Ann}W = \text{Ann}W' \implies W = W'$ e riflessioni sui sottospazi di $V^*$.

Si definisce $\delta : \{ \text{sottospazi proiettivi di }\mathbb{P}(V) \} \to \{ \text{sottospazi proiettivi di }\mathbb{P}(V)^* \}$ bigettiva.

# Principio di dualità
Sia $P$ enunciato su sottospazi proiettivi di $\mathbb{P}(V)$, relazioni di inclusione tra di essi e loro dimensioni. Sia $P^*$ enunciato duale di $P$ ottenuto da $P$ tramite le seguenti sostituzioni:
1. $\mathbb{P}(V) \longleftrightarrow \mathbb{P}(V)^*$
2. $\cdot\subseteq \cdot \longleftrightarrow \cdot \supseteq \cdot$
3. $L(\cdot,\cdot) \longleftrightarrow \cdot \cap \cdot$
4. $\dim = k \longleftrightarrow \dim = n-k-1$
Allora $P$ vero $\iff P^*$ vero.

DIMOSTRAZIONE: Corrispondenza di dualità con $\delta$.

# Sistema lineare
Un sistema lineare in $\mathbb{P}(V)$ è un insieme di iperpiani di $\mathbb{P}(V)$ che tramite dualità corrisponde a un sottospazio proiettivo di $\mathbb{P}(V)^*$.

La dimensione del sistema è la dimensione del sottospazio corrispondente.

Se la dimensione è 1, il sistema lineare si chiama fascio.

Siano $S \subseteq \mathbb{P}(V)$ sottospazio e $P \subseteq \mathbb{P}(V)$ iperpiano, allora $S \subseteq P \iff \delta(P) \subseteq \delta(S)$. Dunque $\delta(S)$ si dice sistema lineare di centro $S$ ed è l'insieme di tutti e soli gli iperpiani che contengono $S$.

Per dualità, tutti i sistemi lineari di iperpiani sono della forma $\delta(S)$ con $S$ sottospazio di $\mathbb{P}(V)$.

Sia $n = \dim \mathbb{P}(V)$, allora $\exists \{ k\text{-sottospazi proiettivi di }\mathbb{P}(V) \} \to \{ n-k-1\text{-sistemi lineari} \}$ bigettiva data da $S \to \delta(S)$ con inversa $\mathscr{L} \to \text{centro}(\mathscr{L}) = \bigcap\limits_{P \in \mathscr{L}} P$.

# Proiettività duale
Sia $f : \mathbb{P}(V) \to \mathbb{P}(W)$ isomorfismo proiettivo tale che $f = [\varphi]$. Si hanno:
- $f_{ip}$ che manda iperpiani di $\mathbb{P}(V)$ in iperpiani di $\mathbb{P}(W)$
- $f^* = [\varphi^*]$ con $\varphi^*$ duale o trasposta di $\varphi$ tale che $\varphi^*(\alpha) = \alpha \circ \varphi$
Inoltre $f^* = f_{ip}^{-1}$.

DIMOSTRAZIONE:
1. $f^*$ manda iperpiani di $\mathbb{P}(W)$ in iperpiani di $\mathbb{P}(V)$ previa identificazione
2. $\text{Ker}\varphi^*(\alpha) = \text{Ker}(\alpha \circ \varphi) = \{ v \in V : \alpha \circ \varphi(v)=0 \} = \{ v \in V : \varphi(v) \in \text{Ker}\alpha \} = \varphi^{-1}(\text{Ker}\alpha)$.
3. Sia $H = \mathbb{P}(\text{Ker}\alpha)$ iperpiano di $\mathbb{P}(W)$
4. $f^*(H)=f^*([\alpha])=[\varphi^*(\alpha)]=\mathbb{P}(\text{Ker}\varphi^*(\alpha))=\mathbb{P}(\varphi^{-1}(\text{Ker}\alpha))=f^{-1}(\mathbb{P}(\text{Ker}\alpha))=f^{-1}_{ip}(H)$

Le matrici associate a $f$ e $f^*$ sono una la trasposta dell'altra.

# Rapporto semplice
Siano $A$ retta affine e $P_{1},P_{2},P_{3} \in A$ con $P_{1} \neq P_{2}$. Si definisce il rapporto semplice $[P_{1},P_{2},P_{3}]$ dato da $\psi(P_{3}) \in \mathbb{K}$ dove $\psi : A \to \mathbb{K}$ è l'unica affinità tale che $\psi(P_{1})=0$ e $\psi(P_{2}) = 1$.

Fissati $P_{1},P_{2} \in A$ distinti, la mappa $[P_{1},P_{2},\cdot] : A \to \mathbb{K}$ è una bigezione.

Sia $\alpha : A \to B$ affinità tra rette, allora preserva il rapporto semplice.

DIMOSTRAZIONE: Se $\psi(\alpha(P_{1}))=0$ e $\psi(\alpha(P_{2}))=1$ allora $[P_{1},P_{2},P_{3}]$ è preservato.

Sia $A = \mathbb{K}$ con la struttura affine standard, allora $[P_{1},P_{2},P_{3}] = \frac{{P_{3}-P_{1}}}{P_{2}-P_{1}}$.

DIMOSTRAZIONE:
1. Le affinità sono della forma $aP+b$, per cui $\frac{{(aP_{3}+b)-(aP_{1}+b)}}{(aP_{2}+b)-(aP_{1}+b)} = \frac{a(P_{3}-P_{1})}{a(P_{2}-P_{1})} = \frac{{P_{3}-P_{1}}}{P_{2}-P_{1}}$
2. Se $P_{1} = 0$ e $P_{2} = 1$, allora $\psi = \text{id}$ e $[P_{1},P_{2},P_{3}]=P_{3}$

# Birapporto
Siano $A$ retta proiettiva, $P_{1},P_{2},P_{3} \in A$ distinti e $P_{4} \in \mathbb{P}(V)$. Si definisce il birapporto $\beta(P_{1},P_{2},P_{3},P_{4})$ che manda $P_{1}$ in $[1,0]$, $P_{2}$ in $[0,1]$, $P_{3}$ in $[1,1]$ e $P_{4}$ nelle coordinate omogenee $[\lambda:\mu]$ di $P_{4}$ nel riferimento $P_{1},P_{2},P_{3}$.

$\beta(P_{1},P_{2},P_{3},P_{4}) = \frac{\mu}{\lambda} \in \mathbb{K} \cup \{ \infty \}$ dove $\frac{\mu}{0} = \infty$.

Fissati $P_{1},P_{2},P_{3}$ distinti, $\psi : P \mapsto \beta(P_{1},P_{2},P_{3},P)$ è una bigezione.

DIMOSTRAZIONE:
1. Sia $f : \mathbb{P}(V) \to \mathbb{P}^1(\mathbb{K})$ associato a $P_{1},P_{2},P_{3}$
2. Sia $h : \mathbb{P}'(\mathbb{K})\to \mathbb{K} \cup \{ \infty \}$ che manda in $j_{0}^{-1}(P)$ se $P \in U_{0}$, altrimenti in $\infty$
3. $\psi = h \circ f$, da cui la tesi in quanto $h$ e $f$ sono bigezioni

$\exists!f : \mathbb{P}'(V) \to \mathbb{P}'(W)$ isomorfismo   $f(P_{i}) = Q_{i}$ $\iff \beta(P_{1},P_{2},P_{3},P_{4})=\beta(Q_{1},Q_{2},Q_{3},Q_{4})$.

DIMOSTRAZIONE:
1. Sia $g : \mathbb{P}(V) \to \mathbb{P}'(\mathbb{K})$ isomorfismo proiettivo associato a $P_{1},P_{2},P_{3}$
2. Sia $h : \mathbb{P}(W) \to \mathbb{P}'(\mathbb{K})$ isomorfismo proiettivo associato a $Q_{1},Q_{2},Q_{3}$
3. $\exists!$ isomorfismo proiettivo $f:\mathbb{P}(V)\to \mathbb{P}(W)$   $f(P_{i})=Q_{i}$   $\forall i = 1,2,3$
4. $f \circ h = g \circ \text{id}_{\mathbb{P}'(\mathbb{K})}$, per cui la parte destra della tesi si verifica $\iff f(P_{4}) = Q_{4}$
5. Di conseguenza $f \circ h = g$

Siano 4 punti $P_{i} = [\lambda_{i}:\mu_{i}] \in \mathbb{P}'(\mathbb{K})$ con $P_{1},P_{2},P_{3}$ distinti. Allora $\beta(P_{1},P_{2},P_{3},P_{4})= \frac{\left|\begin{smallmatrix} \lambda_{1} & \lambda_{4} \\ \mu_{1} & \mu_{4} \end{smallmatrix}\right| \cdot \left|\begin{smallmatrix} \lambda_{2} & \lambda_{3} \\ \mu_{2} & \mu_{3} \end{smallmatrix}\right|}{\left|\begin{smallmatrix} \lambda_{1} & \lambda_{3} \\ \mu_{1} & \mu_{3} \end{smallmatrix}\right| \cdot \left|\begin{smallmatrix} \lambda_{2} & \lambda_{4} \\ \mu_{2} & \mu_{4} \end{smallmatrix}\right|}$.

DIMOSTRAZIONE:
1. Le quantità a sinistra e destra sono invarianti per proiettività di $\mathbb{P}'(\mathbb{K})$
2. L'uguaglianza è verificata per $\bar{P_{1}}, \bar{P_{2}}, \bar{P_{3}}, P$ fissati
3. Dati $P_{1},P_{2},P_{3}$ esiste una proiettività che li porta in $\bar{P_{1}},\bar{P_{2}},\bar{P_{3}}$

Se $P_{i} \in U_{0}$ e si identifica $P_{i}$ con $j_{0}^{-1}(P_{i}) \in K$, allora $\beta(P_{1},P_{2},P_{3},P_{4}) = \frac{(P_{4}-P_{1})(P_{3}-P_{2})}{(P_{3}-P_{1})(P_{4}-P_{2})}$.

# Simmetrie del birapporto
Siano $P_{1},P_{2},P_{3},P_{4} \in \mathbb{P}(V)$ retta proiettiva distinti e $\delta \in S_{4}$.

Se $\delta=(1 \, 2)$ o $\delta = (3 \, 4)$, allora $\beta = \frac{1}{\beta}$.

Le permutazioni $(1 \, 2) (3 \, 4)$, $(1 \, 3)(2 \, 4)$, $(1 \, 4)(2 \, 3)$ lasciano invariate il birapporto.

L'insieme $S(\beta) = \{ \beta(P_{\delta(1)}, P_{\delta(2)}, P_{\delta(3)}, P_{\delta(4)} ) : \delta \in S_{4}\}$ assume al massimo 6 valori.