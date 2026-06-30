# (21ª aula) — Momento Angular e Rotações

## Momento Angular e Rotações

Agora que conhecemos melhor os operadores $\hat{L}_x, \hat{L}_y, \hat{L}_z$ e $\hat{L}^2$, vamos mostrar como eles estão relacionados a rotações. Vamos seguir a mesma linha usada para mostrar que o operador de translação é

$$
\boxed{\text{estudar}} \longrightarrow T(\vec{a}) = \exp\left[-i\,\vec{P}\cdot\vec{a}/\hbar\right]
$$

(nova notação para operadores)

Recapitulando (agora para o espaço vetorial de estados de uma partícula em 3D) o que vimos na 1ª aula.

**1) Definição:**

$$
\langle \vec{r} | T(\vec{a}) |\Psi\rangle = \Psi(\vec{r} - \vec{a})
$$

(a função de onda do estado transladado é $\Psi(\vec{r})$ rigidamente deslocada de $\vec{a}$).

**2) Considerando uma translação infinitesimal na direção $\hat{n}$**

$$
T(\vec{\varepsilon}) = \mathbb{I} + G\varepsilon + \Theta(\varepsilon^2) \qquad \text{($G$ desconhecido)}
$$

$$
\langle \vec{r} | \mathbb{I} + G\varepsilon + \Theta(\varepsilon^2) |\Psi\rangle = \underbrace{\Psi(\vec{r}) - \varepsilon\,\hat{n}\cdot\vec{\nabla}\Psi + \Theta(\varepsilon^2)}_{\Psi(\vec{r}-\vec{\varepsilon})}
$$

$$
\Longrightarrow \quad \langle \vec{r} | G |\Psi\rangle = -\hat{n}\cdot\vec{\nabla}\Psi.
$$

Comparando com

$$
\langle \vec{r} | \vec{P}\cdot\hat{n} |\Psi\rangle = -i\hbar\,\hat{n}\cdot\vec{\nabla}\Psi
$$

concluímos que

$$
\boxed{G = \frac{-i\,\vec{P}\cdot\hat{n}}{\hbar}}
$$

**3) Uma translação finita nessa direção $\hat{n}$ é**

$$
\lim_{N\to\infty}\left[T\left(\frac{\vec{a}}{N}\right)\right]^N = \lim_{N\to\infty}\left[\mathbb{I} - i\frac{\vec{P}\cdot\hat{n}}{\hbar}\frac{a}{N}\right]^N
$$

$$
\boxed{T(\vec{a}) = \exp\left[\frac{-i\,\vec{P}\cdot\vec{a}}{\hbar}\right]} \qquad \text{c.q.d.}
$$

## O que significa "rotacionar" em MQ

Para começar, precisamos saber o que se quer dizer com "rotação". Em MQ, "rotacionar" o estado $(\vec{r}, \vec{p})$ de $\theta$ em torno da direção $\hat{n}$ significa:

*(diagrama: vetores $\vec{r}$, $\vec{p}$ rotacionados de um ângulo $\theta$ em torno do eixo $\hat{n}$, resultando em $\vec{r}\,'$ e $\vec{p}\,'$)*

De forma incremental da translação, o vetor $\vec{p}$ se modifica da mesma maneira que o vetor $\vec{r}$. A relação entre $\vec{r}$ e $\vec{r}\,'$ e $\vec{p}$ e $\vec{p}\,'$ se expressa por meio da chamada **MATRIZ DE ROTAÇÃO**

$$
\begin{bmatrix} x' \\ y' \\ z' \end{bmatrix}
=
R(\theta\hat{n})
\begin{bmatrix} x \\ y \\ z \end{bmatrix}
$$

onde o vetor da esquerda tem componentes de $\vec{r}\,'$ e o vetor da direita tem componentes de $\vec{r}$.

Exatamente a mesma matriz relaciona $\vec{p}$ com $\vec{p}\,'$. Não vamos construir essa matriz pois, como vimos, apenas as propriedades da rotação **INFINITESIMAL** serão usadas. (No curso de Mecânica Clássica obtivemos essas matrizes.)

