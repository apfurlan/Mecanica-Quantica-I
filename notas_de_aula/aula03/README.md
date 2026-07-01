# (3ª aula) — Subespaços, Operadores Lineares e Representação Matricial (seções 1.4–1.6)

## Subespaços (seção 1.4)

> Um **SUBESPAÇO** $S$ de um espaço vetorial $\mathbb{V}^n$ é um subconjunto $S \subset \mathbb{V}^n$ que também é um espaço vetorial com as mesmas operações de soma e multiplicação por escalar.

Para verificar se $S \subset \mathbb{V}^n$ é um subespaço, bastam **duas condições**:

1. $|v\rangle, |w\rangle \in S \Rightarrow |v\rangle + |w\rangle \in S$ (fechado sob adição)
2. $|v\rangle \in S,\ a \in \mathbb{C} \Rightarrow a|v\rangle \in S$ (fechado sob mult. por escalar)

> **Observação:** Com as condições 1 e 2, todas as demais propriedades de espaço vetorial seguem automaticamente (pois valem em $\mathbb{V}^n$). Em particular, com $a=0$ em 2: $|0\rangle \in S$, logo o subespaço sempre contém o vetor nulo.

**Exemplo:** No plano, setas ao longo de uma reta passando pela origem formam um subespaço $S$ de $\mathbb{V}^2$. Setas fora dessa reta não formam subespaço (não são fechadas sob adição).

**Exemplo:** O conjunto das matrizes $2\times2$ reais *simétricas*

$$S = \left\{ \begin{bmatrix} a & b \\ b & d \end{bmatrix} :\ a, b, d \in \mathbb{R} \right\}$$

é subespaço do espaço de todas as matrizes $2\times2$ reais, pois a soma de simétricas é simétrica e $\alpha \cdot$ simétrica é simétrica.

> O **SUBESPAÇO GERADO** por vetores $|v_1\rangle, \dots, |v_k\rangle$ (ou *span*) é o conjunto de todas as combinações lineares:
>
> $$\mathrm{span}\{|v_1\rangle, \dots, |v_k\rangle\} = \left\{ \sum_{i=1}^k a_i |v_i\rangle :\ a_i \in \mathbb{C} \right\}$$

## Operadores Lineares (seção 1.5)

> Um **OPERADOR LINEAR** $\hat{\Omega}$ é um mapeamento de $\mathbb{V}^n$ em $\mathbb{V}^n$
>
> $$\hat{\Omega}:\, \mathbb{V}^n \to \mathbb{V}^n, \qquad |v\rangle \mapsto \hat{\Omega}|v\rangle$$
>
> que satisfaz a linearidade:
>
> $$\hat{\Omega}\left(a|v\rangle + b|w\rangle\right) = a\,\hat{\Omega}|v\rangle + b\,\hat{\Omega}|w\rangle$$

O operador também atua na direita sobre bras: $(\langle v|\hat{\Omega})|w\rangle \equiv \langle v|(\hat{\Omega}|w\rangle)$.

**Exemplos:**
- **Operador de rotação** $\hat{R}(\theta, \hat{z})$: rotaciona setas no plano por ângulo $\theta$. Operador linear.
- **Operador identidade** $\hat{I}$: $\hat{I}|v\rangle = |v\rangle$ para todo $|v\rangle$.
- **Operador nulo** $\hat{0}$: $\hat{0}|v\rangle = |0\rangle$ para todo $|v\rangle$.

## Produto de Operadores e Comutador

O **produto** $\hat{A}\hat{B}$ é definido pela composição:

$$(\hat{A}\hat{B})|v\rangle = \hat{A}\!\left(\hat{B}|v\rangle\right)$$

> **ATENÇÃO:** Em geral $\hat{A}\hat{B} \neq \hat{B}\hat{A}$. O produto de operadores **NÃO é comutativo**.

> O **COMUTADOR** de dois operadores é:
>
> $$[\hat{A},\, \hat{B}] \equiv \hat{A}\hat{B} - \hat{B}\hat{A}$$
>
> Se $[\hat{A}, \hat{B}] = 0$, dizemos que $\hat{A}$ e $\hat{B}$ **comutam**.

Identidades úteis com comutadores:

$$[\hat{A}, \hat{B}] = -[\hat{B}, \hat{A}]$$

$$[\hat{A}, \hat{B} + \hat{C}] = [\hat{A}, \hat{B}] + [\hat{A}, \hat{C}]$$

