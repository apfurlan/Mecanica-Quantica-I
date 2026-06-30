# (20ª aula) — Problemas em 3D: operadores de posição, momento e momento angular; harmônicos esféricos

## Problemas em 3D

Você já foi apresentado a 9 operadores que atuam no espaço vetorial de estados de uma partícula em 3D:

- $\hat{X}, \hat{Y}, \hat{Z}$ — os operadores de posição;
- $\hat{P}_x, \hat{P}_y, \hat{P}_z$ — os operadores de momento linear;
- $\hat{L}_x, \hat{L}_y, \hat{L}_z$ — os operadores de momento angular.

(Além de $\hat{L}^2 = \hat{L}_x^2 + \hat{L}_y^2 + \hat{L}_z^2$, o "tamanho ao quadrado" de $\hat{L}$.)

Os comutadores relevantes:

$$
[\hat{X}_i, \hat{X}_j] = 0 \quad \Longrightarrow \quad \exists \text{ autovetores } |xyz\rangle = |\vec{r}\rangle
$$

$$
[\hat{P}_i, \hat{P}_j] = 0 \quad \Longrightarrow \quad \exists \text{ autovetores } |p_x p_y p_z\rangle = |\vec{p}\rangle
$$

$$
[\hat{X}_i, \hat{P}_j] = i\hbar \delta_{ij}
$$

Desses comutadores obtivemos

$$
[\hat{L}_x, \hat{L}_y] = i\hbar \hat{L}_z \, ; \qquad [\hat{L}_y, \hat{L}_z] = i\hbar \hat{L}_x \, ; \qquad [\hat{L}_z, \hat{L}_x] = i\hbar \hat{L}_y
$$

além de

$$
[\hat{L}^2, \hat{L}_i] = 0 \qquad (i = 1, 2, 3)
$$

## A ação desses operadores na base $|\vec{r}\rangle$

$$
\langle \vec{r}| \hat{X} |\Psi\rangle = x\,\Psi(\vec{r}) = r\sin\theta\cos\varphi\,\Psi(\vec{r})
$$

$$
\langle \vec{r}| \hat{Y} |\Psi\rangle = y\,\Psi(\vec{r}) = r\sin\theta\sin\varphi\,\Psi(\vec{r})
$$

$$
\langle \vec{r}| \hat{Z} |\Psi\rangle = z\,\Psi(\vec{r}) = r\cos\theta\,\Psi(\vec{r})
$$

$$
\langle \vec{r}| \hat{P}_x |\Psi\rangle =
\begin{cases}
-i\hbar \dfrac{\partial \Psi}{\partial x} \\[3mm]
-i\hbar \left[ (\sin\theta\cos\varphi)\dfrac{\partial \Psi}{\partial r} + \left(\dfrac{\cos\theta\cos\varphi}{r}\right)\dfrac{\partial \Psi}{\partial \theta} + \left(\dfrac{-\sin\varphi}{r\sin\theta}\right)\dfrac{\partial \Psi}{\partial \varphi} \right]
\end{cases}
$$

$$
\langle \vec{r}| \hat{P}_y |\Psi\rangle =
\begin{cases}
-i\hbar \dfrac{\partial \Psi}{\partial y} \\[3mm]
-i\hbar \left[ (\sin\theta\sin\varphi)\dfrac{\partial \Psi}{\partial r} + \left(\dfrac{\cos\theta\sin\varphi}{r}\right)\dfrac{\partial \Psi}{\partial \theta} + \left(\dfrac{\cos\varphi}{r\sin\theta}\right)\dfrac{\partial \Psi}{\partial \varphi} \right]
\end{cases}
$$

$$
\langle \vec{r}| \hat{P}_z |\Psi\rangle =
\begin{cases}
-i\hbar \dfrac{\partial \Psi}{\partial z} \\[3mm]
-i\hbar \left[ (\cos\theta)\dfrac{\partial \Psi}{\partial r} + \left(\dfrac{-\sin\theta}{r}\right)\dfrac{\partial \Psi}{\partial \theta} \right]
\end{cases}
$$