## Rotação infinitesimal

No caso de $\theta = \varepsilon$ ser um ângulo muito pequeno:

*(diagrama: rotação infinitesimal de $\vec{r}$ por um ângulo $\varepsilon$ em torno de $\hat{n}$, gerando $d\vec{r}$)*

$$
\vec{r}\,' = \vec{r} + d\vec{r} = \vec{r} + (\hat{n}\times\vec{r})\,\varepsilon + \Theta(\varepsilon^2)
$$

similarmente,

$$
\vec{p}\,' = \vec{p} + (\hat{n}\times\vec{p})\,\varepsilon + \Theta(\varepsilon^2).
$$

Agora a definição da ação do operador de rotação:

$$
\boxed{1)} \qquad \langle \vec{r} | U(\theta,\hat{n}) |\Psi\rangle = \Psi(R^{-1}\vec{r})
$$

ou seja, a função de onda do estado rodado deve ser $\Psi(\vec{r})$ rigidamente girada de $\theta$ na direção $\hat{n}$.

*(diagrama: $\Psi(\vec{r})$ à esquerda e $\Psi(R^{-1}\vec{r})$ à direita, mostrando a função de onda original e a rotacionada)*

O valor da nova função de onda em $\vec{r}$ é igual ao valor da antiga em $R^{-1}\vec{r}$ ($R^{-1}$ representa a matriz de rotação inversa).

| | |
|---|---|
| Função $\Psi(\vec{r})$ transladada de $\vec{a}$: | $\Psi(\vec{r}-\vec{a})$ |
| Função $\Psi(\vec{r})$ girada de $\theta$ na direção $\hat{n}$: | $\Psi\big(R(-\theta,\hat{n})\,\vec{r}\big)$ |

**2) Considerando uma rotação infinitesimal na direção $\hat{n}$**

$$
\langle \vec{r} | \mathbb{I} + G\varepsilon + \Theta(\varepsilon^2) |\Psi\rangle = \Psi\big(\vec{r} - (\hat{n}\times\vec{r})\varepsilon + \Theta(\varepsilon^2)\big)
$$

onde o argumento da direita é a rotação infinitesimal de $\vec{r}$ no sentido contrário.

$$
= \Psi(\vec{r}) - (\hat{n}\times\vec{r})\,\varepsilon\cdot\vec{\nabla}\Psi + \Theta(\varepsilon^2)
$$

$$
\Longrightarrow \quad \langle \vec{r} | G |\Psi\rangle = -(\hat{n}\times\vec{r})\cdot\vec{\nabla}\Psi = -\hat{n}\cdot(\vec{r}\times\vec{\nabla}\Psi)
$$

Comparando com

$$
\langle \vec{r} | \vec{L}\cdot\hat{n} |\Psi\rangle = \hat{n}\cdot\langle \vec{r} | \vec{L} | \Psi\rangle = -i\hbar\,\hat{n}\cdot(\vec{r}\times\vec{\nabla}\Psi)
$$

Concluímos que

$$
\boxed{G = \frac{-i}{\hbar}\,\vec{L}\cdot\hat{n}}
$$

**3) Uma rotação finita na direção $\hat{n}$ pode ser obtida com uma sequência de rotações infinitesimais**, unitárias como $T(\vec{a})$:

$$
\lim_{N\to\infty}\left[\mathbb{I} - i\,\frac{\vec{L}\cdot\hat{n}}{\hbar}\,\frac{\theta}{N}\right]^N = \exp\left[\frac{-i\,\vec{L}\cdot\hat{n}}{\hbar}\,\theta\right] \equiv U(\vec{\theta})
$$

Dizemos que $\vec{P}\cdot\hat{n}$ é o gerador das translações na direção $\hat{n}$, assim como $\dfrac{\vec{L}\cdot\hat{n}}{\hbar}$ é o gerador das rotações na direção $\hat{n}$.

## Comentários

