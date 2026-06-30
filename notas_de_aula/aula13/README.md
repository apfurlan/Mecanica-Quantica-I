# (13ª aula) — Princípio da Incerteza, Estados Impróprios e a Equação de Schrödinger

## O Princípio da Incerteza de Heisenberg (revisitando o exemplo 4.2.4)

O exemplo 4.2.4 ilustra o **princípio da incerteza de Heisenberg**. $\Delta X$ é uma medida da incerteza sobre a posição da partícula, $\Delta P$ é uma medida da incerteza sobre o momentum da partícula:

$$
\Delta X = \frac{\Delta}{\sqrt{2}} \qquad \text{e} \qquad \Delta P = \frac{\hbar}{\sqrt{2}\,\Delta}
$$

Isso mostra que fazer $\Delta \to 0$ torna a posição mais definida, mas faz o momentum da partícula menos preciso. Fazer $\Delta \to \infty$ melhora a definição do momentum, mas torna a posição menos precisa.

Veremos mais adiante que, para qualquer estado,

$$
\boxed{\Delta X \, \Delta P \geq \frac{\hbar}{2}}
$$

> A natureza impõe a impossibilidade de se medir $X$ e $P$ com precisão arbitrária, e isso é incluído na teoria ao associar posição e momentum a dois operadores que **NÃO COMUTAM** (e portanto não têm autovetores comuns).

Os autoestados de posição e momentum são exemplos de funções de onda **IMPRÓPRIAS** (que não podem ser normalizadas a $\langle \Psi|\Psi \rangle = 1$):

$$
\langle x|p \rangle = \Psi_p(x) = \frac{1}{\sqrt{2\pi\hbar}} \, e^{ipx/\hbar} \qquad \text{(momentum $p$)}
$$

$$
\langle x|a \rangle = \delta(x-a) \qquad \text{(posição $a$)}
$$

Ambos os estados são objetos matemáticos úteis para se fazer cálculos, embora apenas estados **PRÓPRIOS** correspondam a estados físicos (que podem ser produzidos em laboratório).

Embora $|\Psi_p(x)|^2 = 1$, o que implicaria que a partícula associada tem igual probabilidade de ser encontrada em qualquer parte do universo, na prática as partículas que saem de um acelerador com energia cinética definida têm certo grau de localização e são estados próprios.

$$
\Psi_p(x) = \frac{1}{\sqrt{2\pi\hbar}} \, e^{ipx/\hbar} \, , \quad \text{estado impróprio}
$$

$$
\tilde{\Psi}_p(x) = \frac{1}{\sqrt{2\pi\hbar}} \, e^{ipx/\hbar} \, f(x) \, , \quad \text{estado próprio}
$$

onde $f(x)$ é uma função envelope, tal que

$$
\int_{-\infty}^{\infty} |\tilde{\Psi}_p(x)|^2 \, dx = 1 \, .
$$

A função envelope $f(x)$ cresce de $0$ a $1$ em torno da origem e permanece igual a $1$ ao longo de um comprimento $L$, decaindo de volta a $0$ em seguida (um patamar suave de largura $L$, como uma função degrau suavizada).

Uma partícula em uma posição bem definida também nunca está em um estado $\delta(x-a)$, e sim em um estado próprio bem localizado:

$$
\Psi(x) = \delta(x-a) \, , \quad \text{estado impróprio}
$$

$$
\tilde{\Psi}(x) = \frac{1}{(\pi\Delta^2)^{1/4}} \, e^{-(x-a)^2/2\Delta^2} \, , \quad \text{estado próprio (representação da função delta)}
$$

A primeira função, $\Psi(x) = \delta(x-a)$, é representada por uma seta vertical de altura infinita localizada em $x=a$ (o símbolo usual da função delta de Dirac). A segunda, $\tilde{\Psi}(x)$, é um pico gaussiano estreito e suave centrado em $x=a$, de largura proporcional a $\Delta$ — uma aproximação suave da função delta.

## Medida Ideal de Posição

A imagem de um ponto produzida por um instrumento óptico não é um ponto, devido ao fato de a luz oriunda do ponto ter que atravessar os orifícios (diafragmas) do aparelho. O grau de resolução de um instrumento dá a separação mínima entre 2 pontos para que suas imagens sejam distinguíveis.

Considere duas fontes pontuais emitindo luz de comprimento de onda $\lambda$, separadas por uma distância $\Delta x$ na direção transversal, vistas através de uma abertura que subtende um ângulo $\Delta\theta$. Se a separação angular entre as imagens é muito menor que a abertura angular do instrumento, as duas fontes aparecem como uma só (caso **não distinguível**); se a separação é suficiente, as imagens aparecem separadas no plano focal (caso **distinguível**). O critério de resolução máxima é

