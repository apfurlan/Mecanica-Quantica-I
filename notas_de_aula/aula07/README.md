# 7ª aula — Operadores em Dimensão Infinita: Momento, Posição e a Equação de Onda

## Operadores em dimensão infinita

Vimos então que, no espaço vetorial de funções complexas definidas no intervalo $x \in [a,b]$, temos

$$
\{|x\rangle, \; x \in [a,b]\} \quad \text{vetores base}
$$
$$
\langle x|x'\rangle = \delta(x-x') \quad \text{ortonormalidade da base}
$$
$$
\hat{I} = \int_a^b dx \,|x\rangle\langle x| \quad \text{identidade}
$$
$$
|f\rangle = \int_a^b dx \,|x\rangle\langle x|f\rangle = \int_a^b dx \,|x\rangle f(x)
$$
$$
\langle g|f\rangle = \int_a^b dx \, g^*(x) f(x) \qquad \text{($g^*(x)f(x)$ é a componente do vetor $|f\rangle$ na base)}
$$

Vamos ver como são os operadores nesse EV de dimensão infinita.

$$
\hat{\Omega}|f\rangle = |\tilde{f}\rangle
$$

$\hat{\Omega}$ transforma a função $f(x)$ em $\tilde{f}(x)$. Um exemplo de operador seria

$$
\hat{D}|f\rangle = |df/dx\rangle
$$

onde $|f\rangle$ é o ket associado a $f(x)$ e $|df/dx\rangle$ é o ket associado a $df/dx$.

Quais são os elementos de matriz do operador $\hat{D}$ na base $|x\rangle$?

$$
\langle x|\hat{D}f\rangle \equiv \langle x|\hat{D}|f\rangle = \langle x|df/dx\rangle = \frac{df}{dx}
$$

Introduzindo a identidade $\hat{I} = \int_a^b dx' |x'\rangle\langle x'|$ entre $\hat{D}$ e $|f\rangle$:

$$
\langle x|\hat{D}|f\rangle = \int_a^b dx' \langle x|\hat{D}|x'\rangle\langle x'|f\rangle = \frac{df}{dx}
$$

então