**(i)** Escolhida a direção $\hat{n}$, tanto $\vec{P}\cdot\hat{n}$ quanto $\vec{L}\cdot\hat{n}$ são operadores perfeitamente bem definidos.

**Exemplo:** $\hat{n} = \dfrac{1}{\sqrt{2}}\hat{i} + \dfrac{1}{\sqrt{2}}\hat{j}$

$$
\hat{n}\cdot\vec{P} = \frac{\hat{P}_x}{\sqrt{2}} + \frac{\hat{P}_y}{\sqrt{2}}
\qquad \text{e} \qquad
\hat{n}\cdot\vec{L} = \frac{\hat{L}_x}{\sqrt{2}} + \frac{\hat{L}_y}{\sqrt{2}}
$$

**(ii)** Os operadores de translação comutam, pois os operadores $\vec{P}$ comutam. Isso não acontece com os operadores de rotação.

**Exemplo:**

$$
T(a\hat{i})\,T(b\hat{j}) = e^{-i\hat{P}_x a/\hbar}\,e^{-i\hat{P}_y b/\hbar} = T(b\hat{j})\,T(a\hat{i})
$$

$$
U(\alpha\hat{i})\,U(\beta\hat{j}) = e^{-i\hat{L}_x\alpha/\hbar}\,e^{-i\hat{L}_y\beta/\hbar}
\;\neq\;
e^{-i\hat{L}_y\beta/\hbar}\,e^{-i\hat{L}_x\alpha/\hbar}
= U(\beta\hat{j})\,U(\alpha\hat{i})
$$

Isso, contudo, não é uma particularidade de **TRANSLAÇÕES e ROTAÇÕES** na MQ. Lembre sempre que os operadores $T$ e $U$ agem sobre as funções de onda, transladando-as e rotacionando-as, como se essas fossem um objeto 3D qualquer. De fato, qualquer objeto (não apenas funções de onda) pode ser transladado em qualquer ordem, mas não pode ser rotacionado em qualquer ordem.

### Translações: a ordem não importa

Considere um cubo sendo transladado por $T_x$ e depois $T_y$, ou na ordem inversa: o estado final é o mesmo (o cubo chega à mesma posição final, deslocado por $\vec{a} = a_x\hat{i} + a_y\hat{j}$).

*(diagrama: cubo transladado por $T_x$ seguido de $T_y$, e por $T_y$ seguido de $T_x$, chegando ao mesmo estado final)*

### Rotações: a ordem importa

Considere um dado (cubo com faces numeradas) sendo rotacionado por $R_y(\pi/2)$ seguido de $R_x(\pi/2)$ (sequência 1), e por $R_x(\pi/2)$ seguido de $R_y(\pi/2)$ (sequência 2). As orientações finais do dado são diferentes nos dois casos.

**(seq. 1):** $R_y(\pi/2)$ depois $R_x(\pi/2)$.

**(seq. 2):** $R_x(\pi/2)$ depois $R_y(\pi/2)$.

Observe que:

$$
\text{(seq. 1)} \qquad R_x(\pi/2)\,R_y(\pi/2) = R\left(\frac{2\pi}{3}, \frac{1}{\sqrt{3}}(\hat{i}+\hat{j}+\hat{k})\right)
$$

onde o eixo $\dfrac{1}{\sqrt{3}}(\hat{i}+\hat{j}+\hat{k})$ é a diagonal do cubo, e o ângulo efetivo é $120^\circ$.

(É sempre possível escrever uma sequência de rotações como uma única rotação.) Você pode verificar também que:

$$
\text{(seq. 2)} \qquad R_y(\pi/2)\,R_x(\pi/2) = R\left(\frac{2\pi}{3}, \frac{1}{\sqrt{3}}(\hat{i}+\hat{j}-\hat{k})\right)
$$

**(iii)** As operações de translação e de rotação são implementadas de maneiras diferentes na MC e na MQ, pois os "estados" são objetos matemáticos diferentes nos dois casos.

