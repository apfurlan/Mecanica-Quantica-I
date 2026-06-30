# 14ª aula — Problemas em 1D: Partícula Livre, Autovalores de $\hat{H}$ e Propagador

## Problemas em 1D (cap. 5)

Nesse capítulo veremos como usar a MQ para descrever uma partícula que se move em 1D.

### 5.1 -- Partícula livre

Aqui temos uma partícula que se move em 1D na **AUSÊNCIA DE QUALQUER TIPO DE FORÇA** (= partícula livre).

$$
\mathcal{L} = \frac{1}{2}m\dot{x}^2 \quad \Longrightarrow \quad H(x,p) = \frac{p^2}{2m}
$$

A "solução" desse problema na Mecânica Clássica é:

$$
\begin{cases}
\dot{x} = \dfrac{\partial H}{\partial p} = \dfrac{p}{m} \quad \Longrightarrow \quad x(t) = \dfrac{p\, t}{m} + x(0) \\[3mm]
\dot{p} = -\dfrac{\partial H}{\partial x} = 0 \quad \Longrightarrow \quad p = \text{const} = p(0)
\end{cases}
$$

Isso está OK se a partícula tiver uma massa apreciável, caso contrário você deve descrever a situação usando a MQ.

$$
\hat{H} = \frac{\hat{P}^2}{2m} \quad \text{é o operador Hamiltoniano}
$$

O ket $|\Psi(t)\rangle$ mora no EV (espaço vetorial) das funções complexas de $x$.

## Autovetores/Autovalores de $\hat{H}$ (calculados de 2 maneiras)

$$
\hat{H}|E\rangle = E|E\rangle
$$

### i) Projetando em $\langle x|$

$$
\langle x|\frac{\hat{P}^2}{2m}|E\rangle = E\langle x|E\rangle
$$

$$
-\frac{\hbar^2}{2m}\frac{d^2}{dx^2}\psi_E(x) = E\,\psi_E(x)
$$

**Atenção!** Isso é uma equação para determinar $E$ e $\psi_E(x)$. Os autovalores $E$ são obtidos da exigência de que $\psi_E(x)$ seja uma função do EV, isto é, $\psi_E(x)$ **NÃO PODE DIVERGIR EM $x = \pm\infty$**!

Funções do EV:

- (i) normalizáveis, $\displaystyle\int_{-\infty}^{\infty} |\psi(x)|^2\, dx < \infty$
- (ii) não-normalizáveis, porém não divergentes em $\pm\infty$

**Caso $E < 0$:** teremos

$$
\psi_E'' = \left(\frac{2m|E|}{\hbar^2}\right)\psi_E \qquad \text{(EQ. de 2ª ordem!)}
$$

com solução

$$
\psi_E(x) = \alpha\, e^{+\sqrt{2m|E|/\hbar^2}\,x} + \beta\, e^{-\sqrt{2m|E|/\hbar^2}\,x}
$$

Claramente isso não pertence ao EV.

$$
\boxed{E \text{ não pode ser negativo!}}
$$

**Caso $E > 0$:** teremos

$$
\psi_E'' = -\frac{2mE}{\hbar^2}\psi_E
$$

**Obs:** como $\hat{H}$ é hermitiano sabemos que seus autovalores são reais; no entanto você pode provar isso observando que, para $E$ complexo, o produto $\psi_E(x)$ diverge no infinito.

com solução

$$
\psi_E(x) = \alpha\, e^{i\sqrt{2mE/\hbar^2}\,x} + \beta\, e^{-i\sqrt{2mE/\hbar^2}\,x}
$$

que é do tipo (ii) e pertence ao EV!

Essa análise é um exemplo de como os autovalores são descobertos. Concluímos que $E$ pode ser qualquer valor real e positivo (ou zero) (**ESPECTRO CONTÍNUO!**).

$$
\boxed{E \geq 0} \qquad \text{autovalores de } \hat{H}
$$

Cada valor de $E$ é **DUPLAMENTE DEGENERADO**:

$$
\langle x|E,+\rangle = \frac{1}{\sqrt{2\pi\hbar}}\, e^{i\sqrt{2mE/\hbar^2}\,x}
$$

