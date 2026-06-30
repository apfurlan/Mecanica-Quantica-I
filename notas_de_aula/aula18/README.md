# (18ª aula) — Operadores de Criação e Destruição

## Operadores de Criação e Destruição

É possível achar o espectro do Hamiltoniano do oscilador harmônico **SEM RECORRER A UMA EDO**.

$$
\hat{H} = \frac{\hat{P}^2}{2m} + \frac{1}{2}m\omega^2\hat{X}^2
$$

Vamos apenas usar a propriedade $[\hat{X}, \hat{P}] = i\hbar$ que, caso você se recorde, foi derivada através da representação de $\hat{X}$ e $\hat{P}$ na base $|x\rangle$.

$$
\langle x|\hat{X}\hat{P}|\Psi\rangle = -i\hbar \, x \frac{d\Psi}{dx}
$$

$$
\langle x|\hat{P}\hat{X}|\Psi\rangle = -i\hbar \frac{d}{dx}(x\Psi) = -i\hbar\Psi - i\hbar\, x \frac{d\Psi}{dx}
$$

então

$$
\langle x|\hat{X}\hat{P} - \hat{P}\hat{X}|\Psi\rangle = i\hbar \langle x|\Psi\rangle \quad \Longrightarrow \quad [\hat{X}, \hat{P}] = i\hbar
$$

Definimos o operador

$$
\hat{a} = \left( \frac{m\omega}{2\hbar} \right)^{1/2} \hat{X} + i \left( \frac{1}{2m\omega\hbar} \right)^{1/2} \hat{P}
$$

$$
= \frac{1}{\sqrt{2}}\frac{\hat{X}}{b} + \frac{i}{\sqrt{2}}\frac{b}{\hbar}\hat{P} \qquad \left( b = \sqrt{\hbar/m\omega} \right)
$$

e seu adjunto

$$
\hat{a}^\dagger = \frac{1}{\sqrt{2}}\frac{\hat{X}}{b} - \frac{i}{\sqrt{2}}\frac{b}{\hbar}\hat{P}
$$

A relação $[\hat{X}, \hat{P}] = i\hbar$ implica em

$$
[\hat{a}, \hat{a}^\dagger] = \left[ \frac{1}{\sqrt{2}}\frac{\hat{X}}{b} + \frac{i}{\sqrt{2}}\frac{b}{\hbar}\hat{P} , \; \frac{1}{\sqrt{2}}\frac{\hat{X}}{b} - \frac{i}{\sqrt{2}}\frac{b}{\hbar}\hat{P} \right]
$$

$$
= \frac{-i}{2\hbar}[\hat{X}, \hat{P}] + \frac{i}{2\hbar}[\hat{P}, \hat{X}] = 1
$$

Podemos escrever $\hat{H}$ usando $\hat{a}^\dagger\hat{a}$.

$$
\hat{a}^\dagger \hat{a} = \frac{1}{2}\frac{\hat{X}^2}{b^2} + \frac{1}{2}\frac{\hat{P}^2 b^2}{\hbar^2} + \frac{i}{2\hbar}(\hat{X}\hat{P} - \hat{P}\hat{X})
$$

$$
= \frac{1}{2}\frac{m\omega \hat{X}^2}{\hbar} + \frac{1}{2}\frac{\hat{P}^2}{m\hbar\omega} - \frac{1}{2}
$$

$$
= \frac{\hat{H}}{\hbar\omega} - \frac{1}{2}
$$

de onde

$$
\boxed{\hat{H} = \hbar\omega\left( \hat{a}^\dagger\hat{a} + \frac{1}{2} \right)}
$$

**Obs:** Note que os operadores $\hat{a}$ e $\hat{a}^\dagger$ não têm dimensão.

$$
\hat{H}|E\rangle = E|E\rangle \quad \text{fica, definindo } \varepsilon = \frac{E}{\hbar\omega},
$$

$$
\left( \hat{a}^\dagger\hat{a} + \frac{1}{2} \right)|\varepsilon\rangle = \varepsilon|\varepsilon\rangle
$$

onde chamamos de $\hat{h} \equiv \hat{a}^\dagger\hat{a} + \dfrac{1}{2}$ o **Hamiltoniano adimensional** e $\varepsilon$ o **autovalor adimensional**.

## Determinação dos Autovalores

Podemos determinar os autovalores $\varepsilon$ usando apenas as propriedades dos comutadores:

$$
[\hat{a}, \hat{h}] = \left[ \hat{a}, \hat{a}^\dagger\hat{a} + \frac{1}{2} \right] = \hat{a}
$$

$$
[\hat{a}^\dagger, \hat{h}] = \left[ \hat{a}^\dagger, \hat{a}^\dagger\hat{a} + \frac{1}{2} \right] = -\hat{a}^\dagger
$$

Se conhecemos um autovetor $|\varepsilon\rangle$ podemos obter outros usando $\hat{a}$ e $\hat{a}^\dagger$.

$$
\hat{h}\left[ \hat{a}|\varepsilon\rangle \right] = \left\{ \hat{a}\hat{h} - [\hat{a}, \hat{h}] \right\}|\varepsilon\rangle
$$

