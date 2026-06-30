# (5ª aula) — Matrizes Hermitianas e Unitárias: Diagonalização Simultânea

## Matrizes Hermitianas e Unitárias (seção 1.8)

Vimos que os autovalores de operadores Hermitianos são REAIS e que autovalores de operadores Unitários são do tipo $e^{i\theta}$.

Vimos também que os autovetores de ambos operadores são mutuamente ortogonais (no caso de haver subespaços degenerados, você é livre para escolher, dentro do subespaço, um conjunto ortogonal).

Um operador $\hat{\Omega}$ (Hermitiano ou Unitário) em $\mathbb{V}^n(\mathbb{C})$ terá $n$ autovetores $\{|w_i\rangle\}$ que podem ser assumidos ortonormais

$$\langle w_i|w_j\rangle = \delta_{ij}$$

Esses autovetores podem ser usados como base ortonormal de $\mathbb{V}^n(\mathbb{C})$, em lugar da base ortonormal original $\{|i\rangle\}$.

O operador que transforma os $\{|i\rangle\}$ nos $\{|w_i\rangle\}$ é um operador unitário

$$|w_i\rangle = \hat{U}|i\rangle$$

> Note que
> $$\sum_{i=1}^n |i\rangle\langle i| = \hat{I} \qquad \text{e} \qquad \sum_{i=1}^n |w_i\rangle\langle w_i| = \hat{I}$$

os elementos de matriz de $\hat{U}$ na base original são

$$\langle j|\hat{U}|i\rangle = \langle j|w_i\rangle \quad \leftarrow \text{componentes dos autovetores}$$

$$\hat{U} \leftrightarrow
\begin{bmatrix}
\langle 1|w_1\rangle & \langle 1|w_2\rangle & \cdots & \langle 1|w_n\rangle \\
\langle 2|w_1\rangle & \langle 2|w_2\rangle & \cdots & \langle 2|w_n\rangle \\
\vdots & \vdots & \ddots & \vdots \\
\langle n|w_1\rangle & \langle n|w_2\rangle & \cdots & \langle n|w_n\rangle
\end{bmatrix}$$

(colunas: componentes de $|w_1\rangle$, componentes de $|w_2\rangle$, etc.)

Na base de autovetores ortonormais, o operador fica diagonal

$$\hat{\Omega} \leftrightarrow
\begin{bmatrix}
w_1 & & & 0 \\
& w_2 & & \\
& & \ddots & \\
0 & & & w_n
\end{bmatrix}$$

pois

$$\langle w_i|\hat{\Omega}|w_j\rangle = w_j \langle w_i|w_j\rangle = w_j \delta_{ij}$$

$$\langle w_i|\hat{\Omega}|w_j\rangle = \langle i|\hat{U}^\dagger \hat{\Omega} \hat{U}|j\rangle \quad \text{é uma matriz diagonal.}$$

$\langle i|\hat{\Omega}|j\rangle$ não é uma matriz diagonal.

**Obs:** Uma matriz genérica $n \times n$ não possui necessariamente $n$ autovetores como ocorre com MATRIZES HERMITIANAS E UNITÁRIAS. Veja o exemplo

$$\Omega = \begin{bmatrix} 4 & 1 \\ -1 & 2 \end{bmatrix}
\quad \Longrightarrow \quad
\Omega - \omega I = \begin{bmatrix} 4-\omega & 1 \\ -1 & 2-\omega \end{bmatrix}$$

Eq. característica: $(4-\omega)(2-\omega) + 1 = 0 \Rightarrow \omega = \{3, 3\}$

Autovetores: (substitua $\omega = 3$ em $\Omega - \omega I$)

$$\begin{bmatrix} 1 & 1 \\ -1 & -1 \end{bmatrix}
\begin{bmatrix} v_1 \\ v_2 \end{bmatrix}
=
\begin{bmatrix} 0 \\ 0 \end{bmatrix}
\quad \Longrightarrow \quad v_1 = -v_2$$

$$|w=3\rangle = (-v_2)|1\rangle + v_2|2\rangle = v_2 \left[ -|1\rangle + |2\rangle \right]$$

Só há um autovetor LI. Isso nunca aconteceria com matrizes Hermitianas ou Unitárias $2\times 2$, onde você encontraria 2 autovetores LI.

## Diagonalização Simultânea

Quando dois operadores COMUTAM, $\hat{\Omega}\hat{\Lambda} = \hat{\Lambda}\hat{\Omega}$, a ordem dos operadores não é importante.