$$
\int_a^b dx' \langle x|\hat{D}|x'\rangle f(x') = \frac{df}{dx}
$$

claramente,

$$
\boxed{\langle x|\hat{D}|x'\rangle = \delta'(x-x') = \frac{d}{dx}\delta(x-x')}
$$

Na prática usaremos poucas vezes esses elementos de matriz. Ao invés disso usaremos com frequência

$$
\boxed{\langle x|\hat{D}|f\rangle = \frac{df}{dx}}
$$

## Hermiticidade de operadores em dimensão infinita

No caso de EV de dimensão FINITA, a maneira simples de determinar se um operador $\hat{\Omega}$ é hermitiano é montar sua matriz em uma base ortonormal e observar se essa matriz é Hermitiana (isto é, se ela é igual à sua transposta conjugada).

Em um EV de dimensão INFINITA se usa um teste alternativo. Vamos aplicar esse teste ao operador derivado de $\hat{D}$, $\hat{K} = -i\hat{D}$.

Se $\hat{K}$ é Hermitiano então, para quaisquer $|f\rangle$ e $|g\rangle$ do EV devemos ter

$$
\langle f|\hat{K}|g\rangle = \langle g|\hat{K}^\dagger|f\rangle^* = \langle g|\hat{K}|f\rangle^* \qquad (\text{pois } \hat{K}^\dagger = \hat{K})
$$

Então, se $\hat{K}$ é Hermitiano, $\langle f|\hat{K}|g\rangle = \langle g|\hat{K}|f\rangle^*$.

$$
\langle f|\hat{K}|g\rangle = \int_a^b \langle f|x\rangle\langle x|(-i\hat{D})|g\rangle\,dx \qquad \text{(coloquei $\hat{I}$ aqui)}
$$
$$
= \int_a^b f^*(x)\left(-i\frac{dg}{dx}\right)dx
$$

Por outro lado,

$$
\langle g|\hat{K}|f\rangle^* = \left[\int_a^b g^*(x)\left(-i\frac{df}{dx}\right)dx\right]^*
$$
$$
= \int_a^b g(x)\, i\,\frac{df^*}{dx}\,dx
$$

Integrando por partes:

$$
\langle g|\hat{K}|f\rangle^* = i\, g(x) f^*(x)\Big|_a^b - i\int_a^b f^*(x)\frac{dg}{dx}\,dx
$$

A equação de $\langle f|\hat{K}|g\rangle$ acima só é igual à expressão obtida por integração por partes se o termo de superfície se anular PARA QUALQUER $f(x)$ e $g(x)$ do EV.

Isso acontece se o EV incluir apenas funções complexas PERIÓDICAS no intervalo $[a,b]$. O caso onde $f(a)=f(b)=0$ sendo um caso especial.

$$
\boxed{\hat{K} = -i\hat{D} \text{ é Hermitiano no EV de funções complexas em } [a,b] \text{ que são periódicas: } f(a)=f(b)}
$$

## Funções físicas e funções impróprias

O EV de funções complexas em $(-\infty,\infty)$ da MQ inclui dois tipos de funções (iremos usar adiante $\hat{I} = \int |x\rangle\langle x|\,dx$):

- **(i)** Funções FÍSICAS, normalizáveis:

$$
\langle f|f\rangle = \int_{-\infty}^{\infty} f^*(x) f(x)\,dx < \infty.
$$

  Isso exige que $f(\infty) = f(-\infty) = 0$. Essas são as funções que descrevem ESTADOS FÍSICOS (possíveis de serem criados) de uma partícula.

- **(ii)** Funções IMPRÓPRIAS, ou não-normalizáveis, tais que $|f(\infty)|, |f(-\infty)| < \infty$ (as funções não podem DIVERGIR no infinito).

Por exemplo:

$$
f(x) = \delta(x-a) \qquad \text{ou} \qquad f(x) = e^{ikx}
$$
$$
\int_{-\infty}^{\infty} \delta(x-a)\,\delta(x-a)\,dx = \delta(0) = \infty
$$
$$
\int_{-\infty}^{\infty} e^{-ikx}e^{ikx}\,dx = \int_{-\infty}^{\infty} dx = \infty
$$

Essas funções são não-físicas, não há como produzir uma partícula em um estado como esses; no entanto elas aparecem como autofunções de certos operadores (ver adiante) e são úteis em cálculos.

A análise anterior sobre a hermiticidade do operador $\hat{K} = -i\hat{D}$ mostra que ele é Hermitiano no EV das funções físicas, pois essas se anulam em $x=\infty$ e $x=-\infty$.

A "prova" de que o operador ainda é Hermitiano com a inclusão das funções impróprias do tipo (ii) é feita na pág. 66 do livro.

Veja por que temos que incluir funções IMPRÓPRIAS no EV das funções físicas: vamos calcular os **autovetores e autovalores do operador $\hat{K}$**.

## Autovetores e autovalores do operador $\hat{K}$

$$
\hat{K}|k\rangle = k|k\rangle
$$

Usando $\langle x|\hat{K}|f\rangle = -i\dfrac{df}{dx}$ e $\langle x|f\rangle = f(x)$, obtemos

$$
-i\frac{d}{dx}\psi_k(x) = k\,\psi_k(x), \qquad \text{onde } \psi_k(x) = \langle x|k\rangle
$$

Veja como a equação de autovalor se transforma em uma EDO. Em EV de dimensão infinita não usamos aquela rotina de encontrar a equação característica por meio de $\det[\hat{\Omega} - \omega \hat{I}] = 0$, pois não há como escrever a matriz dos operadores.

A solução da EDO é

$$
\psi_k(x) = A\, e^{ikx}
$$

- Essa é uma função IMPRÓPRIA do tipo (ii) DESDE QUE o autovalor $k$ seja real.
- Se $k$ tivesse parte imaginária, a autofunção $\psi_k(x)$ não pertenceria ao EV (não seria do tipo (i) nem do tipo (ii), pois divergiria no infinito).
- A constante $A$ reflete o fato de que autovetores envolvem sempre uma constante arbitrária. Usamos $A = 1/\sqrt{2\pi}$ de modo que

$$
\langle x|k\rangle = \psi_k(x) = \frac{1}{\sqrt{2\pi}}\,e^{ikx}
$$

- Com essa escolha, os vetores $|k\rangle$, com $k \in (-\infty,\infty)$, satisfazem

$$
\langle k|k'\rangle = \int_{-\infty}^{\infty}\langle k|x\rangle\langle x|k'\rangle\,dx = \int_{-\infty}^{\infty}\frac{1}{2\pi}e^{-ikx}e^{ik'x}\,dx = \delta(k-k')
$$

  (lembre a representação integral da função delta).

Essa ortonormalização dos vetores $|k\rangle$ permite escrever a identidade como

$$
\hat{I} = \int_{-\infty}^{\infty} dk\,|k\rangle\langle k| \qquad \text{(ortonormais no sentido da função delta)}
$$

Temos agora duas bases para o EV das funções complexas em $(-\infty,\infty)$:

$$
|f\rangle = \int_{-\infty}^{\infty} dx\,|x\rangle\langle x|f\rangle = \int_{-\infty}^{\infty} dx\,|x\rangle\,f(x)
$$
$$
|f\rangle = \int_{-\infty}^{\infty} dk\,|k\rangle\langle k|f\rangle = \int_{-\infty}^{\infty} dk\,|k\rangle\,f(k)
$$

Qual a relação entre $f(k)$ e $f(x)$?

$$
f(k) = \langle k|f\rangle = \int_{-\infty}^{\infty} dx\,\langle k|x\rangle\langle x|f\rangle
$$
$$
= \int_{-\infty}^{\infty} dx\,\frac{1}{\sqrt{2\pi}}\,e^{-ikx}\,f(x)
$$

$\Rightarrow$ $f(k)$ é a **transformada de Fourier** de $f(x)$!

> **Observação:** A Eq. (1.10.35) [do livro-texto] está errada. A expressão correta é
>
> $$
> \langle x|f\rangle = \int_{-\infty}^{\infty} dk\,\langle x|k\rangle\langle k|f\rangle \qquad \text{(CORRIJA)}
> $$

O operador $\hat{K}$, na base de seus autovetores, fica

$$
\langle k|\hat{K}|k'\rangle = k'\langle k|k'\rangle = k'\,\delta(k-k')
$$

## O operador $\hat{X}$

Vamos inventar um operador que tem como autovetores os vetores $|x\rangle$:

$$
\hat{X}|x\rangle = x|x\rangle, \qquad x \in (-\infty,\infty)
$$

A ortonormalização dos autovetores é $\langle x|x'\rangle = \delta(x-x')$ (inteiramente análogo a $\langle k|k'\rangle = \delta(k-k')$ dos autovetores do operador $\hat{K}$).

