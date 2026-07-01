# Aula 1

Você aprendeu em Mecânica Clássica a obter a trajetória de partículas ou sistemas de partículas submetidas a forças conhecidas. Para uma partícula de massa $m$, você deve resolver 3 EDOs:

$$m \frac{d^2 \mathbf{r}}{dt^2} = \mathbf{F}(\mathbf{r}, \mathbf{v}, t)$$

onde $\mathbf{r}(t)$ é o vetor posição (em relação a uma origem previamente escolhida) e $\mathbf{F}(\mathbf{r}, \mathbf{v}, t)$ é a força total que atua sobre a massa. Para que essa equação seja útil, você deve conhecer a dependência de $\mathbf{F}$ com a posição e a velocidade da partícula (a chamada *lei de força*). Algumas forças discutidas no curso de Mecânica Clássica (MC) possuíam leis de força bem definidas, como as **forças de vínculo**, que aprendemos a eliminar no formalismo de Lagrange.

Do ponto de vista clássico e fundamental, apenas dois tipos de força atuam sobre uma partícula, a **força gravitacional** e a **força eletromagnética**. A primeira é devida a todos os corpos massivos nas vizinhanças da massa $m$. A segunda, que só se manifesta se a massa $m$ tiver uma carga $q$, é devida a todas as cargas elétricas nas vizinhanças da massa $m$.

> **Observação:** O comentário sobre a necessidade da massa $m$ ter carga só se aplica se estivermos falando de uma partícula isolada. Um sistema de partículas carregadas, mesmo que neutro (como um átomo), experimenta forças eletromagnéticas.

Tanto a força gravitacional quanto a força eletromagnética são expressas em termos de campos:

$$\mathbf{F}_G(\mathbf{r}, t) = -m \nabla \phi(\mathbf{r}, t)$$

$$\mathbf{F}_{EM}(\mathbf{r}, \mathbf{v}, t) = q \left[ \mathbf{E}(\mathbf{r}, t) + \mathbf{v} \times \mathbf{B}(\mathbf{r}, t) \right]$$

onde $\phi$ é o potencial gravitacional, $\mathbf{E}$ é o campo elétrico e $\mathbf{B}$ é o **campo magnético**. A relação desses campos com as distribuições de massa e carga nas vizinhanças é:

$$\nabla^2 \phi(\mathbf{r}, t) = 4\pi G \rho(\mathbf{r}, t)$$

onde $G$ é a constante de gravitação e $\rho$ é a densidade de massa responsável pelo campo. As equações de Maxwell que relacionam os campos eletromagnéticos com as distribuições de carga e corrente são:

$$\nabla \cdot \mathbf{E} = 4\pi \rho_e \quad \text{(Lei de Gauss)}$$

$$\nabla \times \mathbf{E} = -\frac{1}{c} \frac{\partial \mathbf{B}}{\partial t} \quad \text{(Lei de Faraday)}$$

$$\nabla \cdot \mathbf{B} = 0 \quad \text{(Ausência de monopolos magnéticos)}$$

$$\nabla \times \mathbf{B} = \frac{4\pi}{c} \mathbf{j} + \frac{1}{c} \frac{\partial \mathbf{E}}{\partial t} \quad \text{(Lei de Ampère-Maxwell)}$$

Se você conhece a evolução temporal das distribuições de massa e carga, pode, em princípio, resolver essas equações para determinar $\phi$, $\mathbf{E}$ e $\mathbf{B}$ e, dessa forma, escrever a EDO de Newton para a partícula de massa $m$.

Essas são as equações fundamentais da **FÍSICA CLÁSSICA**. Você aprenderá $\mathbf{F} = m\mathbf{a}$ no curso de Mecânica Clássica e as Eqs. de Maxwell no curso de Eletromagnetismo.

> **Observação:** A Mecânica Estatística, com seus conceitos de Temperatura, Entropia, potenciais termodinâmicos etc., aplica-se a sistemas de MUITAS PARTÍCULAS interagindo por forças usuais e respondendo a essas forças da maneira como uma partícula isolada faria. A diferença é que, ao invés de resolver a equação de Newton (ou de Schrödinger) para cada partícula, resolvem-se equações para as **DISTRIBUIÇÕES DE PROBABILIDADE** do sistema. No curso de Mecânica Estatística, concentramo-nos nas propriedades das distribuições **INDEPENDENTES DO TEMPO**, isto é, no **EQUILÍBRIO TERMODINÂMICO**.

Essas equações da Física Clássica descrevem uma variedade tão grande de fenômenos e de maneira tão compacta e elegante que causou muito desconforto a observação de pequenas falhas nessas equações:

1. As equações de Maxwell prevêem que a velocidade da luz deve ser a mesma para todos os observadores inerciais, e isso é incompatível com a maneira como o tempo é tratado em $\mathbf{F} = m\mathbf{a}$ → **Teoria da Relatividade Especial** (1905 — Lorentz, Poincaré, Einstein).
2. A equação da Gravitação de Newton diz que uma massa em qualquer ponto do universo influencia **instantaneamente** o movimento de qualquer outra massa, e isso é incompatível com a Relatividade Especial → **Teoria da Relatividade Geral** (1915 — Einstein).
3. O grande desastre da Física Clássica ocorreu quando se tentou explicar o comportamento de objetos muito pequenos, os átomos e as moléculas, e sua interação com a radiação eletromagnética.

## Histórico do Desenvolvimento da Teoria Quântica

