# (4ª aula) — Produto de Operadores, Adjunto, Hermitianos, Unitários e Autovalores (seções 1.6–1.8)

## Produto de Operadores em Forma Matricial

Vimos que um operador $\hat{\Omega}$ corresponde à matriz com elementos $\Omega_{ij} = \langle i|\hat{\Omega}|j\rangle$.

O **produto** $\hat{A}\hat{B}$ corresponde ao produto das matrizes:

$$(\hat{A}\hat{B})_{ij} = \langle i|\hat{A}\hat{B}|j\rangle = \langle i|\hat{A}\underbrace{\left(\sum_k |k\rangle\langle k|\right)}_{\hat{I}}\hat{B}|j\rangle = \sum_k \underbrace{\langle i|\hat{A}|k\rangle}_{A_{ik}} \underbrace{\langle k|\hat{B}|j\rangle}_{B_{kj}} = \sum_k A_{ik}\, B_{kj}$$

que é exatamente a regra do **produto matricial**. A correspondência operador $\leftrightarrow$ matriz preserva o produto.

## Operador Adjunto (seção 1.7)

> O **OPERADOR ADJUNTO** $\hat{\Omega}^\dagger$ de $\hat{\Omega}$ é definido por:
>
> $$\langle v|\hat{\Omega}^\dagger|w\rangle \equiv \langle w|\hat{\Omega}|v\rangle^*$$
>
> para todos $|v\rangle, |w\rangle \in \mathbb{V}^n$.

O elemento de matriz $(ij)$ do adjunto é:

$$(\hat{\Omega}^\dagger)_{ij} = \langle i|\hat{\Omega}^\dagger|j\rangle = \langle j|\hat{\Omega}|i\rangle^* = \Omega_{ji}^*$$

A **matriz do adjunto é a transposta conjugada** da matriz original:

$$\hat{\Omega}^\dagger \leftrightarrow (\Omega^T)^* = \Omega^\dagger$$

Propriedades do adjunto:

$$(\hat{A} + \hat{B})^\dagger = \hat{A}^\dagger + \hat{B}^\dagger \qquad (a\hat{A})^\dagger = a^*\hat{A}^\dagger$$

$$(\hat{A}\hat{B})^\dagger = \hat{B}^\dagger\hat{A}^\dagger \qquad (\hat{A}^\dagger)^\dagger = \hat{A}$$

**Prova de $(\hat{A}\hat{B})^\dagger = \hat{B}^\dagger\hat{A}^\dagger$:** Seja $|z\rangle = \hat{B}|v\rangle$; então:

$$\langle v|(\hat{A}\hat{B})^\dagger|w\rangle = \left[\langle w|\hat{A}\hat{B}|v\rangle\right]^* = \left[\langle w|\hat{A}|z\rangle\right]^* = \langle z|\hat{A}^\dagger|w\rangle = \langle v|\hat{B}^\dagger\hat{A}^\dagger|w\rangle \quad \square$$

## Operadores Hermitianos e Unitários (seção 1.8)

> **Operador Hermitiano** (ou auto-adjunto): $\hat{\Omega}^\dagger = \hat{\Omega}$
>
> Elementos de matriz: $\Omega_{ij} = \Omega_{ji}^*$ (a matriz é igual à sua transposta conjugada).

**Exemplo:** $\Omega = \begin{bmatrix} 3 & 1+i \\ 1-i & 0 \end{bmatrix}$ é Hermitiana, pois $\Omega_{12} = 1+i = \Omega_{21}^*$.

> **Operador Unitário**: $\hat{U}^\dagger\hat{U} = \hat{U}\hat{U}^\dagger = \hat{I}$, equivalentemente $\hat{U}^{-1} = \hat{U}^\dagger$.

**Exemplo:** $U = \dfrac{1}{\sqrt{2}}\begin{bmatrix} 1 & 1 \\ 1 & -1 \end{bmatrix}$ é unitária:

$$U^\dagger U = \frac{1}{2}\begin{bmatrix} 1 & 1 \\ 1 & -1 \end{bmatrix}\begin{bmatrix} 1 & 1 \\ 1 & -1 \end{bmatrix} = \begin{bmatrix} 1 & 0 \\ 0 & 1 \end{bmatrix} = I \quad \checkmark$$

> **Operador Anti-Hermitiano:** $\hat{\Omega}^\dagger = -\hat{\Omega}$.
>
> Qualquer operador se decompõe em parte Hermitiana e Anti-Hermitiana:
>
> $$\hat{\Omega} = \underbrace{\frac{\hat{\Omega}+\hat{\Omega}^\dagger}{2}}_{\text{Hermitiana}} + \underbrace{\frac{\hat{\Omega}-\hat{\Omega}^\dagger}{2}}_{\text{Anti-Hermitiana}}$$

## Autovalores e Autovetores (seção 1.8)

> O **PROBLEMA DE AUTOVALORES** de um operador $\hat{\Omega}$: encontrar vetores $|\omega\rangle \neq |0\rangle$ e números $\omega$ tais que
>
> $$\hat{\Omega}|\omega\rangle = \omega\,|\omega\rangle$$
>
> Chamamos $\omega$ de **autovalor** e $|\omega\rangle$ de **autovetor** (ou autoestado) de $\hat{\Omega}$.

Na MQ, grandezas físicas são representadas por operadores Hermitianos e os resultados possíveis de uma medição são os autovalores desses operadores.

Reescrevendo $(\hat{\Omega} - \omega\hat{I})|\omega\rangle = |0\rangle$: para existir solução não trivial, o operador deve ser singular. Em forma matricial:

$$\det(\Omega - \omega\, I) = 0 \qquad \text{(equação característica)}$$

Essa equação de grau $n$ em $\omega$ fornece os $n$ autovalores (com possíveis repetições). Para cada $\omega_k$, o autovetor é encontrado resolvendo o sistema linear $(\Omega - \omega_k I)|\omega_k\rangle = 0$.

## Teoremas sobre Operadores Hermitianos

> **Teorema 1:** Os autovalores de um operador Hermitiano são **REAIS**.

*Prova:* Seja $\hat{\Omega}^\dagger = \hat{\Omega}$ e $\hat{\Omega}|\omega\rangle = \omega|\omega\rangle$. Calcula-se $\langle\omega|\hat{\Omega}|\omega\rangle$ de dois modos:

$$\langle\omega|\hat{\Omega}|\omega\rangle = \omega\langle\omega|\omega\rangle \qquad \langle\omega|\hat{\Omega}^\dagger|\omega\rangle = \left[\langle\omega|\hat{\Omega}|\omega\rangle\right]^* = \omega^*\langle\omega|\omega\rangle$$

Como $\hat{\Omega} = \hat{\Omega}^\dagger$, as expressões são iguais. Como $\langle\omega|\omega\rangle > 0$: $\omega = \omega^* \in \mathbb{R}$. $\square$

> **Teorema 2:** Autovetores de um operador Hermitiano associados a autovalores **DISTINTOS** são **ORTOGONAIS**.

*Prova:* Sejam $\omega_1 \neq \omega_2$ e $\hat{\Omega}|\omega_i\rangle = \omega_i|\omega_i\rangle$. Calculamos $\langle\omega_1|\hat{\Omega}|\omega_2\rangle$:

$$\langle\omega_1|\hat{\Omega}|\omega_2\rangle = \omega_2\langle\omega_1|\omega_2\rangle$$

$$\langle\omega_1|\hat{\Omega}^\dagger|\omega_2\rangle = \left[\langle\omega_2|\hat{\Omega}|\omega_1\rangle\right]^* = \omega_1\langle\omega_1|\omega_2\rangle \quad (\omega_1 \in \mathbb{R})$$

Como $\hat{\Omega} = \hat{\Omega}^\dagger$: $(\omega_2 - \omega_1)\langle\omega_1|\omega_2\rangle = 0$. Como $\omega_2 \neq \omega_1$: $\langle\omega_1|\omega_2\rangle = 0$. $\square$