Se os dois operadores são Hermitianos (o que vou mostrar se aplicaria também a operadores Unitários) E COMUTAM, é possível achar uma base ortonormal de autovetores *simultâneos* de ambos operadores.

Quando um dos operadores, $\hat{\Omega}$ por exemplo, é não degenerado, sua base de autovetores é bem definida e diagonaliza AMBOS operadores. Veja.

$$\langle w_i|\hat{\Omega}|w_j\rangle = w_j \langle w_i|w_j\rangle = w_j \delta_{ij}$$

A ação de $\hat{\Lambda}$ nos vetores $|w_j\rangle$:

$$\hat{\Omega}\left[\hat{\Lambda}|w_j\rangle\right] = \hat{\Lambda}\left[\hat{\Omega}|w_j\rangle\right] = w_j \left[\hat{\Lambda}|w_j\rangle\right]$$

(devido a $\hat{\Omega}\hat{\Lambda} = \hat{\Lambda}\hat{\Omega}$)

a conclusão é que $\hat{\Lambda}|w_j\rangle$ é um autovetor de $\hat{\Omega}$ com autovalor $w_j$; como esse autovalor é não degenerado por hipótese, $\hat{\Lambda}|w_j\rangle$ deve ser um múltiplo de $|w_j\rangle$:

$$\hat{\Lambda}|w_j\rangle = \lambda_j |w_j\rangle$$

($|w_j\rangle$ também é autovetor de $\hat{\Lambda}$)

portanto

$$\langle w_i|\hat{\Lambda}|w_j\rangle = \lambda_j \langle w_i|w_j\rangle = \lambda_j \delta_{ij} \quad \text{é diagonal}$$

$$\hat{\Omega} \leftrightarrow
\begin{bmatrix}
w_1 & & 0 \\
& w_2 & \\
0 & & \ddots \\
& & & w_n
\end{bmatrix}
\qquad
\hat{\Lambda} \leftrightarrow
\begin{bmatrix}
\lambda_1 & & 0 \\
& \lambda_2 & \\
0 & & \ddots \\
& & & \lambda_n
\end{bmatrix}$$

na base $|w_i\rangle$ do operador não degenerado.

**Obs:** Note que $\hat{\Lambda}$ pode ter autovalores degenerados (alguns dos $\lambda_i$ podem ser iguais), a hipótese foi que $\hat{\Omega}$ não tinha autovalores degenerados.

E se tanto $\hat{\Omega}$ quanto $\hat{\Lambda}$ têm autovalores degenerados?

Nesse caso a base de autovetores de $\hat{\Omega}$, por exemplo, não é única. Dentro dos subespaços degenerados temos liberdade de escolher vetores ortogonais. Imagine que uma escolha foi feita.

$$\hat{\Omega}|w_i, \alpha\rangle = w_i |w_i, \alpha\rangle \qquad (\alpha = 1, 2, \dots, m_i)$$

esses são os $m_i$ autovetores ortonormais associados ao autovalor degenerado $w_i$.

Nessa base, $\hat{\Omega}$ é diagonal. E quanto a $\hat{\Lambda}$?

$$\hat{\Omega}\left[\hat{\Lambda}|w_i, \alpha\rangle\right] = \hat{\Lambda}\left[\hat{\Omega}|w_i, \alpha\rangle\right] = w_i \left[\hat{\Lambda}|w_i, \alpha\rangle\right]$$

(pois $\hat{\Omega}\hat{\Lambda} = \hat{\Lambda}\hat{\Omega}$)

Vemos que $\hat{\Lambda}|w_i,\alpha\rangle$ ainda pertence ao subespaço degenerado associado ao autovalor $w_i$. Por isso podemos concluir apenas que $\hat{\Lambda}$ não tem elemento de matriz entre vetores de subespaços degenerados distintos.

$$\langle w_j, \beta| \hat{\Lambda} |w_i, \alpha\rangle = 0 \qquad (w_i \neq w_j)$$

A matriz associada a $\hat{\Lambda}$ na base escolhida fica DIAGONAL POR BLOCOS

$$\hat{\Lambda} \leftrightarrow
\begin{bmatrix}
\Lambda_1 & & & 0 \\
& \Lambda_2 & & \\
0 & & \ddots & \\
& & & \Lambda_n
\end{bmatrix}$$

Temos tantos blocos quanto autovalores $w_i$ DISTINTOS.