$$
\langle \vec{r}| \hat{L}_x |\Psi\rangle =
\begin{cases}
i\hbar \left( z \dfrac{\partial \Psi}{\partial y} - y \dfrac{\partial \Psi}{\partial z} \right) \\[3mm]
i\hbar \left( \sin\varphi \dfrac{\partial \Psi}{\partial \theta} + \cot\theta\cos\varphi \dfrac{\partial \Psi}{\partial \varphi} \right)
\end{cases}
$$

$$
\langle \vec{r}| \hat{L}_y |\Psi\rangle =
\begin{cases}
i\hbar \left( x \dfrac{\partial \Psi}{\partial z} - z \dfrac{\partial \Psi}{\partial x} \right) \\[3mm]
i\hbar \left( -\cos\varphi \dfrac{\partial \Psi}{\partial \theta} + \cot\theta\sin\varphi \dfrac{\partial \Psi}{\partial \varphi} \right)
\end{cases}
$$

$$
\langle \vec{r}| \hat{L}_z |\Psi\rangle =
\begin{cases}
i\hbar \left( y \dfrac{\partial \Psi}{\partial x} - x \dfrac{\partial \Psi}{\partial y} \right) \\[3mm]
i\hbar \left( -\dfrac{\partial \Psi}{\partial \varphi} \right)
\end{cases}
$$

$$
\langle \vec{r}| \hat{L}^2 |\Psi\rangle = (-\hbar^2) \left[ \frac{\partial^2 \Psi}{\partial \theta^2} + \cot\theta \frac{\partial \Psi}{\partial \theta} + \frac{1}{\sin^2\theta} \frac{\partial^2 \Psi}{\partial \varphi^2} \right]
$$

## Ondas planas: autofunções do momento

As autofunções dos operadores $\hat{P}_x$, $\hat{P}_y$ e $\hat{P}_z$ são ondas planas:

$$
\boxed{\langle \vec{r}|\vec{p}\rangle = \frac{e^{\,i\vec{p}\cdot\vec{r}/\hbar}}{(2\pi\hbar)^{3/2}}} \qquad \text{(onda de De Broglie)}
$$

A normalização é no sentido da função delta de Dirac.

$$
\langle p_x p_y p_z|p_x' p_y' p_z'\rangle = \delta(p_x - p_x')\,\delta(p_y - p_y')\,\delta(p_z - p_z') = \delta(\vec{p} - \vec{p}')
$$

Isso pode ser comprovado:

$$
\langle \vec{p}|\vec{p}'\rangle = \iiint d\vec{r} \, \langle \vec{p}|\vec{r}\rangle \langle \vec{r}|\vec{p}'\rangle = \iiint dx\,dy\,dz \; \frac{e^{-i\vec{p}\cdot\vec{r}/\hbar}\, e^{i\vec{p}'\cdot\vec{r}/\hbar}}{(2\pi\hbar)^3}
$$

O integrando é um produto $F(x)G(y)H(z)$, então

$$
\langle \vec{p}|\vec{p}'\rangle = \left[ \int \frac{e^{\,i(p_x'-p_x)x/\hbar}}{2\pi\hbar}\,dx \right] \left[ \int \frac{e^{\,i(p_y'-p_y)y/\hbar}}{2\pi\hbar}\,dy \right] \left[ \int \frac{e^{\,i(p_z'-p_z)z/\hbar}}{2\pi\hbar}\,dz \right]
$$

