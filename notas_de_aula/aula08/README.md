# (8ª aula) — Revisão de Mecânica Clássica: Formalismo Lagrangiano

## Revisão de Mecânica Clássica (seções 2.1–2.3)

Como vimos na primeira aula, o conceito de trajetória e a Eq. de Newton que a determina só são úteis para objetos grandes (ou pesados) o suficiente para serem observados (tipicamente refletindo radiação eletromagnética) sem que a observação perturbe seu movimento.

No curso de Mecânica Clássica estudamos a equação que determina a trajetória de uma partícula de massa $m$ sob ação de uma força $F$, conservativa, derivada da energia potencial $V(x)$ (vamos considerar o caso 1D primeiro):

$$
m\ddot{x} = -\frac{dV}{dx} \quad \Longrightarrow \quad x(t) \text{ a partir do conhecimento das condições iniciais } x(0) \text{ e } \dot{x}(0)
$$

No caso 3D temos 3 coordenadas cartesianas $(x_1, x_2, x_3)$ a determinar, e as Eqs. de Newton ficam

$$
m\ddot{x}_i = -\frac{\partial V}{\partial x_i} \qquad (i = 1, 2, 3)
$$

onde $V$ é uma função das 3 coordenadas. As condições iniciais são 6: $x_1(0)$, $x_2(0)$, $x_3(0)$, $\dot{x}_1(0)$, $\dot{x}_2(0)$ e $\dot{x}_3(0)$.

## O Princípio de Hamilton e o Funcional da Ação

Cada par de condições iniciais $\{x(0), \dot{x}(0)\}$ fornece uma trajetória $x(t)$ distinta. O mesmo $x(0)$, com 2 valores diferentes de $\dot{x}(0)$, dá origem a duas $x(t)$ distintas.

Na formulação Lagrangiana, o problema de determinar $x(t)$ é formulado através do chamado **FUNCIONAL DA AÇÃO**:

$$
S[x(t)] = \int_{t_i}^{t_f} \mathcal{L}(x, \dot{x})\, dt
$$

onde $\mathcal{L}(x, \dot{x}) = \dfrac{1}{2} m \dot{x}^2 - V(x)$ é a função Lagrangiana (ela pode depender explicitamente do tempo se o potencial variar com o tempo).

> **O PRINCÍPIO DE HAMILTON** diz: "De todas as trajetórias tais que $x(t_i) = x_i$ e $x(t_f) = x_f$, a trajetória seguida pela massa $m$ é a que minimiza o valor de $S$."

Ou seja, se $x_1(t)$ e $x_2(t)$ são trajetórias quaisquer ligando os mesmos pontos extremos, e $x_c(t)$ é a trajetória correta (clássica), então o valor da ação da trajetória correta satisfaz

$$
S[x_c(t)] < S[x_1(t)],\ S[x_2(t)]
$$

(Na verdade a trajetória clássica não é necessariamente um **MÍNIMO** do funcional, e sim apenas um extremo, mas tradicionalmente nos referimos ao Princípio de Hamilton como **PRINCÍPIO DA MÍNIMA AÇÃO**.)

Note que as informações iniciais $x(t_i)$ e $\dot{x}(t_i)$, que seriam apropriadas para resolver a Eq. de Newton, se transformam em $x(t_i)$ e $x(t_f)$ na formulação Lagrangiana.

## Equação de Euler-Lagrange

No curso de Mecânica Clássica vimos como encontrar a função $x(t)$ que extremiza um funcional qualquer (se você não lembra, leia as págs. 77 e 78 do livro). Esse $x(t)$ obedece à equação de Euler-Lagrange do funcional:

$$
\frac{d}{dt}\left(\frac{\partial \mathcal{L}}{\partial \dot{x}}\right) = \frac{\partial \mathcal{L}}{\partial x}
$$

Como $\mathcal{L} = \dfrac{1}{2} m \dot{x}^2 - V(x)$, isso é exatamente a Eq. de Newton:

$$
\frac{d}{dt}\left(m\dot{x}\right) = -\frac{dV}{dx}
$$

$$
\boxed{\text{FORMULAÇÃO LAGRANGIANA É EQUIVALENTE A } F = ma}
$$

## Vantagens do Método Lagrangiano sobre $F=ma$

**(i)** A Lagrangiana não envolve vetores.

**(ii)** As equações de Euler-Lagrange são obtidas de $\mathcal{L}$ com derivadas simples.

**(iii)** Coordenadas são as informações que você precisa para localizar as partículas. Nem sempre é conveniente usar coordenadas cartesianas; veja algumas opções em 3D:

- $(x, y, z)$ — cartesianas
- $(r, \theta, \varphi)$ — esféricas
- $(\rho, \varphi, z)$ — cilíndricas

A Eq. de Newton é uma relação entre vetores:

$$
m\ddot{\vec{r}} = -\vec{\nabla} V
$$

Se você usa $\vec{r}(t) = x(t)\hat{i} + y(t)\hat{j} + z(t)\hat{k}$ (coordenadas cartesianas), os versores são constantes e você obtém as 3 equações:

$$
m\frac{d^2x}{dt^2} = -\frac{\partial V}{\partial x}; \qquad
m\frac{d^2y}{dt^2} = -\frac{\partial V}{\partial y}; \qquad
m\frac{d^2z}{dt^2} = -\frac{\partial V}{\partial z}
$$

No entanto, acontece às vezes do potencial ser fornecido em coordenadas esféricas, por exemplo. Nesse caso você calcula

$$
\vec{\nabla} V = \frac{\partial V}{\partial r}\hat{r} + \frac{1}{r}\frac{\partial V}{\partial \theta}\hat{\theta} + \frac{1}{r\sin\theta}\frac{\partial V}{\partial \varphi}\hat{\varphi}
$$

Esse vetor deve ser igualado a $m\ddot{\vec{r}}$ expresso em termos dos mesmos versores (e de $\dot{r}, \dot{\theta}, \dot{\varphi}$, etc).

Usando $\vec{r}(t) = r(t)\,\hat{r}(\theta(t), \varphi(t))$, e as relações

$$
\frac{\partial \hat{r}}{\partial r} = 0, \quad
\frac{\partial \hat{r}}{\partial \theta} = \hat{\theta}, \quad
\frac{\partial \hat{r}}{\partial \varphi} = \sin\theta\,\hat{\varphi}, \quad
\frac{\partial \hat{\theta}}{\partial r} = 0, \quad
\frac{\partial \hat{\theta}}{\partial \theta} = -\hat{r}, \quad
\frac{\partial \hat{\theta}}{\partial \varphi} = \cos\theta\,\hat{\varphi},
$$

$$
\frac{\partial \hat{\varphi}}{\partial r} = 0, \quad
\frac{\partial \hat{\varphi}}{\partial \theta} = 0, \quad
\frac{\partial \hat{\varphi}}{\partial \varphi} = -\sin\theta\,\hat{r} - \cos\theta\,\hat{\theta}
$$

(ver Symon, seção 3-5, para mais detalhes), obtemos

$$
\dot{\vec{r}} = \dot{r}\hat{r} + r\frac{d\hat{r}}{dt} = \dot{r}\hat{r} + r\left(\dot{r}\frac{\partial \hat{r}}{\partial r} + \dot{\theta}\frac{\partial \hat{r}}{\partial \theta} + \dot{\varphi}\frac{\partial \hat{r}}{\partial \varphi}\right) = \dot{r}\hat{r} + r\dot{\theta}\hat{\theta} + r\sin\theta\,\dot{\varphi}\,\hat{\varphi}
$$

e, derivando novamente,

$$
\begin{aligned}
\ddot{\vec{r}} = {}& \left(\ddot{r} - r\dot{\theta}^2 - r\dot{\varphi}^2 \sin^2\theta\right)\hat{r} \\
& + \left(r\ddot{\theta} + 2\dot{r}\dot{\theta} - r\dot{\varphi}^2 \sin\theta\cos\theta\right)\hat{\theta} \\
& + \left(r\ddot{\varphi}\sin\theta + 2\dot{r}\dot{\varphi}\sin\theta + 2r\dot{\theta}\dot{\varphi}\cos\theta\right)\hat{\varphi}
\end{aligned}
$$