$$[\hat{A}, \hat{B}\hat{C}] = [\hat{A}, \hat{B}]\hat{C} + \hat{B}[\hat{A}, \hat{C}]$$

$$[\hat{A}\hat{B}, \hat{C}] = \hat{A}[\hat{B}, \hat{C}] + [\hat{A}, \hat{C}]\hat{B}$$

$$[\hat{A}, [\hat{B}, \hat{C}]] + [\hat{B}, [\hat{C}, \hat{A}]] + [\hat{C}, [\hat{A}, \hat{B}]] = 0 \quad \text{(Identidade de Jacobi)}$$

O **operador inverso** $\hat{\Omega}^{-1}$ satisfaz $\hat{\Omega}\hat{\Omega}^{-1} = \hat{\Omega}^{-1}\hat{\Omega} = \hat{I}$.

## Elementos de Matriz (seção 1.6)

Dado $\hat{\Omega}$ e uma base ortonormal $\{|i\rangle\}$, os **elementos de matriz** de $\hat{\Omega}$ são:

$$\Omega_{ij} \equiv \langle i|\hat{\Omega}|j\rangle$$

A ação de $\hat{\Omega}$ sobre $|V\rangle = \sum_j v_j|j\rangle$ em termos dos elementos de matriz:

$$\hat{\Omega}|V\rangle = \sum_{i,j} \Omega_{ij}\, v_j\,|i\rangle$$

a componente $i$ do vetor resultante é $\sum_j \Omega_{ij} v_j$, que é a regra do produto matricial. Portanto:

$$\hat{\Omega} \leftrightarrow \begin{bmatrix}
\Omega_{11} & \Omega_{12} & \cdots & \Omega_{1n} \\
\Omega_{21} & \Omega_{22} & \cdots & \Omega_{2n} \\
\vdots & \vdots & \ddots & \vdots \\
\Omega_{n1} & \Omega_{n2} & \cdots & \Omega_{nn}
\end{bmatrix}$$

## Borboletas (Produtos Externos)

O objeto $|v\rangle\langle w|$ é um **produto externo** (ou "borboleta"). Ele age como operador:

$$\left(|v\rangle\langle w|\right)|u\rangle = |v\rangle\underbrace{\langle w|u\rangle}_{\text{número}} = \langle w|u\rangle\,|v\rangle$$

Projeta $|u\rangle$ sobre $|w\rangle$ (extraindo um número complexo) e depois reescala $|v\rangle$.

O elemento de matriz $(ij)$ de $|v\rangle\langle w|$ na base $\{|i\rangle\}$:

$$\langle i|\!\left(|v\rangle\langle w|\right)\!|j\rangle = \langle i|v\rangle\langle w|j\rangle$$

Qualquer operador pode ser escrito em termos de borboletas usando os elementos de matriz:

$$\hat{\Omega} = \sum_{i,j} \Omega_{ij}\,|i\rangle\langle j|$$

## Projetores

> O **PROJETOR** sobre $|v\rangle$ (normalizado, $\langle v|v\rangle=1$) é:
>
> $$\hat{P}_v = |v\rangle\langle v|$$
>
> Ele extrai a componente de qualquer ket na direção $|v\rangle$:
>
> $$\hat{P}_v|u\rangle = |v\rangle\underbrace{\langle v|u\rangle}_{\text{componente}} = \langle v|u\rangle\,|v\rangle$$

**Propriedade fundamental — Idempotência:**

$$\hat{P}_v^2 = \hat{P}_v$$

*Prova:* $\hat{P}_v^2|u\rangle = \hat{P}_v\!\left(\langle v|u\rangle|v\rangle\right) = \langle v|u\rangle\underbrace{\langle v|v\rangle}_{=1}|v\rangle = \langle v|u\rangle\,|v\rangle = \hat{P}_v|u\rangle$. $\square$

**Relação de completeza** (resolução da identidade) em uma base ortonormal $\{|i\rangle\}$:

$$\sum_{i=1}^n |i\rangle\langle i| = \hat{I}$$

*Prova:* Para $|V\rangle = \sum_j v_j|j\rangle$:

$$\sum_i |i\rangle\langle i|\,|V\rangle = \sum_i |i\rangle\underbrace{\langle i|V\rangle}_{=\,v_i} = \sum_i v_i|i\rangle = |V\rangle \quad \square$$

> A relação de completeza é extremamente útil na notação de Dirac: podemos **inserir $\hat{I} = \sum_i |i\rangle\langle i|$** em qualquer produto sem alterar o resultado, uma técnica de uso frequente no cálculo com operadores e produtos internos.
