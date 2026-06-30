# (6ª aula) — Funções de Operadores e Espaços Vetoriais de Dimensão Infinita (seções 1.9, 1.10)

## Funções de Operadores

Vimos 2 objetos que podem atuar em vetores e transformá-los em outros vetores: números e operadores.

$$\alpha |V\rangle = |W\rangle \qquad \text{($\alpha$ é um número complexo)}$$

$$\hat{L}|V\rangle = |Z\rangle \qquad \text{($\hat{L}$ é um operador)}$$

A soma de vetores e o produto interno não "atuam" em vetores, eles "associam" um par de vetores produzindo um outro vetor, no primeiro caso, ou um número, no segundo caso.

$$\underbrace{|Z\rangle}_{\text{vetor}} = |V\rangle + |W\rangle \qquad\qquad \underbrace{\alpha}_{\text{número}} = \langle V|W\rangle$$

Queremos aqui definir uma **FUNÇÃO DE UM OPERADOR**:

$$f(\hat{L})|V\rangle = |W\rangle$$

Por exemplo, $f(x) = e^x$ ou $f(x) = \cos x$ resultariam em

$$e^{\hat{L}}|V\rangle \qquad \text{ou} \qquad \cos\hat{L}|V\rangle \, .$$

Como interpretar esses operadores? Pela representação em série das funções!

Se $f(x) = \displaystyle\sum_{n=0}^{\infty} a_n x^n$, então

$$f(\hat{L}) \equiv \sum_{n=0}^{\infty} a_n \hat{L}^n \, .$$

A introdução da série é necessária pois sabemos o significado do **PRODUTO DE OPERADORES**. Por exemplo,

$$\hat{L}^2 |V\rangle = \hat{L}\left[\hat{L}|V\rangle\right]$$

onde o termo entre colchetes é o vetor resultante da ação de $\hat{L}$ em $|V\rangle$.

No entanto, a representação em série de algumas funções é restrita a um domínio específico. Por exemplo,

$$e^x = \sum_{n=0}^{\infty} \frac{x^n}{n!} \qquad \text{para qualquer valor de } x \, ,$$

$$\frac{1}{1-x} = \sum_{n=0}^{\infty} x^n \qquad \text{apenas para } |x| < 1 \, .$$

No caso de funções de operadores **HERMITIANOS** (o único exemplo que encontraremos), a função do operador só pode ser identificada com a série se TODOS os autovalores de $\hat{L}$ estiverem dentro do domínio de validade da série.

Por que? Porque, em uma base de **AUTOVETORES** de $\hat{L}$ (base ortonormal, pois o operador é Hermitiano por hipótese),

$$\hat{L} \leftrightarrow
\begin{bmatrix}
    \omega_1 & & 0 \\
    & \omega_2 & \\
    0 & & \ddots \\
    & & & \omega_n
\end{bmatrix}$$

portanto (multiplique a matriz $m$ vezes)

$$\hat{L}^m \leftrightarrow
\begin{bmatrix}
    \omega_1^m & & 0 \\
    & \omega_2^m & \\
    0 & & \ddots \\
    & & & \omega_n^m
\end{bmatrix}$$

então

$$f(\hat{L}) \equiv \sum_{m=0}^{\infty} a_m \hat{L}^m \, , \quad \text{nessa base de autovetores de } \hat{L} \, ,$$

fica

$$f(\hat{L}) \leftrightarrow
\begin{bmatrix}
    \displaystyle\sum_m a_m \omega_1^m & & \\
    & \displaystyle\sum_m a_m \omega_2^m & \\
    & & \ddots \\
    & & & \displaystyle\sum_m a_m \omega_n^m
\end{bmatrix}$$

Se todos os autovalores estão dentro do domínio de validade da representação em série,

$$f(\hat{L}) \leftrightarrow
\begin{bmatrix}
    f(\omega_1) & & 0 \\
    & f(\omega_2) & \\
    0 & & \ddots \\
    & & & f(\omega_n)
\end{bmatrix}$$

e a identificação $f(\hat{L}) = \displaystyle\sum_m a_m \hat{L}^m$ pode ser feita.

Em particular,

$$\hat{L}|\omega_1\rangle = \omega_1 |\omega_1\rangle \qquad\qquad \underbrace{f(\hat{L})}_{\text{operador}} |\omega_1\rangle = \underbrace{f(\omega_1)}_{\text{número, autovalor}} |\omega_1\rangle$$

