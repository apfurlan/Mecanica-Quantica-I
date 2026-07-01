# (2ª aula) Espaços Vetoriais (seções 1.1–1.3)

A ferramenta matemática essencial da Mecânica Clássica é a Teoria de Equações Diferenciais Ordinárias. Na Mecânica Quântica (MQ) temos a **Álgebra Linear** e a **Teoria das Equações Diferenciais Parciais** como ferramentas fundamentais. Nosso curso começa com uma revisão de **Álgebra Linear**.

Por que Álgebra Linear? Como veremos nos postulados da MQ, o estado de uma partícula é representado não por uma função vetorial $\mathbf{r}(t)$ (como na Mecânica Clássica), mas como um elemento de um espaço vetorial, denotado pelo símbolo $|\psi(t)\rangle$. Esqueça a Física por enquanto e concentre-se em entender as propriedades dos **ESPAÇOS VETORIAIS**.

## Espaço Vetorial (seção 1.1)

> Um **ESPAÇO VETORIAL** $V$ é uma coleção de objetos chamados **VETORES** $|v_1\rangle, |v_2\rangle, |v_3\rangle, \dots$ com duas operações definidas:
>
> $$\text{Soma: } |u\rangle + |v\rangle \in V \qquad \text{Multiplicação por escalar: } a|v\rangle \in V$$

O escalar pode ser real (EV real) ou complexo (EV complexo). As propriedades que a soma e a multiplicação por escalar devem satisfazer são:

1. $a(|u\rangle + |w\rangle) = a|u\rangle + a|w\rangle$ (distributiva)
2. $(a + b)|v\rangle = a|v\rangle + b|v\rangle$ (distributiva)
3. $a(b|v\rangle) = (ab)|v\rangle$ (associativa)
4. $|v\rangle + |w\rangle = |w\rangle + |v\rangle$ (comutativa)
5. $|v\rangle + (|w\rangle + |z\rangle) = (|v\rangle + |w\rangle) + |z\rangle$ (associativa)
6. $|v\rangle + |0\rangle = |v\rangle$ (existe vetor nulo)
7. $|v\rangle + (-|v\rangle) = |0\rangle$ (existe inverso)

> **Observação:** Não se preocupe com as 7 regras acima. Elas impõem propriedades inteiramente naturais para a soma de vetores e multiplicação por escalar. Por exemplo (tente demonstrar): $0|V\rangle = |0\rangle$ e $(-1)|V\rangle = -|V\rangle$.

**Exemplo:** Prove que só existe um único vetor nulo em $V$. Suponha que $|0\rangle$ e $|0'\rangle$ sejam vetores nulos:

$$|0\rangle + |0'\rangle = |0\rangle \quad \text{(por 6, pois $|0'\rangle$ é nulo)}$$
$$|0\rangle + |0'\rangle = |0'\rangle \quad \text{(por 6, pois $|0\rangle$ é nulo)}$$

Logo $|0\rangle = |0'\rangle$.

**Exemplo:** Setas em um plano formam um EV real: a soma é a regra do paralelogramo; $\vec{0}$ é uma seta de tamanho zero.

**Exemplo:** O conjunto de todas as matrizes reais $2\times2$ forma um EV real com:

$$\begin{bmatrix} a & b \\ c & d \end{bmatrix} + \begin{bmatrix} a' & b' \\ c' & d' \end{bmatrix} = \begin{bmatrix} a+a' & b+b' \\ c+c' & d+d' \end{bmatrix} \qquad \alpha \begin{bmatrix} a & b \\ c & d \end{bmatrix} = \begin{bmatrix} \alpha a & \alpha b \\ \alpha c & \alpha d \end{bmatrix}$$

No entanto, o conjunto das matrizes $\begin{bmatrix} a & b \\ c & 1 \end{bmatrix}$ (com $a,b,c \in \mathbb{R}$) **não** forma EV, pois a soma de dois elementos tem "2" no lugar do "1", saindo do conjunto.

