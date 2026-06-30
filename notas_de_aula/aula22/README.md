# (22ª aula) — Translações e Rotações de Funções de Onda; Identidade com Autoestados de $\hat{L}^2$ e $\hat{L}_z$

## Translação de uma Função de Onda

Para obter uma função de onda **transladada**, a partir de uma função de onda conhecida, faça

$$
\widetilde{\Psi}(\vec{r}) = \Psi(\vec{r} - \vec{a}) \qquad (*)
$$

onde $\widetilde{\Psi}$ é o que queremos e $\Psi$ é supostamente conhecida.

Se $\vec{a} = a_x\hat{i} + a_y\hat{j} + a_z\hat{k}$, o significado de $(*)$ é: "na função $\Psi$ troque $x \to x - a_x$, $y \to y - a_y$ e $z \to z - a_z$".

É sempre mais fácil fazer isso quando $\Psi$ já está em termos de variáveis cartesianas.

**Exemplo:** $\Psi(\vec{r}) = R(r)\sin\theta$, com $\vec{a} = a(\hat{i} + \hat{j})$.

Em coordenadas cartesianas (usando $\sin\theta = \sqrt{x^2+y^2}/r$):

$$
\Psi(\vec{r}) = R\left(\sqrt{x^2+y^2+z^2}\right) \frac{\sqrt{x^2+y^2}}{\sqrt{x^2+y^2+z^2}}
$$

Logo, a função transladada é

$$
\widetilde{\Psi}(\vec{r}) = R\left(\sqrt{(x-a)^2+(y-a)^2+z^2}\right) \frac{\sqrt{(x-a)^2+(y-a)^2}}{\sqrt{(x-a)^2+(y-a)^2+z^2}}
$$

## Rotação de uma Função de Onda

Para obter uma função de onda **girada**, faça

$$
\widetilde{\Psi}(\vec{r}) = \Psi(R^{-1}\vec{r}) \qquad (**)
$$

onde $R^{-1}$ é a rotação **inversa** à rotação da função.

Se $R = R(\alpha, \hat{j})$ (rotação de ângulo $\alpha$ em torno do eixo $\hat{j}$), então o significado de $(**)$ é: "na função $\Psi$ troque $x \to (\cos\alpha)x - (\sin\alpha)z$, $y \to y$ e $z \to (\sin\alpha)x + (\cos\alpha)z$". Isso corresponde à matriz de rotação inversa

$$
R(\alpha, \hat{j})^{-1} =
\begin{bmatrix}
\cos\alpha & 0 & -\sin\alpha \\
0 & 1 & 0 \\
\sin\alpha & 0 & \cos\alpha
\end{bmatrix}
= R(-\alpha, \hat{j})
$$

**Exemplo:** $\Psi(\vec{r}) = R(r)\sin\theta = R(r)\dfrac{\sqrt{x^2+y^2}}{r}$.

Escrevemos a função a ser operada em termos de variáveis cartesianas e de $r$ (que permanece **inalterado**):

$$
\widetilde{\Psi}(\vec{r}) = \frac{R(r)}{r}\sqrt{\left[(\cos\alpha)x - (\sin\alpha)z\right]^2 + y^2}
$$

## Identidade Usando Autoestados de $\hat{L}^2$ e $\hat{L}_z$

Duas das formas usuais de escrever o operador identidade são

$$
\hat{I} = \int_{-\infty}^{\infty}dx\int_{-\infty}^{\infty}dy\int_{-\infty}^{\infty}dz \; |xyz\rangle\langle xyz| \tag{1}
$$

que usa os autoestados simultâneos de $\hat{X}$, $\hat{Y}$ e $\hat{Z}$ (somando sobre todos os autovalores possíveis), e

$$
\hat{I} = \int_{-\infty}^{\infty}dp_x\int_{-\infty}^{\infty}dp_y\int_{-\infty}^{\infty}dp_z \; |p_xp_yp_z\rangle\langle p_xp_yp_z| \tag{2}
$$