No formalismo Lagrangiano, basta escrever $\mathcal{L} = T - V$ em termos das coordenadas escolhidas. As equações de Euler-Lagrange têm a mesma forma (é possível demonstrar isso) em qualquer sistema de coordenadas:

$$
\frac{d}{dt}\left(\frac{\partial \mathcal{L}}{\partial \dot{q}_i}\right) = \frac{\partial \mathcal{L}}{\partial q_i} \qquad (i = 1, \dots, N)
$$

onde $N$ é o número mínimo de coordenadas.

**Exemplo: Queda livre com coordenadas cartesianas e esféricas.**

$$
T = \frac{1}{2} m(\dot{x}^2 + \dot{y}^2 + \dot{z}^2) = \frac{1}{2} m\left(\dot{r}^2 + r^2\dot{\theta}^2 + r^2\sin^2\theta\,\dot{\varphi}^2\right)
$$

onde usei $x = r\sin\theta\cos\varphi \Rightarrow \dot{x} = \dot{r}\sin\theta\cos\varphi + \dot{\theta} r\cos\theta\cos\varphi - \dot{\varphi} r \sin\theta\sin\varphi$, etc.

$$
V(x, y, z) = mgz = mgr\cos\theta = V(r, \theta, \varphi)
$$

(aqui estou usando um sistema de eixos cartesianos com $z$ na direção vertical).

$$
\mathcal{L}(x, y, z, \dot{x}, \dot{y}, \dot{z}) = \frac{1}{2} m(\dot{x}^2 + \dot{y}^2 + \dot{z}^2) - mgz
$$

$$
\mathcal{L}(r, \theta, \varphi, \dot{r}, \dot{\theta}, \dot{\varphi}) = \frac{1}{2} m\left(\dot{r}^2 + r^2\dot{\theta}^2 + r^2\sin^2\theta\,\dot{\varphi}^2\right) - mgr\cos\theta
$$

Em coordenadas cartesianas, as equações de Euler-Lagrange dão

$$
\frac{d}{dt}(m\dot{x}) = 0\, ; \qquad \frac{d}{dt}(m\dot{y}) = 0\, ; \qquad \frac{d}{dt}(m\dot{z}) = -mg
$$

ou, em coordenadas esféricas,

$$
\begin{aligned}
\frac{d}{dt}(m\dot{r}) &= mr\dot{\theta}^2 + mr\sin^2\theta\,\dot{\varphi}^2 - mg\cos\theta \\
\frac{d}{dt}(mr^2\dot{\theta}) &= mr^2\sin\theta\cos\theta\,\dot{\varphi}^2 + mgr\sin\theta \\
\frac{d}{dt}\left(mr^2\sin^2\theta\,\dot{\varphi}\right) &= 0
\end{aligned}
$$

> É muito mais fácil obter as equações para coordenadas não-cartesianas usando a Lagrangiana.
>
> Obtenha essas 3 equações usando $m\vec{a} = -\vec{\nabla}V$, com $\vec{a}$ expresso em termos de $\hat{r}, \hat{\theta}$ e $\hat{\varphi}$ e tomando o gradiente de $mgr\cos\theta$.

**(iv)** Leis de conservação aparecem naturalmente nas Eqs. de Euler-Lagrange. Quando uma coordenada não está presente na Lagrangiana (a coordenada é dita **CÍCLICA**):

$$
\frac{\partial \mathcal{L}}{\partial q_i} = 0 \quad \Longrightarrow \quad \boxed{\frac{\partial \mathcal{L}}{\partial \dot{q}_i} = \text{const}}
$$

Um exemplo é a conservação de $\left(mr^2\sin^2\theta\,\dot{\varphi}\right)$, $(m\dot{x})$ e $(m\dot{y})$ no problema de queda livre.