$$
\boxed{\Delta x \sim \frac{\lambda}{\sin\Delta\theta}}
$$

(A resolução é importante pois você, na medida de posição, tenta localizar o elétron em relação a alguma referência.)

Se você quer localizar com precisão, use $\lambda \to 0$ (essa seria a medida ideal de posição).

O problema é que fótons que entram no aparelho (após espalharem no elétron) terão momentum na faixa

$$
-\frac{h}{\lambda}\sin\Delta\theta \;\leq\; p_x \;\leq\; \frac{h}{\lambda}\sin\Delta\theta
$$

Como os fótons ganharam esse momentum na colisão com o elétron, isso implica que a incerteza no momentum $P_x$ do elétron é

$$
\Delta P_x = \frac{h}{\lambda}\sin\Delta\theta \qquad \text{(por causa da colisão)}
$$

$$
\Delta x = \frac{\lambda}{\sin\Delta\theta} \qquad \text{(por causa da resolução óptica)}
$$

Multiplicando as duas expressões, o produto $\lambda$ e $\sin\Delta\theta$ se cancela:

$$
\boxed{\Delta x \, \Delta P_x \sim h}
$$

Claro que isso só é problema para objetos muito pequenos e muito leves; para bolas de gude, grãos de areia, etc., podemos ignorar $h$ e imaginar que é possível medir $X$ e $P_x$ com precisão arbitrária. (Veremos que nesses casos as previsões da MQ coincidem com as da MC.)

## Generalização para Mais Graus de Liberdade

Para estudar um sistema de $N$ coordenadas cartesianas $x_1, \dots, x_N$, que podem ser $N$ partículas se movendo em 1D, $N/3$ partículas se movendo em 3D, etc.

Modificamos o postulado II para:

A cada coordenada cartesiana clássica $x_i$ temos um operador $\hat{X}_i$. Os operadores $\hat{X}_i$ comutam entre si e sua base de autovetores comuns é

$$
|x_1, x_2, \dots, x_N\rangle
$$

por exemplo, $\hat{X}_3 |x_1, x_2, \dots, x_N\rangle = x_3 |x_1, \dots, x_N\rangle$.