> **LINEARMENTE INDEPENDENTE (LI):** um conjunto de $N$ vetores não-nulos é LI se
> $$\sum_{i=1}^N a_i |v_i\rangle = |0\rangle$$
> só tem solução trivial (todos $a_i = 0$). Caso contrário, é **LINEARMENTE DEPENDENTE (LD)**.

**Exemplo:** No plano, dois vetores não colineares são LI; três vetores no plano são LD.

**Exemplo:** São LI ou LD os vetores $|1\rangle = \begin{bmatrix} 0 & 1 \\ 0 & 0 \end{bmatrix}$, $|2\rangle = \begin{bmatrix} 1 & 1 \\ 0 & 1 \end{bmatrix}$, $|3\rangle = \begin{bmatrix} -2 & -1 \\ 0 & -2 \end{bmatrix}$?

Formamos $a|1\rangle + b|2\rangle + c|3\rangle = |0\rangle$:

$$\begin{bmatrix} b-2c & a+b-c \\ 0 & b-2c \end{bmatrix} = \begin{bmatrix} 0 & 0 \\ 0 & 0 \end{bmatrix} \quad \Longrightarrow \quad b = 2c,\ a + b - c = 0$$

Uma solução não trivial é $a=-1$, $b=2$, $c=1$; logo os vetores são **LD**.

> A **DIMENSÃO** de um EV é o número máximo de vetores LI que ele pode acomodar. $\mathbb{V}^n(\mathbb{R})$ tem dimensão $n$; $\mathbb{V}^n(\mathbb{C})$ idem.

**TEOREMA:** Qualquer vetor em um EV de dimensão $n$ pode ser escrito como combinação linear de $n$ vetores LI (BASE):

$$|V\rangle = \sum_{i=1}^n v_i |i\rangle$$

As componentes $v_i$ são únicas (prova: subtraindo duas representações e usando que a base é LI).

**DEFINIÇÃO:** Qualquer conjunto de $n$ vetores LI em $\mathbb{V}^n$ forma uma **BASE**.

As operações sobre vetores na base $\{|i\rangle\}$ ficam:

$$|V\rangle + |W\rangle = \sum_{i=1}^n (v_i + w_i)|i\rangle \qquad \alpha|V\rangle = \sum_{i=1}^n (\alpha v_i)|i\rangle$$

As equações da MQ são relações entre vetores de um espaço vetorial de estados físicos. Os cálculos são feitos escolhendo-se uma base e escrevendo os vetores nessa base — exatamente como nas equações de Maxwell:

$$\nabla\times\mathbf{E} + \frac{1}{c}\frac{\partial\mathbf{B}}{\partial t} = 0 \quad \Longrightarrow \quad \begin{cases} \dfrac{\partial E_z}{\partial y} - \dfrac{\partial E_y}{\partial z} + \dfrac{1}{c}\dfrac{\partial B_x}{\partial t} = 0 \\[4pt] \dfrac{\partial E_x}{\partial z} - \dfrac{\partial E_z}{\partial x} + \dfrac{1}{c}\dfrac{\partial B_y}{\partial t} = 0 \\[4pt] \dfrac{\partial E_y}{\partial x} - \dfrac{\partial E_x}{\partial y} + \dfrac{1}{c}\dfrac{\partial B_z}{\partial t} = 0 \end{cases}$$

## Produto Interno (seção 1.2)

O produto interno associa um número (real ou complexo) a um par de vetores. Para setas temos $\mathbf{v}\cdot\mathbf{w} = |\mathbf{v}||\mathbf{w}|\cos\theta$.

Para EVs gerais exigimos três propriedades do produto interno:

1. $\langle U|W\rangle = \langle W|U\rangle^*$
2. $\langle V|V\rangle \geq 0$, com igualdade somente se $|V\rangle = |0\rangle$
3. $\langle V|(a|W\rangle + b|Z\rangle) = a\langle V|W\rangle + b\langle V|Z\rangle$