$$
= \hat{a}\varepsilon|\varepsilon\rangle - \hat{a}|\varepsilon\rangle = (\varepsilon - 1)\left[ \hat{a}|\varepsilon\rangle \right]
$$

$\Longrightarrow \hat{a}|\varepsilon\rangle$ é autovetor de $\hat{h}$ com autovalor $(\varepsilon - 1)$!

Analogamente,

$$
\hat{h}\left[ \hat{a}^\dagger|\varepsilon\rangle \right] = \left\{ \hat{a}^\dagger\hat{h} - [\hat{a}^\dagger, \hat{h}] \right\}|\varepsilon\rangle
$$

$$
= \hat{a}^\dagger\varepsilon|\varepsilon\rangle + \hat{a}^\dagger|\varepsilon\rangle = (\varepsilon + 1)\left[ \hat{a}^\dagger|\varepsilon\rangle \right]
$$

$\Longrightarrow \hat{a}^\dagger|\varepsilon\rangle$ é autovetor de $\hat{h}$ com autovalor $(\varepsilon + 1)$!

Isso mostra que se $\varepsilon$ é um autovalor de $\hat{h}$, $\varepsilon - 1, \varepsilon - 2, \varepsilon - 3, \dots$ também o são, bem como $\varepsilon + 1, \varepsilon + 2, \varepsilon + 3, \dots$.

Como sabemos que os autovalores não podem ser negativos[^1], deve haver um autovetor $|\varepsilon_0\rangle$ tal que

$$
\hat{a}|\varepsilon_0\rangle = 0 \quad \Longrightarrow \quad \hat{a}^\dagger\hat{a}|\varepsilon_0\rangle = 0
$$

ou

$$
\left( \hat{h} - \frac{1}{2} \right)|\varepsilon_0\rangle = 0 \quad \Longrightarrow \quad \hat{h}|\varepsilon_0\rangle = \frac{1}{2}|\varepsilon_0\rangle
$$

> O menor autovalor de $\hat{h}$ é $1/2$!

Atuando com $\hat{a}^\dagger$ no autovetor $|1/2\rangle$ obtemos $\varepsilon = 3/2, 5/2, 7/2, \dots$, então os autovalores de $\hat{h}$ são

$$
\varepsilon_n = n + \frac{1}{2} \qquad (n = 0, 1, 2, \dots)
$$

Correspondentemente, os autovalores de $\hat{H}$ são

$$
\boxed{E_n = \hbar\omega\left( n + \frac{1}{2} \right) \qquad (n = 0, 1, 2, \dots)}
$$

O autovetor de $\hat{h}$ que é aniquilado por $\hat{a}$ é único pois, como vimos, ele tem autovalor $1/2$ e os autovalores discutidos são **NÃO-DEGENERADOS** em 1D.

## Normalização dos Autovetores

Vamos chamar $|\varepsilon_n\rangle = |n\rangle$. Assim, $\hat{a}^\dagger\hat{a}|n\rangle = n|n\rangle$ e $\hat{h}|n\rangle = (n+1/2)|n\rangle$.

Vimos que $\hat{a}|n\rangle = c_n |n-1\rangle$, se $|n\rangle$ e $|n-1\rangle$ estão normalizados quem é $c_n$? Tome o adjunto

$$
\langle n|\hat{a}^\dagger = \langle n-1|c_n^*
$$

e tome o produto interno

$$
\langle n|\hat{a}^\dagger\hat{a}|n\rangle = |c_n|^2 \langle n-1|n-1\rangle
$$

$$
n = |c_n|^2 \quad \longrightarrow \quad \text{escolhemos } \boxed{c_n = \sqrt{n}}
$$

(usei $\hat{a}^\dagger\hat{a} = \hat{h} - 1/2$ e $\hat{h}|n\rangle = (n+1/2)|n\rangle$).

Analogamente

$$
\hat{a}^\dagger|n\rangle = c_{n+1}|n+1\rangle \quad \Longrightarrow \quad \langle n|\hat{a} = \langle n+1|c_{n+1}^*
$$

$$
\langle n|\hat{a}\hat{a}^\dagger|n\rangle = |c_{n+1}|^2\langle n+1|n+1\rangle
$$

usando $\hat{a}\hat{a}^\dagger = \hat{a}^\dagger\hat{a} + 1$ (isso vem do comutador) e $\langle n|\hat{a}^\dagger\hat{a}|n\rangle = n$, temos

$$
n + 1 = |c_{n+1}|^2 \quad \longrightarrow \quad \text{escolhemos } \boxed{c_{n+1} = \sqrt{n+1}}
$$

Assim

$$
\boxed{\hat{a}|n\rangle = \sqrt{n}|n-1\rangle} \qquad \text{e} \qquad \boxed{\hat{a}^\dagger|n\rangle = \sqrt{n+1}|n+1\rangle}
$$

O operador $\hat{a}^\dagger\hat{a}$ ($=\hat{h} - 1/2$) se chama **operador número** pois