**(v)** Quando o problema tem vínculos entre as coordenadas cartesianas, o uso de coordenadas que automaticamente respeitam os vínculos elimina as forças de vínculo do problema.

## A Lagrangiana de uma Carga em um Campo Eletromagnético

Se uma carga $q$ se move em uma região onde existem os campos $\vec{E}(\vec{r}, t)$ e $\vec{B}(\vec{r}, t)$ conhecidos, sua equação de Newton é:

$$
m\ddot{\vec{r}} = q\left[\vec{E}(\vec{r}, t) + \frac{\dot{\vec{r}}}{c} \times \vec{B}(\vec{r}, t)\right]
$$

onde $\dot{\vec{r}}$ é a velocidade da partícula, $\vec{r}$ é a posição da partícula, e $c$ é a velocidade da luz (os campos estão em unidades CGS, assim como a carga $q$).

Nesse problema, que aparecerá quando estudarmos a interação dos átomos com a radiação, a força não é derivada de uma função $V(x,y,z)$. No entanto, é possível encontrar uma função $\mathcal{L}(\vec{r}, \vec{v}, t)$ tal que as Eqs. de Euler-Lagrange são exatamente as Eqs. de Newton acima.

$$
\mathcal{L}(\vec{r}, \vec{v}, t) = \frac{1}{2} m \vec{v}^2 - q\phi(\vec{r}, t) + \frac{q}{c}\vec{v}\cdot\vec{A}(\vec{r}, t)
$$

A relação dos potenciais $\phi$ e $\vec{A}$ com os campos $\vec{E}$ e $\vec{B}$ é

$$
\vec{E} = -\vec{\nabla}\phi - \frac{1}{c}\frac{\partial \vec{A}}{\partial t} \qquad\qquad \vec{B} = \vec{\nabla}\times \vec{A}
$$

Esses potenciais são introduzidos dessa forma devido às duas equações homogêneas de Maxwell:

$$
\begin{aligned}
&\text{i)} \quad \vec{\nabla}\cdot\vec{B} = 0 \quad \Longrightarrow \quad \boxed{\vec{B} = \vec{\nabla}\times\vec{A}} \\[2mm]
&\text{ii)} \quad \vec{\nabla}\times\vec{E} + \frac{1}{c}\frac{\partial \vec{B}}{\partial t} = 0 \quad \Longrightarrow \quad \vec{\nabla}\times\vec{E} + \frac{1}{c}\frac{\partial}{\partial t}(\vec{\nabla}\times\vec{A}) = 0 \\
&\hspace{2cm}\Longrightarrow\quad \vec{\nabla}\times\left(\vec{E} + \frac{1}{c}\frac{\partial \vec{A}}{\partial t}\right) = 0 \quad \Longrightarrow \quad \boxed{\vec{E} + \frac{1}{c}\frac{\partial \vec{A}}{\partial t} = -\vec{\nabla}\phi}
\end{aligned}
$$

$\vec{A}$ e $\phi$ determinam $\vec{E}$ e $\vec{B}$ de modo único, mas $\vec{E}$ e $\vec{B}$ não determinam $\phi$ e $\vec{A}$ de modo único:

$$
\text{se } \{\vec{A}, \phi\} \longrightarrow \{\vec{E}, \vec{B}\}
$$

$$
\text{então } \left\{\vec{A} + \vec{\nabla}\chi,\ \phi - \frac{1}{c}\frac{\partial \chi}{\partial t}\right\} \longrightarrow \{\vec{E}, \vec{B}\}
$$

onde $\chi(\vec{r}, t)$ pode ser qualquer função (verifique isso).

Colocamos na Lagrangiana um par qualquer $\{\phi, \vec{A}\}$ que reproduza os campos reais $\{\vec{E}, \vec{B}\}$.

As 3 equações de Euler-Lagrange ($i = 1, 2, 3$):

