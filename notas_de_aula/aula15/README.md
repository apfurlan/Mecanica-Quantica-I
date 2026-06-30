# (15ª aula) — O Limite Clássico (cap. 6) e o Teorema de Ehrenfest

## O Limite Clássico

O estado quântico abaixo,

$$\Psi(x,0) = \frac{e^{ip_0 x/\hbar} \, e^{-(x-x_0)^2/2\Delta^2}}{(\pi \Delta^2)^{1/4}}$$

tem $\langle X \rangle = x_0$, $\Delta X = \dfrac{\Delta}{\sqrt{2}}$, $\langle P \rangle = p_0$ e $\Delta P = \dfrac{\hbar}{\sqrt{2}\Delta}$. Esse estado pode ser pensado como a melhor versão quântica da partícula clássica.

Vimos que se $\Delta X \sim 10^{-15}\,\text{m}$ temos $\Delta P \sim 10^{-19}\,\text{kg}\cdot\text{m/s}$, que para uma partícula de massa $m = 1\,\text{g}$ implica em uma velocidade conhecida com precisão de $\Delta V = \dfrac{\Delta P}{m} \sim 10^{-16}\,\text{m/s}$, maior precisão que qualquer instrumento de medida pode proporcionar.

Vimos também que esse estado, na ausência de forças, evolui para

$$|\Psi(x,t)|^2 = \frac{1}{\sqrt{\pi}\,\Delta(t)} \exp\left[ -\frac{(x - x_0 - p_0 t/m)^2}{\Delta(t)^2} \right]$$

com

$$\Delta(t) = \sqrt{\Delta^2 + \frac{\hbar^2 t^2}{m^2 \Delta^2}},$$

a largura do pacote, crescendo muito lentamente para $m \sim 1\,\text{g}$.

Concluímos que, para uma partícula livre, a Eq. de Schrödinger contém o resultado clássico da partícula se movendo com velocidade constante $p_0/m$ e $|\Psi(x,t)|^2$ tem características de "partícula" (não apresentando alargamento do pacote).

## Teorema de Ehrenfest

Vamos agora derivar o **Teorema de Ehrenfest** e ver como exatamente $F = ma$ se esconde na Eq. de Schrödinger.

Seja um operador $\hat{\Omega}$, independente do tempo, e um estado $|\Psi(t)\rangle$ que evolui de acordo com a E.S.

$$i\hbar \frac{d}{dt}|\Psi(t)\rangle = \hat{H}|\Psi(t)\rangle.$$

O valor médio de $\hat{\Omega}$ muda com o tempo de acordo com

$$\frac{d}{dt}\langle\Psi(t)|\hat{\Omega}|\Psi(t)\rangle = \left[\frac{d}{dt}\langle\Psi|\right]\hat{\Omega}|\Psi\rangle + \langle\Psi|\hat{\Omega}\left[\frac{d}{dt}|\Psi\rangle\right].$$

Tome o adjunto da E.S. para encontrar

$$-i\hbar \frac{d}{dt}\langle\Psi| = \langle\Psi|\hat{H}.$$

Substituindo as derivadas de $\langle\Psi|$ e $|\Psi\rangle$ usando a E.S. e seu adjunto,

$$\frac{d}{dt}\langle \hat{\Omega} \rangle = \frac{i}{\hbar}\langle\Psi|\hat{H}\hat{\Omega}|\Psi\rangle - \frac{i}{\hbar}\langle\Psi|\hat{\Omega}\hat{H}|\Psi\rangle.$$

$$\boxed{\frac{d\langle \hat{\Omega} \rangle}{dt} = \frac{1}{i\hbar}\langle\Psi|[\hat{\Omega}, \hat{H}]|\Psi\rangle} \qquad \text{(Teorema de Ehrenfest)}$$

Compare isso com a relação da Mecânica Hamiltoniana

$$\frac{d}{dt}w(p,q) = \{w, H\} = \frac{\partial w}{\partial q}\frac{\partial H}{\partial p} - \frac{\partial w}{\partial p}\frac{\partial H}{\partial q}.$$

Usando $\hat{\Omega} = \hat{X}$ temos