A dimensão das matrizes é igual à dimensão do subespaço associado ao autovalor $w_i$; em particular, se o autovalor é não degenerado, a matriz é um número apenas.

Os blocos são matrizes Hermitianas e podemos reconstruir os vetores $|w_i, \alpha\rangle$, definindo um novo conjunto de vetores ortogonais, para tornar os blocos diagonais.

Dentro de cada subespaço degenerado de $\hat{\Omega}$ mudamos de base ortonormal

$$|w_i, \alpha\rangle \to |w_i, a\rangle \qquad (\alpha = 1, \dots, m_i) \quad (a = 1, \dots, m_i)$$

$\hat{\Omega}$ continua diagonal e $\hat{\Lambda}$ se torna diagonal (por hipótese)

$$\hat{\Lambda}|w_i, a\rangle = \lambda_i^{(a)} |w_i, a\rangle \qquad (a = 1, \dots, m_i)$$

Se os autovalores de $\hat{\Lambda}$ nos subespaços $w_i$ são todos diferentes, podemos caracterizar a base informando os autovalores $w$ e $\lambda$. Mudamos o nome de $|w_i, a\rangle$ para $|w_i, \lambda_i^a\rangle$. Dizemos que $\hat{\Omega}$ e $\hat{\Lambda}$ constituem um **CONJUNTO COMPLETO DE OPERADORES QUE COMUTAM**.

Caso alguns dos $\lambda_i^a$ sejam iguais, a informação dos autovalores não especifica unicamente um estado.

## Exemplo

Em uma base $|1\rangle, |2\rangle, |3\rangle$ ortonormal temos duas matrizes Hermitianas.

$$\Omega = \begin{bmatrix} 2 & 0 & 0 \\ 0 & 2 & 0 \\ 0 & 0 & 1 \end{bmatrix}
\qquad
\Lambda = \begin{bmatrix} -1 & 1 & 0 \\ 1 & -1 & 0 \\ 0 & 0 & 3 \end{bmatrix}$$

Verifique que $\Omega\Lambda = \Lambda\Omega$. Veja que a base já diagonaliza $\Omega$ e deixa $\Lambda$ na forma em bloco.

Encontre autovetores de $\Lambda$ no subespaço $\{|1\rangle, |2\rangle\}$ associado ao autovalor $w=2$.

$$\det \begin{bmatrix} -1-\lambda & 1 \\ 1 & -1-\lambda \end{bmatrix} = 0
\quad \Longrightarrow \quad
(1+\lambda)^2 - 1 = 0
\quad \Longrightarrow \quad
\lambda = \{0, -2\}$$

$(\lambda = 0)$

$$\begin{bmatrix} -1 & 1 \\ 1 & -1 \end{bmatrix}
\begin{bmatrix} v_1 \\ v_2 \end{bmatrix}
=
\begin{bmatrix} 0 \\ 0 \end{bmatrix}
\quad \Longrightarrow \quad
|\lambda=0, w=2\rangle = \frac{1}{\sqrt{2}}|1\rangle + \frac{1}{\sqrt{2}}|2\rangle$$

$(\lambda = -2)$

$$\begin{bmatrix} 1 & 1 \\ 1 & 1 \end{bmatrix}
\begin{bmatrix} v_1 \\ v_2 \end{bmatrix}
=
\begin{bmatrix} 0 \\ 0 \end{bmatrix}
\quad \Longrightarrow \quad
|\lambda=-2, w=2\rangle = \frac{1}{\sqrt{2}}|1\rangle - \frac{1}{\sqrt{2}}|2\rangle$$

Finalmente, $|\lambda=3, w=1\rangle = |3\rangle$. Nessa base $|\lambda, w\rangle$ ortonormal temos:

$$\Omega \leftrightarrow \begin{bmatrix} 2 & 0 & 0 \\ 0 & 2 & 0 \\ 0 & 0 & 1 \end{bmatrix}
\qquad
\Lambda \leftrightarrow \begin{bmatrix} 0 & 0 & 0 \\ 0 & -2 & 0 \\ 0 & 0 & 3 \end{bmatrix}$$

> **Lembre:** Quando dois operadores comutam, a ação de um deles em um vetor dentro de um subespaço degenerado do outro resulta em um vetor dentro do mesmo subespaço.
> $$\hat{\Omega}\left[\hat{\Lambda}|w_i, \alpha\rangle\right] = \hat{\Lambda}\left[\hat{\Omega}|w_i, \alpha\rangle\right] = w_i \left[\hat{\Lambda}|w_i, \alpha\rangle\right]$$
> $$\Longrightarrow \quad \hat{\Lambda}|w_i, \alpha\rangle \text{ permanece no subespaço do autovalor } w_i$$

