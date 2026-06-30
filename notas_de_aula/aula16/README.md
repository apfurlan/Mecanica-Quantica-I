# (16ª aula) --- Oscilador Harmônico (Cap. 7)

## A Hamiltoniana Clássica do Oscilador Harmônico

A Hamiltoniana clássica de uma massa $m$, que se move em 1D sob a ação de uma força do tipo $F = -kx$, onde $x$ é a posição da partícula, é

$$H(x,p) = \frac{p^2}{2m} + \frac{1}{2}kx^2$$

Ou, usando $\omega = \sqrt{\dfrac{k}{m}}$,

$$H(x,p) = \frac{p^2}{2m} + \frac{1}{2}m\omega^2 x^2 .$$

Essa Hamiltoniana aparece em inúmeras situações na Física pois ela é a forma **APROXIMADA** da Hamiltoniana de uma partícula que se move nas proximidades de um mínimo de um potencial $V(x)$ genérico.

*(figura: poço de potencial genérico com mínimo em $x_0$)*

$$H(x,p) = \frac{p^2}{2m} + V(x), \quad \text{para movimentos próximos a } x_0$$

$$\simeq \frac{p^2}{2m} + V(x_0) + \overbrace{V'(x_0)}^{0}(x-x_0) + \frac{1}{2}V''(x_0)(x-x_0)^2 + \cdots$$

Eliminando a constante $V(x_0)$ temos uma Hamiltoniana de oscilador harmônico com "constante de mola" $k = V''(x_0)$ (derivada segunda do potencial no mínimo).

Se mudamos a origem do eixo $x$ para $x_0$ temos exatamente

$$H(x,p) = \frac{p^2}{2m} + \frac{1}{2}kx^2 .$$

> **Obs:** Não se deve perder de vista que essa forma da Hamiltoniana só é válida se $x$ permanecer próximo à origem (o ponto de equilíbrio). Para grandes deslocamentos, a força completa, com $V(x)$, deve ser usada.

## Modos Normais

Quando temos um sistema com várias partículas em mais de 1 dimensão, encontramos situações próximas do equilíbrio descritas por Lagrangianas e Hamiltonianas na forma

$$\mathcal{L}(\vec{q}, \dot{\vec{q}}) = \sum_{i=1}^{N}\sum_{j=1}^{N} \frac{1}{2}M_{ij}\dot{q}_i\dot{q}_j - \frac{1}{2}V_{ij}q_i q_j$$

$$H(\vec{p}, \vec{q}) = \sum_{i=1}^{N}\sum_{j=1}^{N} \frac{1}{2}(M^{-1})_{ij}p_i p_j + \frac{1}{2}V_{ij}q_i q_j$$

onde $M_{ij}$ e $V_{ij}$ são matrizes simétricas, e $q_i$ é a coordenada (não necessariamente cartesiana) correspondente ao deslocamento do ponto de equilíbrio.

Mudando as coordenadas: $\vec{q} = (q_1, q_2, \dots, q_N)$,

$$\vec{q}(t) = \sum_{k=1}^{N} c_k(t)\,\vec{v}_k$$

onde os $N$ vetores $\vec{v}_k$ são autovetores de

$$\omega_k^2 \, M \, \vec{v}_k = V\, \vec{v}_k$$

com "ortonormalização"

$$\vec{v}_k \cdot M \cdot \vec{v}_\ell = \delta_{k\ell} \qquad \text{e} \qquad \vec{v}_k \cdot V \cdot \vec{v}_\ell = \omega_k^2\,\delta_{k\ell}.$$

A Lagrangiana para as novas coordenadas $c_k(t)$ é

$$\mathcal{L}(\vec{c}, \dot{\vec{c}}) = \sum_{k=1}^{N} \left( \frac{1}{2}\dot{c}_k^2 - \frac{1}{2}\omega_k^2 c_k^2 \right)$$

igual a $N$ osciladores harmônicos 1D *INDEPENDENTES*.

Isso justifica o interesse em conhecer, clássica e quanticamente, a solução do problema associado a

$$H(x,p) = \frac{p^2}{2m} + \frac{1}{2}m\omega^2 x^2 .$$

## Mecânica Clássica

As equações de Hamilton para $x(t)$ e $p(t)$ são

$$\dot{p} = -m\omega^2 x \qquad \text{e} \qquad \dot{x} = \frac{p}{m}.$$

Eliminando $p(t)$ obtemos a equação de Newton

$$\ddot{x} = -\omega^2 x$$

com solução

$$x(t) = A\cos\omega t + B \sin\omega t,$$

onde $A, B$ são determinados pelas condições iniciais $x(0)$ e $\dot{x}(0)$.

A Hamiltoniana é conservada (porque?) e é igual à energia cinética mais a energia potencial. Usando $p(t) = m\dot{x} = -m\omega A \sin\omega t + m\omega B\cos\omega t$ em

$$H = \frac{p^2}{2m} + \frac{1}{2}m\omega^2 x^2$$
$$= \frac{1}{2m}\left(-m\omega A\sin\omega t + m\omega B \cos\omega t\right)^2 + \frac{1}{2}m\omega^2\left(A\cos\omega t + B \sin\omega t\right)^2$$
$$= \frac{1}{2}m\omega^2 (A^2 + B^2)$$

A energia total pode ter qualquer valor $E \geq 0$.

## Mecânica Quântica

Como fizemos com todos os problemas até aqui, vamos começar procurando os autoestados e autovalores do operador

$$\hat{H} = \frac{\hat{P}^2}{2m} + \frac{1}{2}m\omega^2 \hat{X}^2 .$$

Da forma do potencial *(figura: poço parabólico com níveis $E_1, E_2, E_3, E_4$)*

vemos que os autovalores são **DISCRETOS**, **NÃO-DEGENERADOS** e **POSITIVOS** (você sabe porquê?).

Até agora só vimos potenciais constantes aos pedaços (i.e. descontínuos) *(figuras: poços retangulares)*

O potencial harmônico fornece uma equação de autovalor na forma

$$\hat{H}|E\rangle = E|E\rangle$$

$$\Longrightarrow \quad -\frac{\hbar^2}{2m}\frac{d^2\psi_E}{dx^2} + \frac{1}{2}m\omega^2 x^2 \psi_E(x) = E\,\psi_E(x)$$

válida em todo o eixo-$x$.

Essa equação pode ser resolvida para qualquer valor de $E$, mas apenas **CERTOS VALORES DE $E$** têm como solução funções $\psi_E(x)$ que $\to 0$ quando $x \to \pm\infty$.

Vamos encontrar os autovalores $E$ e as autofunções $\psi_E(x)$ usando uma técnica de série de potências que será útil em outros casos (por exemplo no caso do potencial coulombiano).

## 1 --- Torne a EDO adimensional

Fazemos $x = by$, onde $y$ é a variável adimensional e $b$ é uma unidade de comprimento.

$$\psi_E(x) = \psi_E(by)$$

$$\frac{d\psi_E}{dx} = \frac{d\psi_E}{dy}\frac{dy}{dx} = \frac{d\psi_E}{dy}\frac{1}{b}$$

Substituindo na equação de Schrödinger,

$$-\frac{\hbar^2}{2mb^2}\frac{d^2\psi_E}{dy^2} + \frac{1}{2}m\omega^2 b^2 y^2 \psi_E = E\,\psi_E$$

$$\psi_E'' + \left( \underbrace{\frac{2mEb^2}{\hbar^2}}_{\text{sem dimensão}} - \underbrace{\frac{m^2\omega^2 b^4}{\hbar^2}y^2}_{\text{sem dimensão}} \right)\psi_E = 0$$

Escolhemos $b = \sqrt{\dfrac{\hbar}{m\omega}}$ para tornar o segundo termo igual a $1$, e definimos a energia adimensional

$$\varepsilon = \frac{mb^2 E}{\hbar^2} = \frac{E}{\hbar\omega}.$$

Assim temos a EDO adimensional

$$\boxed{\psi_E'' + (2\varepsilon - y^2)\psi_E = 0}$$

Queremos encontrar os valores de $\varepsilon$ que têm como solução $\psi_E(y)$ tal que $\psi_E \to 0$ quando $y \to \pm\infty$.

## Análise Assintótica

Como essa EDO não é conhecida, analisamos a forma de sua solução (para um $\varepsilon$ genérico) em $y \to 0$ e $|y| \to \infty$.

$$y \to 0: \quad \psi_E'' + 2\varepsilon\,\psi_E = 0 \;\Longrightarrow\; \psi_E(y) = A\cos\left(\sqrt{2\varepsilon}\,y\right) + B\sin\left(\sqrt{2\varepsilon}\,y\right)$$
$$\simeq A + B\sqrt{2\varepsilon}\,y + O(y^2)$$

$$|y| \to \infty: \quad \psi_E'' - y^2 \psi_E = 0$$
$$\psi_E(y) = y^m e^{\pm y^2/2} \quad \text{satisfaz essa equação \textbf{NESSE LIMITE}}$$
$$\psi_E''(y) = y^{m+2}e^{\pm y^2/2}\left( 1 \pm \frac{2m+1}{y} + \frac{m(m-1)}{y^2} \right) \simeq y^2 \psi_E(y)$$

Essas análises mostram que, para um $\varepsilon$ **GENÉRICO**,

$$\psi_E \to
\begin{cases}
A + By & y \to 0 \quad \text{(regular na origem)} \\
y^m e^{\pm y^2/2} & |y| \to \infty
\end{cases}$$

Quando $\varepsilon$ **NÃO** corresponde a um autovalor, as 2 soluções independentes divergem no infinito como $y^m e^{y^2/2}$ e $y^n e^{y^2/2}$. Quando $\varepsilon$ é um dos autovalores, uma das soluções vai como $y^m e^{-y^2/2}$ (e a outra continua divergindo como $y^n e^{y^2/2}$).

## Série de Potências

Usamos $\psi_E(y) = u(y)\,e^{-y^2/2}$ na EDO.

$$\psi_E'' = \left[u'' - 2yu' + (y^2-1)u\right]e^{-y^2/2}$$

e obtemos a seguinte EDO para $u(y)$:

$$\boxed{u'' - 2yu' + (2\varepsilon - 1)u = 0}$$

Essa EDO, diferentemente da $\psi_E'' + (2\varepsilon - y^2)\psi_E = 0$, se presta à solução por série de potências

$$u(y) = \sum_{n=0}^{\infty} c_n y^n \qquad \text{(regular na origem!)}$$

$$\sum_{n=0}^{\infty} n(n-1)c_n y^{n-2} - 2n\,c_n y^n + (2\varepsilon - 1)c_n y^n = 0$$

reescrevemos a 1ª série como

$$\sum_{n=0}^{\infty} n(n-1)c_n y^{n-2} = \sum_{n=2}^{\infty} n(n-1)c_n y^{n-2}$$
$$= \sum_{m=0}^{\infty} (m+2)(m+1)c_{m+2}\, y^m$$

$$\sum_{n=0}^{\infty} \left[ (n+2)(n+1)c_{n+2} - (2n+1-2\varepsilon)c_n \right] y^n = 0$$

O termo entre colchetes deve ser nulo, e obtemos uma relação entre $c_n$ e $c_{n+2}$ $\Rightarrow$ por isso a EDO se presta à solução por séries!

Tratamos $c_0$ e $c_1$ como as 2 constantes arbitrárias e encontramos

$$\psi(y) = \; c_0\left[ 1 + \frac{(1-2\varepsilon)}{2}y^2 + \frac{(1-2\varepsilon)(5-2\varepsilon)}{2\cdot 12}y^4 + \cdots \right]e^{-y^2/2}$$
$$+ \; c_1\left[ y + \frac{(3-2\varepsilon)}{6}y^3 + \frac{(3-2\varepsilon)(7-2\varepsilon)}{6\cdot 24}y^5 + \cdots \right]e^{-y^2/2}$$

onde usei

$$\boxed{c_{n+2} = \frac{2n+1-2\varepsilon}{(n+2)(n+1)}c_n}$$

para obter $\{c_2, c_4, c_6, \dots\}$ em termos de $c_0$ e $\{c_3, c_5, c_7, \dots\}$ em termos de $c_1$.

Essa é a solução geral de $\psi'' + (2\varepsilon - y^2)\psi = 0$ para um $\varepsilon$ genérico.

Veja que se $2\varepsilon = \{1,3,5,\dots\}$ um dos dois colchetes se torna um polinômio **FINITO** e obtemos uma solução que pertence à classe de funções da MQ (e que multiplicado é $y^n e^{-y^2/2}$).

Caso $2\varepsilon \neq \{1,3,5,\dots\}$, **AMBAS** as soluções divergem no infinito como $y^m e^{y^2/2}$ (isso pode não ser óbvio mas é demonstrável).

## Autoenergias e Autofunções

$$\text{AUTOENERGIAS:} \quad 2\varepsilon = 2n+1 \qquad (n=0,1,2,\dots)$$

$$\frac{2E}{\hbar\omega} = 2n+1 \;\Longrightarrow\; \boxed{E = \left(n+\frac{1}{2}\right)\hbar\omega}$$

AUTOFUNÇÕES (não normalizadas):

$$n=0 \;\; (2\varepsilon=1): \quad \psi_0(y) = e^{-y^2/2}$$
$$n=1 \;\; (2\varepsilon=3): \quad \psi_1(y) = y\,e^{-y^2/2}$$
$$n=2 \;\; (2\varepsilon=5): \quad \psi_2(y) = (1-2y^2)\,e^{-y^2/2}$$
$$n=3 \;\; (2\varepsilon=7): \quad \psi_3(y) = \left(y - \frac{2}{3}y^3\right)e^{-y^2/2}, \quad \text{etc.}$$

## Polinômios de Hermite

Esses polinômios multiplicando $e^{-y^2/2}$ são os **POLINÔMIOS DE HERMITE**. Sua definição correta é

$$H_0(y) = 1$$
$$H_1(y) = 2y$$
$$H_2(y) = -2(1-2y^2)$$
$$H_3(y) = -12\left(y - \frac{2}{3}y^3\right)$$
$$H_4(y) = 12\left(1 - 4y^2 + \frac{4}{3}y^4\right), \quad \text{etc.}$$

Basta lembrar $H_0$ e $H_1$ pois a **FÓRMULA DE RECORRÊNCIA** determina os demais

$$\boxed{H_{n+1} = 2y H_n - 2n H_{n-1}}$$

Temos também a relação de ortogonalidade:

$$\int_{-\infty}^{\infty} H_n(y) H_m(y)\, e^{-y^2}\, dy = \delta_{mn}\left(\sqrt{\pi}\,2^n n!\right),$$

que faz com que as autofunções **NORMALIZADAS** do oscilador harmônico sejam

$$\boxed{\psi_n(x) = \frac{1}{\sqrt{b}}\left(\frac{1}{\sqrt{\pi}\,2^n n!}\right)^{1/2} H_n(x/b)\, e^{-x^2/2b^2}}$$

onde $b = \sqrt{\dfrac{\hbar}{m\omega}}$.

## Estado Fundamental e Primeiro Estado Excitado

$E_0 = \dfrac{\hbar\omega}{2}$ *(figuras: poço parabólico com nível $E_0$ e a autofunção $\psi_0$, gaussiana simétrica)*

$E_1 = \dfrac{3\hbar\omega}{2}$ *(figuras: poço parabólico com nível $E_1$ e a autofunção $\psi_1$, ímpar)*

$\to$ Note o comportamento oscilatório na região classicamente permitida e o decaimento na região proibida.

$\to$ Note que para $n$ par a função é par, $\psi_n(x) = \psi_n(-x)$, enquanto para $n$ ímpar a função é ímpar, $\psi_n(x) = -\psi_n(-x)$.

Isso ajuda a calcular alguns integrais como

$$\langle 4|\hat{X}|6\rangle = \int_{-\infty}^{\infty} \underbrace{\psi_4(x)}_{\text{par}} \, x \, \underbrace{\psi_6(x)}_{\text{par}}\, dx = 0$$

Existe uma outra fórmula de recorrência útil entre os polinômios de Hermite

$$\boxed{H_n' = 2n\,H_{n-1}}$$

Use isso em cálculos envolvendo o operador $\hat{P}$.

Por exemplo:

$$\frac{d}{dx}\psi_5(x/b) = \frac{1}{b}\frac{d}{dy}\left[ A_5 H_5(y) e^{-y^2/2} \right] \qquad (A_5: \text{const. de normalização})$$
$$= \frac{A_5}{b}\left[ 10\,H_4(y) - y\,H_5(y) \right] e^{-y^2/2}$$

Portanto a energia de um oscilador harmônico é **QUANTIZADA** em múltiplos de $\hbar\omega$. Além disso a menor energia possível de ser encontrada em uma medida é $\dfrac{\hbar\omega}{2}$, a energia do **ESTADO FUNDAMENTAL**.

## Comparação com a Caixa Infinita

A situação no potencial harmônico é semelhante à encontrada na caixa infinita.

*(figura: oscilador harmônico)*

$$\boxed{E_n = \left(n+\tfrac{1}{2}\right)\hbar\omega} \quad (n=0,1,2,\dots)$$

*(figura: autofunção do estado fundamental)*

estado fundamental

*(figura: poço infinito)*

$$\boxed{E_n = \dfrac{n^2\pi^2\hbar^2}{2mL^2}} \quad (n=1,2,3,\dots)$$

*(figura: autofunção do estado fundamental da caixa)*

apenas na caixa os níveis de energia não são uniformemente espaçados.

## Combinação Linear de Autoestados

Os autoestados do operador $\hat{H}$ são os estados de energia bem definida. Assim, por exemplo, no estado (normalizado)

$$|\Psi\rangle = \frac{1}{\sqrt{6}}|0\rangle + \frac{2}{\sqrt{6}}|2\rangle + \frac{1}{\sqrt{6}}|7\rangle$$

em uma medida de energia, só podemos encontrar

- $\dfrac{\hbar\omega}{2}$, com probabilidade $1/6$
- $\dfrac{5\hbar\omega}{2}$, com probabilidade $4/6$
- $\dfrac{15\hbar\omega}{2}$, com probabilidade $1/6$

## Operador de Evolução e Propagador

Esses autoestados permitem a construção do operador de evolução e do propagador desse Hamiltoniano.

$$\hat{U}(t) = \sum_{n=0}^{\infty} e^{-iE_n t/\hbar}|n\rangle\langle n| \qquad \left(E_n = \left(n+\tfrac{1}{2}\right)\hbar\omega\right)$$

$$\langle x|\hat{U}(t)|x'\rangle = \sum_{n=0}^{\infty} e^{-iE_n t/\hbar} A_n^2 H_n(x/b) H_n(x'/b)\, e^{-(x^2+x'^2)/2b^2}$$

isso pode ser somado e é igual a (com $b = \sqrt{\hbar/m\omega}$)

$$\boxed{U(x,x';t) = \left( \frac{1}{b^2 2\pi i \sin\omega t} \right)^{1/2} \exp\left[ \frac{i}{b^2}\frac{(x^2+x'^2)\cos\omega t - 2xx'}{2\sin\omega t} \right]}$$

Com o propagador podemos conhecer (a princípio) a evolução de qualquer estado inicial $\Psi(x,0)$

$$\Psi(x,t) = \int_{-\infty}^{\infty} dx' \, U(x,x';t)\,\Psi(x',0)$$

## Limite Clássico

**LIMITE CLÁSSICO** --- No caso do potencial quadrático, o teorema de Ehrenfest diz que os valores médios

$$\langle x(t) \rangle = \langle \Psi(t)| \hat{X} |\Psi(t)\rangle \qquad \text{e} \qquad \langle p(t) \rangle = \langle \Psi(t)| \hat{P} |\Psi(t)\rangle$$

de **QUALQUER** $|\Psi(t)\rangle$ que evolua com o $\hat{H}$ do oscilador harmônico obedecem às equações clássicas.

$$\frac{d\langle x \rangle}{dt} = \frac{\langle p \rangle}{m} \qquad \text{(qualquer potencial tem essa propriedade)}$$

$$\frac{d\langle p \rangle}{dt} = \underbrace{F(\langle x \rangle)}_{\text{força}} \qquad \text{(apenas os potenciais quadrático, linear e constante têm essa propriedade; em geral o lado direito é } \langle F(x) \rangle \text{)}$$

No caso de um "pacote clássico" gaussiano

$$\Psi(x,0) = \left( \frac{1}{\pi\Delta^2} \right)^{1/4} e^{ip_0 x/\hbar}\, e^{-(x-x_0)^2/2\Delta^2}$$

veremos a evolução no tempo *(figuras: pacote de onda oscilando entre $-A$ e $A$, passando por $O$ com velocidade máxima)*

O valor médio $\langle x \rangle$ oscila exatamente como a partícula clássica e a força (o pacote se alarga e se estreita durante a oscilação).

## Quantização Imperceptível para Massas/Sistemas Grandes

Além disso, a quantização dos níveis de energia é **IMPERCEPTÍVEL** no caso de massas grandes.

Imagine uma massa pequena e uma grande sob a ação de um mesmo potencial $V(x) = \dfrac{1}{2}kx^2$

*(figuras: níveis espaçados por $\hbar\omega$ para m pequena; níveis muito próximos para m grande)*

Isso ocorre pois $\hbar\omega = \hbar\sqrt{\dfrac{k}{m}}$ é o espaçamento dos níveis.

O mesmo ocorre no poço infinito. Imagine uma massa grande e uma pequena confinadas em uma região de tamanho $L$.

*(figuras: níveis $E_1, E_2, E_3$ para m pequena; níveis muito próximos para m grande)*

Isso ocorre pois $E_n = \dfrac{n^2\pi^2\hbar^2}{2mL^2}$ é inversamente proporcional à massa.