| | Mec. Clássica | Mec. Quântica |
|---|---|---|
| transl.: | $(\vec{r},\vec{p}) \to (\vec{r}+\vec{a},\,\vec{p})$ | $\|\Psi\rangle \to e^{-i\vec{P}\cdot\vec{a}/\hbar}\|\Psi\rangle$ |
| rotação: | $(\vec{r},\vec{p}) \to (R\vec{r},\,R\vec{p})$ | $\|\Psi\rangle \to e^{-i\vec{L}\cdot\hat{n}\,\theta/\hbar}\|\Psi\rangle$ |

onde $R$ (matriz $3\times 3$ de rotação) é a matriz de rotação $3\times 3$.

## Invariância de Rotação

Um problema com simetria de rotação em relação ao eixo $\hat{n}$ é caracterizado, na MC, como aquele cuja função Hamiltoniana satisfaz

$$
H(\vec{r},\vec{p}) = H\big(R(\hat{n}\theta)\vec{r},\, R(\hat{n}\theta)\vec{p}\big) \qquad \forall\,\theta,\ \forall\,(\vec{r},\vec{p})
$$

onde $R(\hat{n}\theta)$ é a matriz de rotação $3\times 3$.

Isso é equivalente à invariância sob rotação infinitesimal.

$$
H(\vec{r},\vec{p}) = H\big(R(\hat{n}\varepsilon)\vec{r},\, R(\hat{n}\varepsilon)\vec{p}\big)
$$

$$
= H\big(\vec{r}+(\hat{n}\times\vec{r})\varepsilon,\ \vec{p}+(\hat{n}\times\vec{p})\varepsilon\big)
$$

$$
= H(\vec{r},\vec{p}) + \frac{\partial H}{\partial \vec{r}}\cdot(\hat{n}\times\vec{r})\,\varepsilon + \frac{\partial H}{\partial \vec{p}}\cdot(\hat{n}\times\vec{p})\,\varepsilon + \Theta(\varepsilon^2)
$$

Assim, a invariância de rotação é equivalente a

$$
\frac{\partial H}{\partial \vec{r}}\cdot(\hat{n}\times\vec{r}) + \frac{\partial H}{\partial \vec{p}}\cdot(\hat{n}\times\vec{p}) = 0
$$

Da definição de parênteses de Poisson, $\{A(\vec{r},\vec{p}), B(\vec{r},\vec{p})\} = \dfrac{\partial A}{\partial \vec{r}}\cdot\dfrac{\partial B}{\partial \vec{p}} - \dfrac{\partial A}{\partial \vec{p}}\cdot\dfrac{\partial B}{\partial \vec{r}}$,

$$
\text{(i)} \qquad \boxed{\{H,\ \hat{n}\cdot(\vec{r}\times\vec{p})\} = 0}
$$

Da expressão da taxa de variação do valor de $A(\vec{r},\vec{p})$ durante a evolução do sistema sob $H$, $\dfrac{dA}{dt} = \{H, A\}$,

$$
\text{(ii)} \quad \Longrightarrow \quad \boxed{\frac{d}{dt}(\hat{n}\cdot\vec{L}) = 0}
$$

A componente $\hat{n}$ de $\vec{L}$ permanece inalterada durante a evolução do sistema.

Correspondentemente, em MQ, temos invariância quando (a rotação no valor esperado de $\hat{n}$):

$$
\langle \Psi | H |\Psi\rangle = \langle \Psi | U^{\dagger}(\theta\hat{n})\, H\, U(\theta\hat{n}) |\Psi\rangle \qquad \forall\,\theta\ \text{e}\ \forall\,|\Psi\rangle
$$

isso é equivalente a:

$$
\langle \Psi | H |\Psi\rangle = \langle \Psi | U^{\dagger}(\varepsilon\hat{n})\, H\, U(\varepsilon\hat{n}) |\Psi\rangle \qquad \forall\,|\Psi\rangle
$$

ou,

$$
H = U^{\dagger}(\varepsilon\hat{n})\, H\, U(\varepsilon\hat{n}) \quad \Longrightarrow \quad [H, U(\varepsilon\hat{n})] = 0
$$