que usa os autoestados simultâneos de $\hat{P}_x$, $\hat{P}_y$ e $\hat{P}_z$.

Esses 2 conjuntos de 3 operadores são exemplos de **Conjunto Completo de Observáveis que Comutam**.

Claramente os estados $|x_0y_0z_0\rangle$ são bem definidos; sua função de onda (imprópria) é:

$$
\langle\vec{r}|x_0y_0z_0\rangle = \delta(x-x_0)\delta(y-y_0)\delta(z-z_0) = \delta(\vec{r}-\vec{r}_0)
$$

Similarmente, os estados $|p_xp_yp_z\rangle$ correspondem à função de onda de de Broglie (uma onda plana)

$$
\langle\vec{r}|p_xp_yp_z\rangle = \frac{e^{i\vec{p}\cdot\vec{r}/\hbar}}{(2\pi\hbar)^{3/2}}
$$

O fato de, tanto $|x_0y_0z_0\rangle$ quanto $|p_xp_yp_z\rangle$, serem normalizados no sentido da função delta de Dirac (os autovalores são contínuos):

$$
\langle x_0'y_0'z_0'|x_0y_0z_0\rangle = \delta(x_0-x_0')\delta(y_0-y_0')\delta(z_0-z_0')
$$

$$
\langle p_x'p_y'p_z'|p_xp_yp_z\rangle = \delta(p_x-p_x')\delta(p_y-p_y')\delta(p_z-p_z')
$$

garante que a identidade pode ser escrita como uma soma sobre todos os autovalores possíveis, na forma mostrada em (1) e (2).

## Outra Forma de Escrever a Identidade

Essas expressões da identidade não são as únicas possíveis. Você poderia usar os autoestados de $\hat{X}$, $\hat{Y}$ e $\hat{P}_z$ (que comutam) para escrever

$$
\hat{I} = \int_{-\infty}^{\infty}dx_0\int_{-\infty}^{\infty}dy_0\int_{-\infty}^{\infty}dp_z \; |x_0y_0p_z\rangle\langle x_0y_0p_z|
$$

*soma sobre todos os autovalores possíveis de $\hat{X}$, $\hat{Y}$ e $\hat{P}_z$*.

A função de onda associada a $|x_0y_0p_z\rangle$ é

$$
\langle\vec{r}|x_0y_0p_z\rangle = \delta(x-x_0)\delta(y-y_0)\frac{e^{ip_zz/\hbar}}{\sqrt{2\pi\hbar}}
$$

e você pode verificar a ortonormalização

$$
\langle x_0'y_0'p_z'|x_0y_0p_z\rangle = \delta(x_0-x_0')\delta(y_0-y_0')\delta(p_z-p_z')
$$

Veja como verificar isso:

$$
\langle x_0'y_0'p_z'|x_0y_0p_z\rangle = \int d\vec{r} \; \delta(x_0'-x)\delta(y_0'-y)\frac{e^{-ip_z'z/\hbar}}{\sqrt{2\pi\hbar}} \, \delta(x_0-x)\delta(y_0-y)\frac{e^{ip_zz/\hbar}}{\sqrt{2\pi\hbar}}
$$