Na prática só encontraremos operadores do tipo $e^{\hat{L}}$, e a representação em série de $e^x$ é válida para qualquer valor de $x$.

## Derivadas de Operadores

Iremos encontrar operadores na forma $e^{\hat{L}t}$, onde $\hat{L}$ é um operador e $t$ é um parâmetro (um número). Você tem um operador diferente para cada valor do parâmetro $t$.

Podemos definir $\hat{U}(t) = e^{\hat{L}t}$ e tentar avaliar $\dfrac{d\hat{U}}{dt}$.

Da representação em série,

$$\frac{d}{dt} e^{\hat{L}t} = \frac{d}{dt}\left[\sum_{m=0}^{\infty} \frac{\hat{L}^m t^m}{m!}\right]$$

$$= \sum_{m=1}^{\infty} \frac{\hat{L}^m t^{m-1}}{(m-1)!}$$

$$= \hat{L}\left(\sum_{m=0}^{\infty} \frac{\hat{L}^m t^m}{m!}\right) = \hat{L}\, e^{\hat{L}t}$$

ou, isolando o $\hat{L}$ à direita,

$$\frac{d\hat{U}}{dt} = \hat{L}\, e^{\hat{L}t} = e^{\hat{L}t}\, \hat{L} \, .$$

Vemos que a derivada atua na função como se $\hat{L}$ fosse uma constante.

**Exemplo:**

$$\frac{d}{dt}\cos(\hat{L}t) = -\hat{L}\sin(\hat{L}t) = -\sin(\hat{L}t)\,\hat{L}$$

A ordem aqui não importa pois $\hat{L} f(\hat{L}) = f(\hat{L})\hat{L}$ (imagine a série de $f(\hat{L})$ e se convença).

**Exemplo:** Seja um sistema de 2 EDOs

$$\frac{d}{dt}
\begin{bmatrix}
    x_1(t) \\ x_2(t)
\end{bmatrix}
=
\begin{bmatrix}
    L_{11} & L_{12} \\
    L_{21} & L_{22}
\end{bmatrix}
\begin{bmatrix}
    x_1(t) \\ x_2(t)
\end{bmatrix}
\qquad \text{(4 números conhecidos)}$$

Podemos pensar nessa equação como a equação para as componentes de um vetor abstrato (como na aula passada) em uma base ortonormal $\{|1\rangle, |2\rangle\}$:

$$|x(t)\rangle = x_1(t)|1\rangle + x_2(t)|2\rangle$$

e $L_{11} = \langle 1|\hat{L}|1\rangle$, etc. Assim temos (abstratamente)

$$\frac{d}{dt}|x(t)\rangle = \hat{L}|x(t)\rangle \tag{$*$}$$

definimos o **OPERADOR DE EVOLUÇÃO**

$$|x(t)\rangle \equiv \hat{U}(t)\underbrace{|x(0)\rangle}_{\text{vetor inicial}}$$

onde o vetor à esquerda é o vetor em um tempo $t$ posterior.

Podemos obter uma **EQUAÇÃO DIFERENCIAL** para o operador $\hat{U}(t)$ levando isso na equação $(*)$:

$$\frac{d}{dt}\left[\hat{U}(t)|x(0)\rangle\right] = \hat{L}\left[\hat{U}(t)|x(0)\rangle\right]$$

como isso deve ser verdade para qualquer vetor inicial:

$$\frac{d\hat{U}}{dt} = \hat{L}\,\hat{U}(t) \, .$$

Como qualquer equação diferencial, isso é uma pergunta: "Que operador, que tem o tempo como parâmetro, quando diferenciado produz $\hat{L}\hat{U}(t)$?"

A **CONDIÇÃO INICIAL** para o operador é $\hat{U}(0) = \hat{I}$, isso vem da própria definição do operador de evolução: $|x(t)\rangle = \hat{U}(t)|x(0)\rangle$.

A resposta é

$$\boxed{\hat{U}(t) = e^{\hat{L}t}}$$

(verifique que $\hat{U}(t)$ satisfaz a equação diferencial e a condição inicial)

Formalmente escrevemos $|x(t)\rangle = e^{\hat{L}t}|x(0)\rangle$. Veremos exemplos como esse no decorrer do curso.

## Produto de Funções de Operadores Diferentes