$$
\langle x_1' \cdots x_N'|x_1 \cdots x_N \rangle = \delta(x_1 - x_1')\,\delta(x_2 - x_2') \cdots \delta(x_N - x_N')
$$

A função de onda é uma função de $N$ variáveis:

$$
\langle x_1 \cdots x_N|\Psi \rangle = \Psi(x_1, x_2, \dots, x_N)
$$

$$
\langle x_1 \cdots x_N|\hat{P}_i|\Psi\rangle = -i\hbar \frac{\partial}{\partial x_i} \Psi(x_1, x_2, \dots, x_N) \, ,
$$

define a ação do operador momentum $P_i$.

Temos os comutadores $[\hat{X}_\alpha, \hat{P}_\beta] = i\hbar\,\delta_{\alpha\beta}$ (apenas as coordenadas e momenta conjugados não comutam).

## Exemplo: Partícula em um Potencial Harmônico em 3D

Uma partícula de massa $m$ se move em 3D, $x$, $y$ e $z$ são suas coordenadas cartesianas (em um potencial harmônico).

$$
H(p_x, p_y, p_z, x, y, z) = \frac{p_x^2 + p_y^2 + p_z^2}{2m} + \frac{1}{2}m\omega^2(x^2+y^2+z^2)
$$

é a hamiltoniana clássica. O operador quântico fica

$$
\hat{H} = \frac{\hat{P}_x^2 + \hat{P}_y^2 + \hat{P}_z^2}{2m} + \frac{1}{2}m\omega^2(\hat{X}^2+\hat{Y}^2+\hat{Z}^2)
$$

(pois são 3 variáveis).

A EDP que determina os autovalores e autovetores de $\hat{H}$:

$$
\hat{H}|E\rangle = E|E\rangle
$$

onde $|E\rangle$ representa uma função complexa no espaço das funções $f(x,y,z)$.

Tome produto interno com $\langle x,y,z|$:

$$
\langle x,y,z| \frac{\hat{P}_x^2+\hat{P}_y^2+\hat{P}_z^2}{2m} + \frac{1}{2}m\omega^2(\hat{X}^2+\hat{Y}^2+\hat{Z}^2) |E\rangle = E\,\Psi_E(x,y,z)
$$

Use

$$
\langle x,y,z|\hat{P}_x^2|E\rangle = -\hbar^2 \frac{\partial^2}{\partial x^2}\Psi_E(x,y,z)
$$

$$
\langle x,y,z|\hat{X}^2|E\rangle = x^2\,\Psi_E(x,y,z)
$$

e outros (análogos para $\hat{P}_y^2$, $\hat{P}_z^2$, $\hat{Y}^2$, $\hat{Z}^2$). Encontro

$$
-\frac{\hbar^2}{2m}\left(\frac{\partial^2}{\partial x^2} + \frac{\partial^2}{\partial y^2} + \frac{\partial^2}{\partial z^2}\right)\Psi_E(x,y,z) + \frac{1}{2}m\omega^2(x^2+y^2+z^2)\,\Psi_E = E\,\Psi_E
$$

## Antecipação: Momento Angular

Só como antecipação: $\vec{L} = \vec{r}\times\vec{p}$ é o momento angular em relação à origem. Em componentes,

$$
L_x = yp_z - zp_y \, ; \qquad L_y = zp_x - xp_z \, ; \qquad L_z = xp_y - yp_x
$$

Os operadores da MQ comutam a menos de

$$
[\hat{X},\hat{P}_x] = [\hat{Y},\hat{P}_y] = [\hat{Z},\hat{P}_z] = i\hbar
$$

por isso podemos definir os operadores

$$
\hat{L}_x = \hat{Y}\hat{P}_z - \hat{Z}\hat{P}_y \, , \quad \text{etc.}
$$

sem risco de ambiguidade.

Sua EDP de autovalores fica

$$
\langle x,y,z|\hat{L}_x|\Psi\rangle = \ell_x \langle x,y,z|\Psi\rangle
$$

$$
\left(-i\hbar y\frac{\partial}{\partial z} - i\hbar z\frac{\partial}{\partial y}\right)\Psi(x,y,z) = \ell_x\,\Psi(x,y,z)
$$

Vamos aprender a resolver essas equações no cap. 12.

## A Equação de Schrödinger (seção 4.3)

O postulado IV diz que a evolução no tempo do vetor de estado se dá de acordo com

$$
i\hbar \frac{d}{dt}|\Psi(t)\rangle = \hat{H}|\Psi(t)\rangle
$$

onde $\hat{H}$ é o operador Hamiltoniano associado à função Hamiltoniana clássica.

**Exemplos:**

**(i)**

$$
H(p,x) = \frac{p^2}{2m} + \frac{1}{2}m\omega^2 x^2 \quad \longrightarrow \quad \hat{H} = \frac{\hat{P}^2}{2m} + \frac{1}{2}m\omega^2\hat{X}^2
$$

(aqui o vetor de estado $|\Psi(t)\rangle$ representa uma função de onda $\langle x|\Psi(t)\rangle = \Psi(x,t)$.)

**(ii)**

$$
H(x,y,z,p_x,p_y,p_z) = \frac{1}{2m}(p_x^2+p_y^2+p_z^2) + V(x,y,z)
$$

$$
\longrightarrow \quad \hat{H} = \frac{\hat{P}_x^2+\hat{P}_y^2+\hat{P}_z^2}{2m} + V(\hat{X},\hat{Y},\hat{Z})
$$

aqui $V(\hat{X},\hat{Y},\hat{Z})$ é uma função dos operadores $\hat{X}$, $\hat{Y}$ e $\hat{Z}$.

$$
V = \begin{cases}
-F\hat{X} & \to \text{força constante $F$ na direção $x$} \\[2mm]
\dfrac{1}{2}m\omega^2(\hat{X}^2+\hat{Y}^2+\hat{Z}^2) & \to \text{força harmônica em direção à origem} \\[2mm]
\text{etc.}
\end{cases}
$$

Nesses casos, o vetor de estado representa uma função de onda $\langle x,y,z|\Psi(t)\rangle = \Psi(x,y,z,t)$.

**(iii)**

$$
H(x,y,z,p_x,p_y,p_z) = \frac{\left(p_x - \frac{q}{c}A_x\right)^2 + \left(p_y - \frac{q}{c}A_y\right)^2 + \left(p_z - \frac{q}{c}A_z\right)^2}{2m} + q\phi(x,y,z,t)
$$

Nesse caso temos uma carga $q$ interagindo com campos $\vec{E}$ e $\vec{B}$ descritos pelos potenciais $\vec{A}$ e $\phi$.

O operador quântico desse problema é obtido fazendo

$$
p_x \to \hat{P}_x \, , \qquad x \to \hat{X} \, , \qquad \text{etc.}
$$

As funções $A_x(x,y,z,t)$ viram funções dos operadores $\hat{X}$, $\hat{Y}$, $\hat{Z}$ (o mesmo para $\phi$).

O único cuidado que você deve ter é caso $A_x$ dependa de $x$ (ou $A_y$ de $y$, ou $A_z$ de $z$), nesses casos onde

$$
\vec{\nabla}\cdot\vec{A} \neq 0 \, ,
$$

você deve simetrizar os $\left(P_i - \dfrac{q}{c}A_i\right)^2$. Por exemplo,

$$
\left(P_x - \frac{q}{c}A_x\right)^2 \;\to\; \left(\hat{P}_x - \frac{q}{c}A_x\hat{X}\right)^2 = \hat{P}_x^2 - \frac{qA}{c}\underbrace{\left(\hat{P}_x\hat{X} + \hat{X}\hat{P}_x\right)}_{\text{simetrização}} + \left(\frac{qA}{c}\right)^2\hat{X}^2
$$

## Resolvendo a Equação de Schrödinger

Durante esse 1º semestre nossos $\hat{H}$'s **NÃO DEPENDEM DO TEMPO**.

**1) Determine os autovetores/autovalores de $\hat{H}$**