como $U(\varepsilon\hat{n}) = \mathbb{I} - i\dfrac{\vec{L}\cdot\hat{n}}{\hbar}\varepsilon$,

$$
\boxed{[H, \vec{L}\cdot\hat{n}] = 0} \qquad \text{(compare com (i))}
$$

De $\dfrac{d}{dt}\langle \Psi(t) | \hat{A} |\Psi(t)\rangle = \dfrac{1}{i\hbar}\langle \Psi(t) | [\hat{H},\hat{A}] |\Psi(t)\rangle$,

$$
\boxed{\frac{d}{dt}\langle \vec{L}\cdot\hat{n} \rangle = 0} \qquad \text{(compare com (ii))}
$$

A conclusão de que um dado problema mecânico é invariante sob translação/rotação é independente da maneira como você vai tratá-lo (usando MC ou MQ).

## Exemplos

**1)** Partícula interagindo com fio uniforme infinito (na direção $\hat{n}$).

*(diagrama: massa $m$ próxima a um fio retilíneo infinito, com eixo $\hat{n}$ ao longo do fio)*

$\Rightarrow$ invariância sob rotação e translação na direção $\hat{n}$.

**2)** Partícula interagindo com um hemisfério (ver figura).

*(diagrama: massa $m$ sobre um hemisfério, com eixo $z$ vertical)*

$\Rightarrow$ invariância sob rotação na direção $\hat{z}$.

**3)** Partícula interagindo com uma esfera perfeita.

*(diagrama: massa $m$ próxima a uma esfera)*

$\Rightarrow$ invariância sob rotação **EM QUALQUER EIXO**.

Nesse caso (3) temos $L_x(t), L_y(t)$ e $L_z(t) = \text{const}$ na MC, e $\langle L_x\rangle, \langle L_y\rangle, \langle L_z\rangle = \text{const}$ na MQ.

## Invariância sob translação e conservação de momento linear

De modo análogo podemos conectar invariância sob translação e conservação de momento linear.

**Mec. Clássica:**

$$
H(\vec{r}+a\hat{n}, \vec{p}) = H(\vec{r},\vec{p}) \qquad \forall\,a,\ \forall\,(\vec{r},\vec{p})
$$

$$
\Longrightarrow \quad H(\vec{r}+\varepsilon\hat{n}, \vec{p}) = H(\vec{r},\vec{p})
$$

$$
\Longrightarrow \quad H(\vec{r},\vec{p}) + \varepsilon\,\hat{n}\cdot\frac{\partial H}{\partial \vec{r}} + \dots = H(\vec{r},\vec{p})
$$

$$
\Longrightarrow \quad \hat{n}\cdot\frac{\partial H}{\partial \vec{r}} = 0
\quad \Longrightarrow \quad
\boxed{\{H,\ \hat{n}\cdot\vec{p}\} = 0 \;\Longrightarrow\; \frac{d}{dt}(\hat{n}\cdot\vec{p}) = 0}
$$

**Mec. Quântica:**

$$
\langle \Psi | T^{\dagger}(a\hat{n})\, H\, T(a\hat{n}) |\Psi\rangle = \langle \Psi | H |\Psi\rangle \qquad \forall\,a,\ \forall\,|\Psi\rangle
$$

$$
\Longrightarrow \quad \langle \Psi | T^{\dagger}(\varepsilon\hat{n})\, H\, T(\varepsilon\hat{n}) |\Psi\rangle = \langle \Psi | H |\Psi\rangle
$$

$$
\Longrightarrow \quad [H, T(\varepsilon\hat{n})] = 0
$$

usando $T(\varepsilon\hat{n}) = \mathbb{I} - i\,\hat{n}\cdot\hat{P}\,\varepsilon/\hbar + \dots$

$$
\Longrightarrow \quad \boxed{[H,\ \hat{n}\cdot\vec{P}] = 0 \;\Longrightarrow\; \frac{d}{dt}\langle \hat{n}\cdot\vec{P} \rangle = 0}
$$