Da representação em série de $f(\hat{L})$ e $g(\hat{\Lambda})$ você pode se convencer que $f(\hat{L})g(\hat{\Lambda}) = g(\hat{\Lambda})f(\hat{L})$ **APENAS SE** $\hat{L}$ e $\hat{\Lambda}$ **COMUTAM**. Em particular,

$$e^{\hat{\Lambda}} e^{\hat{L}} \neq e^{\hat{L}} e^{\hat{\Lambda}} \quad \text{com } [\hat{L}, \hat{\Lambda}] \neq 0$$

$$e^{\hat{\Lambda}} e^{\hat{L}} \neq e^{(\hat{\Lambda}+\hat{L})} \quad \text{com } [\hat{L}, \hat{\Lambda}] \neq 0$$

(compare as séries e se convença)

No entanto,

$$e^{\hat{\Lambda}} e^{\hat{L}} = e^{\hat{L}} e^{\hat{\Lambda}} = e^{(\hat{L}+\hat{\Lambda})} \quad \text{com } [\hat{L}, \hat{\Lambda}] = 0$$

(mostre isso!)

> **EM RESUMO**, $f(\hat{L})$ é um símbolo para a soma $\displaystyle\sum_{m=0}^{\infty} a_m \hat{L}^m$.

## Espaços Vetoriais de Dimensão Infinita

Na MQ o espaço vetorial dos estados físicos tem dimensão infinita.

Como exemplo desse tipo de espaço vetorial, considere o conjunto das funções da variável $x$ no intervalo $[a,b]$ tais que $f(a) = f(b) = 0$. Definimos a soma e a multiplicação por escalar (real):

$$g(x) = f(x) + h(x)$$

$$h(x) = \alpha f(x)$$

(verifique que o conjunto de funções proposto é fechado em relação a esta soma e esta multiplicação por escalar)

O que seria uma base nesse espaço vetorial?

Como definir um produto interno?

Uma função é uma lista dos valores de $f$ para um contínuo de valores de $x$. Uma representação aproximada seria uma lista dos valores de $f$ em um conjunto discreto de valores de $x$, por exemplo

$$x_i = a + \frac{i}{N+1}(b-a) \qquad (i = 1, 2, \dots, N)$$

Assim como identificamos $\begin{bmatrix} x_1 \\ x_2 \end{bmatrix}$ com as componentes de um vetor $|x\rangle$ em uma base $\{|1\rangle, |2\rangle\}$ de um espaço vetorial de dimensão 2, podemos identificar o conjunto de $N$ valores $[f(x_1), f(x_2), \dots, f(x_N)]$ com as componentes de um vetor abstrato $|f_N\rangle$, que representa a função, em uma base $\{|x_1\rangle, |x_2\rangle, \dots, |x_N\rangle\}$. O espaço vetorial teria dimensão $N$, portanto. Usaríamos:

$$|f_N\rangle = \sum_{i=1}^N \underbrace{f(x_i)}_{\text{componentes do vetor (números)}} \underbrace{|x_i\rangle}_{\text{base}}$$

$$\langle x_i|x_j\rangle = \delta_{ij} \qquad \text{(ortonormalidade da base)}$$

$$\sum_{i=1}^N |x_i\rangle\langle x_i| = \hat{I} \qquad \text{(operador identidade)}$$

Qualquer função no intervalo $[a,b]$ seria representada por um vetor abstrato nesse espaço vetorial de dimensão $N$ a partir do conhecimento dos $N$ valores $f(x_i)$.

Vamos supor que as funções são reais e o espaço vetorial é real (só podemos multiplicar funções por números reais).

Temos um espaço vetorial real de dimensão **FINITA** e igual a $N$. Ele não é em nada diferente dos exemplos que já vimos.

Por exemplo, o produto interno seria

$$\langle g_N|f_N\rangle = \sum_{i=1}^N g(x_i) f(x_i) \tag{$*$}$$

a soma de dois vetores poderia ser escrita como

$$|f_N\rangle + |g_N\rangle = \sum_{i=1}^N \left(f(x_i) + g(x_i)\right)|x_i\rangle$$

a norma seria:

$$\sqrt{\langle f_N|f_N\rangle} = \sqrt{\sum_{i=1}^N f(x_i)f(x_i)}$$

O problema aqui é que $N$ valores não especificam univocamente uma função. Poderíamos melhorar se fizéssemos $N \to \infty$.

Para que o produto interno $(*)$ seja um número finito, temos que redefini-lo, nesse limite, como