$$
\frac{d}{dt}\left(m\dot{x}_i + \frac{q}{c}A_i(\vec{r}, t)\right) = -q\frac{\partial \phi(\vec{r}, t)}{\partial x_i} + \frac{q}{c}\frac{\partial}{\partial x_i}\left(\vec{v}\cdot\vec{A}(\vec{r}, t)\right)
$$

ou, em uma única equação vetorial,

$$
\frac{d}{dt}\left(m\vec{v} + \frac{q}{c}\vec{A}(\vec{r}, t)\right) = -q\vec{\nabla}\phi(\vec{r}, t) + \frac{q}{c}\vec{\nabla}\left(\vec{v}\cdot\vec{A}(\vec{r}, t)\right)
$$

O **momentum canônico** é, portanto,

$$
p_i = \frac{\partial \mathcal{L}}{\partial \dot{x}_i} \quad \Longrightarrow \quad \boxed{\vec{P} = m\vec{v} + \frac{q}{c}\vec{A}(\vec{r}, t)}
$$

Assim,

$$
m\vec{a} = -q\vec{\nabla}\phi + \frac{q}{c}\left[\vec{\nabla}(\vec{v}\cdot\vec{A}) - \frac{d\vec{A}}{dt}\right]
$$

Aqui você deve lembrar que $\phi$ e $\vec{A}$ estão avaliados na posição instantânea da partícula, portanto:

$$
\frac{d\vec{A}}{dt} = \frac{\partial \vec{A}}{\partial t} + \dot{x}\frac{\partial \vec{A}}{\partial x} + \dot{y}\frac{\partial \vec{A}}{\partial y} + \dot{z}\frac{\partial \vec{A}}{\partial z} = \frac{\partial \vec{A}}{\partial t} + (\vec{v}\cdot\vec{\nabla})\vec{A}
$$

Então

$$
m\vec{a} = -q\vec{\nabla}\phi - \frac{q}{c}\frac{\partial \vec{A}}{\partial t} + \frac{q}{c}\underbrace{\left[\vec{\nabla}(\vec{v}\cdot\vec{A}) - (\vec{v}\cdot\vec{\nabla})\vec{A}\right]}_{\vec{v}\times(\vec{\nabla}\times\vec{A})}
$$

(isso é uma identidade do cálculo vetorial). Usando de novo os campos $\vec{E}$ e $\vec{B}$:

$$
m\vec{a} = q\vec{E} + \frac{q}{c}\vec{v}\times\vec{B}
$$

Para o problema da carga interagindo com um campo EM usamos, portanto,

$$
\boxed{\mathcal{L} = \frac{1}{2} m \vec{v}^2 - q\phi + \frac{q}{c}\vec{v}\cdot\vec{A}}
$$

onde $\phi$ e $\vec{A}$ devem corresponder aos campos $\vec{E}$ e $\vec{B}$ aos quais a carga está submetida.

**Obs:** Veja que aqui $\mathcal{L} \neq T - V$; de fato não há uma energia potencial eletromagnética definida nesse problema.

**Exemplo:** Campo magnético uniforme $\vec{B} = B_0\hat{k}$, campo elétrico nulo $\vec{E} = 0$.

Podemos usar:

$$
\left\{\vec{A} = -\frac{1}{2}(B_0 y)\hat{i} + \frac{1}{2}(B_0 x)\hat{j}, \quad \phi = 0\right\}
$$

ou

$$
\left\{\vec{A}' = (B_0 x)\hat{j}, \quad \phi' = 0\right\}
$$

Verifique que as duas escolhas levam a $\vec{E} = 0$ e $\vec{B} = B_0\hat{k}$.

Temos 2 opções equivalentes de Lagrangiana:

$$
\mathcal{L} = \frac{1}{2} m(\dot{x}^2 + \dot{y}^2 + \dot{z}^2) + \frac{qB_0}{c}\cdot\frac{(-\dot{x}y + \dot{y}x)}{2}
$$

ou

$$
\mathcal{L}' = \frac{1}{2} m(\dot{x}^2 + \dot{y}^2 + \dot{z}^2) + \frac{qB_0}{c}(x\dot{y})
$$