## Exemplo 1.8.6

Esse exemplo ilustra a maneira como vetores, operadores, autovalores, etc. aparecem em Mecânica Quântica. O exemplo vem extraído da Mecânica Clássica.

*(duas massas $m$ ligadas por três molas de constante $k$ entre paredes fixas, com deslocamentos $x_1$ e $x_2$ em relação às posições de equilíbrio)*

Vamos estudar as oscilações lineares dessas duas massas. $x_1(t)$ e $x_2(t)$ são o que queremos determinar. Essas funções medem a distância das massas aos pontos de equilíbrio.

A equação que determina $x_1(t)$ e $x_2(t)$

$$\begin{cases}
m\ddot{x}_1 = -2kx_1 + kx_2 \\
m\ddot{x}_2 = kx_1 - 2kx_2
\end{cases}$$

Em forma matricial

$$\frac{d^2}{dt^2} \begin{bmatrix} x_1 \\ x_2 \end{bmatrix}
=
\begin{bmatrix} -2k/m & k/m \\ k/m & -2k/m \end{bmatrix}
\begin{bmatrix} x_1 \\ x_2 \end{bmatrix}$$

Assim como

$$\begin{bmatrix} v_1' \\ \vdots \\ v_n' \end{bmatrix}
=
\begin{bmatrix} \Omega_{11} & \Omega_{12} & \cdots & \Omega_{1n} \\ \vdots & & & \vdots \\ \Omega_{n1} & \cdots & & \Omega_{nn} \end{bmatrix}
\begin{bmatrix} v_1 \\ \vdots \\ v_n \end{bmatrix}$$

é a versão matricial de $|V'\rangle = \hat{\Omega}|V\rangle$, na base $\{|i\rangle\}$, podemos dizer que a equação diferencial é a versão matricial da equação abstrata

$$\frac{d^2}{dt^2}|x(t)\rangle = \hat{\Omega}|x(t)\rangle$$

na base ortonormal $|1\rangle, |2\rangle$. Por exemplo, $x_1(t) = \langle 1|x(t)\rangle$, $\Omega_{11} = -\dfrac{2k}{m} = \langle 1|\hat{\Omega}|1\rangle$, etc.

Como $\hat{\Omega}$ é Hermitiano, vamos tentar usar seus autovetores como base para simplificar o problema.

$$\det \begin{bmatrix} -2k/m - \omega & k/m \\ k/m & -2k/m - \omega \end{bmatrix} = 0
\quad \Longrightarrow \quad
\omega = \left\{ -\frac{3k}{m}, -\frac{k}{m} \right\}$$

$\omega = -\dfrac{k}{m}$ tem autovetor $|I\rangle = \dfrac{1}{\sqrt{2}}|1\rangle + \dfrac{1}{\sqrt{2}}|2\rangle$

$\omega = -\dfrac{3k}{m}$ tem autovetor $|II\rangle = \dfrac{1}{\sqrt{2}}|1\rangle - \dfrac{1}{\sqrt{2}}|2\rangle$

na base $|I\rangle, |II\rangle$ (ortonormal) a equação abstrata fica

$$\frac{d^2}{dt^2} \begin{bmatrix} x_I \\ x_{II} \end{bmatrix}
=
\begin{bmatrix} -k/m & 0 \\ 0 & -3k/m \end{bmatrix}
\begin{bmatrix} x_I \\ x_{II} \end{bmatrix}$$

ou

$$\begin{cases}
\ddot{x}_I = -\dfrac{k}{m} x_I \\[4pt]
\ddot{x}_{II} = -\dfrac{3k}{m} x_{II}
\end{cases}
\quad \Longrightarrow \quad
\begin{cases}
x_I(t) = x_I(0) \cos\left( \sqrt{\dfrac{k}{m}}\, t \right) \\[4pt]
x_{II}(t) = x_{II}(0) \cos\left( \sqrt{\dfrac{3k}{m}}\, t \right)
\end{cases}$$

onde usei que as massas estavam paradas em $t=0$ (senão teria que incluir $\dot{x}_I(0)\sqrt{\dfrac{m}{k}}\sin\left(\sqrt{\dfrac{k}{m}}t\right)$ etc.)

> **A solução do problema usando a base de autovetores de $\hat{\Omega}$ é muito mais simples!**

Escrevo a solução na forma matricial