$$\langle f|g\rangle = \lim_{N \to \infty} \sum_{i=1}^N f(x_i) g(x_i)\, \Delta$$

$\Delta = \dfrac{(b-a)}{N+1}$ é o espaçamento $x_{i+1} - x_i$. Claramente isso é

$$\boxed{\langle f|g\rangle = \int_a^b f(x) g(x)\, dx}$$

No caso da MQ teremos funções **COMPLEXAS** de $x$ e o produto interno será definido como

$$\langle f|g\rangle = \int_a^b f^*(x) g(x)\, dx = \langle g|f\rangle^*$$

para o espaço vetorial complexo de funções complexas no intervalo $x \in [a,b]$, tais que $f(a) = f(b) = 0$.

Como fica a base anterior $|x_i\rangle$? Temos agora um **CONTÍNUO** de vetores base.

$$\{|x_1\rangle, \dots, |x_N\rangle\} \longrightarrow \{|x\rangle\, ; \, x \in [a,b]\}$$

$N$ vetores base &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; infinitos vetores base

A ortogonalidade dos vetores base é definida como:

$$\langle x_i|x_j\rangle = \delta_{ij} \longrightarrow \langle x|x'\rangle = \delta(x - x')$$

onde $\delta(x-x')$ é a função dita de Dirac. Ela é nula se $x \neq x'$ (ortogonalidade dos vetores da base), mas é infinita se $x = x'$ (isso implica que os vetores base $|x\rangle$ não têm norma unitária).

A identidade fica (como consequência dessa normalização da base)

$$\sum_{i=1}^N |x_i\rangle\langle x_i| = \hat{I} \longrightarrow \int_a^b |x\rangle\langle x|\, dx = \hat{I} \, .$$

## Propriedades de $\delta(x-x')$

A função $\delta(x-x')$ tem área unitária:

$$\int_{x-\varepsilon}^{x+\varepsilon} \delta(x-x')\, dx' = 1 \tag{$*$}$$

e é simétrica com relação ao seu argumento

$$\delta(x-x') = \delta(x'-x) \, .$$

Essa função aparece sempre dentro de uma integral e sua ação é

$$\int_a^b \delta(x-x') f(x')\, dx' = f(x)$$

Isso na verdade é uma consequência de $(*)$. Em geral, quando temos a integral de uma função muito concentrada vezes uma $f(x)$ suave, obtemos:

$$\int_a^b \delta(x-x') f(x')\, dx' \simeq f(x) \int_a^b \delta(x-x')\, dx' = f(x)$$

("$\simeq$" pois a área da função concentrada é unitária)

apenas para a função de Dirac o "$\simeq$" vira uma igualdade.

Sempre que encontrarmos uma base **CONTÍNUA** (como $|x\rangle$) vamos definir sua ortonormalidade com a função delta de Dirac. A expressão da identidade como uma integral de $|x\rangle\langle x|$ é consequência dessa normalização, pois

$$\underbrace{\langle x_1|x_2\rangle}_{\text{(por hipótese)}} = \delta(x_1 - x_2) = \underbrace{\int_a^b \delta(x_1-x)\,\delta(x_2-x)\, dx}_{\text{(propriedade da função delta)}}$$

$$= \underbrace{\int_a^b \langle x_1|x\rangle\langle x|x_2\rangle\, dx}_{\text{(por hipótese)}} = \langle x_1|\hat{I}|x_2\rangle$$

$$\Longrightarrow \hat{I} = \int_a^b dx\, |x\rangle\langle x|$$

(É possível também mostrar que $\hat{I} = \int dx\, |x\rangle\langle x|$ implica que a normalização da base tem que ser $\langle x|x'\rangle = \delta(x-x')$.)

Identificamos $f(x) = \langle x|f\rangle$ de modo que:

$$|f\rangle = \hat{I}|f\rangle = \int_a^b |x\rangle\langle x|f\rangle\, dx = \int_a^b \underbrace{|x\rangle}_{\text{base}} f(x)\, dx$$

> **RESUMO**
>
> $$\hat{I} = \int_a^b dx\, |x\rangle\langle x| \quad \longleftrightarrow \quad \hat{I} = \sum_{i=1}^N |x_i\rangle\langle x_i|$$
>
> $$\langle x|x'\rangle = \delta(x-x') \quad \longleftrightarrow \quad \langle x_i|x_j\rangle = \delta_{ij}$$
>
> $$|f\rangle = \int_a^b f(x)|x\rangle\, dx \quad \longleftrightarrow \quad |f\rangle = \sum_{i=1}^N f(x_i)|x_i\rangle$$
>
> $$f(x) = \langle x|f\rangle \quad \longleftrightarrow \quad f(x_i) = \langle x_i|f\rangle$$

