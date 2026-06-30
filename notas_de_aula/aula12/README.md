# (12ª aula) — Como testar a MQ: ensembles, valores médios e variáveis compatíveis

## Como testar a MQ?

O colapso do vetor de estado após uma medida ideal é a ferramenta usada para se preparar estados quânticos específicos e se testar as predições da teoria (em uma partícula em um estado desconhecido).

Se ao medir $\hat{R}$ obtemos como resultado um autovalor **NÃO DEGENERADO**, o postulado III diz que o estado da partícula passa a ser o autovetor associado (unicamente definido, a menos de uma constante multiplicativa). Se o resultado da medida for um autovalor **DEGENERADO**, sabemos apenas que o estado, após a medida, está no subespaço degenerado; para especificar o estado temos que fazer uma medida de **OUTRO OBSERVÁVEL** cujo operador comute com $\hat{R}$ (verdadeiramente).

*(diagrama: no caso da direita, o autovalor $\omega_1$ é não degenerado, mas $\omega_2$ é degenerado, com o subespaço gerado por $|\omega_2,1\rangle$ e $|\omega_2,2\rangle$; o operador que vai especificar o estado dentro desse subespaço deve comutar com $\hat{R}$.)*

## Ensemble quântico

Um conjunto de $N$ partículas no **MESMO ESTADO** $|\Psi\rangle$ se chama um **ENSEMBLE QUÂNTICO**.

Se $|\Psi\rangle$ é conhecido você pode fazer previsões sobre a distribuição de resultados experimentais.

**Exemplo:**

$$
|\Psi\rangle = \sum_{i=1}^{6} c_i |\omega_i\rangle \qquad \text{(base ortonormal de autovetores de } \hat{R}\text{, normalizado, } \sum_{i=1}^{6}|c_i|^2 = 1 \text{)}
$$

Fazendo medidas de $\hat{R}$ em um ensemble de $N$ partículas no estado $|\Psi\rangle$ acima você terá (no limite $N\to\infty$)

$$
\begin{cases}
N|c_1|^2 \text{ resultados } \omega_1 \\
N|c_2|^2 \text{ \quad ''\ \ } \omega_2 \\
\quad \vdots \\
N|c_6|^2 \text{ \quad ''\ \ } \omega_6
\end{cases}
$$

onde $N|c_i|^2$ é o número de ocorrências do resultado $\omega_i$.

A média dos $N$ resultados é