$$\frac{d\langle \hat{X} \rangle}{dt} = \frac{1}{i\hbar}\langle [\hat{X}, \hat{H}] \rangle.$$

## Aplicação: $\hat{H} = \dfrac{\hat{P}^2}{2m} + V(\hat{X})$

Se $\hat{H} = \dfrac{\hat{P}^2}{2m} + V(\hat{X})$, então

$$[\hat{X}, \hat{H}] = \left[\hat{X}, \frac{\hat{P}^2}{2m}\right] + [\hat{X}, V(\hat{X})] = \frac{i\hbar}{m}\hat{P}.$$

Aqui usei a propriedade de comutadores (1.5.10):

$$[\hat{X}, \hat{P}^2] = \hat{P}\underbrace{[\hat{X}, \hat{P}]}_{i\hbar} + \underbrace{[\hat{X}, \hat{P}]}_{i\hbar}\hat{P} = 2i\hbar\hat{P}.$$

Portanto

$$\boxed{\frac{d\langle \hat{X} \rangle}{dt} = \frac{\langle \hat{P} \rangle}{m}}$$

ou seja, a taxa de variação do valor médio de $\hat{X}$ é igual ao valor médio de $\hat{P}/m$.

Usando agora $\hat{\Omega} = \hat{P}$ no Teorema de Ehrenfest encontro

$$\frac{d\langle \hat{P} \rangle}{dt} = \frac{1}{i\hbar}\langle [\hat{P}, \hat{H}] \rangle,$$

e usando $\hat{H} = \dfrac{\hat{P}^2}{2m} + V(\hat{X})$ temos $\dfrac{1}{i\hbar}[\hat{P}, \hat{H}] = \dfrac{1}{i\hbar}[\hat{P}, V(\hat{X})]$.

## Comutadores $[\hat{P}, V(\hat{X})]$ e $[\hat{X}, f(\hat{P})]$

Sempre que encontrar $[\hat{P}, V(\hat{X})]$ ou $[\hat{X}, f(\hat{P})]$ use o resultado

$$[\hat{P}, \hat{X}^n] = (-i\hbar)\, n\, \hat{X}^{n-1}, \qquad [\hat{X}, \hat{P}^n] = (i\hbar)\, n\, \hat{P}^{n-1},$$

que é demonstrado por **indução**:

(i) As expressões são válidas para $n = 1$ (cheque).

(ii) Se as expressões são válidas para $n$, elas também valerão para $n+1$.

Veja como o passo (ii) se verifica:

$$[\hat{P}, \hat{X}^n] = (-i\hbar)\, n\, \hat{X}^{n-1} \quad \text{(válido por hipótese)}$$

$$
\begin{aligned}
[\hat{P}, \hat{X}^{n+1}] &= \hat{X}\,[\hat{P}, \hat{X}^n] + [\hat{P}, \hat{X}]\,\hat{X}^n \qquad \text{(prop. dos comutadores)} \\
&= \hat{X}(-i\hbar)\, n\, \hat{X}^{n-1} + (-i\hbar)\hat{X}^n \qquad \text{(usando a hipótese e } [\hat{P}, \hat{X}] = -i\hbar\text{)} \\
&= (-i\hbar)(n+1)\,\hat{X}^n \qquad \text{(verificando a validade da fórmula para } n+1\text{)}.
\end{aligned}
$$

Agora use a definição $V(\hat{X}) = \displaystyle\sum_{n=0}^{\infty} a_n \hat{X}^n$ para concluir

$$
\begin{aligned}
[\hat{P}, V(\hat{X})] &= \sum_{n=0}^{\infty} a_n [\hat{P}, \hat{X}^n] = \sum_{n=1}^{\infty} a_n (-i\hbar)\, n\, \hat{X}^{n-1} \\
&= (-i\hbar)\frac{dV}{d\hat{X}}
\end{aligned}
$$

onde $\dfrac{dV}{d\hat{X}}$ representa o operador obtido derivando $V(\hat{X})$ como se fosse uma função normal da variável $\hat{X}$. Assim:

$$\boxed{[\hat{P}, V(\hat{X})] = -i\hbar \frac{dV}{d\hat{X}}} \qquad \boxed{[\hat{X}, f(\hat{P})] = i\hbar \frac{df}{d\hat{P}}}$$

