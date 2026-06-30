# (9ª aula) (seções 2.4-2.7) --- Formalismo Hamiltoniano

## Formalismo Hamiltoniano

O método Lagrangiano tem uma conexão direta com a MQ. Veremos essa conexão, proposta por Feynman, quando estudarmos o capítulo 8.

**Antecipando:** De todas as maneiras de ir do ponto $x_i$ ao ponto $x_f$ em um intervalo de tempo fixo $\Delta t = t_f - t_i$, a partícula **CLÁSSICA** escolhe o caminho de **MENOR** valor da ação

$$
S[x(t)] = \int_{t_i}^{t_f} \mathcal{L}(x(t), \dot{x}(t), t) \, dt
$$

*(Diagrama: trajetória $x(t)$ entre os instantes $t_i$ e $t_f$, mostrando o caminho clássico que vai de $x_i$ a $x_f$.)*

Na MQ veremos que, para calcular a **PROBABILIDADE** da partícula, que estava em $x_i$ no instante $t_i$, ser encontrada em $x_f$ no instante $t_f$, somamos $e^{iS[x(t)]/\hbar}$ de **TODOS os caminhos**. Como veremos, o caminho que mais contribui para determinar a probabilidade é o caminho clássico $x_c(t)$. A MQ se transforma em Mecânica Clássica quando o valor de $S[x(t)] \gg \hbar$ (sem ser muito rigoroso).

Essa maneira de conectar a Mecânica Clássica com a MQ foi proposta por Feynman em 1940.

Historicamente, a conexão entre MQ e MC foi feita via Hamiltoniana, por isso vamos rever o papel da função Hamiltoniana em MC.

> **Obs:** Se você não lembra dos detalhes, leia a seção 2.5 com atenção, aqui serei mais breve.

Da função Lagrangiana de um sistema que possui $N$ coordenadas $\{q_1(t), \dots, q_N(t)\}$, podemos construir uma função das coordenadas e momenta chamada Hamiltoniana:

De $\mathcal{L}(\vec{q}, \dot{\vec{q}}, t)$ construo primeiramente

$$
h(\vec{q}, \dot{\vec{q}}, t) = \left( \sum_{i=1}^{N} \dot{q}_i \frac{\partial \mathcal{L}}{\partial \dot{q}_i} \right) - \mathcal{L}(\vec{q}, \dot{\vec{q}}, t)
$$

A função Hamiltoniana propriamente dita é essa função com a **SUBSTITUIÇÃO** de $\dot{q}_i$ por $p_i$, onde

$$
p_i = \frac{\partial \mathcal{L}}{\partial \dot{q}_i}
$$

é o momento conjugado a $q_i$.

Você deve, portanto, inverter essa relação para obter

$$
\dot{q}_i(\vec{p}, \vec{q}, t) \quad (i = 1, \dots, N)
$$

Levando isso na expressão de $h(\vec{q}, \dot{\vec{q}}, t)$ você obtém $H(\vec{q}, \vec{p}, t)$.

As equações de Hamilton, que determinam os $q_i(t)$ e os $p_i(t)$, são consequência da definição da Hamiltoniana e das equações de Euler-Lagrange.

$$
H = \left( \sum_{j=1}^{N} \dot{q}_j p_j \right) - \mathcal{L}(\vec{q}, \dot{\vec{q}}, t) \quad \text{(com } \dot{q}_i(\vec{q}, \vec{p}, t) \text{)}
$$

$$
\frac{\partial H}{\partial p_i} = \dot{q}_i + \sum_{j=1}^{N} \left( p_j \frac{\partial \dot{q}_j}{\partial p_i} - \frac{\partial \mathcal{L}}{\partial \dot{q}_j} \frac{\partial \dot{q}_j}{\partial p_i} \right) \quad \left( \text{usando que } p_j = \frac{\partial \mathcal{L}}{\partial \dot{q}_j} \right)
$$

Os dois últimos termos se cancelam, pois $p_j = \dfrac{\partial \mathcal{L}}{\partial \dot{q}_j}$, restando