$$
\hat{H}|E,\alpha\rangle = E|E,\alpha\rangle
$$

onde $\alpha$ é um índice adicional necessário caso $E$ seja um autovalor degenerado.

(Na prática essa equação é resolvida como uma EDP.)

**2) Determine a evolução temporal dos coeficientes**

$$
|\Psi(t)\rangle = \sum_{E,\alpha} a_{E\alpha}(t) |E,\alpha\rangle
$$

Usando essa expressão na equação de Schrödinger:

$$
\underbrace{i\hbar \sum_{E,\alpha} \dot{a}_{E\alpha}(t)|E,\alpha\rangle}_{i\hbar \frac{d}{dt}|\Psi(t)\rangle} = \underbrace{\sum_{E,\alpha} E\,a_{E\alpha}(t)|E,\alpha\rangle}_{\hat{H}|\Psi(t)\rangle}
$$

Como $|E,\alpha\rangle$ forma uma base:

$$
i\hbar \frac{da_{E\alpha}}{dt} = E\,a_{E\alpha} \quad \Longrightarrow \quad \boxed{a_{E\alpha}(t) = e^{-iEt/\hbar}\,a_{E\alpha}(0)}
$$

onde $a_{E\alpha}(0)$ são os coeficientes de $|\Psi(0)\rangle$ (condição inicial que deve ser fornecida).

**3) Levando na expressão de $|\Psi(t)\rangle$, obtenho $\hat{U}(t)$**

$$
\begin{aligned}
|\Psi(t)\rangle &= \sum_{E,\alpha} a_{E\alpha}(t)|E,\alpha\rangle \\
&= \sum_{E,\alpha} e^{-iEt/\hbar}\, a_{E\alpha}(0)\,|E,\alpha\rangle \\
&= \sum_{E,\alpha} e^{-iEt/\hbar}\,|E,\alpha\rangle\underbrace{\langle\alpha,E|\Psi(0)\rangle}_{a_{E\alpha}(0)}
\end{aligned}
$$

$$
\Longrightarrow \quad \boxed{\hat{U}(t) = \sum_{E,\alpha} e^{-iEt/\hbar}\,|E,\alpha\rangle\langle E,\alpha| = e^{-i\hat{H}t/\hbar}}
$$

**4)** Esse operador de evolução, atuando em qualquer $|\Psi(0)\rangle$, fornece $|\Psi(t)\rangle$. Seus elementos de matriz na base $|x\rangle$ (ou $|x,y,z\rangle$ se o problema é em 3D) formam o **PROPAGADOR**.

Observe que a forma do operador de evolução será sempre essa (quando $\hat{H}$ é independente do tempo). O que muda de problema para problema é o operador $\hat{H}$ e seus autovalores/autovetores.

## O Caso $\hat{H}(t)$

Nesses casos não adianta encontrar os autovetores/autovalores de $\hat{H}$, pois, como a cada instante temos um operador diferente, esses autovetores/autovalores mudam com o tempo.

Na maioria dos casos vamos recorrer a um método aproximado chamado **TEORIA DE PERTURBAÇÃO**, que permite tratar satisfatoriamente casos onde

$$
\hat{H}(t) = \hat{H}_0 + \hat{H}_1(t)
$$

e onde $\hat{H}_1(t)$ é "pequeno" em comparação ao pedaço constante $\hat{H}_0$ do Hamiltoniano total.

## Escolha de Base

A determinação dos autovetores e autovalores de $\hat{H}$ sempre envolve uma equação diferencial.