A ação de $\hat{X}$ em um vetor qualquer:

$$
\hat{X}|f\rangle = |\tilde{f}\rangle
$$
$$
\Rightarrow \int_{-\infty}^{\infty} \langle x|\hat{X}|x'\rangle\langle x'|f\rangle\,dx' = \langle x|\tilde{f}\rangle
$$
$$
\int_{-\infty}^{\infty} x'\,\delta(x-x')\,f(x')\,dx' = \tilde{f}(x)
$$
$$
x\,f(x) = \tilde{f}(x)
$$

portanto

$$
\boxed{\langle x|\hat{X}|f\rangle = x\,f(x)} \qquad \left(\text{compare com } \langle x|\hat{K}|f\rangle = -i\frac{df}{dx}\right)
$$

## Hermiticidade de $\hat{X}$ e o comutador $[\hat{X},\hat{K}]$

O operador $\hat{X}$ é Hermitiano pois, para quaisquer $|f\rangle$ e $|g\rangle$,

$$
\langle f|\hat{X}|g\rangle = \int_{-\infty}^{\infty} \langle f|x\rangle\langle x|\hat{X}|g\rangle\,dx
$$
$$
= \int_{-\infty}^{\infty} f^*(x)\,x\,g(x)\,dx
$$
$$
\langle g|\hat{X}|f\rangle^* = \left[\int_{-\infty}^{\infty}\langle g|x\rangle\langle x|\hat{X}|f\rangle\,dx\right]^*
$$
$$
= \left[\int_{-\infty}^{\infty} g^*(x)\,x\,f(x)\,dx\right]^*
$$
$$
= \int_{-\infty}^{\infty} g(x)\,x\,f^*(x)\,dx
$$

(aqui não temos os termos de superfície para atrapalhar).

### O comutador $[\hat{X},\hat{K}]$

Vimos que $\langle x|\hat{X}|f\rangle = x f(x)$ e $\langle x|\hat{K}|f\rangle = -i\dfrac{df}{dx}$.

Então

$$
\langle x|\hat{X}\hat{K}|f\rangle = x\underbrace{\left(-i\frac{df}{dx}\right)}_{\text{ket associado à função } -i\,df/dx}
$$
$$
\langle x|\hat{K}\hat{X}|f\rangle = \underbrace{-i\frac{d}{dx}\big(x f(x)\big)}_{\text{ket associado à função } x f(x)} = -i f(x) - i\,x\,\frac{df}{dx}
$$

Portanto

$$
\langle x|\hat{X}\hat{K} - \hat{K}\hat{X}|f\rangle = \langle x|\hat{X}\hat{K}|f\rangle - \langle x|\hat{K}\hat{X}|f\rangle
$$
$$
= i\,f(x)
$$
$$
= i\langle x|f\rangle = \langle x|i\hat{I}|f\rangle
$$

Como $\langle x|$ e $|f\rangle$ podem ser quaisquer, temos a igualdade de OPERADORES

$$
\boxed{[\hat{X},\hat{K}] = i\hat{I}}
$$

Esses dois operadores Hermitianos, no EV de dimensão infinita associado às funções complexas dos tipos

- **(i)** $\displaystyle\int_{-\infty}^{\infty}|f(x)|^2\,dx < \infty$ (normalizáveis)
- **(ii)** não-normalizáveis (porém não-divergentes no infinito)

são os operadores básicos da MQ.

## Exemplo 1.10.1 — Aplicação à equação de onda

Mostramos no exemplo 1.8.6 como formular o problema de 2 EDOs acopladas usando um EV de dimensão 2. Veremos agora como formular o problema de uma EDP (Equação Diferencial Parcial) usando um EV de dimensão infinita.

$$
\frac{\partial^2 \Psi}{\partial t^2} = \frac{\partial^2 \Psi}{\partial x^2}
$$

é a equação de onda que governa a evolução temporal de uma deformação em uma corda. $\Psi(x,t)$ é o deslocamento vertical do ponto $x$ da corda no instante $t$.

*(Figura: corda de comprimento $L$ com deslocamento $\Psi(x,t)$ no ponto $x$.)*

Compare com o sistema de EDOs

$$
\begin{bmatrix} \ddot{x}_1 \\ \ddot{x}_2 \end{bmatrix}
= \hat{\Omega} \begin{bmatrix} x_1 \\ x_2 \end{bmatrix}
$$

É como se a Eq. de onda fosse um sistema de infinitas EDOs, uma para cada ponto $x$ da corda.

Pensaremos em $\Psi(x,t)$ como $\langle x|\Psi(t)\rangle$, assim como usamos $x_1(t) = \langle 1|X(t)\rangle$ e $x_2(t) = \langle 2|X(t)\rangle$.

$$
\frac{\partial^2 \Psi}{\partial x^2} = -\langle x|\hat{K}\hat{K}|\Psi(t)\rangle
$$

Portanto a Eq. de onda é a equação abstrata

$$
\boxed{\frac{d^2}{dt^2}|\Psi(t)\rangle = -\hat{K}^2|\Psi(t)\rangle}
$$

projetada nos bras $\langle x|$. Compare com

$$
\frac{d^2}{dt^2}|X(t)\rangle = \hat{\Omega}|X(t)\rangle
$$

do outro exemplo.

### Autovetores e autovalores de $-\hat{K}^2$

(Observe que o tipo de função do EV determina ao mesmo tempo os autovetores e os autovalores, através da condição $\Psi(0)=\Psi(L)=0$.)

Determinamos os autovetores e autovalores de $-\hat{K}^2$:

$$
\hat{K}^2|\Psi\rangle = k^2|\Psi\rangle \qquad \hookrightarrow \text{os autovalores serão positivos}
$$

(se tentasse autovalores negativos, você veria que $\psi_k(x) = A e^{\kappa x} + B e^{-\kappa x}$ não pertenceria ao EV)

Projetando com $\langle x|$:

$$
-\frac{d^2}{dx^2}\psi_k(x) = k^2\,\psi_k(x)
$$

cuja solução é

$$
\psi_k(x) = A\cos(kx) + B\sin(kx)
$$

Como nosso EV só contempla funções tais que $\Psi(0) = \Psi(L) = 0$, temos

$$
\psi_k(0) = A = 0
$$
$$
\psi_k(L) = B\sin(kL) = 0 \;\Rightarrow\; k = \frac{m\pi}{L} \quad (m=1,2,3,\dots)
$$

(Os valores negativos de $k$ produzem as mesmas autofunções.)

Descobrimos os autovetores e autovalores:

$$
\boxed{\hat{K}^2|m\rangle = \frac{m^2\pi^2}{L^2}|m\rangle \qquad \text{onde} \qquad \langle x|m\rangle = \sqrt{\frac{2}{L}}\sin\left(\frac{m\pi x}{L}\right)}
$$

Observe que os autovalores são reais e que os autovetores são ortonormais:

$$
\langle m|m'\rangle = \int_0^L \langle m|x\rangle\langle x|m'\rangle\,dx = \int_0^L \frac{2}{L}\sin\left(\frac{m\pi x}{L}\right)\sin\left(\frac{m'\pi x}{L}\right)dx = \delta_{m,m'} \quad \text{(faça a integral)}
$$

Esses $\{|m\rangle\}$ são análogos aos $|I\rangle$ e $|II\rangle$ do exemplo anterior.

$$
\frac{d^2}{dt^2}|\Psi(t)\rangle = -\hat{K}^2|\Psi(t)\rangle
$$

Projetando com $\langle m|$:

$$
\frac{d^2}{dt^2}\langle m|\Psi(t)\rangle = -\frac{m^2\pi^2}{L^2}\langle m|\Psi(t)\rangle
$$

Uma EDO simples! A derivada $\partial^2/\partial x^2$ desapareceu!

Solução:

$$
\langle m|\Psi(t)\rangle = \langle m|\Psi(0)\rangle\cos\left(\frac{m\pi t}{L}\right)
$$

onde supus que a corda está parada em $t=0$ (senão teria que acrescentar $B\sin\!\left(\dfrac{m\pi t}{L}\right)$ e determinar $B$ das velocidades iniciais).

Assim como $|I\rangle$ e $|II\rangle$, autovetores de $\hat{\Omega}$ Hermitiano, formavam uma base ortonormal do EV de dimensão 2, os $\{|m\rangle\}$, autovetores de $\hat{K}^2$, formam uma base ortonormal no EV de dimensão infinita

$$
\hat{I} = \sum_{m=1}^{\infty}|m\rangle\langle m| \qquad \langle m|m'\rangle = \delta_{mm'}
$$

Assim:

$$
\boxed{|\Psi(t)\rangle = \sum_{m=1}^{\infty}|m\rangle\langle m|\Psi(t)\rangle = \sum_{m=1}^{\infty}\cos(\omega_m t)\,|m\rangle\langle m|\Psi(0)\rangle}
$$

## O operador de evolução e o propagador

O operador de evolução fica

$$
\hat{U}(t) = \sum_{m=1}^{\infty}\cos(\omega_m t)\,|m\rangle\langle m| \qquad \left(\omega_m = \frac{m\pi}{L}\right)
$$

O propagador na base $|x\rangle$ é obtido facilmente:

$$
\langle x|\Psi(t)\rangle = \langle x|\hat{U}(t)|\Psi(0)\rangle
$$
$$
= \int_0^L \underbrace{\langle x|\hat{U}(t)|x'\rangle}_{\text{propagador}}\langle x'|\Psi(0)\rangle\,dx'
$$

O propagador não pode ser escrito como uma matriz (como no caso do EV de dimensão finita); no entanto,

$$
\langle x|\hat{U}(t)|x'\rangle = \sum_{m=1}^{\infty}\cos(\omega_m t)\,\langle x|m\rangle\langle m|x'\rangle
$$
$$
= \sum_{m=1}^{\infty}\left(\frac{2}{L}\right)\cos(\omega_m t)\,\sin\left(\frac{m\pi x}{L}\right)\sin\left(\frac{m\pi x'}{L}\right)
$$

Finalmente:

$$
\boxed{\Psi(x,t) = \int_0^L \left[\underbrace{\sum_{m=1}^{\infty}\frac{2}{L}\cos(\omega_m t)\sin\left(\frac{m\pi x}{L}\right)\sin\left(\frac{m\pi x'}{L}\right)}_{\text{propagador}}\right]\Psi(x',0)\,dx'}
$$

onde $\Psi(x,t)$ (à esquerda) é a forma da corda no instante $t$, e $\Psi(x,0)$ (dentro da integral) é a forma inicial da corda.

Compare com

$$
\begin{bmatrix} x_1(t) \\ x_2(t) \end{bmatrix}
=
\begin{bmatrix}
\tfrac{1}{2}\cos\omega_I t + \tfrac{1}{2}\cos\omega_{II}t & \tfrac{1}{2}\cos\omega_I t - \tfrac{1}{2}\cos\omega_{II}t \\[4pt]
\tfrac{1}{2}\cos\omega_I t - \tfrac{1}{2}\cos\omega_{II}t & \tfrac{1}{2}\cos\omega_I t + \tfrac{1}{2}\cos\omega_{II}t
\end{bmatrix}
\begin{bmatrix} x_1(0) \\ x_2(0) \end{bmatrix}
$$

## O operador identidade: base discreta vs. base contínua

Vimos duas maneiras de escrever o operador $\hat{I}$ (no EV das funções em 1D):

$$
\hat{I} = \int_{-\infty}^{\infty} dx\,|x\rangle\langle x| = \int_{-\infty}^{\infty} dk\,|k\rangle\langle k|
$$

Dizemos que os autovetores de $\hat{X}$ e $\hat{K}$ formam uma BASE CONTÍNUA (o rótulo dos vetores é uma variável contínua).

Essencial aqui é o fato de que a base contínua é ortonormal (por isso o operador $\hat{I}$ se escreve como uma soma simples de "borboletas"):

$$
\langle x|x'\rangle = \delta(x-x') \qquad \text{e} \qquad \langle k|k'\rangle = \delta(k-k')
$$

Um conjunto restrito de "borboletas" de vetores ortonormalizados constitui um PROJETOR. Por exemplo:

$$
\hat{P} = \int_a^b dx\,|x\rangle\langle x| \quad \text{é um projetor.}
$$

Se $|f\rangle$ é o ket associado à função $f(x) = \langle x|f\rangle$, então a função correspondente a $\hat{P}|f\rangle$ é

$$
f_P(x) = \langle x|\hat{P}|f\rangle = \int_a^b dx'\,\langle x|x'\rangle\langle x'|f\rangle = \int_a^b dx'\,\delta(x-x')\,f(x')
$$

$$
f_P(x) =
\begin{cases}
f(x), & \text{se } x \in [a,b] \\
0, & \text{se } x \notin [a,b]
\end{cases}
$$

> **Observação:** o projetor $\hat{P} = \int_a^b dx\,|x\rangle\langle x|$ atua "recortando" a função $f(x)$, mantendo seus valores apenas no intervalo $[a,b]$ e anulando-a fora desse intervalo. Esquematicamente, o gráfico de $f(x)$ (uma curva suave) dá origem ao gráfico de $f_P(x)$, que coincide com $f(x)$ em $[a,b]$ e é nulo fora dele, apresentando em geral uma descontinuidade nos pontos $x=a$ e $x=b$.