$$
\frac{\partial H}{\partial q_i} = \left( \sum_{j=1}^{N} p_j \frac{\partial \dot{q}_j}{\partial q_i} - \frac{\partial \mathcal{L}}{\partial \dot{q}_j} \frac{\partial \dot{q}_j}{\partial q_i} \right) - \frac{\partial \mathcal{L}}{\partial q_i} \quad (\text{idem})
$$

Novamente os dois primeiros termos dentro do parêntese se cancelam, e usando a equação de Euler-Lagrange $\dfrac{\partial \mathcal{L}}{\partial q_i} = \dfrac{d}{dt}\dfrac{\partial \mathcal{L}}{\partial \dot{q}_i} = \dot{p}_i$, obtemos

$$
\frac{\partial H}{\partial q_i} = -\dot{p}_i \quad \text{(da Eq. de Euler-Lagrange)}
$$

Logo, chegamos às equações de Hamilton:

$$
\boxed{\dot{q}_i = \frac{\partial H}{\partial p_i}} \qquad \boxed{\dot{p}_i = -\frac{\partial H}{\partial q_i}} \qquad (i = 1, \dots, N)
$$

Temos $2N$ EDOs de 1ª ordem, inteiramente equivalentes às $N$ EDOs de 2ª ordem

$$
\frac{d}{dt}\left( \frac{\partial \mathcal{L}}{\partial \dot{q}_i} \right) = \frac{\partial \mathcal{L}}{\partial q_i} \qquad (i = 1, \dots, N)
$$

## Construção de $H(\vec{q}, \vec{p}, t)$

A construção de $H(\vec{q}, \vec{p}, t)$ envolve 2 passos:

1. $$
   h(\vec{q}, \dot{\vec{q}}, t) = \left( \sum_{i=1}^{N} \dot{q}_i \frac{\partial \mathcal{L}}{\partial \dot{q}_i} \right) - \mathcal{L}(\vec{q}, \dot{\vec{q}}, t)
   $$
2. Trocar $\dot{q}_i$ por sua expressão em termos de $\vec{p}$ e $\vec{q}$, usando

   $$
   p_i = \frac{\partial \mathcal{L}}{\partial \dot{q}_i}
   $$

O passo (1) é facilitado quando a energia cinética é puramente quadrática nas velocidades

$$
T = \sum_{i,j=1}^{N} T_{ij}(\vec{q}) \, \dot{q}_i \dot{q}_j
$$

Nesse caso,

$$
\sum_i \dot{q}_i \frac{\partial \mathcal{L}}{\partial \dot{q}_i} = 2 \sum_{i,j} T_{ij}(\vec{q}) \, \dot{q}_i \dot{q}_j = 2T
$$

e, portanto,

$$
h = 2T - \underbrace{(T - V)}_{\mathcal{L}} = T + V
$$

**Exemplo:** $\mathcal{L} = \dfrac{1}{2}\dot{q}_1^2 + \dfrac{1}{2}\dot{q}_2^2 + 2\dot{q}_1 \dot{q}_2 - 2q_1 q_2$, obtenha a Hamiltoniana.

$$
\begin{aligned}
h &= \dot{q}_1(\dot{q}_1 + 2\dot{q}_2) + \dot{q}_2(\dot{q}_2 + 2\dot{q}_1) - \frac{1}{2}\dot{q}_1^2 - \frac{1}{2}\dot{q}_2^2 - 2\dot{q}_1 \dot{q}_2 + 2 q_1 q_2 \\
&= \frac{1}{2}\dot{q}_1^2 + \frac{1}{2}\dot{q}_2^2 + 2\dot{q}_1\dot{q}_2 + 2q_1 q_2 \qquad (= T + V !)
\end{aligned}
$$

Os momenta conjugados são

$$
\begin{cases}
p_1 = \dot{q}_1 + 2\dot{q}_2 \\
p_2 = \dot{q}_2 + 2\dot{q}_1
\end{cases}
\quad \Longrightarrow \quad
\begin{cases}
\dot{q}_1 = \dfrac{1}{3}(2p_2 - p_1) \\[2mm]
\dot{q}_2 = \dfrac{1}{3}(2p_1 - p_2)
\end{cases}
$$

Substituindo na expressão de $h$, obtemos a Hamiltoniana em termos de $q_1, q_2, p_1, p_2$:

$$
H(q_1, q_2, p_1, p_2) = \frac{1}{18}(2p_2 - p_1)^2 + \frac{1}{18}(2p_1 - p_2)^2 + \frac{2}{9}(2p_2 - p_1)(2p_1 - p_2) + 2 q_1 q_2
$$

## Hamiltoniana da Interação Eletromagnética

$$
\mathcal{L}(\vec{r}, \vec{v}, t) = \frac{1}{2}m\vec{v}^2 - q\phi(\vec{r}, t) + \frac{q}{c}\vec{v}\cdot\vec{A}(\vec{r}, t)
$$

$$
\vec{p} = \frac{\partial \mathcal{L}}{\partial \vec{v}} = m\vec{v} + \frac{q}{c}\vec{A}(\vec{r}, t)
$$

$$
\begin{aligned}
h &= \vec{v} \cdot \left( m\vec{v} + \frac{q}{c}\vec{A} \right) - \frac{1}{2}m\vec{v}^2 + q\phi - \frac{q}{c}\vec{v}\cdot\vec{A} \\
&= \frac{1}{2}m\vec{v}^2 + q\phi
\end{aligned}
$$

Invertendo $\vec{p} = m\vec{v} + \dfrac{q}{c}\vec{A}(\vec{r},t)$ para obter $\vec{v}$ em termos de $\vec{p}$ e substituindo, chegamos a

$$
\boxed{H(\vec{r}, \vec{p}, t) = \frac{1}{2m}\left( \vec{p} - \frac{q}{c}\vec{A}(\vec{r}, t) \right)^2 + q\phi(\vec{r}, t)}
$$

## Coordenada Cíclica

Coordenada que não aparece em $H(\vec{q}, \vec{p}, t)$. Isso acarreta na conservação de seu momento conjugado.

$$
\dot{p}_i = -\frac{\partial H}{\partial q_i} = 0 \quad \Longrightarrow \quad \boxed{p_i(t) \text{ é constante}}
$$

## Parênteses de Poisson

As equações de Hamilton governam a evolução de $\vec{q}(t)$ e $\vec{p}(t)$. Podemos determinar como qualquer função de $\vec{q}$ e $\vec{p}$ evolui no tempo.

Seja $w(\vec{q}, \vec{p}, t)$ uma função dos $q_i$'s e $p_i$'s e do tempo.

$$
\begin{aligned}
\frac{dw}{dt} &= \sum_i \frac{\partial w}{\partial q_i}\frac{dq_i}{dt} + \frac{\partial w}{\partial p_i}\frac{dp_i}{dt} + \frac{\partial w}{\partial t} \\
&= \sum_i \frac{\partial w}{\partial q_i}\frac{\partial H}{\partial p_i} - \frac{\partial w}{\partial p_i}\frac{\partial H}{\partial q_i} + \frac{\partial w}{\partial t} \\
&\equiv \{w, H\} + \frac{\partial w}{\partial t}
\end{aligned}
$$

Usamos o símbolo

$$
\{A(\vec{q}, \vec{p}), B(\vec{q}, \vec{p})\} = \sum_{i=1}^{N} \frac{\partial A}{\partial q_i}\frac{\partial B}{\partial p_i} - \frac{\partial A}{\partial p_i}\frac{\partial B}{\partial q_i}
$$

chamado **parênteses de Poisson**.

Se a função $w(\vec{q}, \vec{p})$, que não depende explicitamente do tempo, não se altera durante a evolução do sistema, $\dfrac{dw}{dt} = 0$ e $\{w, H\} = 0$.

Calcular $\{w, H\}$ permite prever se uma quantidade será ou não conservada.

> **Parênteses de Poisson Básicos**
>
> $$
> \{q_\alpha, q_\beta\} = \{p_\alpha, p_\beta\} = 0 \qquad \{q_\alpha, p_\beta\} = \delta_{\alpha\beta}
> $$
>
> (onde $q_\alpha$ e $p_\beta$ são uma das coordenadas e um dos momenta)

Reproduzindo as equações de Hamilton:

$$
\begin{aligned}
\dot{q}_\alpha = \{q_\alpha, H\} &= \sum_i \frac{\partial q_\alpha}{\partial q_i}\frac{\partial H}{\partial p_i} - \underbrace{\frac{\partial q_\alpha}{\partial p_i}}_{0}\frac{\partial H}{\partial q_i} = \sum_i \delta_{\alpha,i}\frac{\partial H}{\partial p_i} = \frac{\partial H}{\partial p_\alpha} \qquad \text{(OK)} \\
\dot{p}_\alpha = \{p_\alpha, H\} &= \sum_i \underbrace{\frac{\partial p_\alpha}{\partial q_i}}_{0}\frac{\partial H}{\partial p_i} - \frac{\partial p_\alpha}{\partial p_i}\frac{\partial H}{\partial q_i} = -\sum_i \delta_{\alpha, i}\frac{\partial H}{\partial q_i} = -\frac{\partial H}{\partial q_\alpha} \qquad \text{(OK)}
\end{aligned}
$$

Veremos que a Eq. fundamental da MQ é construída a partir da Hamiltoniana do sistema considerado. Apenas transformamos a função $p(t)$ clássica no **OPERADOR** $\hat{P}$ e a função $q(t)$ no operador $\hat{Q}$, dessa forma obtendo o **OPERADOR Hamiltoniano**. Esse operador determina como o ket associado ao **ESTADO FÍSICO** do sistema evolui:

$$
i\hbar \frac{d}{dt}|\Psi(t)\rangle = \hat{H}|\Psi(t)\rangle
$$

onde $\hat{H}$ é o **operador Hamiltoniano**.

Por isso é importante saber construir a função Hamiltoniana (clássica) de vários sistemas físicos.

## Conservação da Hamiltoniana

$$
\frac{dH(\vec{q}, \vec{p}, t)}{dt} = \left( \sum_i \frac{\partial H}{\partial q_i}\dot{q}_i + \frac{\partial H}{\partial p_i}\dot{p}_i \right) + \frac{\partial H}{\partial t}
$$

é a taxa de variação no valor de $H$ com a evolução do sistema. Como $\dot{q}_i = \dfrac{\partial H}{\partial p_i}$ e $\dot{p}_i = -\dfrac{\partial H}{\partial q_i}$, o termo entre parênteses é zero e

$$
\boxed{\frac{dH}{dt} = \frac{\partial H}{\partial t}}
$$

> Se o tempo não aparece explicitamente em $H$, esta é conservada.

## Propriedades dos Parênteses de Poisson

Os parênteses de Poisson satisfazem às propriedades

- (i) $\{AB, C\} = A\{B, C\} + B\{A, C\}$
- (ii) $\{A, B+C\} = \{A, B\} + \{A, C\}$
- (iii) $\{A, B\} = -\{B, A\}$ (em particular, $\{A, A\} = 0$)

Essas propriedades, facilmente verificadas a partir da definição de $\{A, B\}$ em termos de derivadas, permitem reduzir qualquer parênteses de Poisson aos parênteses de Poisson básicos.

**Exemplo:** Seja um sistema com coordenadas $q_1$ e $q_2$ e momenta $p_1$ e $p_2$.

$$
\begin{aligned}
\{p_1 q_2^2, \, q_1 + q_2\} &\overset{\text{(ii)}}{=} \{p_1 q_2^2, q_1\} + \{p_1 q_2^2, q_2\} \\
&\overset{\text{(i)}}{=} p_1\{q_2^2, q_1\} + q_2^2\{p_1, q_1\} + p_1\{q_2^2, q_2\} + q_2^2\{p_1, q_2\} \\
&= p_1\{q_2^2, q_1\} + q_2^2\underbrace{\{p_1, q_1\}}_{-1} + p_1\underbrace{\{q_2^2, q_2\}}_{0} + q_2^2\underbrace{\{p_1, q_2\}}_{0} \\
&= p_1\{q_2^2, q_1\} - q_2^2 \\
&= -q_2^2
\end{aligned}
$$

(onde usei os parênteses básicos, junto com a propriedade (iii), notando que $\{q_2^2, q_1\} = 0$ pois $q_2^2$ só depende de coordenadas).