$$
\hat{a}^\dagger\hat{a}|n\rangle = \left( \hat{h} - \frac{1}{2} \right)|n\rangle = n|n\rangle \qquad \text{($n$ = número de excitação do estado $|n\rangle$)}
$$

**Obs:** Como os $|n\rangle$ são autovetores de um operador Hermitiano, segue que $\langle n|m\rangle = 0$ se $m \neq n$. Admitimos que $\langle n|n\rangle = 1$ para todos os $n$.

Note que ainda não falamos em autofunções, mesmo assim podemos calcular valores médios de qualquer operador que envolve $\hat{X}$ ou $\hat{P}$ usando os estados $|n\rangle$.

## Valores Médios sem Integrais

$$
\boxed{\hat{X} = \frac{1}{\sqrt{2}}b\left( \hat{a} + \hat{a}^\dagger \right)} \qquad \text{e} \qquad \boxed{\hat{P} = \frac{i}{\sqrt{2}}\frac{\hbar}{b}\left( \hat{a}^\dagger - \hat{a} \right)}
$$

Por exemplo, para o estado fundamental

$$
\langle 0|\hat{X}|0\rangle = \frac{b}{\sqrt{2}}\langle 0|\hat{a} + \hat{a}^\dagger|0\rangle
$$

agora usamos $\hat{a}|0\rangle = 0$ e $\hat{a}^\dagger|0\rangle = |1\rangle$

$$
= \frac{b}{\sqrt{2}}\langle 0|1\rangle = 0
$$

$$
\langle 0|\hat{X}^2|0\rangle = \frac{b^2}{2}\langle 0|\hat{a}\hat{a} + \hat{a}\hat{a}^\dagger + \hat{a}^\dagger\hat{a} + \hat{a}^\dagger\hat{a}^\dagger|0\rangle
$$

Claramente os únicos termos não nulos serão os que envolverem o mesmo número de $\hat{a}$'s e $\hat{a}^\dagger$'s.

Ainda assim:

$$
\langle 0|\hat{a}\hat{a}^\dagger|0\rangle = \langle 0|\hat{a}|1\rangle = \langle 0|0\rangle = 1
$$

$$
\langle 0|\hat{a}^\dagger\hat{a}|0\rangle = 0 \qquad \text{(operador número)}
$$

então

$$
\langle 0|\hat{X}^2|0\rangle = \frac{b^2}{2} = \frac{\hbar}{2m\omega}
$$

> Veja que não foi preciso fazer nenhuma integral!

Nos exercícios você irá praticar com esses operadores.

## As Autofunções

E as autofunções, $\langle x|n\rangle = \psi_n(x)$, será que dá para obtê-las com esses operadores? Sim. Começamos com o estado fundamental. Usamos

$$
\hat{a}|0\rangle = 0,
$$

projetando em $\langle x|$ e usando $\hat{a} = \dfrac{1}{\sqrt{2}}\dfrac{\hat{X}}{b} + \dfrac{i}{\sqrt{2}}\dfrac{b}{\hbar}\hat{P}$ obtenho uma EDO para $\langle x|0\rangle = \psi_0(x)$.

$$
\frac{1}{\sqrt{2}}\frac{x}{b}\psi_0(x) + \frac{b}{\sqrt{2}}\frac{d\psi_0(x)}{dx} = 0
$$

$$
\psi_0' = -\left( \frac{x}{b^2} \right)\psi_0 \, , \quad \text{cuja solução normalizada é}
$$

$$
\boxed{\psi_0(x) = \left( \frac{1}{\pi b^2} \right)^{1/4} e^{-x^2/2b^2}}
$$

E as outras autofunções? Use o operador $\hat{a}^\dagger$

$$
|1\rangle = \hat{a}^\dagger|0\rangle, \quad \text{com} \quad \hat{a}^\dagger = \frac{1}{\sqrt{2}}\frac{\hat{X}}{b} - \frac{i}{\sqrt{2}}\frac{b}{\hbar}\hat{P}
$$

projetando em $\langle x|$:

$$
\psi_1(x) = \frac{1}{\sqrt{2}}\frac{x}{b}\psi_0 - \frac{b}{\sqrt{2}}\psi_0'
$$

$$
= \frac{1}{\sqrt{2}}\frac{x}{b}\psi_0 + \left( \frac{b}{\sqrt{2}} \right)\left( \frac{x}{b^2} \right)\psi_0
$$

$$
= \boxed{\sqrt{2}\,\frac{x}{b}\left( \frac{1}{\pi b^2} \right)^{1/4} e^{-x^2/2b^2}} \qquad \text{(já normalizado!)}
$$

$$
= \frac{1}{\sqrt{b}}\left( \frac{1}{\sqrt{\pi}\,2} \right)^{1/2} H_1(x/b)\, e^{-x^2/2b^2}
$$

[^1]: O operador $\hat{H} = \dfrac{\hat{P}^2}{2m} + \dfrac{1}{2}m\omega^2\hat{X}^2$ é positivo definido, i.e., por envolver operadores ao quadrado, todos os autovalores são positivos.
