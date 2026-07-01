# (4ª aula) — Produto de Operadores, Adjunto, Hermitianos, Unitários e Autovalores (seções 1.6–1.8)

## Produto de Operadores em Forma Matricial

O produto $\hat{A}\hat{B}$ corresponde ao produto das matrizes:

$$(\hat{A}\hat{B})_{ij} = \langle i|\hat{A}\hat{B}|j\rangle = \sum_k \langle i|\hat{A}|k\rangle\langle k|\hat{B}|j\rangle = \sum_k A_{ik} B_{kj}$$

(inserindo a relação de completeza $\sum_k |k\rangle\langle k| = \hat{I}$). A correspondência operador $\leftrightarrow$ matriz **preserva o produto**.

## Operador Adjunto (seção 1.7)

> O **OPERADOR ADJUNTO** $\hat{\Omega}^\dagger$ é definido por:
> $$\langle v|\hat{\Omega}^\dagger|w\rangle \equiv \langle w|\hat{\Omega}|v\rangle^*$$

O elemento de matriz do adjunto:

$$(\hat{\Omega}^\dagger)_{ij} = \Omega_{ji}^*$$

A **matriz do adjunto é a transposta conjugada** da matriz original.

Propriedades:

$$(\hat{A}+\hat{B})^\dagger = \hat{A}^\dagger + \hat{B}^\dagger \qquad (a\hat{A})^\dagger = a^*\hat{A}^\dagger$$

$$(\hat{A}\hat{B})^\dagger = \hat{B}^\dagger\hat{A}^\dagger \qquad (\hat{A}^\dagger)^\dagger = \hat{A}$$

## Operadores Hermitianos e Unitários (seção 1.8)

> **Operador Hermitiano** (auto-adjunto): $\hat{\Omega}^\dagger = \hat{\Omega}$
>
> Elementos de matriz: $\Omega_{ij} = \Omega_{ji}^*$ (igual à sua transposta conjugada).

> **Operador Unitário**: $\hat{U}^\dagger\hat{U} = \hat{U}\hat{U}^\dagger = \hat{I}$, i.e., $\hat{U}^{-1} = \hat{U}^\dagger$.

**Operador Anti-Hermitiano:** $\hat{\Omega}^\dagger = -\hat{\Omega}$. Qualquer operador se decompõe em parte Hermitiana e Anti-Hermitiana:

$$\hat{\Omega} = \frac{\hat{\Omega}+\hat{\Omega}^\dagger}{2} + \frac{\hat{\Omega}-\hat{\Omega}^\dagger}{2}$$

## Autovalores e Autovetores (seção 1.8)

> O **PROBLEMA DE AUTOVALORES** de $\hat{\Omega}$: encontrar $|\omega\rangle \neq |0\rangle$ e $\omega$ tais que
> $$\hat{\Omega}|\omega\rangle = \omega\,|\omega\rangle$$

Na MQ, grandezas físicas são representadas por operadores Hermitianos e os resultados de uma medição são os autovalores.

Para encontrar autovalores, usa-se a **equação característica**:

$$\det(\Omega - \omega I) = 0$$

equação de grau $n$ que fornece os $n$ autovalores (com possíveis repetições).

## Teoremas sobre Operadores Hermitianos

> **Teorema 1:** Os autovalores de um operador Hermitiano são **REAIS**.

*Prova:* De $\langle\omega|\hat{\Omega}|\omega\rangle = \omega\langle\omega|\omega\rangle$ e $\langle\omega|\hat{\Omega}^\dagger|\omega\rangle = \omega^*\langle\omega|\omega\rangle$, como $\hat{\Omega}=\hat{\Omega}^\dagger$ e $\langle\omega|\omega\rangle > 0$: $\omega = \omega^*$. $\square$

> **Teorema 2:** Autovetores com autovalores **DISTINTOS** são **ORTOGONAIS**.

*Prova:* De $\hat{\Omega}|\omega_1\rangle = \omega_1|\omega_1\rangle$ e $\hat{\Omega}|\omega_2\rangle = \omega_2|\omega_2\rangle$ com $\omega_1 \neq \omega_2$:

$$(\omega_2 - \omega_1)\langle\omega_1|\omega_2\rangle = 0 \implies \langle\omega_1|\omega_2\rangle = 0 \quad \square$$

## Autovalores Degenerados

Dizemos que $\omega$ é **degenerado** com degenerescência $m$ se existem $m$ autovetores LI com esse autovalor. Eles formam um **autoespaço** (subespaço) de dimensão $m$.

Dentro do autoespaço pode-se escolher $m$ autovetores ortonormais. Qualquer combinação linear de autovetores de $\omega$ ainda é autovetor de $\omega$.

## Teoremas sobre Operadores Unitários

> **Teorema 3:** Os autovalores de um operador Unitário têm $|\omega| = 1$, i.e., $\omega = e^{i\theta}$.

*Prova:* De $\hat{U}^\dagger\hat{U} = \hat{I}$ e $\hat{U}|\omega\rangle = \omega|\omega\rangle$: $\langle\omega|\omega\rangle = |\omega|^2\langle\omega|\omega\rangle \Rightarrow |\omega|^2 = 1$. $\square$

> **Teorema 4:** Autovetores de $\hat{U}$ com autovalores DISTINTOS são ORTOGONAIS.

## Exemplo: Operador com Autovalor Degenerado

$$\Omega = \begin{bmatrix} 2 & 1 & 0 \\ 1 & 2 & 0 \\ 0 & 0 & 3 \end{bmatrix}$$

**Equação característica:** $(3-\omega)[(2-\omega)^2-1] = 0 \Rightarrow \omega = 1,\ \omega = 3$ (mult. 2).

**Autovetor de $\omega = 1$:**

$$|\omega=1\rangle = \frac{1}{\sqrt{2}}(|1\rangle - |2\rangle)$$

**Autoespaço de $\omega = 3$** (dimensão 2):

$$|\omega=3, a=1\rangle = \frac{1}{\sqrt{2}}(|1\rangle + |2\rangle), \qquad |\omega=3, a=2\rangle = |3\rangle$$

Na base de autovetores, $\Omega$ é diagonal:

$$\Omega \leftrightarrow \begin{bmatrix} 1 & 0 & 0 \\ 0 & 3 & 0 \\ 0 & 0 & 3 \end{bmatrix}$$