$$
\langle x|E,-\rangle = \frac{1}{\sqrt{2\pi\hbar}}\, e^{-i\sqrt{2mE/\hbar^2}\,x}
$$

(não normalizados). Esses estados formam uma base do subespaço de energia $E$.

**Obs:** essa escolha da constante de normalização não faz com que $\langle E\alpha|E'\beta\rangle = \delta(E-E')\,\delta_{\alpha\beta}$.

### ii) Usando a base $|p\rangle$

Aqui nem precisamos projetar $\hat{H}|E\rangle = E|E\rangle$ em $|x\rangle$. Como $\hat{H} = \dfrac{\hat{P}^2}{2m}$, segue que $|p\rangle$ é um autovetor de $\hat{H}$ com autoenergia $E$:

$$
\hat{H}|p\rangle = \frac{\hat{P}^2}{2m}|p\rangle = \frac{p^2}{2m}|p\rangle
$$

Veja que aqui descobrimos que $E \geq 0$ sem muito esforço. Qual a relação dos $|p\rangle$ com $|E,+\rangle$ e $|E,-\rangle$?

$$
|p = \sqrt{2mE}\rangle = |E,+\rangle
$$

$$
|p = -\sqrt{2mE}\rangle = |E,-\rangle
$$

Para obter essa identificação é que escolhemos as constantes de normalização acima como $(2\pi\hbar)^{-1/2}$.

De fato, ambos os estados têm autovalor $E = p^2/2m$, e são a base, obtida acima, do subespaço de energia $E$.

## Operador de evolução

Conhecendo os autovalores/autovetores de $\hat{H}$ podemos montar o operador de evolução. Vimos que

$$
\hat{U}(t) = e^{-i\hat{H}t/\hbar}
$$

Agora podemos usar $\hat{\mathbb{1}} = \displaystyle\int_{-\infty}^{\infty} dp\, |p\rangle\langle p|$ (pois $\langle p|p'\rangle = \delta(p-p')$) e obter

$$
\boxed{\hat{U}(t) = \int_{-\infty}^{\infty} dp\, |p\rangle\langle p|\, e^{-ip^2t/2m\hbar}}
$$

onde usei que $\hat{H}|p\rangle = \dfrac{p^2}{2m}|p\rangle$.

No entanto, **NÃO PODEMOS USAR** $\hat{\mathbb{1}} = \displaystyle\int_0^{\infty} dE \sum_{\alpha = +,-} |E\alpha\rangle\langle E\alpha|$, uma vez que $\langle E\alpha|E'\beta\rangle \neq \delta(E-E')\,\delta_{\alpha\beta}$, para exprimir $\hat{U}(t)$ como uma integral em $E$.

### A identidade usando os $|E\alpha\rangle$

**Atenção:** como não temos $\langle E\alpha|E'\beta\rangle = \delta(E-E')\,\delta_{\alpha\beta}$ (onde $\alpha,\beta = +,-$) no nosso caso (pois a constante de normalização não foi escolhida para isso acontecer), **NÃO TEMOS**

$$
\hat{\mathbb{1}} \neq \int_0^{\infty} dE\, \underbrace{\left[|E,+\rangle\langle E,+| + |E,-\rangle\langle E,-|\right]}_{\text{``borboletas'' do subespaço de energia } E}
$$

como seria de esperar. Ao invés:

$$
\hat{\mathbb{1}} = \int_{-\infty}^{\infty} dp\, |p\rangle\langle p| = \int_{-\infty}^{0} dp\, |p\rangle\langle p| + \int_0^{\infty} dp\, |p\rangle\langle p|
$$

Mudando a variável para $p = -\sqrt{2mE}$ na 1ª integral e $p = +\sqrt{2mE}$ na 2ª:

$$
\hat{\mathbb{1}} = \int_0^{\infty} \sqrt{\frac{m}{2E}}\,|E,-\rangle\langle E,-|\, dE + \int_0^{\infty} \sqrt{\frac{m}{2E}}\,|E,+\rangle\langle E,+|\, dE
$$

$$
\hat{\mathbb{1}} = \int_0^{\infty} dE\, \sqrt{\frac{m}{2E}}\, \underbrace{\left[|E,-\rangle\langle E,-| + |E,+\rangle\langle E,+|\right]}_{\displaystyle\sum_{\alpha = +,-}}
$$

