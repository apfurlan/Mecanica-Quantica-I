# (2ª aula) Espaços Vetoriais (seções 1.1–1.3)

A ferramenta matemática central da Mecânica Quântica é a **Álgebra Linear**. O estado de uma partícula é representado não por $\mathbf{r}(t)$, mas por um elemento de um espaço vetorial, denotado $|\psi(t)\rangle$.

## Espaço Vetorial (seção 1.1)

> Um **ESPAÇO VETORIAL** $V$ é uma coleção de objetos chamados **VETORES** $|v_1\rangle, |v_2\rangle, \dots$ com duas operações:
> $$\text{Soma: } |u\rangle + |v\rangle \in V \qquad \text{Multiplicação por escalar: } a|v\rangle \in V$$

O escalar pode ser real (EV real) ou complexo (EV complexo). As 7 propriedades exigidas:

1. $a(|u\rangle + |w\rangle) = a|u\rangle + a|w\rangle$
2. $(a+b)|v\rangle = a|v\rangle + b|v\rangle$
3. $a(b|v\rangle) = (ab)|v\rangle$
4. $|v\rangle + |w\rangle = |w\rangle + |v\rangle$
5. $|v\rangle + (|w\rangle + |z\rangle) = (|v\rangle + |w\rangle) + |z\rangle$
6. $|v\rangle + |0\rangle = |v\rangle$ (existe vetor nulo)
7. $|v\rangle + (-|v\rangle) = |0\rangle$ (existe inverso)

**Exemplos:** setas em um plano; matrizes $2\times2$ reais (com soma e mult. escalar componente a componente).

> **LINEARMENTE INDEPENDENTE (LI):** um conjunto de $N$ vetores não-nulos é LI se $\sum_i a_i |v_i\rangle = |0\rangle$ só tem solução trivial ($a_i = 0$ para todo $i$). Caso contrário, é **LD**.

> A **DIMENSÃO** de um EV é o número máximo de vetores LI que ele pode acomodar. $\mathbb{V}^n(\mathbb{R})$ tem dimensão $n$; $\mathbb{V}^n(\mathbb{C})$ idem.

**TEOREMA:** Qualquer vetor em $\mathbb{V}^n$ pode ser escrito como combinação linear de $n$ vetores LI (base):

$$|V\rangle = \sum_{i=1}^n v_i |i\rangle$$

As componentes $v_i$ são únicas. Operações em componentes:

$$|V\rangle + |W\rangle = \sum_i (v_i + w_i)|i\rangle \qquad \alpha|V\rangle = \sum_i (\alpha v_i)|i\rangle$$

## Produto Interno (seção 1.2)

O produto interno associa um número a um par de vetores. Para EVs gerais, exigem-se três propriedades:

1. $\langle U|W\rangle = \langle W|U\rangle^*$
2. $\langle V|V\rangle \geq 0$, com igualdade só se $|V\rangle = |0\rangle$
3. $\langle V|(a|W\rangle + b|Z\rangle) = a\langle V|W\rangle + b\langle V|Z\rangle$

Em uma **base ortonormal** ($\langle i|j\rangle = \delta_{ij}$):

$$\langle V|W\rangle = \sum_{i=1}^n v_i^* w_i$$

A **norma** (comprimento) de $|V\rangle$:

$$\|V\| = \sqrt{\langle V|V\rangle} = \sqrt{\sum_i |v_i|^2}$$

> Para uma base **não ortonormal**, deve-se fornecer os valores $\langle j|i\rangle$ e usar:
> $$\langle V|W\rangle = \sum_{i,j} v_j^* w_i \langle j|i\rangle$$

## Espaço Vetorial Dual (seção 1.3)

A forma assimétrica como $|V\rangle$ aparece no produto interno (componentes conjugadas) nos leva a definir um EV **dual**, cujos vetores usam o símbolo $\langle V|$ (chamados **bras**) para distingui-los dos **kets** $|V\rangle$ do EV original.

A correspondência entre kets e bras:

$$|V\rangle = \sum_i v_i |i\rangle \quad \longleftrightarrow \quad \langle V| = \sum_i v_i^* \langle i|$$

$$|aV\rangle = a|V\rangle \quad \Longrightarrow \quad \langle aV| = a^* \langle V|$$

O produto interno $\langle W|U\rangle$ é calculado diretamente:

$$\underbrace{\left(\sum_i w_i^* \langle i|\right)}_{\langle W|} \underbrace{\left(\sum_j u_j |j\rangle\right)}_{|U\rangle} = \sum_{i,j} w_i^* u_j \underbrace{\langle i|j\rangle}_{\delta_{ij}} = \sum_i w_i^* u_i$$

> **ATENÇÃO:** $\langle U| + |W\rangle$ **NÃO EXISTE**. Bras e kets vivem em espaços diferentes; a única "comunicação" é no produto interno $\langle V|W\rangle$.

Em uma base ortonormal, a componente $v_j$ de $|V\rangle$ é a projeção:

$$\langle j|V\rangle = v_j$$

análogo a $v_1 = \mathbf{V} \cdot \hat{i}$ para setas.