Veja que a diferença $\mathcal{L}' - \mathcal{L} = \dfrac{qB_0}{2c}(x\dot{y} + y\dot{x})$ é uma derivada temporal,

$$
\mathcal{L}' - \mathcal{L} = \frac{d}{dt}\left(\frac{qB_0}{2c}xy\right)
$$

e derivadas temporais não alteram as equações de Euler-Lagrange $\Rightarrow$ por isso $\mathcal{L}$ e $\mathcal{L}'$ conduzem às mesmas equações de movimento!

> Na verdade isso sempre acontece: se temos $\vec{A}' - \vec{A} = \vec{\nabla}\chi$ e $\phi' - \phi = -\dfrac{1}{c}\dfrac{\partial \chi}{\partial t}$, então
>
> $$
> \mathcal{L}' - \mathcal{L} = \frac{q}{c}\frac{\partial \chi}{\partial t} + \frac{q}{c}\vec{v}\cdot\vec{\nabla}\chi = \underbrace{\frac{d}{dt}\left(\frac{q}{c}\chi(\vec{r}, t)\right)}_{\text{derivada total}}
> $$

## Problema de 2 Corpos Interagentes

Além do problema de uma carga em um campo EM, veremos também o problema de duas massas $m_1$ e $m_2$ interagindo por meio de um potencial $V(\vec{r}_1 - \vec{r}_2)$ (o potencial de interação não depende de $\vec{r}_1$ e $\vec{r}_2$ separadamente).

**Exemplo:**

$$
V(\vec{r}_1 - \vec{r}_2) = \frac{q_1 q_2}{4\pi\epsilon_0}\frac{1}{|\vec{r}_1 - \vec{r}_2|}
$$

Temos:

$$
\mathcal{L}(\vec{r}_1, \vec{r}_2, \dot{\vec{r}}_1, \dot{\vec{r}}_2) = \frac{1}{2} m_1 \dot{\vec{r}}_1^2 + \frac{1}{2} m_2 \dot{\vec{r}}_2^2 - V(\vec{r}_1 - \vec{r}_2)
$$

É conveniente usar outras 6 coordenadas:

$$
\vec{r} = \vec{r}_1 - \vec{r}_2 \qquad \text{e} \qquad \vec{R} = \frac{m_1\vec{r}_1 + m_2\vec{r}_2}{m_1 + m_2} \quad \text{(centro de massa)}
$$

Invertendo as relações:

$$
\vec{r}_1 = \vec{R} + \frac{m_2}{m_1+m_2}\vec{r} \qquad\qquad \vec{r}_2 = \vec{R} - \frac{m_1}{m_1+m_2}\vec{r} \qquad (*)
$$

Tomando a derivada e levando na expressão de $\mathcal{L}$:

$$
\mathcal{L}(\vec{R}, \dot{\vec{R}}, \vec{r}, \dot{\vec{r}}) = \frac{1}{2}(m_1+m_2)\dot{\vec{R}}^2 + \frac{1}{2}\frac{m_1 m_2}{m_1+m_2}\dot{\vec{r}}^2 - V(\vec{r})
$$

As 3 coordenadas $\vec{R}$ são cíclicas e

$$
(m_1+m_2)\dot{\vec{R}} = \text{const} \qquad \text{(o centro de massa tem velocidade constante)}
$$

Geralmente colocamo-nos em um referencial onde $\dot{\vec{R}} = 0$ e eliminamos o centro de massa do problema.

$$
\boxed{\mathcal{L}(\vec{r}, \dot{\vec{r}}) = \frac{1}{2}\mu\dot{\vec{r}}^2 - V(\vec{r})}
$$

onde $\mu = \dfrac{m_1 m_2}{m_1+m_2}$ é a massa reduzida e $V(\vec{r})$ é o potencial original.

Determinando $\vec{r}(t)$, podemos reconstituir $\vec{r}_1(t)$ e $\vec{r}_2(t)$ por $(*)$.