**Obs:** o fator $\sqrt{m/2E}$ não estaria aqui se $\langle E\alpha|E'\beta\rangle = \delta(E-E')\,\delta_{\alpha\beta}$.

## Propagador

Como vimos, um estado inicial qualquer $|\Psi(0)\rangle$, com função de onda conhecida $\langle x|\Psi(0)\rangle = \Psi(x,0)$, evolui no tempo para

$$
|\Psi(t)\rangle = \hat{U}(t)|\Psi(0)\rangle
$$

$$
\Longrightarrow \quad \langle x|\Psi(t)\rangle = \int_{-\infty}^{\infty} dx'\, \langle x|\hat{U}(t)|x'\rangle\langle x'|\Psi(0)\rangle
$$

$$
\Psi(x,t) = \int_{-\infty}^{\infty} dx'\, \underbrace{\langle x|\hat{U}(t)|x'\rangle}_{U(x,x';t)\ \text{propagador}}\, \Psi(x',0) \tag{$*$}
$$

$$
\langle x|\hat{U}(t)|x'\rangle = \int_{-\infty}^{\infty} dp\, \langle x|p\rangle\langle p|x'\rangle\, e^{-i\frac{p^2}{2m}\frac{t}{\hbar}}
$$

$$
= \frac{1}{2\pi\hbar}\int_{-\infty}^{\infty} dp\, e^{i\frac{p(x-x')}{\hbar}}\, e^{-i\frac{p^2}{2m}\frac{t}{\hbar}}
$$

Aqui usamos

$$
\int_{-\infty}^{\infty} e^{-\alpha x^2 + \beta x}\, dx = \sqrt{\frac{\pi}{\alpha}}\, e^{\beta^2/4\alpha}
$$

válido mesmo que $\alpha$ e $\beta$ sejam complexos, **DESDE QUE** $\text{Re}\,\alpha \geq 0$.

Com isso

$$
\langle x|\hat{U}(t)|x'\rangle = \frac{1}{2\pi\hbar}\left(\frac{\pi\, 2m\hbar}{i t}\right)^{1/2} e^{-\frac{(x-x')^2 m\hbar}{\hbar^2\, 2it}}
$$

$$
= \sqrt{\frac{m}{it\, 2\pi\hbar}}\; e^{i\frac{(x-x')^2 m}{2\hbar t}}
$$

Para qualquer função de onda inicial $\Psi(x,0)$, o estado da partícula em $t$ será obtido da integração ($*$).

No caso particular do estado inicial ser

$$
\Psi(x,0) = \delta(x-a)
$$

(isso é incomum, dizer que a partícula está em um estado impróprio...), a integração é trivial e

$$
\Psi(x,t) = \int_{-\infty}^{\infty} dx'\, U(x,x';t)\, \delta(x'-a)
$$

$$
= U(x,a;t)
$$

Portanto você pode interpretar o propagador como a função de onda da partícula, no instante $t$, que, em $t=0$, estava infinitamente localizada em $x = x'$.

## Evolução de um pacote gaussiano

$$
\Psi(x,0) = \left(\frac{1}{\pi\Delta^2}\right)^{1/4} e^{i p_0 x/\hbar}\, e^{-x^2/2\Delta^2} \qquad \text{(função própria)}
$$

Você pode verificar que o estado está normalizado

$$
\int_{-\infty}^{\infty} |\Psi(x,0)|^2\, dx = 1
$$

$$
\langle x\rangle = 0 \qquad \Delta x = \frac{\Delta}{\sqrt{2}}
$$

Você pode calcular facilmente $\langle p\rangle = p_0$ e $\Delta p = \dfrac{\hbar}{\sqrt{2}\Delta}$. Esse estado representaria uma partícula em uma região $\Delta$ em torno da origem e com velocidade em torno de $p_0/m$.

$$
\frac{p_0}{m} - \frac{\Delta p}{m} < v < \frac{p_0}{m} + \frac{\Delta p}{m}
$$

Em um instante $t$ posterior, o estado da partícula é descrito pela função de onda

$$
\Psi(x,t) = \int_{-\infty}^{\infty} \underbrace{\left(\frac{m}{it\, 2\pi\hbar}\right)^{1/2} e^{i\frac{(x-x')^2 m}{2\hbar t}}}_{U(x,x';t)}\; \underbrace{\left(\frac{1}{\pi\Delta^2}\right)^{1/4} e^{ip_0 x'/\hbar}\, e^{-x'^2/2\Delta^2}}_{\Psi(x',0)}\; dx'
$$

Veja que a integral é da forma $\displaystyle\int_{-\infty}^{\infty} e^{-\alpha x'^2 + \beta x'}\, dx'$ com

$$
\alpha = \frac{1}{2\Delta^2} - \frac{im}{2\hbar t} \qquad \text{e} \qquad \beta = -\frac{im}{\hbar t}x + \frac{ip_0}{\hbar}
$$

usando $\sqrt{\pi/\alpha}\, e^{\beta^2/4\alpha}$ para o resultado da integral (veja que $\text{Re}\,\alpha \geq 0$!):

$$
\Psi(x,t) = \left[\pi^{1/2}\left(\Delta + \frac{i\hbar t}{m\Delta}\right)\right]^{-1/2} \exp\left[-\frac{(x-p_0 t/m)^2}{2\Delta^2(1+i\hbar t/m\Delta^2)}\right] \times
$$

$$
\times\, \exp\left[\frac{ip_0}{\hbar}\left(x - \frac{p_0 t}{2m}\right)\right]
$$

A densidade de probabilidade é

$$
|\Psi(x,t)|^2 = \left(\frac{1}{\pi\Delta^2(t)}\right)^{1/2} \exp\left[-\frac{(x-p_0t/m)^2}{\Delta^2(t)}\right]
$$

onde

$$
\Delta^2(t) = \Delta^2 + \frac{\hbar^2 t^2}{m^2\Delta^2}
$$

1. Verifique que o argumento das exponenciais é adimensional.
2. Verifique que $[\Psi(x)] = [L]^{-1/2}$.
3. Verifique que $\displaystyle\int_{-\infty}^{\infty} |\Psi(x,t)|^2\, dx = 1$.

Da expressão de $|\Psi(x,t)|^2$ podemos concluir (sem fazer conta!) que

$$
\langle x\rangle = \frac{p_0 t}{m} \qquad \Delta x = \frac{\Delta(t)}{\sqrt{2}} = \frac{\sqrt{\Delta^2 + \hbar^2t^2/m^2\Delta^2}}{\sqrt{2}}
$$

Veja como a densidade de probabilidade inicial evolui no tempo: o centro avança com velocidade constante $p_0/m$ e a largura cresce com o tempo.

O alargamento da gaussiana pode ser entendido da incerteza inicial na velocidade.

**Obs:** aproximadamente $\Delta(t) \approx \dfrac{\hbar t}{\Delta}\dfrac{1}{m}$ para $t$ grande.

Saindo da origem em $t=0$:

$$
\left(p_0 - \frac{\hbar}{\Delta}\right)\frac{t}{m} \quad \text{(menor velocidade)} \qquad \left(p_0 + \frac{\hbar}{\Delta}\right)\frac{t}{m} \quad \text{(maior velocidade)}
$$

em $t$ a partícula poderá estar entre

$$
\frac{p_0 t}{m} - \frac{\hbar t}{m\Delta} < x < \frac{p_0 t}{m} + \frac{\hbar t}{m\Delta} \quad \Longrightarrow \quad \Delta x(t) \sim \frac{\hbar t}{m\Delta}
$$

Classicamente você poderia dizer "tenho uma partícula na origem com velocidade $p_0/m$". Em MQ isso não existe. O estado que mais se assemelha a essa condição inicial clássica é exatamente essa gaussiana.

Se a MQ é a teoria correta, por que você nunca viu uma bola de futebol lançada com velocidade $p_0/m$ se tornar cada vez mais "difusa" (correspondendo ao alargamento da gaussiana)?

A razão é que a incerteza em velocidade imposta pela MQ é inobservável para objetos massivos usuais.

### Quanto à incerteza na velocidade

Use $\Delta x = 10^{-15}$ m (precisão total na posição)

$$
\Delta p = \frac{\hbar}{2\Delta x} \quad \Longrightarrow \quad \Delta v = \frac{\hbar}{2m\Delta x} =
\begin{cases}
5{,}3 \times 10^{-17} \text{ m/s} & (m = 1\text{g}) \\
5{,}8 \times 10^{10} \text{ m/s} & (\text{elétron})
\end{cases}
$$

### Quanto ao alargamento durante a evolução

A imprecisão na posição no instante $t$ é da ordem de $(\Delta v)\,t$. Temos que isso se torna igual a 1 mm após

$$
1{,}9 \times 10^{13}\ \text{seg} \ (\sim 600.000 \text{ anos}) \quad \text{para a massa de 1g}
$$

$$
1{,}7 \times 10^{-14}\ \text{seg} \quad \text{para o elétron}
$$

$$
\Longrightarrow \quad \boxed{\text{para partículas do dia-a-dia você NÃO PRECISA tratar o caso livre usando a MQ!!!}}
$$

Mesmo estado inicial, mesma velocidade média. O alargamento da gaussiana ocorre muito mais rapidamente quando a partícula é leve!

Aqui você vê que para partículas pesadas o que a MQ diz coincide com o que a MC diz. Para todos os efeitos o pacote gaussiano é a partícula clássica, e este se move com a velocidade esperada (**CONSTANTE**), além de não apresentar alargamento do pacote (que seria algo extremamente bizarro do ponto de vista clássico).

Isso ocorre pois você pode construir um estado quântico com $\Delta x \sim 10^{-15}$ m e $\Delta v \sim 10^{-17}$ m/s, que são incertezas inobserváveis por qualquer instrumento de medida de posição ou velocidade que possam ser construídos.

## Pacote livre -- distribuição de momenta

$$
\Psi(x,t) = \frac{1}{\pi^{1/4}\Delta^{1/2}f^{1/2}}\, \exp\left[-\frac{(x-p_0t/m)^2}{2\Delta^2 f} + \frac{ip_0 x}{\hbar} - \frac{ip_0^2}{2m}\frac{t}{\hbar}\right]
$$

onde

$$
f = 1 + \frac{i\hbar t}{m\Delta^2}
$$

$$
|\Psi(x,t)|^2 = \frac{1}{\sqrt{\pi}\,\Delta\,|f|}\, \exp\left[-\frac{(x-p_0t/m)^2}{\Delta^2|f|^2}\right] \qquad \text{(densidade de prob. de posição)}
$$

Podemos calcular também (tomando a transformada de Fourier de $\Psi(x,t)$)

$$
\widetilde{\Psi}(p,t) = \left(\frac{\Delta}{\hbar}\right)^{1/2} \frac{1}{\pi^{1/4}}\, \exp\left[-\frac{(p-p_0)^2\Delta^2 f}{2\hbar^2} + \frac{i(p_0-p)p_0t}{\hbar m} - \frac{ip_0^2}{2m}\frac{t}{\hbar}\right]
$$

$$
= \left(\frac{\Delta}{\hbar}\right)^{1/2} \frac{1}{\pi^{1/4}}\, \exp\left[-\frac{(p-p_0)^2\Delta^2}{2\hbar^2} - \frac{ip^2}{2m}\frac{t}{\hbar}\right]
$$

$$
|\widetilde{\Psi}(p,t)|^2 = \frac{\Delta}{\hbar\sqrt{\pi}}\, \exp\left[-\frac{(p-p_0)^2\Delta^2}{\hbar^2}\right] \qquad \text{(densidade de prob. de MOMENTO)}
$$

Note que a distribuição de momenta $|\widetilde{\Psi}(p,t)|^2$ permanece constante enquanto $|\Psi(x,t)|^2$ se alarga.

Isso era de se esperar, pois:

$$
|\Psi(t)\rangle = e^{-i\hat{H}t/\hbar}|\Psi(0)\rangle
$$

$$
\langle p|\Psi(t)\rangle = \langle p|e^{-i\hat{H}t/\hbar}|\Psi(0)\rangle
$$

$$
= e^{-i\frac{p^2t}{2m\hbar}}\langle p|\Psi(0)\rangle \quad \Longrightarrow \quad |\widetilde{\Psi}(p,t)|^2 = |\widetilde{\Psi}(p,0)|^2
$$