(a segunda relação se demonstra da mesma forma).

**Ex.:** $[\hat{P}, \sin \hat{X}] = (-i\hbar)\cos\hat{X}$ e $[\hat{X}, e^{\hat{P}}] = i\hbar\, e^{\hat{P}}$.

Dessa forma:

$$\frac{d\langle \hat{P} \rangle}{dt} = \left\langle -\frac{dV}{d\hat{X}} \right\rangle = \langle F(\hat{X}) \rangle$$

onde $-\dfrac{dV}{d\hat{X}}$ é o **operador força**.

A taxa de variação do valor médio de $\hat{P}$ é igual ao valor médio do operador força.

## $\langle X(t) \rangle$ obedece a Equação de Newton?

Obtemos as equações clássicas apenas para os valores médios.

Essas duas equações para $\langle X \rangle$ e $\langle P \rangle$ implicam que o valor médio $\langle X(t) \rangle$ obedece à Eq. de Newton?

**Não!** Pois para isso acontecer deveríamos ter obtido:

$$\frac{d\langle \hat{X} \rangle}{dt} = \frac{\langle \hat{P} \rangle}{m} \quad \text{e} \quad \frac{d\langle \hat{P} \rangle}{dt} = F(\langle \hat{X} \rangle) \quad \Longrightarrow \quad m\frac{d^2\langle \hat{X} \rangle}{dt^2} = F(\langle \hat{X} \rangle),$$

no entanto obtivemos:

$$\frac{d\langle \hat{X} \rangle}{dt} = \frac{\langle \hat{P} \rangle}{m} \quad \text{e} \quad \frac{d\langle \hat{P} \rangle}{dt} = \langle F(\hat{X}) \rangle \quad \Longrightarrow \quad m\frac{d^2\langle \hat{X} \rangle}{dt^2} = \langle F(\hat{X}) \rangle.$$

Qual a diferença entre $F(\langle \hat{X} \rangle)$ e $\langle F(\hat{X}) \rangle$? Uma é a força clássica avaliada em $\langle \hat{X} \rangle$, a outra é a média da força clássica sobre toda a função de onda da partícula.

$$\langle F(\hat{X}) \rangle = \int_{-\infty}^{\infty} |\Psi(x,t)|^2 F(x) \, dx \quad \neq \quad F\left(\int_{-\infty}^{\infty} |\Psi(x,t)|^2 x \, dx\right) = F(x_0), \qquad \langle \hat{X} \rangle \equiv x_0.$$

Usando a série de Taylor de $F(x)$ em torno do valor médio $\langle \hat{X} \rangle \equiv x_0$ temos