**i)** A função

$$g(x-x') = \frac{1}{\sqrt{\pi \Delta^2}} \exp\left[-\frac{(x-x')^2}{\Delta^2}\right]$$

se chama **gaussiana**. Ela é um pico simétrico em torno do máximo em $x' = x$, $g(x-x') = g(x'-x)$. A largura do pico é proporcional a $\Delta$.

A sua área é unitária, **INDEPENDENTE DO VALOR DE $\Delta$**.

$$\int_{-\infty}^{\infty} g(x-x')\, dx' = 1$$

No limite $\Delta \to 0$ o pico se torna mais estreito e mais alto, e a função se torna uma representação da função delta (simétrica, infinitamente concentrada em $x' = x$, área unitária).

$$\boxed{\delta(x-x') = \lim_{\Delta \to 0} \frac{1}{\sqrt{\pi \Delta^2}} \exp\left[-\frac{(x-x')^2}{\Delta^2}\right]}$$

**ii)** A derivada da função delta pode ser definida

$$\frac{d}{dx}\delta(x-x') = -\frac{d}{dx'}\delta(x-x')$$

o seu efeito dentro de uma integral é obtido facilmente

$$\int_{-\infty}^{\infty} \left[\frac{d}{dx}\delta(x-x')\right] f(x')\, dx' = \frac{d}{dx}\underbrace{\int_{-\infty}^{\infty} \delta(x-x') f(x')\, dx'}_{\text{não é a variável de integração}} = \frac{d}{dx}f(x)$$

**Cuidado!** O símbolo $\delta'(x-x')$ significa $\dfrac{d}{dx}\delta(x-x')$ e não $\dfrac{d}{dx'}\delta(x-x')$, que é $-\delta'(x-x')$.

**iii)** Vimos $\delta(x-x')$ como o limite de uma função gaussiana, agora vamos obter $\delta(x-x')$ como uma integral.

A relação entre $f(x)$ e sua **TRANSFORMADA DE FOURIER** é

$$f(k) = \frac{1}{\sqrt{2\pi}} \int_{-\infty}^{\infty} e^{-ikx} f(x)\, dx \tag{1}$$

e

$$f(x) = \frac{1}{\sqrt{2\pi}} \int_{-\infty}^{\infty} e^{ikx} f(k)\, dk \tag{2}$$

Por exemplo, $f(x) = e^{-x^2}$ tem

$$f(k) = \frac{1}{\sqrt{2\pi}} \int_{-\infty}^{\infty} e^{-ikx}\, e^{-x^2}\, dx$$

$$= \frac{1}{\sqrt{2\pi}} \int_{-\infty}^{\infty} e^{-\left(x+\frac{ik}{2}\right)^2} e^{-k^2/4}\, dx$$

A integral $\displaystyle\int_{-\infty}^{\infty} e^{-(x-a)^2}\, dx = \sqrt{\pi}$, mesmo que $a$ seja complexo.

$$f(k) = \frac{1}{\sqrt{2}}\, e^{-k^2/4}$$

é a Transformada de Fourier de $e^{-x^2}$.

Observe que $f(k)$ **NÃO É** $f(x)$ com a troca $x \to k$! Por isso alguns autores usam um símbolo diferente, $\tilde{f}(k)$, para a transformada de Fourier.

Levando (1) em (2):

$$f(x) = \frac{1}{\sqrt{2\pi}} \int_{-\infty}^{\infty} dk\, e^{ikx} \underbrace{\left(\frac{1}{\sqrt{2\pi}} \int_{-\infty}^{\infty} e^{-ikx'} f(x')\, dx'\right)}_{f(k)}$$

$$= \int_{-\infty}^{\infty} \left(\frac{1}{2\pi}\int_{-\infty}^{\infty} dk\, e^{ik(x-x')}\right) f(x')\, dx'$$

portanto

$$\boxed{\delta(x-x') = \frac{1}{2\pi} \int_{-\infty}^{\infty} dk\, e^{ik(x-x')}}$$
