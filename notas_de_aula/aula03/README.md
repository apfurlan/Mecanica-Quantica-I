# (3ª aula) — Subespaços, Operadores Lineares e Representação Matricial (seções 1.4–1.6)

## Subespaços (seção 1.4)

> Um **SUBESPAÇO** $S$ de um espaço vetorial $\mathbb{V}^n$ é um subconjunto $S \subset \mathbb{V}^n$ que também é um espaço vetorial com as mesmas operações.

Para verificar se $S \subset \mathbb{V}^n$ é um subespaço, bastam **duas condições**:

1. $|v\rangle, |w\rangle \in S \Rightarrow |v\rangle + |w\rangle \in S$ (fechado sob adição)
2. $|v\rangle \in S,\ a \in \mathbb{C} \Rightarrow a|v\rangle \in S$ (fechado sob mult. escalar)

Com essas condições, o subespaço sempre contém o vetor nulo ($a=0$ em 2).

**Exemplos:** setas ao longo de uma reta na origem; matrizes simétricas $2\times2$.

> O **SUBESPAÇO GERADO** por $|v_1\rangle, \dots, |v_k\rangle$ é o conjunto de todas as combinações lineares:
> $$\mathrm{span}\{|v_1\rangle, \dots, |v_k\rangle\} = \left\{ \sum_{i=1}^k a_i |v_i\rangle \right\}$$

## Operadores Lineares (seção 1.5)

> Um **OPERADOR LINEAR** $\hat{\Omega}$ mapeia kets em kets de forma linear:
> $$\hat{\Omega}\left(a|v\rangle + b|w\rangle\right) = a\,\hat{\Omega}|v\rangle + b\,\hat{\Omega}|w\rangle$$

O operador também atua sobre bras pela direita: $(\langle v|\hat{\Omega})|w\rangle \equiv \langle v|(\hat{\Omega}|w\rangle)$.

**Exemplos:** operador de rotação $\hat{R}(\theta, \hat{z})$; operador identidade $\hat{I}$; operador nulo $\hat{0}$.

## Produto de Operadores e Comutador

O produto $\hat{A}\hat{B}$ é definido por composição: $(\hat{A}\hat{B})|v\rangle = \hat{A}(\hat{B}|v\rangle)$.

> **ATENÇÃO:** Em geral $\hat{A}\hat{B} \neq \hat{B}\hat{A}$. O produto de operadores **NÃO é comutativo**.

> O **COMUTADOR** de dois operadores é:
> $$[\hat{A},\hat{B}] \equiv \hat{A}\hat{B} - \hat{B}\hat{A}$$
> Se $[\hat{A},\hat{B}] = 0$, dizemos que $\hat{A}$ e $\hat{B}$ **comutam**.

Identidades úteis:

$$[\hat{A},\hat{B}] = -[\hat{B},\hat{A}]$$

$$[\hat{A}, \hat{B}\hat{C}] = [\hat{A},\hat{B}]\hat{C} + \hat{B}[\hat{A},\hat{C}]$$

$$[\hat{A},[\hat{B},\hat{C}]] + [\hat{B},[\hat{C},\hat{A}]] + [\hat{C},[\hat{A},\hat{B}]] = 0 \quad \text{(Jacobi)}$$

O **operador inverso** $\hat{\Omega}^{-1}$ satisfaz $\hat{\Omega}\hat{\Omega}^{-1} = \hat{\Omega}^{-1}\hat{\Omega} = \hat{I}$.

## Elementos de Matriz (seção 1.6)

Dado $\hat{\Omega}$ e base ortonormal $\{|i\rangle\}$, os **elementos de matriz** são:

$$\Omega_{ij} \equiv \langle i|\hat{\Omega}|j\rangle$$

A ação de $\hat{\Omega}$ sobre $|V\rangle = \sum_j v_j|j\rangle$:

$$\hat{\Omega}|V\rangle = \sum_{i,j} \Omega_{ij}\, v_j\,|i\rangle$$

que é a regra do produto matricial. O operador corresponde à matriz:

$$\hat{\Omega} \leftrightarrow \begin{bmatrix}
\Omega_{11} & \Omega_{12} & \cdots & \Omega_{1n} \\
\Omega_{21} & \Omega_{22} & \cdots & \Omega_{2n} \\
\vdots & \vdots & \ddots & \vdots \\
\Omega_{n1} & \Omega_{n2} & \cdots & \Omega_{nn}
\end{bmatrix}$$

## Borboletas (Produtos Externos)

O produto externo $|v\rangle\langle w|$ age como operador:

$$\left(|v\rangle\langle w|\right)|u\rangle = |v\rangle \underbrace{\langle w|u\rangle}_{\text{número}} = \langle w|u\rangle\,|v\rangle$$

Qualquer operador se escreve em termos de borboletas:

$$\hat{\Omega} = \sum_{i,j} \Omega_{ij}\,|i\rangle\langle j|$$

## Projetores

> O **PROJETOR** sobre $|v\rangle$ (normalizado) é: $\hat{P}_v = |v\rangle\langle v|$
>
> Ele extrai a componente de qualquer ket na direção $|v\rangle$:
> $$\hat{P}_v|u\rangle = |v\rangle\langle v|u\rangle = \langle v|u\rangle\,|v\rangle$$

**Idempotência:** $\hat{P}_v^2 = \hat{P}_v$ (consequência direta de $\langle v|v\rangle = 1$).

**Relação de completeza** em base ortonormal $\{|i\rangle\}$:

$$\sum_{i=1}^n |i\rangle\langle i| = \hat{I}$$

Essa identidade é extremamente útil: pode-se **inserir** $\hat{I} = \sum_i |i\rangle\langle i|$ em qualquer produto, sem alterar o resultado.