$$
= \left[\int_{-\infty}^{\infty}dx \; \delta(x_0'-x)\delta(x_0-x)\right]\left[\int_{-\infty}^{\infty}dy \; \delta(y_0'-y)\delta(y_0-y)\right]\left[\int_{-\infty}^{\infty}dz \; \frac{e^{i(p_z-p_z')z/\hbar}}{2\pi\hbar}\right]
$$

$$
= \delta(x_0'-x_0)\delta(y_0'-y_0)\delta(p_z-p_z')
$$

## Projetores Associados a Medidas

As diversas expressões da identidade permitem construir projetores apropriados aos diversos medidos que podem ser feitos em uma partícula.

**Exemplo:** Projetor associado à probabilidade de medir a posição da partícula e encontrá-la entre $x=a$ e $x=b$ (com quaisquer $y$ e $z$):

$$
\hat{P} = \int_a^b dx \int_{-\infty}^{\infty}dy\int_{-\infty}^{\infty}dz \; |xyz\rangle\langle xyz|
$$

*autovalores associados ao resultado proposto*.

**Exemplo:** Projetor associado à probabilidade de, medindo $|\vec{p}|$, encontrar um resultado inferior a $|\vec{p}| = p_0$:

$$
\hat{P} = \int dp_x \int dp_y \int dp_z \; |\vec{p}\rangle\langle\vec{p}|
$$

*soma restrita a: $p_x^2 + p_y^2 + p_z^2 \le p_0^2$*.

Construir o projetor associado a um resultado de medida é a chave para encontrar a probabilidade do resultado, $\langle\Psi|\hat{P}|\Psi\rangle$, e o estado da partícula após o resultado ser obtido, $\hat{P}|\Psi\rangle$.

> supondo $\langle\Psi|\Psi\rangle = 1$

## O Operador $\hat{R}$

Para responder a respeito de medidas de $\hat{L}^2$ e $\hat{L}_z$ temos que começar escrevendo a identidade usando os autoestados $|\ell m\rangle$. O problema é que esses estados não são bem definidos.

$$
\langle\vec{r}|\ell m\rangle = R(r) Y_{\ell m}(\theta,\varphi) \qquad \text{(\textit{qualquer})}
$$

Precisamos introduzir um outro operador, que comute com $\hat{L}^2$ e $\hat{L}_z$, de tal modo que a informação do autovalor desse operador, junto com $(\ell, m)$, permita escrever uma função de onda bem definida.

**O OPERADOR $\hat{R}$**

$$
\hat{R}^2 = \hat{X}^2 + \hat{Y}^2 + \hat{Z}^2
$$

corresponde à distância da partícula à origem (ao quadrado).

$\hat{R}^2$ comuta com $\hat{L}_x$, $\hat{L}_y$ e $\hat{L}_z$.

$$
\left[\hat{X}^2+\hat{Y}^2+\hat{Z}^2, \; \underbrace{\hat{X}\hat{P}_y - \hat{Y}\hat{P}_x}_{\hat{L}_z}\right]
= -\hat{Y}\left[\hat{X}^2,\hat{P}_x\right] + \hat{X}\left[\hat{Y}^2,\hat{P}_y\right]
$$

$$
= -\hat{Y}(2i\hbar\hat{X}) + \hat{X}(2i\hbar\hat{Y}) = 0
$$

e similarmente com $\hat{L}_x$ e $\hat{L}_y$. Consequentemente temos $[\hat{R}^2,\hat{L}^2] = [\hat{R}^2,\hat{L}_z] = 0$.

O operador que vamos usar é, na verdade, $\hat{R} = \sqrt{\hat{X}^2+\hat{Y}^2+\hat{Z}^2}$, que comuta com $\hat{L}^2$ e $\hat{L}_z$ por ser uma função do operador $\hat{R}^2$.

## Autovalores/Autofunções de $\hat{R}$

$$
\hat{R}|r_0\rangle = r_0|r_0\rangle
$$

Tomando produto interno com $\langle\vec{r}|$:

$$
\langle\vec{r}|\hat{R}|r_0\rangle = r_0\langle\vec{r}|r_0\rangle
$$

$$
\sqrt{x^2+y^2+z^2}\,\langle\vec{r}|r_0\rangle = r_0\langle\vec{r}|r_0\rangle \qquad (*)
$$

*pois $|\vec{r}\rangle$ é autovetor de $\hat{R}$*.

Dessa igualdade somos forçados a concluir que $r_0 \ge 0$ (autovalores são positivos e formam um espectro contínuo).

$\langle\vec{r}|r_0\rangle$ é uma função de $x,y,z$, com $r_0$ como parâmetro. A única função que torna $(*)$ possível é

$$
\langle\vec{r}|r_0\rangle = \delta(r-r_0)\,f(\theta,\varphi) \qquad \text{(\textit{qualquer})}
$$

A parte angular de $\langle\vec{r}|r_0\rangle$ é arbitrária. Modificamos a parte radial para

$$
\langle\vec{r}|r_0\rangle = \frac{\delta(r-r_0)}{r_0}f(\theta,\varphi)
$$

para que a normalização de delta de Dirac saia diretamente da parte radial.

$$
\langle r_0|r_0'\rangle = \int d\vec{r}\,\langle r_0|\vec{r}\rangle\langle\vec{r}|r_0'\rangle
$$

$$
= \int_0^\infty r^2\,dr \int d\Omega \; \frac{\delta(r-r_0)}{r_0}f^*(\theta,\varphi)\,\frac{\delta(r-r_0')}{r_0'}g(\theta,\varphi)
$$

$$
= \left[\int_0^\infty dr \; \frac{r^2}{r_0 r_0'}\delta(r-r_0)\delta(r-r_0')\right]\left[\int d\Omega \; f^*(\Omega)g(\Omega)\right]
$$

$$
= \delta(r_0-r_0')\left[\int d\Omega \; f^*(\Omega)g(\Omega)\right]
$$

Dessa forma o estado $|r_0\ell m\rangle$ é completamente bem definido:

$$
\langle\vec{r}|r_0\ell m\rangle = \frac{\delta(r-r_0)}{r_0}Y_{\ell m}(\theta,\varphi)
$$

e a normalização é:

$$
\langle r_0'\ell'm'|r_0\ell m\rangle = \delta(r_0-r_0')\,\delta_{\ell\ell'}\,\delta_{mm'}
$$

onde usei

$$
\int d\Omega \; Y_{\ell'm'}^*(\Omega)\,Y_{\ell m}(\Omega) = \delta_{\ell\ell'}\,\delta_{mm'}
$$

Somando sobre todos os autovalores de $\hat{R}$, $\hat{L}^2$ e $\hat{L}_z$ obtemos uma expressão do operador identidade

$$
\hat{I} = \int_0^\infty dr_0 \underbrace{\sum_{\ell=0}^{\infty}\sum_{m=-\ell}^{\ell}}_{\text{não são independentes!}} |r_0\ell m\rangle\langle r_0\ell m|
$$

## Projetores

- Projetor associado à medida de $\hat{L}^2$ com resultado $6\hbar^2$ ($\ell=2$):

$$
\hat{P} = \int_0^\infty dr_0 \sum_{m=-2}^{2} |r_0 2 m\rangle\langle r_0 2 m|
$$

- Projetor associado à medida de $L_z$ com resultado $3\hbar$ ($m=3$):

$$
\hat{P} = \int_0^\infty dr_0 \sum_{\ell=3}^{\infty} |r_0\,\ell\,3\rangle\langle r_0\,\ell\,3|
$$

- Projetor associado à medida de $R$ (distância da partícula à origem) com resultado $R < a$:

$$
\hat{P} = \int_0^a dr_0 \sum_{\ell=0}^{\infty}\sum_{m=-\ell}^{\ell} |r_0\ell m\rangle\langle r_0\ell m|
$$

> $\to$ selecione da identidade os autovalores correspondentes ao resultado da medida!

## Cálculo de $\langle r_0\ell m|\Psi\rangle$

Como as probabilidades saem de $\langle\Psi|\hat{P}|\Psi\rangle$ (supondo que $\langle\Psi|\Psi\rangle=1$) é fundamental saber calcular

$$
\langle r_0\ell m|\Psi\rangle
$$

Isso é particularmente simples quando a função de onda $\langle\vec{r}|\Psi\rangle$ é fornecida em coordenadas esféricas.

**Exemplo:** $\langle\vec{r}|\Psi\rangle = e^{-\alpha r}\cos^2\theta$ (*não está normalizada*), calcule $\langle r_0\ell m|\Psi\rangle$.

$$
\langle r_0\ell m|\Psi\rangle = \int_0^\infty r^2 dr \int d\Omega \; \frac{\delta(r-r_0)}{r_0}Y_{\ell m}^*(\Omega)\,e^{-\alpha r}\cos^2\theta
$$

$$
= r_0\,e^{-\alpha r_0}\int d\Omega \; Y_{\ell m}^*(\theta,\varphi)\cos^2\theta
$$

Integrais angulares como essa são facilmente calculadas quando a parte angular de $\langle\vec{r}|\Psi\rangle$ é dada em termos de harmônicos esféricos (nesse caso basta usar $\int d\Omega \, Y_{\ell'm'}^*(\Omega)Y_{\ell m}(\Omega) = \delta_{\ell\ell'}\delta_{mm'}$).

Uma função regular de $(\theta,\varphi)$ **sempre** pode ser escrita como combinação linear de harmônicos esféricos:

$$
f(\theta,\varphi) = \sum_{\ell=0}^{\infty}\sum_{m=-\ell}^{\ell} c_{\ell m}\,Y_{\ell m}(\theta,\varphi) \qquad (*)
$$

com

$$
c_{\ell m} = \iint f(\theta,\varphi)\,Y_{\ell m}^*(\theta,\varphi)\,\sin\theta \, d\theta \, d\varphi
$$

## Completeza dos Harmônicos Esféricos

A completeza dos harmônicos esféricos se expressa matematicamente como (coloque a expressão de $c_{\ell m}$ em $(*)$):

$$
\sum_{\ell=0}^{\infty}\sum_{m=-\ell}^{\ell} Y_{\ell m}^*(\theta,\varphi)\,Y_{\ell m}(\theta',\varphi') = \frac{\delta(\theta-\theta')\,\delta(\varphi-\varphi')}{\sin\theta}
$$

$$
= \delta(\cos\theta-\cos\theta')\,\delta(\varphi-\varphi')
$$

A normalização de $f(\theta,\varphi)$ se manifesta nos coeficientes como (derive isso):

$$
\iint |f(\theta,\varphi)|^2 \sin\theta \, d\theta \, d\varphi = \sum_{\ell,m} |c_{\ell m}|^2
$$

## Dicas Práticas para Encontrar os $c_{\ell m}$ de uma $f(\theta,\varphi)$

1. Escreva a dependência em $\varphi$ na forma $e^{im\varphi}$ para saber os $m$'s que produzem $c_{\ell m} \ne 0$.

$$
\sin\theta\cos2\varphi = \sin\theta\left(\frac{e^{i2\varphi}+e^{-i2\varphi}}{2}\right)
$$

$\Rightarrow$ apenas $c_{2,2}$ e $c_{2,\bar{2}}$ (isto é, $c_{2,-2}$) são não nulos.

2. Observe a paridade da função de $\theta$ em relação a $\cos\theta \to -\cos\theta$ (use $x=\cos\theta$):

$$
\sin\theta\cos2\varphi = \sqrt{1-x^2}\cos2\varphi \quad \to \text{PAR}
$$

$$
\sin\theta\cos\theta\,e^{i3\varphi} = x\sqrt{1-x^2}\,e^{i3\varphi} \quad \to \text{ÍMPAR}
$$

Como a paridade dos harmônicos esféricos em relação a $\cos\theta \to -\cos\theta$ é determinada por $\ell+|m|$ (ver exercício I da lista), temos:

$$
\sin\theta\cos2\varphi \to m=\pm2,\;\ell=2,4,6,\dots \quad (\ell+|m| \text{ PAR})
$$

$$
\sin\theta\cos\theta\,e^{i3\varphi} \to m=3,\;\ell=4,6,8,\dots \quad (\ell+|m| \text{ ÍMPAR})
$$

3. Comece pelos menores $\ell$'s e vá registrando os $c_{\ell m}$ diferentes de zero. Pare quando $\displaystyle\sum_{\ell,m}|c_{\ell m}|^2$ for igual a $\displaystyle\iint |f(\theta,\varphi)|^2 \, d\Omega$.

## Exemplo Completo: Previsão de Medidas de $\hat{L}^2$ e $\hat{L}_z$

Quando a parte angular de $\langle\vec{r}|\Psi\rangle$ está expressa em termos de $Y_{\ell m}$'s fica fácil de prever os possíveis resultados de medidas de $\hat{L}^2$ e $\hat{L}_z$.

**Exemplo:**

$$
\Psi(\vec{r}) = R(r)\,Y_{22}(\theta,\varphi) + G(r)\left[\sqrt{2}\,Y_{10}(\theta,\varphi) + Y_{1\bar{1}}(\theta,\varphi)\right]
$$

$R(r)$ e $G(r)$ são funções radiais das quais precisamos conhecer as integrais

$$
\int_0^\infty |R(r)|^2 r^2 \, dr = A \qquad \text{e} \qquad \int_0^\infty |G(r)|^2 r^2 \, dr = B
$$

Normalizamos $\Psi(\vec{r})$ calculando (mostre isso)

$$
\int d\vec{r} \; |\Psi(\vec{r})|^2 = A + 3B
$$

$$
\Psi(\vec{r}) = (A+3B)^{-1/2}\left[R(r)\,Y_{22} + \sqrt{2}\,G\,Y_{10} + G\,Y_{1\bar{1}}\right] \quad \text{(normalizada)}
$$

Os valores de $\hat{L}^2$ e $\hat{L}_z$ possíveis de serem obtidos são

$$
L^2 = \{2\hbar^2 \text{ e } 6\hbar^2\} \qquad L_z = \{-\hbar, 0, 2\hbar\}
$$

**Probabilidade de encontrar $\ell=2$:**

$$
\hat{P} = \int_0^\infty dr_0 \sum_{m=-2}^{2} |r_0\,2\,m\rangle\langle r_0\,2\,m|
$$

$$
\langle r_0\,2\,m|\Psi\rangle = \int_0^\infty r^2 dr \int d\Omega \; \frac{\delta(r-r_0)}{r_0}Y_{2m}^*(\Omega)\,\frac{R(r)\,Y_{22}+\sqrt{2}\,G\,Y_{10}+G\,Y_{1\bar{1}}}{\sqrt{A+3B}}
= \frac{r_0\,R(r_0)\,\delta_{m2}}{\sqrt{A+3B}}
$$

(da ortogonalidade dos $Y_{\ell m}$).

Segue que

$$
\langle\Psi|\hat{P}|\Psi\rangle = \int_0^\infty dr_0 \; \frac{r_0^2\,|R(r_0)|^2}{A+3B} = \boxed{\frac{A}{A+3B}}
$$

**A função de onda após medir $\hat{L}^2$ e obter $6\hbar^2$ ($\ell=2$):**

$$
\langle\vec{r}|\hat{P}|\Psi\rangle = \int_0^\infty dr_0 \sum_{m=-2}^{2} \langle\vec{r}|r_0\,2\,m\rangle\,\frac{r_0\,R(r_0)\,\delta_{m2}}{\sqrt{A+3B}}
$$

$$
= \int_0^\infty dr_0 \; \delta(r-r_0)\,Y_{22}(\theta,\varphi)\,\frac{r_0\,R(r_0)}{\sqrt{A+3B}}
$$

$$
= \frac{R(r)\,Y_{22}(\theta,\varphi)}{\sqrt{A+3B}} \qquad \text{(não normalizada)}
$$

$$
= \frac{R(r)\,Y_{22}(\theta,\varphi)}{\sqrt{A}} \qquad \text{(normalizada)}
$$