$$\begin{bmatrix} x_I(t) \\ x_{II}(t) \end{bmatrix}
=
\begin{bmatrix} \cos\sqrt{\dfrac{k}{m}}\, t & 0 \\[6pt] 0 & \cos\sqrt{\dfrac{3k}{m}}\, t \end{bmatrix}
\begin{bmatrix} x_I(0) \\ x_{II}(0) \end{bmatrix}$$

essa matriz que fornece valores futuros de $x_I$ e $x_{II}$ a partir dos valores iniciais se chama **PROPAGADOR**.

Assim como fizemos antes, podemos ver essa equação matricial como a versão em componentes na base $|I\rangle, |II\rangle$ da equação abstrata

$$|x(t)\rangle = \hat{U}(t) |x(0)\rangle$$

onde $\hat{U}(t)$ se chama **OPERADOR DE EVOLUÇÃO**.

Como obter os $x_1(t)$ e $x_2(t)$ originais? Perceba que a versão "em borboletas" (notação de projetores) do operador $\hat{U}(t)$ é

$$\hat{U}(t) = \cos\left(\sqrt{\frac{k}{m}}\, t\right) |I\rangle\langle I| + \cos\left(\sqrt{\frac{3k}{m}}\, t\right) |II\rangle\langle II|$$

Podemos obter a matriz desse operador na base $|1\rangle, |2\rangle$ usando os produtos internos conhecidos.

$$\langle 1|I\rangle = \frac{1}{\sqrt{2}} \qquad \langle 1|II\rangle = \frac{1}{\sqrt{2}} \qquad \langle 2|I\rangle = \frac{1}{\sqrt{2}} \qquad \langle 2|II\rangle = -\frac{1}{\sqrt{2}}$$

$$\langle 1|\hat{U}(t)|1\rangle = \frac{1}{2}\cos(\omega_I t) + \frac{1}{2}\cos(\omega_{II} t)$$
$$\langle 1|\hat{U}(t)|2\rangle = \frac{1}{2}\cos(\omega_I t) - \frac{1}{2}\cos(\omega_{II} t) \qquad \text{onde } \omega_I = \sqrt{\frac{k}{m}}$$
$$\langle 2|\hat{U}(t)|1\rangle = \frac{1}{2}\cos(\omega_I t) - \frac{1}{2}\cos(\omega_{II} t) \qquad \text{e } \omega_{II} = \sqrt{\frac{3k}{m}}$$
$$\langle 2|\hat{U}(t)|2\rangle = \frac{1}{2}\cos(\omega_I t) + \frac{1}{2}\cos(\omega_{II} t)$$

Na base $|1\rangle, |2\rangle$, a equação $|x(t)\rangle = \hat{U}(t)|x(0)\rangle$ fica

$$\begin{bmatrix} x_1(t) \\ x_2(t) \end{bmatrix}
=
\begin{bmatrix}
\dfrac{\cos\omega_I t + \cos\omega_{II} t}{2} & \dfrac{\cos\omega_I t - \cos\omega_{II} t}{2} \\[8pt]
\dfrac{\cos\omega_I t - \cos\omega_{II} t}{2} & \dfrac{\cos\omega_I t + \cos\omega_{II} t}{2}
\end{bmatrix}
\begin{bmatrix} x_1(0) \\ x_2(0) \end{bmatrix}$$

> **O operador de evolução abstrato tem uma forma simples na base de autovetores de $\hat{\Omega}$ e podemos encontrar sua matriz em qualquer base posteriormente.**

## Conexão com a Mecânica Quântica

A Equação de evolução dos estados quânticos é muito parecida com essa equação que vimos no exemplo. Sua versão abstrata é

$$i\hbar \frac{d}{dt} |\Psi(t)\rangle = \hat{H} |\Psi(t)\rangle$$

onde $\hbar = \dfrac{h}{2\pi}$, $|\Psi(t)\rangle$ é o estado da partícula microscópica (que desejamos conhecer), $\hat{H}$ é o operador Hamiltoniano (relacionado à função Hamiltoniana da Mecânica Clássica).

Note que é uma equação de 1ª ordem, de modo que precisaremos fornecer apenas o estado $|\Psi(0)\rangle$ inicial.

Os autovetores do operador $\hat{H}$ serão cruciais para escrever o operador de evolução como acima. Esse operador evolui o estado inicial

$$|\Psi(t)\rangle = \hat{U}(t) |\Psi(0)\rangle$$

e é a chave do problema.