$$
= \delta(p_x - p_x')\,\delta(p_y - p_y')\,\delta(p_z - p_z')
$$

## Harmônicos esféricos: autofunções de $\hat{L}^2$ e $\hat{L}_z$

As autofunções dos operadores $\hat{L}^2$ e $\hat{L}_z$ são

$$
\boxed{\langle \vec{r}|\ell m\rangle = R(r)\, Y_\ell^m(\theta, \varphi)} \qquad \text{($R(r)$ é uma função qualquer)}
$$

onde

$$
Y_\ell^m(\theta,\varphi) = \sqrt{\frac{2\ell+1}{4\pi} \frac{(\ell-|m|)!}{(\ell+|m|)!}} \; P_\ell^{|m|}(\cos\theta) \; e^{im\varphi} \;(\pm)^m
$$

com a convenção de sinal $(-1)^m$ para $m \geq 0$ e $(+1)^m$ para $m < 0$.

Essa função se chama **harmônico esférico**. As funções $P_\ell^{|m|}(x)$ se chamam **polinômios associados de Legendre** e são tabelados.

Os autovalores:

$$
\hat{L}^2 |\ell m\rangle = \hbar^2 \ell(\ell+1) |\ell m\rangle, \qquad \hat{L}_z |\ell m\rangle = \hbar m |\ell m\rangle, \qquad \boxed{\ell \geq |m|}
$$

A normalização (da parte angular):

$$
\int_0^\pi \int_0^{2\pi} \left[Y_\ell^m(\theta,\varphi)\right]^* Y_{\ell'}^{m'}(\theta,\varphi) \, \sin\theta \, d\theta \, d\varphi = \delta_{\ell\ell'}\,\delta_{mm'}
$$

Assim como em 1D tanto a base $|x\rangle$ quanto a base $|p\rangle$ podem ser usadas para exprimir a identidade, em 3D temos

$$
\hat{\mathbb{1}} = \iiint_{-\infty}^{\infty} |\vec{r}\rangle\langle \vec{r}| \, \underbrace{d\vec{r}}_{dx\,dy\,dz} = \iiint_{-\infty}^{\infty} |\vec{p}\rangle\langle \vec{p}| \, \underbrace{d\vec{p}}_{dp_x\,dp_y\,dp_z}
$$

(mais adiante veremos outras bases possíveis).

## Rederivação de $\hat{L}^2$ e $\hat{L}_z$ via método de operadores

Iremos agora rederivar os autovalores/autoestados de $\hat{L}^2$ e $\hat{L}_z$ usando um método de operadores, semelhante ao que usamos no caso do oscilador harmônico.

Das equações de autovalor abstratas

$$
\hat{L}^2 |\alpha\beta\rangle = \alpha |\alpha\beta\rangle \qquad \text{e} \qquad \hat{L}_z |\alpha\beta\rangle = \beta |\alpha\beta\rangle
$$

onde $|\alpha\beta\rangle$ é o autovetor simultâneo de $\hat{L}^2$ e $\hat{L}_z$.

Definimos os operadores de "levantamento" e "abaixamento"

$$
\hat{L}_+ = \hat{L}_x + i\hat{L}_y \qquad \text{e} \qquad \hat{L}_- = \hat{L}_x - i\hat{L}_y
$$

análogos, no caso do oscilador 1D, a

$$
\hat{a}^\dagger = \frac{1}{\sqrt{2}}\left(\frac{\hat{X}}{b} - i\frac{b\hat{P}}{\hbar}\right) \qquad \text{e} \qquad \hat{a} = \frac{1}{\sqrt{2}}\left(\frac{\hat{X}}{b} + i\frac{b\hat{P}}{\hbar}\right)
$$

Temos:

$$
[\hat{L}_z, \hat{L}_+] = \hbar \hat{L}_+ \qquad \text{e} \qquad [\hat{L}_z, \hat{L}_-] = -\hbar \hat{L}_-
$$

(análogo a $[\hat{H}, \hat{a}^\dagger] = \hbar\omega\,\hat{a}^\dagger$ e $[\hat{H}, \hat{a}] = -\hbar\omega\,\hat{a}$)

além de

$$
[\hat{L}^2, \hat{L}_+] = [\hat{L}^2, \hat{L}_-] = 0 \qquad \text{(não há análogo no caso do oscilador)}
$$

Essas relações mostram que $\hat{L}_+$ "levanta" o autovalor de $\hat{L}_z$ de $\hbar$ enquanto $\hat{L}_-$ "abaixa" o autovalor de $\hat{L}_z$ de $\hbar$, **sem alterar o autovalor de $\hat{L}^2$**.

Veja porque:

$$
\hat{L}_z \left[ \hat{L}_+ |\alpha\beta\rangle \right] = (\hat{L}_+ \hat{L}_z + \hbar \hat{L}_+) |\alpha\beta\rangle = (\hat{L}_+ \beta + \hbar \hat{L}_+) |\alpha\beta\rangle = (\hbar + \beta) \underbrace{\left[ \hat{L}_+ |\alpha\beta\rangle \right]}_{\text{autovalor de } \hat{L}_+|\alpha\beta\rangle \text{ é } \beta+\hbar}
$$

enquanto

$$
\hat{L}^2 \left[ \hat{L}_+ |\alpha\beta\rangle \right] = \hat{L}_+ \hat{L}^2 |\alpha\beta\rangle = \alpha \underbrace{\left[ \hat{L}_+ |\alpha\beta\rangle \right]}_{\text{autovalor de } \hat{L}_+|\alpha\beta\rangle \text{ é } \alpha}
$$

Podemos concluir:

$$
\hat{L}_+ |\alpha\beta\rangle = C_+(\alpha\beta) |\alpha, \beta+\hbar\rangle
$$

onde $C_+(\alpha\beta)$ é um coeficiente a determinar (analogamente a $\hat{a}^\dagger |E\rangle = C_+ |E+\hbar\omega\rangle$).

Similarmente (demonstre isso!):

$$
\hat{L}_- |\alpha\beta\rangle = C_-(\alpha\beta) |\alpha, \beta-\hbar\rangle
$$

com $C_-(\alpha\beta)$ a determinar (analogamente a $\hat{a}|E\rangle = C_- |E-\hbar\omega\rangle$).

No caso do oscilador, estávamos resolvendo $\hat{H}|E\rangle = E|E\rangle$ e concluímos que, se um autovetor $|E\rangle$ existe, então $|E+\hbar\omega\rangle, |E+2\hbar\omega\rangle, \dots, |E-\hbar\omega\rangle, |E-2\hbar\omega\rangle$, também existem. A observação crucial foi a de que todos os autovalores tinham que ser positivos, portanto devia existir $|E_{min}\rangle$ tal que $\hat{a}|E_{min}\rangle = 0$ (e então $\hat{a}^\dagger \hat{a} |E_{min}\rangle = 0 \Rightarrow E_{min} = \hbar\omega/2$).

## Limites de $\beta$: existência de $|\alpha\beta_{max}\rangle$ e $|\alpha\beta_{min}\rangle$

No caso do momento angular a observação análoga é a de que $\beta^2$, o autovalor de $\hat{L}_z^2$, não pode ser maior que $\alpha$, o autovalor de $\hat{L}^2$.

$$
\langle \alpha\beta| \hat{L}^2 - \hat{L}_z^2 |\alpha\beta\rangle = \langle \alpha\beta| \hat{L}_x^2 + \hat{L}_y^2 |\alpha\beta\rangle \geq 0
$$

Onde usei que $\langle \Psi| \hat{O}^2 |\Psi\rangle = \langle \hat{O}\Psi|\hat{O}\Psi\rangle \geq 0$, para $\hat{O}$ Hermitiano. Dessa forma $\alpha \geq \beta^2$.

Isso permite concluir que devem existir $|\alpha\beta_{max}\rangle$ e $|\alpha\beta_{min}\rangle$ tais que

$$
\hat{L}_+ |\alpha\beta_{max}\rangle = 0 \qquad \text{e} \qquad \hat{L}_- |\alpha\beta_{min}\rangle = 0
$$

(analogamente a $\hat{a}|E_{min}\rangle = 0$).

Dessas relações podemos determinar $\alpha$ e $\beta$. Veja como:

$$
\hat{L}_- \hat{L}_+ = (\hat{L}_x - i\hat{L}_y)(\hat{L}_x + i\hat{L}_y) = \hat{L}_x^2 + \hat{L}_y^2 + i\hat{L}_x\hat{L}_y - i\hat{L}_y\hat{L}_x = \hat{L}_x^2 + \hat{L}_y^2 - \hbar \hat{L}_z = \hat{L}^2 - \hat{L}_z^2 - \hbar \hat{L}_z
$$

similarmente $\hat{L}_+ \hat{L}_- = \hat{L}^2 - \hat{L}_z^2 + \hbar \hat{L}_z$, então

$$
\hat{L}_- \hat{L}_+ |\alpha\beta_{max}\rangle = (\hat{L}^2 - \hat{L}_z^2 - \hbar \hat{L}_z) |\alpha\beta_{max}\rangle = 0
$$

$$
= (\alpha - \beta_{max}^2 - \hbar\beta_{max}) |\alpha\beta_{max}\rangle = 0
$$

$$
\alpha = \beta_{max}(\beta_{max} + \hbar)
$$

Similarmente $\hat{L}_+ \hat{L}_- |\alpha\beta_{min}\rangle = 0$ produz

$$
\alpha = \beta_{min}(\beta_{min} - \hbar)
$$

Igualando as duas expressões encontramos

$$
\beta_{max} = -\beta_{min}
$$

Como $\beta_{min}$ e $\beta_{max}$ devem estar separados por um número inteiro de $\hbar$ (você sabe argumentar por quê?), temos

$$
\beta_{max} - \beta_{min} = 2\beta_{max} = \hbar K \qquad (K = 0, 1, 2, \dots)
$$

Os valores possíveis de $\beta$ são:

$$
\boxed{\beta : \left\{ -\frac{K}{2}, -\frac{K}{2}+1, \dots, \frac{K}{2}-1, \frac{K}{2} \right\} \hbar}
$$

Os valores possíveis de $\alpha$ são $(K = 0, 1, 2, 3, \dots)$:

$$
\alpha = \frac{\hbar K}{2}\left( \frac{\hbar K}{2} + \hbar \right) = \boxed{\hbar^2 \, \frac{K}{2}\left(\frac{K}{2}+1\right)}
$$

O autovalor $\alpha$ é normalmente caracterizado pelo valor de $K/2$, que chamamos de **número quântico $\ell$**. O autovalor $\beta$ é caracterizado pelo número multiplicado por $\hbar$ que é chamado de **número quântico $m$**.

$$
(K=0) \qquad |0\,0\rangle \qquad (\ell = 0)
$$

$$
(K=1) \qquad |1/2, -1/2\rangle \;\, \text{e} \;\, |1/2, 1/2\rangle \qquad (\ell = 1/2)
$$

## Constantes de normalização $C_+$ e $C_-$

As constantes $C_+(\alpha\beta)$ e $C_-(\alpha\beta)$ podem ser determinadas assumindo que os estados $|\ell m\rangle$ são normalizados.

$$
\hat{L}_+ |\ell m\rangle = C_+(\ell m) |\ell, m+1\rangle
$$

$$
\langle \ell m| \hat{L}_- \hat{L}_+ |\ell m\rangle = |C_+(\ell m)|^2
$$

usando $\hat{L}_- \hat{L}_+ = \hat{L}^2 - \hat{L}_z^2 - \hbar \hat{L}_z$ obtenho

$$
\hbar^2 \ell(\ell+1) - \hbar^2 m^2 - \hbar^2 m = |C_+(\ell m)|^2
$$

ou

$$
C_+(\ell m) = \hbar \sqrt{\ell(\ell+1) - m(m+1)} \; \left( = \hbar\sqrt{(\ell-m)(\ell+m+1)} \right)
$$

(análogo a $\hat{a}^\dagger |n\rangle = C_+ |n+1\rangle$, $C_+ = \sqrt{n+1}$).

similarmente

$$
C_-(\ell m) = \hbar \sqrt{\ell(\ell+1) - m(m-1)} \; \left( = \hbar\sqrt{(\ell+m)(\ell-m+1)} \right)
$$

(análogo a $\hat{a}|n\rangle = C_- |n-1\rangle$, $C_- = \sqrt{n}$).

Veja como $C_+(\ell,\ell) = 0$ e $C_-(\ell,-\ell) = 0$.

Assim como os operadores $\hat{a}$ e $\hat{a}^\dagger$ facilitam o cálculo de elementos de matriz entre estados $|n\rangle$, os operadores $\hat{L}_+$ e $\hat{L}_-$ fazem o mesmo para elementos de matriz entre estados $|\ell m\rangle$.

## Exemplo: $\langle \ell m| \hat{L}_x |\ell m\rangle = 0$

**Exemplo.** Mostre que $\langle \ell m| \hat{L}_x |\ell m\rangle = 0$.

Como $\hat{L}_+ = \hat{L}_x + i\hat{L}_y$ e $\hat{L}_- = \hat{L}_x - i\hat{L}_y$, segue que $\hat{L}_x = \dfrac{1}{2}(\hat{L}_+ + \hat{L}_-)$.

(Observe que você não sabe prever a ação de $\hat{L}_x$ na base $|\ell m\rangle$, mas através dos operadores de levantamento e abaixamento é possível escrever $\hat{L}_x$ em termos de $\hat{L}_+$ e $\hat{L}_-$, que nós sabemos como são.)

Então

$$
\langle \ell m| \hat{L}_x |\ell m\rangle = \frac{1}{2} \langle \ell m| \hat{L}_+ + \hat{L}_- |\ell m\rangle = \frac{1}{2}\left[ C_+(\ell m) \underbrace{\langle \ell m|\ell, m+1\rangle}_{0} + C_-(\ell m) \underbrace{\langle \ell m|\ell, m-1\rangle}_{0} \right] = 0
$$

Onde usei $\langle \ell m'|\ell m\rangle = \delta_{\ell\ell'}\delta_{mm'}$.

A alternativa a esse cálculo usaria a integral:

$$
\langle \ell m| \hat{L}_x |\ell m\rangle = \iiint d\vec{r} \, \langle \ell m|\vec{r}\rangle \langle \vec{r}|\hat{L}_x|\ell m\rangle = \iiint d\vec{r} \; R^*(r) \left[Y_\ell^{m}(\theta,\varphi)\right]^* \left\{ i\hbar \left( \sin\varphi \frac{\partial}{\partial \theta} + \cot\theta\cos\varphi \frac{\partial}{\partial \varphi} \right) \right\} R(r)\, Y_\ell^m(\theta,\varphi)
$$

$\Rightarrow$ Os operadores $\hat{L}_+$ e $\hat{L}_-$ são seus amigos, aprenda a usá-los! (Embora eles só sejam realmente úteis quando os estados envolvidos são do tipo $|\ell m\rangle$.)

## Determinação de $\langle \vec{r}|\ell m\rangle$ pelo método diferencial

Assim como usamos $\langle x|\hat{a}|0\rangle = 0$ para obter uma EDO de 1ª ordem para determinar $\langle x|0\rangle = \psi_0(x)$ do oscilador harmônico, podemos encontrar $\langle \vec{r}|\ell m\rangle$ do mesmo modo.

$$
\langle \vec{r}| \hat{L}_+ |\ell\ell\rangle = 0 \quad \Longrightarrow \quad \langle \vec{r}| \hat{L}_x + i\hat{L}_y |\ell\ell\rangle = 0
$$

Obtemos $\langle \vec{r}|\ell\ell\rangle = F_{\ell\ell}(r,\theta,\varphi)$, e

$$
\hbar\, e^{i\varphi} \left[ \frac{\partial}{\partial \theta} + i\cot\theta \frac{\partial}{\partial \varphi} \right] F_{\ell\ell}(r,\theta,\varphi) = 0 \qquad \text{(EDP de 1ª ordem)}
$$

Claramente $F_{\ell\ell}(r,\theta,\varphi) = R(r)\, Y_\ell^\ell(\theta,\varphi)$, com $R(r)$ uma função arbitrária, e

$$
\frac{\partial Y_\ell^\ell}{\partial \theta} + i\cot\theta \frac{\partial Y_\ell^\ell}{\partial \varphi} = 0
$$

usando o fato de que uma autofunção de $\hat{L}_z$ deve ser do tipo $f(r,\theta)\, e^{im\varphi}$, escrevemos

$$
Y_\ell^\ell(\theta,\varphi) = U_\ell^\ell(\theta)\, e^{i\ell\varphi}
$$

onde

$$
\frac{dU_\ell^\ell}{d\theta} - \ell\cot\theta\, U_\ell^\ell = 0 \quad \Longrightarrow \quad U_\ell^\ell(\theta) = A(\sin\theta)^\ell
$$

é a solução geral. Assim,

$$
Y_\ell^\ell(\theta,\varphi) = A(\sin\theta)^\ell\, e^{i\ell\varphi}
$$

A constante $A$ é obtida da normalização

$$
1 = \int_0^\pi \sin\theta\,d\theta \int_0^{2\pi} d\varphi \; \left[Y_\ell^\ell\right]^* Y_\ell^\ell = |A|^2 \, 2\pi \underbrace{\int_0^\pi \sin^{2\ell+1}(\theta)\, d\theta}_{\displaystyle \frac{2(2\ell)!!}{(2\ell+1)!!}}
$$

$$
4\pi\,\frac{(2\ell)!!}{(2\ell+1)!!} = 4\pi\,\frac{2\cdot4\cdots2\ell}{1\cdot3\cdots(2\ell+1)} = \frac{4\pi\,(2^\ell\,\ell!)^2}{(2\ell+1)!}
$$

Assim

$$
A = (-1)^\ell \left[ \frac{(2\ell+1)!}{4\pi} \right]^{1/2} \frac{1}{2^\ell\,\ell!}
$$

onde o sinal $(-1)^\ell$ é uma convenção.

Dessa forma obtemos os harmônicos esféricos com $m = \ell$.

$$
\boxed{Y_\ell^\ell(\theta,\varphi) = (-1)^\ell \sqrt{\frac{(2\ell+1)!}{4\pi}} \; \frac{1}{2^\ell\,\ell!}\, (\sin\theta)^\ell\, e^{i\ell\varphi}}
$$

usando

$$
\langle \vec{r}| \hat{L}_- |\ell\ell\rangle = \hbar\sqrt{2\ell}\;\langle \vec{r}|\ell,\ell-1\rangle
$$

e a forma diferencial do operador $\hat{L}_-$, podemos obter todos os harmônicos esféricos **normalizados**.

$$
\iint \left[Y_\ell^m(\theta,\varphi)\right]^* Y_{\ell'}^{m'}(\theta,\varphi) \, d\Omega = \delta_{\ell\ell'}\,\delta_{mm'}
$$

onde $d\Omega = \sin\theta\,d\theta\,d\varphi$ é o elemento de ângulo sólido.

## Exemplo: verificação da ortogonalidade de $Y_2^1$ e $Y_1^1$

**Exemplo.** Verifique a ortogonalidade de $Y_2^1$ e $Y_1^1$.

$$
Y_2^1(\theta,\varphi) = -\sqrt{\frac{15}{8\pi}}\,\cos\theta\sin\theta\, e^{i\varphi}
$$

$$
Y_1^1(\theta,\varphi) = -\sqrt{\frac{3}{8\pi}}\,\sin\theta\, e^{i\varphi}
$$

$$
\int \left(Y_2^1\right)^* Y_1^1 \, d\Omega = \int_0^\pi \sin\theta\,d\theta \int_0^{2\pi} d\varphi \; \left( \frac{3\sqrt{15}}{8\pi} \right) \cos\theta\sin^2\theta = \frac{3\sqrt{15}}{4} \int_0^\pi \underbrace{\cos\theta \sin^3\theta}_{\substack{\text{ímpar em relação a } \theta=\pi/2 \\ \text{par em relação a } \theta=\pi/2}} d\theta = 0
$$

$\Rightarrow$ Explore a paridade nas integrais em $\theta$!