$$
\begin{aligned}
\langle F(\hat{X}) \rangle &= \int_{-\infty}^{\infty} |\Psi(x,t)|^2 \left[ F(x_0) + F'(x_0)(x - x_0) + \frac{1}{2}F''(x_0)(x-x_0)^2 + \dots \right] dx \\
&= F(x_0) + F'(x_0)\underbrace{(x_0 - x_0)}_{0} + \frac{1}{2}F''(x_0)\underbrace{\left(\langle \hat{X}^2 \rangle - x_0^2\right)}_{\Delta X^2} + \dots
\end{aligned}
$$

*(Diagrama: curva $F(x)$ suavemente crescente sobre o eixo $x$, com uma distribuição $|\Psi(x)|^2$ em forma de sino estreita, de largura $\Delta X$, centrada em uma região onde $F(x)$ não varia apreciavelmente.)*

Nesse desenho $F(x)$ não varia apreciavelmente na escala $\Delta X$.

Portanto, se a força não varia apreciavelmente em uma distância da ordem da largura de $\Psi$, $\Delta X$:

$$\underbrace{F(x_0) \gg F''(x_0)\,\Delta X^2 \quad \Longrightarrow \quad \langle F(\hat{X}) \rangle \sim F(\langle \hat{X} \rangle)}_{(*)},$$

e $\langle X(t) \rangle$ obedece $F = ma$!

## Discussão: massas pequenas vs. massas grandes

Se na função de onda gaussiana do início da aula temos $\Delta X \sim 10^{-15}\,\text{m}$, e a partícula associada tem massa $m \sim 1\,\text{g}$, $\Delta V \sim 10^{-16}\,\text{m/s}$. Como é essencialmente a incerteza na velocidade da partícula que leva ao alargamento do pacote, $\Delta X$ permanece pequeno e a condição acima é certamente válida por longos tempos $\Rightarrow$ o valor médio $\langle X \rangle$ segue a trajetória ditada por $F = ma$. Como o pacote permanece estreito, a função de onda **É** a partícula clássica, com posição e velocidade bem definidas.

Com esse mesmo estado, caso $m \sim m_e$ (massa do elétron), a incerteza na velocidade seria $\Delta V \sim 10^{12}\,\text{m/s}$ e o pacote se alargaria muito rapidamente, rapidamente invalidando a condição $(*)$ acima. O valor médio $\langle \hat{X} \rangle$ não seguiria a trajetória clássica.

**Caso $m \sim 1\,\text{g}$:** não há alargamento, e $\langle X \rangle$ obedece $F = ma$ — a partícula segue uma trajetória clássica bem definida.

**Caso $m \sim m_e$:** há alargamento do pacote (ilustrado por duas regiões sobrepostas, alargadas e irregulares, centradas na trajetória), e $\langle X \rangle$ não obedece $F = ma$.

## Caso do potencial harmônico

No caso do potencial harmônico $V(x) = \dfrac{1}{2}m\omega^2 x^2$, a força é a lei de Hooke $F(x) = -m\omega^2 x$ e $F''(x) = 0$, portanto a condição $(*)$ é sempre satisfeita, **independente do tamanho de $\Delta X$**.

Aqui, mesmo para partículas leves, $\langle X \rangle$ segue $F = ma$, isto é

$$m\frac{d^2\langle X \rangle}{dt^2} = -m\omega^2 \langle X \rangle.$$

A diferença entre uma partícula leve e uma pesada está em que a primeira exibe o alargamento do pacote enquanto a segunda não.

## Potenciais descontínuos

No caso dos potenciais descontínuos que já discutimos, a variação abrupta do potencial faz com que a condição $(*)$ não seja satisfeita mesmo para $\Delta X$ muito pequeno. $\Rightarrow$ $\langle X \rangle$ não obedece $F = ma$ nesses casos.

**Ex.:** No caso do poço infinito vimos a simulação da dinâmica de um pacote gaussiano. Observamos desvios de $\langle X(t) \rangle$ da trajetória clássica nas proximidades das paredes.

*(Diagrama: gráfico de $x$ por $t$ mostrando a trajetória clássica $F=ma$ em ziguezague entre as paredes $+L/2$ e $-L/2$, comparada à curva suave de $\langle X \rangle$ obtida da simulação quântica.)*

**Ex.:** No caso de um pacote incidindo em um degrau com $\langle E \rangle > V_0$ (classicamente a partícula não seria refletida):

*(Diagrama: dois esquemas — no primeiro, um pacote de onda $\langle X \rangle$ se aproxima do degrau de potencial $V_0$; no segundo, após a colisão, parte do pacote é refletida (movendo-se para a esquerda) e parte é transmitida (movendo-se para a direita), ambos rotulados $\langle X \rangle$.)*

Após a colisão com o degrau, $\langle X \rangle$ avança mais lentamente (devido ao pacote refletido) que o previsto por $F = ma$.

## Conclusão

> Em suma: para se observar $F = ma$ na Eq. de Schrödinger há dois pontos a considerar.
>
> 1. Um pacote "clássico" como o $\Psi(x)$ do início da aula deve se manter estreito durante a evolução do sistema (isso ocorre com **massas grandes**).
> 2. O potencial deve ser tal que, para o $\Delta X$ do pacote, $F''(\langle X \rangle)\,\Delta X^2 \ll F(\langle X \rangle)$ se verifique. Isso implica que $\langle X \rangle$ seguirá a trajetória clássica determinada por $F = ma$.
>
> Caso essas duas condições se verifiquem, a descrição quântica do problema em questão é **desnecessária**. Basta usar $F = ma$.