$$
\hat{H} = \frac{\hat{P}^2}{2m} + V(\hat{X}) \, ,
$$

a equação de autovalor $\hat{H}|E\rangle = E|E\rangle$, quando tomamos o produto interno com $\langle x|$, fica:

$$
\underbrace{-\frac{\hbar^2}{2m}\frac{d^2}{dx^2}\Psi_E(x)}_{\langle x|\frac{\hat{P}^2}{2m}|E\rangle} + \underbrace{V(x)\Psi_E(x)}_{\langle x|V(\hat{X})|E\rangle} = E\,\underbrace{\Psi_E(x)}_{\langle x|E\rangle}
$$

**Obs:** Lembre que $\hat{X}|x\rangle = x|x\rangle$ implica que $|x\rangle$ é autovetor de **QUALQUER FUNÇÃO** de $\hat{X}$:

$$
f(\hat{X})|x\rangle = f(x)|x\rangle
$$

Normalmente optamos por projetar a equação de Schrödinger **INDEPENDENTE DO TEMPO** (a de autovalor) na base $|x\rangle$, embora pudéssemos usar qualquer base. Por exemplo,

$$
\hat{H} = \frac{\hat{P}^2}{2m} - f\hat{X} \qquad \text{(força constante)}
$$

na base $|p\rangle$:

$$
\langle p|\frac{\hat{P}^2}{2m}|E\rangle + \langle p|{-f\hat{X}}|E\rangle = E\langle p|E\rangle
$$

$$
\frac{p^2}{2m}\Psi_E(p) - f\langle p|\hat{X}|E\rangle = E\,\Psi_E(p)
$$

onde usei $\langle p|\hat{P} = \langle p|p$. Mas o que é $\langle p|\hat{X}|E\rangle$?

$$
\begin{aligned}
\langle p|\hat{X}|E\rangle &= \int_{-\infty}^{\infty} dx \, \langle p|x\rangle\langle x|\hat{X}|E\rangle = \int_{-\infty}^{\infty} dx \, \frac{e^{-ipx/\hbar}}{\sqrt{2\pi\hbar}}\, x\,\Psi_E(x) \\
&= i\hbar \frac{d}{dp}\underbrace{\int_{-\infty}^{\infty} dx \, \frac{e^{-ipx/\hbar}}{\sqrt{2\pi\hbar}}\,\Psi_E(x)}_{\text{(truque)}} = i\hbar\frac{d}{dp}\underbrace{\int_{-\infty}^{\infty} dx \, \langle p|x\rangle\langle x|E\rangle}_{\Psi_E(p)}
\end{aligned}
$$

obtemos uma EDO de 1ª ordem para $\Psi_E(p) = \langle p|E\rangle$:

$$
\frac{p^2}{2m}\Psi_E(p) - i\hbar f\,\frac{d\Psi_E(p)}{dp} = E\,\Psi_E(p)
$$

Se tivesse projetado na base $\langle x|$:

$$
-\frac{\hbar^2}{2m}\frac{d^2\Psi_E(x)}{dx^2} - fx\,\Psi_E(x) = E\,\Psi_E(x)
$$

uma EDO de 2ª ordem para $\Psi_E(x) = \langle x|E\rangle$.

Normalmente iremos sempre resolver a equação de Schrödinger (independente do tempo) na base $|x\rangle$ (ou $|x,y,z\rangle$ se for um problema em 3D). O exemplo acima é um caso muito especial onde a base $|p\rangle$ é conveniente.

Funções de operadores, como $V(\hat{X})$ ou $e^{-\hat{P}^2}$, etc., são fáceis de tratar quando você lembra que $|x\rangle$ e $|p\rangle$ são autovetores de $\hat{X}$ e $\hat{P}$ e, consequentemente, de **QUALQUER FUNÇÃO** de $\hat{X}$ ou $\hat{P}$.

Por exemplo, o valor médio de uma série de medidas de $V(\hat{X})$ seria

$$
\begin{aligned}
\langle\Psi|V(\hat{X})|\Psi\rangle &= \int_{-\infty}^{\infty} \langle\Psi|x\rangle\langle x|V(\hat{X})|\Psi\rangle\,dx \\
&= \int_{-\infty}^{\infty} \Psi^*(x)\,V(x)\,\Psi(x)\,dx
\end{aligned}
$$

$$
\langle\Psi|e^{-\hat{P}^2}|\Psi\rangle = \int_{-\infty}^{\infty} \langle\Psi|p\rangle\langle p|e^{-\hat{P}^2}|\Psi\rangle\,dp = \int_{-\infty}^{\infty} \Psi^*(p)\,e^{-p^2}\,\Psi(p)\,dp
$$