## Autovalores Degenerados

Dizemos que $\omega$ é **degenerado** com **degenerescência** $m$ se existem $m$ autovetores LI com esse autovalor. Eles formam um subespaço de dimensão $m$, o **autoespaço** de $\omega$.

Dentro do autoespaço pode-se escolher $m$ autovetores ortonormais, e qualquer combinação linear deles é autovetor de $\omega$:

$$\hat{\Omega}\left(\sum_{a=1}^m c_a|\omega,a\rangle\right) = \omega\sum_{a=1}^m c_a|\omega,a\rangle$$

## Teoremas sobre Operadores Unitários

> **Teorema 3:** Os autovalores de um operador Unitário têm módulo 1: $|\omega| = 1$, isto é, $\omega = e^{i\theta}$ para algum $\theta \in \mathbb{R}$.

*Prova:* De $\hat{U}^\dagger\hat{U} = \hat{I}$ e $\hat{U}|\omega\rangle = \omega|\omega\rangle$:

$$\langle\omega|\omega\rangle = \langle\omega|\hat{U}^\dagger\hat{U}|\omega\rangle = |\omega|^2\langle\omega|\omega\rangle \quad \Longrightarrow \quad |\omega|^2 = 1 \quad \square$$

> **Teorema 4:** Autovetores de um operador Unitário com autovalores DISTINTOS são ORTOGONAIS.

A prova é análoga ao Teorema 2.

## Exemplo: Operador Hermitiano com Autovalor Degenerado

Considere, na base $|1\rangle, |2\rangle, |3\rangle$, o operador Hermitiano:

$$\Omega = \begin{bmatrix} 2 & 1 & 0 \\ 1 & 2 & 0 \\ 0 & 0 & 3 \end{bmatrix}$$

**Equação característica:**

$$(3-\omega)\bigl[(2-\omega)^2 - 1\bigr] = 0 \quad \Longrightarrow \quad \omega = 1,\quad \omega = 3\ \text{(degenerado, mult. 2)}$$

**Autovetor de $\omega = 1$:**

$$(\Omega - I)|\omega_1\rangle = 0 \quad \Longrightarrow \quad \begin{bmatrix} 1 & 1 & 0 \\ 1 & 1 & 0 \\ 0 & 0 & 2 \end{bmatrix} \begin{bmatrix} v_1 \\ v_2 \\ v_3 \end{bmatrix} = 0 \quad \Longrightarrow \quad v_3 = 0,\ v_1 = -v_2$$

$$|\omega=1\rangle = \frac{1}{\sqrt{2}}\bigl(|1\rangle - |2\rangle\bigr)$$

**Autoespaço de $\omega = 3$** (dimensão 2):

$$(\Omega - 3I)|\omega_3\rangle = 0 \quad \Longrightarrow \quad \begin{bmatrix} -1 & 1 & 0 \\ 1 & -1 & 0 \\ 0 & 0 & 0 \end{bmatrix} \begin{bmatrix} v_1 \\ v_2 \\ v_3 \end{bmatrix} = 0 \quad \Longrightarrow \quad v_1 = v_2,\ v_3\ \text{livre}$$

Escolhe-se dois autovetores ortonormais dentro do autoespaço:

$$|\omega=3, a=1\rangle = \frac{1}{\sqrt{2}}\bigl(|1\rangle+|2\rangle\bigr), \qquad |\omega=3, a=2\rangle = |3\rangle$$

A base ortonormal de autovetores é $\left\{\dfrac{1}{\sqrt{2}}(|1\rangle-|2\rangle),\ \dfrac{1}{\sqrt{2}}(|1\rangle+|2\rangle),\ |3\rangle\right\}$, e nessa base $\Omega$ é diagonal:

$$\Omega \leftrightarrow \begin{bmatrix} 1 & 0 & 0 \\ 0 & 3 & 0 \\ 0 & 0 & 3 \end{bmatrix}$$