Em uma **base ortonormal** ($\langle i|j\rangle = \delta_{ij}$), o produto interno de $|V\rangle = \sum_i v_i|i\rangle$ e $|W\rangle = \sum_j w_j|j\rangle$ é:

$$\langle V|W\rangle = \sum_{i=1}^n v_i^* w_i$$

A **norma** (comprimento) de $|V\rangle$:

$$\|V\| = \sqrt{\langle V|V\rangle} = \sqrt{\sum_i |v_i|^2}$$

**Exemplo:** Para setas com base ortonormal $\hat{i},\hat{j},\hat{k}$: $\mathbf{v}\cdot\mathbf{w} = \sum_{k=1}^3 v_k w_k$.

**Exemplo:** Para matrizes $2\times2$ com base $|1\rangle=\begin{bmatrix}1&0\\0&0\end{bmatrix}$, $|2\rangle=\begin{bmatrix}0&1\\0&0\end{bmatrix}$, $|3\rangle=\begin{bmatrix}0&0\\1&0\end{bmatrix}$, $|4\rangle=\begin{bmatrix}0&0\\0&1\end{bmatrix}$ e $\langle i|j\rangle=\delta_{ij}$:

$$\left\|\begin{bmatrix} 1 & 2 \\ 0 & 1 \end{bmatrix}\right\| = \sqrt{1^2+2^2+0^2+1^2} = \sqrt{6}$$

> **Observação:** Para uma base **não ortonormal**, o produto interno deve ser calculado usando os $n^2$ valores $\langle j|i\rangle$ que definem o produto interno naquela base:
> $$\langle V|W\rangle = \sum_{i,j=1}^n v_j^* w_i \langle j|i\rangle$$

## Espaço Vetorial Dual (seção 1.3)

A forma assimétrica como $|V\rangle$ aparece no produto interno (seus componentes são conjugados) nos leva a definir um EV **dual**: os vetores do espaço dual usam o símbolo $\langle V|$ (chamados **bras**) para se distinguirem dos **kets** $|V\rangle$ do EV original.

A correspondência entre kets e bras:

$$|V\rangle = \sum_i v_i |i\rangle \quad \longleftrightarrow \quad \langle V| = \sum_i v_i^* \langle i|$$

$$|U\rangle + |Z\rangle = |W\rangle \quad \Longrightarrow \quad \langle U| + \langle Z| = \langle W|$$

$$|aV\rangle = a|V\rangle \quad \Longrightarrow \quad \langle aV| = a^*\langle V|$$

O símbolo $\langle W|U\rangle$ é lido como "produto interno do bra $\langle W|$ com o ket $|U\rangle$". Calcula-se diretamente:

$$\underbrace{\left(\sum_i w_i^* \langle i|\right)}_{\langle W|} \underbrace{\left(\sum_j u_j |j\rangle\right)}_{|U\rangle} = \sum_{i,j} w_i^* u_j \underbrace{\langle i|j\rangle}_{\delta_{ij}} = \sum_i w_i^* u_i$$

A operação de encontrar o bra correspondente a um ket se chama **OPERAÇÃO ADJUNTA**. Pense no EV dual como a imagem no espelho do EV original.

> **ATENÇÃO:** NÃO FAZ SENTIDO SOMAR UM BRA E UM KET. $\langle U| + |W\rangle$ **NÃO EXISTE**. A única comunicação entre o EV original e o EV dual se dá no produto interno $\langle V|W\rangle$.

Em uma **base ortonormal**, a componente $v_j$ de $|V\rangle$ é dada pelo produto interno:

$$\langle j|V\rangle = \sum_i v_i \underbrace{\langle j|i\rangle}_{\delta_{ij}} = v_j$$

isto é, $v_j$ é a "projeção" de $|V\rangle$ na "direção" $|j\rangle$ — análogo a $v_1 = \mathbf{V}\cdot\hat{i}$ para setas.