$$
\frac{1}{N}\sum_i \underbrace{N|c_i|^2}_{\text{\# ocorrências}} \omega_i = \sum_i |c_i|^2 \omega_i
$$

Não podemos prever o resultado de uma medida em particular, mas podemos prever a **MÉDIA** dos $N$ resultados (no limite $N\to\infty$).

*(gráfico: distribuição dos resultados $\omega$ ao longo dos elementos do ensemble)*

## Valor esperado ou valor médio (espectro discreto)

A média dos resultados experimentais pode ser prevista:

$$
\begin{aligned}
\langle R \rangle &= \sum_i \underbrace{P(\omega_i)}_{\text{probabilidade}} \underbrace{\omega_i}_{\text{resultado}} \\
&= \sum_i \langle \Psi|\hat{P}_{\omega_i}|\Psi\rangle\, \omega_i \qquad \text{(supondo } \langle\Psi|\Psi\rangle=1 \text{, usando expressão de } \hat{P}_{\omega_i}\text{)} \\
&= \sum_i \sum_\alpha |\langle\Psi|\omega_i,\alpha\rangle|^2\, \omega_i \qquad (\alpha \to \text{autovalor})
\end{aligned}
$$

Lembrando que $\hat{R}|\omega_i,\alpha\rangle = \omega_i|\omega_i,\alpha\rangle$,

$$
\langle R \rangle = \sum_i \sum_\alpha \langle \Psi|\hat{R}|\omega_i,\alpha\rangle\langle\omega_i,\alpha|\Psi\rangle \qquad \left(\text{usando } \sum_{i,\alpha} |\omega_i,\alpha\rangle\langle\omega_i,\alpha| = \hat{\mathbb{1}}\right)
$$

$$
\boxed{\langle R \rangle = \langle \Psi|\hat{R}|\Psi\rangle}
$$

A primeira expressão é conveniente quando $|\Psi\rangle$ já está expresso na base de autovetores de $\hat{R}$, e a expressão em caixa nos demais casos (quando $|\Psi\rangle$ é conhecido em uma base genérica do EV).

**Ex:** $|\Psi\rangle = \dfrac{1}{\sqrt{2}}|\omega_1\rangle + \dfrac{1}{2}|\omega_2\rangle + \dfrac{1}{2}|\omega_3\rangle$ (normalizado)

$$
\langle R \rangle = \frac{1}{2}\omega_1 + \frac{1}{4}\omega_2 + \frac{1}{4}\omega_3
$$

Se (em um EV de dimensão 3, com $|1\rangle, |2\rangle, |3\rangle$ como base):

$$
|\Psi\rangle = \frac{1}{\sqrt{2}}|1\rangle + \frac{1}{\sqrt{2}}|2\rangle \qquad \text{(normalizado)}
$$

**Obs:** O EV da MQ é de dimensão infinita, quase nunca escreveremos operadores como matriz. No caso 1D teremos

$$
\langle \Psi|\hat{R}|\Psi\rangle = \int_{-\infty}^{\infty}\int_{-\infty}^{\infty} dx\, dx' \; \langle\Psi|x\rangle\langle x|\hat{R}|x'\rangle\langle x'|\Psi\rangle
$$

e

$$
\hat{R} \leftrightarrow
\begin{pmatrix}
1 & 0 & 1 \\
0 & 1 & 0 \\
1 & 0 & 2
\end{pmatrix}
\qquad \text{(Hermitiana)}
$$

$$
\langle \Psi|\hat{R}|\Psi\rangle = \sum_{i=1}^{3}\sum_{j=1}^{3} \langle\Psi|i\rangle\langle i|\hat{R}|j\rangle\langle j|\Psi\rangle
$$

em forma matricial:

$$
\begin{pmatrix} \psi_1^* & \psi_2^* & \psi_3^* \end{pmatrix}
\begin{pmatrix} \hat{R} \end{pmatrix}
\begin{pmatrix} \psi_1 \\ \psi_2 \\ \psi_3 \end{pmatrix}
$$

$$
= \begin{pmatrix} \dfrac{1}{\sqrt{2}} & \dfrac{1}{\sqrt{2}} & 0 \end{pmatrix}
\begin{pmatrix} 1 & 0 & 1 \\ 0 & 1 & 0 \\ 1 & 0 & 2 \end{pmatrix}
\begin{pmatrix} 1/\sqrt{2} \\ 1/\sqrt{2} \\ 0 \end{pmatrix}
$$

$$
= \begin{pmatrix} 1/\sqrt{2} & 1/\sqrt{2} & 0 \end{pmatrix}
\begin{pmatrix} 1/\sqrt{2} \\ 1/\sqrt{2} \\ 1/\sqrt{2} \end{pmatrix}
= \frac{1}{2} + \frac{1}{2} + 0 = \boxed{1}
$$

## Variância (desvio padrão) ou incerteza (espectro discreto)

A distribuição dos resultados em torno da média pode também ser prevista:

$$
\Delta R = \sqrt{\langle (\hat{R} - \langle R \rangle)^2 \rangle}
$$

O termo que está sendo promediado é o quadrado da diferença entre o resultado da medida $R$ e o valor médio $\langle R \rangle$.

**Exemplo.** Na turma as notas foram $\{5, 10, 8, 7, 8\}$.

Qual a nota média?

$$
\frac{1}{5}(5+10+8+7+8) = \boxed{7{,}6} = \langle N \rangle
$$

Qual o desvio padrão (ao quadrado)?

$$
\begin{aligned}
&\frac{1}{5}\Big[(5-7{,}6)^2 + (10-7{,}6)^2 + (8-7{,}6)^2 + (7-7{,}6)^2 + (8-7{,}6)^2\Big] \\
&= \boxed{2{,}64} = (\Delta N)^2
\end{aligned}
$$

$$
(\Delta N)^2 = \frac{1}{N}\sum_{i=1}^{N}(N_i - \langle N \rangle)^2 = \frac{1}{N}\sum_{i=1}^{N}\left(N_i^2 - 2N_i\langle N \rangle + \langle N \rangle^2\right) = \langle N^2 \rangle - \langle N \rangle^2
$$

onde $\langle N^2 \rangle = \dfrac{1}{N}\sum_i N_i^2$ e $\langle N \rangle = \dfrac{1}{N}\sum_i N_i$.

No nosso caso:

$$
\langle N^2 \rangle = \frac{1}{5}\left(5^2+10^2+8^2+7^2+8^2\right) = 60{,}4
$$

$$
\langle N \rangle^2 = 57{,}76 \qquad \left(\Rightarrow (\Delta N)^2 = 60{,}4 - 57{,}76 = 2{,}64\right)
$$

$\Delta N = \sqrt{2{,}64} = 1{,}6$ informa a faixa **EM TORNO DA MÉDIA** onde as notas se distribuem.

*(gráfico: notas dos alunos distribuídas em torno de $\langle N \rangle$, com faixa $\Delta N$ indicada)*

Assim,

$$
\boxed{(\Delta R)^2 = \langle R^2 \rangle - \langle R \rangle^2}
$$

onde $\langle R^2 \rangle = \langle \Psi|\hat{R}^2|\Psi\rangle$ e $\langle R \rangle = \langle \Psi|\hat{R}|\Psi\rangle$ (supondo $\langle\Psi|\Psi\rangle=1$).

**Exemplo.**

$$
|\Psi\rangle = \frac{1}{\sqrt{2}}|\omega{=}1\rangle + \frac{1}{2}|\omega{=}{-}1\rangle + \frac{1}{2}|\omega{=}2\rangle \qquad \text{(normalizado)}
$$

$$
\langle R \rangle = \frac{1}{2}(1) + \frac{1}{4}(-1) + \frac{1}{4}(2) = \frac{3}{4} = \boxed{0{,}75}
$$

$$
\langle R^2 \rangle = \frac{1}{2}(1)^2 + \frac{1}{4}(-1)^2 + \frac{1}{4}(2)^2 = \frac{7}{4} = \boxed{1{,}75}
$$

$$
\Delta R = \sqrt{1{,}75 - 0{,}75^2} = \boxed{1{,}09}
$$

Assim como no cálculo de $\langle R \rangle$, é conveniente ter $|\Psi\rangle$ expresso em termos dos autovetores de $\hat{R}$:

$$
\begin{aligned}
\langle R^2 \rangle &= \sum_{i,\alpha} \langle \Psi|\hat{R}^2|\omega_i,\alpha\rangle\langle\omega_i,\alpha|\Psi\rangle \\
&= \sum_{i,\alpha} \omega_i^2 \langle\Psi|\omega_i,\alpha\rangle\langle\omega_i,\alpha|\Psi\rangle \\
&= \sum_{i,\alpha} \omega_i^2 \,\big|\langle\Psi|\omega_i,\alpha\rangle\big|^2 \qquad \text{(coeficiente da expansão ao quadrado)}
\end{aligned}
$$

onde usei que $|\omega_i,\alpha\rangle$ é autovetor de **QUALQUER POTÊNCIA** do operador $\hat{R}$.

**Obs.** A incerteza é nula, $\Delta R = 0$, quando $|\Psi\rangle$ é uma combinação linear de autovetores de $\hat{R}$ de **MESMO AUTOVALOR**. Nesse caso $\hat{R}|\Psi\rangle = \omega|\Psi\rangle$ e $\hat{R}^2|\Psi\rangle = \omega^2|\Psi\rangle$.

Isso faz com que $\langle \Psi|\hat{R}|\Psi\rangle = \omega$ e $\langle \Psi|\hat{R}^2|\Psi\rangle = \omega^2$

$$
\Delta R^2 = \omega^2 - \omega^2 = 0
$$

**TODAS AS MEDIDAS PRODUZEM $\omega$ COMO RESULTADO!**

| EXPERIMENTO | CÁLCULO |
|---|---|
| $\dfrac{1}{N}(\omega_1+\omega_2+\cdots+\omega_N) \;(=\overline{\omega})$ | $\langle \Psi|\hat{R}|\Psi\rangle$ |
| $\dfrac{1}{N}\left[(\omega_1-\overline{\omega})^2+(\omega_2-\overline{\omega})^2+\cdots+(\omega_N-\overline{\omega})^2\right]$ $(=\Delta\omega^2)$ | $\langle \Psi|\hat{R}^2|\Psi\rangle - \langle \Psi|\hat{R}|\Psi\rangle^2$ |

> **VERIFIQUE SEMPRE** se seu cálculo de $\langle R \rangle$ é um valor entre o maior e o menor autovalor presente em $|\Psi\rangle$. (Mas, em geral, $\langle R \rangle$ **NÃO** é um dos autovalores!)

## Variáveis compatíveis e incompatíveis

Duas variáveis são **COMPATÍVEIS** quando seus operadores comutam. Nesse caso existem autovetores comuns a ambos operadores.

A medida em sequência de operadores compatíveis é a maneira de se preparar um estado quântico bem definido (ver a observação do início da aula).

Suponha que medimos $\hat{R}$ em um estado desconhecido e obtivemos $\omega_2$, um autovalor degenerado.

$$
|?\rangle \xrightarrow{\;\hat{R}\;} |\omega_2\rangle
$$

O estado $|\omega_2\rangle$ não é definido, sabemos apenas que ele está no subespaço do autovalor $\omega_2$.

Outra medida de $\hat{R}$ não adianta, pois o estado já é um autovetor de $\hat{R}$ e não será alterado pela medida (postulado III).

*(diagrama: vetores $|\omega_1\rangle=|\lambda_1\rangle$, $|\omega_2,1\rangle$, $|\omega_2,2\rangle$, $|\lambda_2\rangle$, $|\lambda_3\rangle$)*

Se $\hat{A}$ e $\hat{R}$ comutam, seus autovetores são comuns. Na figura os autovetores de $\hat{A}$ são não degenerados.

Note que

$$
\hat{R}|\lambda_1\rangle = \omega_1|\lambda_1\rangle, \qquad \hat{R}|\lambda_2\rangle = \omega_2|\lambda_2\rangle, \qquad \hat{R}|\lambda_3\rangle = \omega_2|\lambda_3\rangle
$$

($|\lambda_2\rangle$ e $|\lambda_3\rangle$ estão no subespaço $\omega_2$).

Uma medida de $\hat{A}$ no estado indeterminado $|\omega_2\rangle$ vai produzir $|\lambda_2\rangle$ ou $|\lambda_3\rangle$, um estado determinado.

$$
|\omega_2\rangle \xrightarrow{\;\hat{A}\;}
\begin{cases}
|\omega_2,\lambda_2\rangle \\
|\omega_2,\lambda_3\rangle
\end{cases}
$$

> **Um CONJUNTO COMPLETO DE OBSERVÁVEIS QUE COMUTAM** é um conjunto de operadores que comutam (portanto com autovetores comuns) e que especificam **UNICAMENTE** um estado com a informação dos autovalores.
>
> Um único operador com autovalores **NÃO degenerados** tem essa propriedade.
>
> Dois operadores com autovalores **degenerados** têm essa propriedade se, dentro do subespaço degenerado de $\hat{R}$, os autovalores de $\hat{A}$ são **DISTINTOS**.

$$
\boxed{\text{Se } |\omega,\lambda\rangle \text{ é estado único} \;\Leftrightarrow\; \hat{R} \text{ e } \hat{A} \text{ são C.C.O.C.}}
$$

## Sequência de medidas

**(i)** $[\hat{R}, \hat{A}] = 0$

$$
|\Psi\rangle \xrightarrow{\;\hat{R}\;} |\omega_1\rangle \xrightarrow{\;\hat{A}\;} |\lambda_1\rangle = |\omega_1,\lambda_1\rangle
$$

*(diagrama: vetores $|\omega_1\rangle=|\lambda_1\rangle$, $|\omega_2\rangle=|\lambda_2\rangle$, $|\omega_3\rangle=|\lambda_3\rangle$)*

O estado $|\lambda_1\rangle$ é um autoestado de $\hat{A}$ **DENTRO DO** subespaço do autovalor $\omega_1$, portanto qualquer medida de $\hat{R}$ ou $\hat{A}$ após essas 2 medidas irá dar sempre $\omega_1$ ou $\lambda_1$.

**(ii)** $[\hat{R}, \hat{A}] \neq 0$ (não há autovetores comuns)

*(diagrama: vetores $|\omega_3\rangle$, $|\omega_2\rangle$, $|\omega_1\rangle$, $|\lambda_2\rangle$, $|\lambda_1\rangle$)*

$$
|\Psi\rangle \xrightarrow{\;\hat{R}\;} |\omega_1\rangle \xrightarrow{\;\hat{A}\;} |\lambda_2\rangle
$$

O vetor $|\lambda_2\rangle$ **NÃO É AUTOVETOR** de $\hat{R}$, medida de $\hat{R}$ nesse estado pode dar qualquer resultado $\{\omega_1, \omega_2, \omega_3\}$.

O caso clássico de variáveis que não comutam é o dos operadores posição $\hat{X}$ e momentum $\hat{P} = \hbar\hat{K}$

$$
[\hat{X}, \hat{P}] = i\hbar
$$

Não há autovetores simultâneos, não existe um estado quântico que produza uma posição bem definida (seja autovetor de $\hat{X}$) **E** um momentum bem definido (seja autovetor de $\hat{P}$).

**Obs:** Mesmo quando 2 operadores **NÃO COMUTAM**, $[\hat{R},\hat{A}] = \hat{\Sigma}$, onde $\hat{\Sigma}$ é um operador não nulo, ainda podemos encontrar um **NÚMERO LIMITADO** de autovetores comuns de $\hat{R}$ e $\hat{A}$. Isso pode acontecer caso o operador $\hat{\Sigma}$ tenha autovalores nulos. Suponha que $|\omega\lambda\rangle$, um autovetor comum, exista

$$
\begin{aligned}
\hat{R}\hat{A}|\omega\lambda\rangle &= \hat{R}\,\lambda|\omega\lambda\rangle = \lambda\omega|\omega\lambda\rangle \\
\hat{A}\hat{R}|\omega\lambda\rangle &= \hat{A}\,\omega|\omega\lambda\rangle = \lambda\omega|\omega\lambda\rangle
\end{aligned}
$$

subtraindo,

$$
[\hat{R},\hat{A}]|\omega\lambda\rangle = 0 \;\Rightarrow\; \hat{\Sigma}|\omega\lambda\rangle = 0
$$

O autovetor comum é autovetor de $\hat{\Sigma}$ com autovalor nulo! No caso $[\hat{X},\hat{P}] = i\hbar$ isso não ocorre, pois $(i\hbar)\hat{\mathbb{1}} = \hat{\Sigma}$ não tem autovalor nulo.

## Valores médios de operadores de espectro contínuo

**Exemplo 4.2.4** — Seja uma partícula no estado

$$
|\Psi\rangle = \int_{-\infty}^{\infty} dx \, |x\rangle\langle x|\Psi\rangle
$$

onde a função de onda $\langle x|\Psi\rangle = \Psi(x) = A \exp\left[-(x-a)^2/2\Delta^2\right]$ (essa função se chama **Gaussiana**).

*(gráfico: $\Psi(x)$ centrada em $a$, com largura $\Delta$)*

**Normalizando** $|\Psi\rangle$ (trata-se de um vetor próprio):

$$
\begin{aligned}
\langle\Psi|\Psi\rangle &= \int_{-\infty}^{\infty} dx \, \langle\Psi|x\rangle\langle x|\Psi\rangle = 1 \\
&= A^2 \int_{-\infty}^{\infty} dx\, e^{-(x-a)^2/\Delta^2} = A^2\sqrt{\pi\Delta^2} \;\Rightarrow\; \boxed{A = \frac{1}{(\pi\Delta^2)^{1/4}}}
\end{aligned}
$$

> **Integral de Gaussiana:**
>
> $$
> \int_{-\infty}^{\infty} e^{-\alpha x^2}\, dx = \sqrt{\frac{\pi}{\alpha}}
> $$

A função de onda normalizada é

$$
\Psi(x) = \frac{1}{(\pi\Delta^2)^{1/4}}\, e^{-(x-a)^2/2\Delta^2}
$$

A probabilidade de encontrar a partícula entre $[x_1,x_2]$:

$$
P([x_1,x_2]) = \int_{x_1}^{x_2} dx \, |\langle x|\Psi\rangle|^2 = \int_{x_1}^{x_2} \frac{1}{\sqrt{\pi\Delta^2}}\, e^{-(x-a)^2/\Delta^2}\, dx
$$

(projetor da medida: $\displaystyle \hat{P}([x_1,x_2]) = \int_{x_1}^{x_2} dx\, |x\rangle\langle x|$)

**\*** Aqui estou imaginando que a "largura natural do aparelho de medida" é infinitesimal.

Uma série de medidas de posição nesse estado tem como média dos resultados experimentais:

$$
\langle X \rangle = \langle \Psi|\hat{X}|\Psi\rangle = \int_{-\infty}^{\infty} dx \, \underbrace{\langle\Psi|x\rangle}_{\Psi^*(x)}\underbrace{\langle x|\hat{X}|\Psi\rangle}_{x\,\Psi(x)}
$$

$$
= \int_{-\infty}^{\infty} dx\; \underbrace{x}_{\text{resultado}}\, \underbrace{|\Psi(x)|^2}_{\text{dens. prob.}}
$$

**Obs:** Essa é a versão contínua de $\displaystyle\sum_i \omega_i P(\omega_i) = \langle R \rangle$.

$$
= \int_{-\infty}^{\infty} dx\; x\, \frac{1}{\sqrt{\pi\Delta^2}}\, e^{-(x-a)^2/\Delta^2}
= \int_{-\infty}^{\infty} dy\; (y+a)\, \frac{1}{\sqrt{\pi\Delta^2}}\, e^{-y^2/\Delta^2} = a \qquad (y = x-a)
$$

$$
\boxed{\langle X \rangle = a} \qquad \text{(dimensão de comprimento)}
$$

O desvio padrão em torno desse valor médio é dado por

$$
\Delta X = \sqrt{\langle X^2 \rangle - \langle X \rangle^2} = \sqrt{\langle X^2 \rangle - a^2}
$$

$$
\langle X^2 \rangle = \langle \Psi|\hat{X}\hat{X}|\Psi\rangle = \int_{-\infty}^{\infty} dx\; \underbrace{\langle\Psi|x\rangle}_{\Psi^*(x)}\underbrace{\langle x|\hat{X}\hat{X}|\Psi\rangle}_{x^2\Psi(x)}
$$

$$
= \int_{-\infty}^{\infty} dx\; x^2\, \frac{1}{\sqrt{\pi\Delta^2}}\, e^{-(x-a)^2/\Delta^2}
= \int_{-\infty}^{\infty} dy\; (y^2+2ya+a^2)\, \frac{e^{-y^2/\Delta^2}}{\sqrt{\pi\Delta^2}} \qquad (y=x-a)
$$

$$
= \Delta^2/2 + a^2 \qquad \text{(dimensão de } [L]^2 \text{)}
$$

> **Integral de Gaussianas e potências:**
>
> $$
> \begin{aligned}
> \int_{-\infty}^{\infty} dx\; x\, e^{-\alpha x^2} &= 0 \qquad \text{(pois o integrando é ímpar)} \\
> \int_{-\infty}^{\infty} dx\; x^2\, e^{-\alpha x^2} &= -\frac{d}{d\alpha}\left[\int_{-\infty}^{\infty} dx\, e^{-\alpha x^2}\right] = -\frac{d}{d\alpha}\left(\sqrt{\frac{\pi}{\alpha}}\right) = \frac{\sqrt{\pi}}{2\alpha^{3/2}} \\
> \int_{-\infty}^{\infty} dx\; x^4\, e^{-\alpha x^2} &= \frac{d^2}{d\alpha^2}\left[\int_{-\infty}^{\infty} dx\, e^{-\alpha x^2}\right] = \frac{3}{4}\frac{\sqrt{\pi}}{\alpha^{5/2}}, \quad \text{etc.}
> \end{aligned}
> $$

Portanto $\boxed{\Delta X = \dfrac{\Delta}{\sqrt{2}}}$ (dimensão de $[L]$).

Uma série de medidas de momentum nesse estado tem como média dos resultados experimentais:

$$
\langle P \rangle = \langle \Psi|\hat{P}|\Psi\rangle = \int_{-\infty}^{\infty} dx\; \underbrace{\langle\Psi|x\rangle}_{\Psi^*(x)}\underbrace{\langle x|\hat{P}|\Psi\rangle}_{-i\hbar \frac{d\Psi}{dx}}
$$

$$
= -i\hbar \int_{-\infty}^{\infty} dx\; \Psi(x)\frac{d\Psi}{dx} = -\frac{i\hbar}{2}\int_{-\infty}^{\infty} \frac{d}{dx}\left[\Psi^2(x)\right] dx
$$

$$
= -\frac{i\hbar}{2}\Big[\Psi^2(\infty) - \Psi^2(-\infty)\Big] = 0 \qquad (\Rightarrow \text{ ver Ex. 4.2.2})
$$

Para calcular o desvio padrão dos resultados:

$$
\langle P^2 \rangle = \int_{-\infty}^{\infty} dx\; \underbrace{\langle\Psi|x\rangle}_{\Psi^*(x)}\underbrace{\langle x|\hat{P}\hat{P}|\Psi\rangle}_{-\hbar^2 \frac{d^2}{dx^2}\Psi(x)} = \frac{\hbar^2}{2\Delta^2} \qquad \text{(dimensão } [\text{momento}]^2 \text{)}
$$

(faça a conta, é importante praticar com essas integrais Gaussianas!)

Portanto $\boxed{\Delta P = \dfrac{\hbar}{\sqrt{2}\,\Delta}}$ (dimensão momentum).

**Obs:** A dimensão de $\Delta X$ deve ser **DISTÂNCIA** e a dimensão de $\Delta P$ deve ser **MOMENTUM**!

A amplitude de probabilidade associada à medida de $P$ é (isso é a "função de onda na representação $p$")

$$
\langle p|\Psi\rangle = \int_{-\infty}^{\infty} dx\; \underbrace{\langle p|x\rangle}_{\Psi_p^*(x)}\underbrace{\langle x|\Psi\rangle}_{\Psi(x)}
$$

Quem é $\Psi_p(x) = \langle x|p\rangle$, a autofunção do operador $\hat{P}$?

$$
\hat{P}|p\rangle = p|p\rangle \quad (\text{\# real}) \;\Rightarrow\; \langle x|\hat{P}|p\rangle = p\langle x|p\rangle
$$

Como em geral acontece, a equação de autovetores vira uma EDO.

$$
-i\hbar \frac{d\Psi_p}{dx} = p\,\Psi_p(x) \;\Rightarrow\; \Psi_p(x) = A\, e^{ipx/\hbar}
$$

Claramente é um vetor impróprio, como o $|k\rangle$ da seção 1.10. Escolhemos $A = \dfrac{1}{\sqrt{2\pi\hbar}}$ para obter a normalização de delta de Dirac.

$$
\langle p|p'\rangle = \int_{-\infty}^{\infty} dx\, \Psi_p^*(x)\Psi_{p'}(x) = A^2\int_{-\infty}^{\infty} dx\, e^{i(p'-p)x/\hbar} = 2\pi\,\delta\!\left(\frac{p'-p}{\hbar}\right) = \delta(p-p')
$$

Usando $\delta\!\left(\dfrac{p-p'}{\hbar}\right) = \hbar\,\delta(p-p')$ (lembre do Exercício 1.10.1)

$$
\Rightarrow \boxed{A^2 = \frac{1}{2\pi\hbar}}
$$

$$
\langle x|p\rangle = \frac{1}{\sqrt{2\pi\hbar}}\, e^{ipx/\hbar}
$$

é uma função de onda (imprópria) de momentum bem definido (igual a $p$).

$$
\langle x|a\rangle = \delta(x-a)
$$

é uma função de onda (imprópria) de posição bem definida (igual a $a$).

## Finalmente

$$
\langle p|\Psi\rangle = \int_{-\infty}^{\infty} dx\; \frac{1}{\sqrt{2\pi\hbar}}\, e^{-ipx/\hbar}\; \frac{1}{(\pi\Delta^2)^{1/4}}\, e^{-(x-a)^2/2\Delta^2}
$$

$$
= \left(\frac{\Delta^2}{\pi\hbar^2}\right)^{1/4} e^{-ipa/\hbar}\, e^{-p^2\Delta^2/2\hbar^2}
$$

$$
|\langle p|\Psi\rangle|^2 = \left(\frac{\Delta^2}{\pi\hbar^2}\right)^{1/2} e^{-p^2\Delta^2/\hbar^2}
$$

*(gráfico: $|\Psi(p)|^2$, uma Gaussiana centrada em $p=0$, de largura $\hbar/\Delta$)*

Trata-se de uma Gaussiana (como $|\Psi(x)|^2$) centrada em $p=0$, de largura $\dfrac{\hbar}{\Delta}$.

## Transformada de Fourier de Gaussianas

$$
\int_{-\infty}^{\infty} dx\; e^{-ikx}\, e^{-\alpha x^2} = \int_{-\infty}^{\infty} e^{-\alpha\left(x+\frac{ik}{2\alpha}\right)^2}\, e^{-k^2/4\alpha}\, dx
$$

Esse procedimento, que se aplica quando você tem $\int e^{f(x)}\,dx$ e $f(x)$ é uma função **QUADRÁTICA** de $x$, se chama "completar os quadrados".

$$
= \sqrt{\frac{\pi}{\alpha}}\; e^{-k^2/4\alpha}
$$

onde se usou que $\displaystyle\int_{-\infty}^{\infty} e^{-\alpha(x+x_0)^2}\,dx = \sqrt{\frac{\pi}{\alpha}}$ (mesmo que $x_0$ seja complexo!).

**TESTE DIMENSIONAL:** A integral acima deve ter dimensão $[x]$. Do argumento das exponenciais, $k = [x]^{-1}$ e $\alpha = [x]^{-2}$. No argumento da exponencial final temos

$$
\frac{k^2}{\alpha} = \frac{[x]^{-2}}{[x]^{-2}} = 1 \qquad \text{OK}
$$

Na frente da exponencial temos

$$
\frac{1}{\sqrt{\alpha}} = \frac{1}{[x]^{-1}} = [x] \qquad \text{OK}
$$

> Cheque **SEMPRE** se $\langle R \rangle$ e $\Delta R$ têm dimensão de $[R]$ e se $\langle R^2 \rangle$ tem dimensão de $[R]^2$ (e se são **REAIS**).
>
> **ERRO DIMENSIONAL NA PROVA SERÁ PUNIDO COM MORTE LENTA E DOLOROSA!**