- **1834** — Michael Faraday — Eletrólise de várias substâncias.
- **1867** — Fórmulas para moléculas $\text{H}_2\text{O}$, $\text{H}_2$, $\text{CO}$.
- **1897** — J.J. Thomson — Descoberta do elétron.
- **1909** — R.A. Millikan — Medida da carga do elétron ($e$) e consequências:
  - Valor de $m_e$ é obtido (dos resultados de Thomson)
  - Valor de $N_A = 6{,}022 \times 10^{23}$ é obtido (dos resultados de Faraday)
  - Tamanho do átomo $\sim 1$ Å é obtido (das densidades)
  - Massa dos átomos é obtida (de $N_A$)

A imagem que surge é a do átomo como uma pequena esfera composta de uma carga positiva massiva e de uma carga negativa muito leve (a massa dos elétrons é muito menor que a massa dos átomos). Como se dá o movimento e a distribuição dessas cargas no átomo? Esse movimento deve ser a causa do espectro característico das substâncias no estado gasoso (o movimento de cargas causa a emissão de radiação eletromagnética com frequência igual à frequência do movimento das cargas, segundo Maxwell).

## Espectros Atômicos

J.R. Rydberg (1900) e W. Ritz (1908) mostraram que os comprimentos de onda característicos de cada substância podiam ser compreendidos como diferenças entre **termos**. Por exemplo, na série de Balmer do Hidrogênio:

$$\frac{1}{\lambda} = R_H \left( \frac{1}{2^2} - \frac{1}{n^2} \right) \quad (n = 3, 4, 5, \dots)$$

onde $R_H$ é a **constante de Rydberg** para o hidrogênio. O número de termos necessários para explicar um dado espectro era muito menor que o número de comprimentos de onda característicos.

## Modelo de Rutherford (1911)

Nesse modelo, o núcleo, de tamanho $\sim 10^{-4}$ Å (muito menor que o átomo, de tamanho $\approx 1$ Å), faz o papel do Sol, e os elétrons, o dos planetas. O número de elétrons (e a carga do núcleo), o número atômico $Z$, foi medido por Rutherford.

O problema é que cargas orbitando um núcleo carregado deveriam emitir energia eletromagnética continuamente até colapsar no interior do núcleo. Esse é o problema da **ESTABILIDADE DA MATÉRIA**, que $\mathbf{F} = m\mathbf{a}$ + Eqs. de Maxwell **não conseguem resolver**!

## Resumo dos Problemas com $\mathbf{F} = m\mathbf{a}$ e Eqs. de Maxwell

- **Átomo:**
  - Estabilidade da matéria
  - Espectro discreto dos átomos dado como diferença de energias

- **Ondas Eletromagnéticas:**
  - Energia de um campo EM clássico confinado em uma cavidade seria infinita (**Problema da Radiação de Corpo Negro** — Max Planck, 1900)
  - Efeito fotoelétrico (Einstein, 1905)
  - Espalhamento Compton (A.H. Compton, 1919–1923)

Nesses fenômenos, a radiação eletromagnética se comporta como partícula de energia $E = h\nu$ e momento $p = h/\lambda$ (onde $\nu$ e $\lambda$ são a frequência e o comprimento de onda da onda eletromagnética).

## Espalhamento de Elétrons

Elétrons espalhados por uma superfície metálica apresentam um padrão de difração (a rede de difração são os átomos na superfície) — C.J. Davisson e L.H. Germer (1925).

Nesse experimento, o comprimento de onda da "onda eletrônica" é dado por:

$$\lambda = \frac{h}{p}$$

onde $p$ é o momento usual do elétron clássico. G.P. Thomson (1927–28) fez experiências semelhantes e provou, com um campo magnético, que o padrão de difração era devido a elétrons.

## Conclusão

Vemos portanto que não apenas as equações da Física Clássica não conseguem explicar o comportamento interno dos átomos, mas os próprios conceitos de **PARTÍCULA** e **ONDA** parecem inadequados para descrever o universo na escala de distâncias atômicas ($L \sim 1$ Å).

## O que acontece de especial nessa escala de tamanho?

A Ciência depende de observações: medimos $\mathbf{r}(t)$ e verificamos que $\mathbf{F} = m\mathbf{a}$; medimos $\mathbf{E}$ e $\mathbf{B}$ e verificamos as Eqs. de Maxwell. A Física clássica pressupõe que o ato da observação pode ser feito de forma arbitrariamente não perturbadora.

No caso do átomo, imaginamos que seria possível medir $\mathbf{r}(t)$ do elétron com uma radiação EM "muito delicada" (que não carregaria momento linear apreciável), de modo a não alterar o movimento eletrônico. Se isso fosse possível, poderíamos verificar $\mathbf{F} = m\mathbf{a}$, onde $\mathbf{F}$ seria a força elétrica do núcleo.

**MAS ISSO NÃO É POSSÍVEL!** Não há como medir a posição do elétron sem alterar sua velocidade, e isso não é uma impossibilidade técnica, mas sim uma impossibilidade de fato.

> "A NATUREZA TEM UM LIMITE FUNDAMENTAL PARA O PEQUENO: aquele que, ao ser observado, é sempre perturbado, independente do esforço do observador."

A descrição das partículas subatômicas não pode ser em termos de trajetórias. É aqui que entra a **Mecânica Quântica** e sua **onda de probabilidade**.

A razão da descrição ter necessariamente que ser probabilística está no fato de que, após cada medida, o sistema se modifica de maneira a tornar impossível prever o resultado de uma medida subsequente (exceto em alguns casos especiais). Tudo o que poderemos fornecer, em geral, é a **probabilidade** dos resultados das medidas.

Neste curso, trataremos da descrição quântica de partículas materiais. A descrição quântica do campo EM e o fóton terão que esperar.
