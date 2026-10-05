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