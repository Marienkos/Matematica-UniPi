# Metodo a un passo
Sia un problema $(I,f(t,y),t_{0},y_{0})$ ai valori iniziali nelle ipotesi di esistenza e unicità.

La procedura è la seguente:
1. passo di discretizzazione: fissato $ℎ >0$, si definisce $t_{n} = t_{0} +hn$ nella partizione
2. si pone $u_{n+1}=u_{n} + h\Phi(t_{n}, u_{n}, u_{n+1}, f_{n+1}, h)$ con $u_{0} = y_{0}$.

$\Phi$ identifica il metodo in uso, detto:
- a un passo se $u_{n+1}$ dipende solo da $u_{n}$
- a $l$ passi se $u_{n+1}$ dipende da $u_{n-l+1},\dots,u_{n}$
- esplicito se $\Phi$ non dipende da $u_{n+1}$
- implicito se $\Phi$ dipende da $u_{n+1}$

# Errore del metodo
Sia $\varepsilon_{n+1} = y_{n+1} - (y_{n} + h\Phi(t_{n},y_{n},y_{n+1},f(t_{n},y_{n}),h))$, si definiscono:
- errore locale di troncamento $\tau_{n+1}(h)=\frac{\varepsilon_{n+1}}{h}$
- errore globale di troncamento $\tau(h)=\max\limits_{n=0,\dots,N_{h}-1} |\tau_{n+1}(h)|$

Si definisce l'errore globale $e_{n} = y_{n} - u_{n}$.

Il metodo si dice:
- consistente se $\lim\limits_{h \to 0} \tau(h)=0$ 
- consistente di ordine $p$ se $\tau(h)=O(h^p)$
- convergente se $|e_{n}| \leq C(h)$ con $\lim\limits_{h \to 0} C(h)=0$
- convergente di ordine $p$ se $C(h) = O(h^p)$

# Metodo di Eulero
Il metodo di Eulero usa $u_{n+1} = u_{n} + hf_{n}$.

Fissato $\xi_{n}$, vale $\tau_{n+1}(h) = \frac{h}{2}y''(\xi_{n})$.

DIMOSTRAZIONE: $\tau_{n+1}(h) =$
- $\frac{1}{h}(y_{n+1} - (y_{n} + hf(t_{n},y_{n})))$
- $\frac{1}{h}(y(t_{n+1}) - y(t_{n}) - hy'(t_{n}))$
- $\frac{1}{h}(y(t_{n}+h)-y(t_{n})-hy'(t_{n}))$
- Se $y \in C^2(I)$ segue la tesi