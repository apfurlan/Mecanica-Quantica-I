# (10ª aula) — Problemas com a Mecânica Clássica e Dualidade Onda-Partícula (cap. 3)

## Problemas com a Mecânica Clássica

Vimos na 1ª aula um apanhado dos problemas que apontavam para a inadequação da Mecânica Clássica para descrever certos resultados experimentais.

**Física Atômica:**

- (i) Por que os átomos, quando excitados, só emitem radiação EM em certas frequências bem definidas? (problema do espectro atômico)
- (ii) Por que os elétrons dos átomos, atraídos pelo núcleo positivo, não emitem continuamente radiação e colapsam no interior do núcleo? (problema da estabilidade da matéria)

Esses problemas não podem ser solucionados caso se insista em descrever o movimento dos elétrons de maneira clássica, através de uma trajetória $\vec{r}(t)$ que obedeça à Eq. de Newton, $\vec{F} = m\ddot{\vec{r}}$.

A evidência mais concreta da necessidade de se usar outro tipo de descrição para a dinâmica de elétrons veio da experiência de Davisson e Germer ($\sim 1925$), que mostrou que elétrons se **difratavam** quando incidentes em uma superfície metálica. Vamos discutir essa experiência (ou uma versão idealizada dela) na aula de hoje.

Com respeito à **radiação EM**, os problemas que não tinham explicação clássica (em termos de uma onda dos campos $\vec{E}$ e $\vec{B}$) eram (entre outros):

- (i) Problema da radiação emitida por um corpo à temperatura $T$
- (ii) Problema do efeito fotoelétrico
- (iii) Problema do espalhamento Compton

Esses três fenômenos evidenciavam que a radiação EM carrega energia e momentum em "pacotes", relacionados à frequência e ao comprimento de onda por

$$
E = h\nu \qquad \text{e} \qquad p = \frac{h}{\lambda}
$$

O capítulo 3 do livro é dedicado a descrever um experimento idealizado que ilustra como a natureza **corpuscular** e **ondulatória** dos elétrons, fótons, prótons, átomos, etc., pode se manifestar simultaneamente.

## Partícula vs. Onda

Classicamente, um objeto da natureza é classificado ou como uma **PARTÍCULA** (localizado espacialmente, carrega energia e momentum), à qual se pode associar uma posição $\vec{r}(t)$ e uma velocidade $\vec{v}(t)$ em qualquer instante de tempo, ou como uma **ONDA** (perturbação que se estende por todo o espaço), à qual se pode associar um campo $\Psi(\vec{r}, t)$.

**Ondas planas** são um tipo de perturbação descrita, por exemplo, pelo campo

$$
\Psi(x,t) = A\cos(kx - \omega t)
$$

ou, em 3D,

$$
\Psi(\vec{r}, t) = A\cos(\vec{k}\cdot\vec{r} - \omega t)
$$

$k = 2\pi/\lambda$ é o vetor de onda, $\lambda$ é o comprimento de onda, $\omega = 2\pi\nu$ é a frequência angular e $\nu = 1/T$ é a frequência (inverso do período).

Em qualquer tempo, o valor de $\Psi$ em pontos espaçados de $\lambda$ é o mesmo (no caso 3D, o valor de $\Psi$ em planos perpendiculares ao vetor $\vec{k}$ e espaçados de $\lambda = 2\pi/|\vec{k}|$ é o mesmo, daí o nome "onda plana"). O valor de $\Psi$ em um dado ponto $\vec{r}$ se repete a cada $T$ segundos.

## Interferência: Experimento de Dupla Fenda

Ondas planas experimentam **INTERFERÊNCIA** quando forçadas a passar simultaneamente por 2 orifícios separados por uma distância $d \sim \lambda$.

*(diagrama: onda plana incidente com vetor de onda $\vec{k}$ atinge uma barreira com dois orifícios $S_1$ e $S_2$ separados por distância $d$; os sinais que saem de $S_1$ e $S_2$ se propagam até um anteparo a uma distância $D$, formando um padrão de interferência com franjas espaçadas de $\lambda D/d$.)*

Você já deve ter visto esse experimento com luz. As franjas claras e escuras são consequência da soma do sinal que passou por $S_1$ com o sinal que passou por $S_2$; como eles devem percorrer distâncias diferentes para chegar ao anteparo, em alguns pontos $\Psi_1 + \Psi_2 = 0$ e em outros $\Psi_1 + \Psi_2 = 2\Psi_1$. Como o sinal luminoso é proporcional ao **QUADRADO** do valor de $\Psi$ no ponto, se observam as franjas características.

Esse fenômeno, tipicamente ondulatório, permite concluir que a radiação EM deve ser descrita como **ONDA**.

## Mas e os fótons do efeito fotoelétrico?

Se você diminuir a intensidade da radiação incidente nos orifícios, você vê que a radiação chega ao anteparo em "pacotes". É irresistível imaginar que esses pacotes são partículas e, portanto, não deveriam exibir o padrão de interferência.

**No entanto**, mesmo chegando na forma de partícula, os fótons constroem o padrão de interferência quando os deixamos se acumular no anteparo.

**Conclusão:** A **ONDA** EM de alguma maneira governa a distribuição de suas **PARTÍCULAS** associadas. É possível determinar como a onda irá se distribuir no anteparo, mas é impossível saber onde os fótons irão aparecer. De algum modo, $|\vec{E}(\vec{r},t)|^2$ está relacionado à **PROBABILIDADE** de encontrar um fóton em $\vec{r}$ no instante $t$.

A isso se chama **dualidade onda-partícula**. A razão pela qual a natureza-partícula da radiação EM demorou tanto tempo para ser percebida está no fato de que, para intensidades encontradas no dia a dia, o número de fótons é tão grande que não há como perceber que eles chegam individualmente.

> **Exemplo:** Lâmpada de 100 W a 10 m de distância.
>
> *(diagrama: lâmpada emitindo luz a uma distância de 10 m de um olho observador.)*
>
> A intensidade que chega ao olho é
>
> $$
> I = \frac{100\,\text{W}}{4\pi(10\,\text{m})^2} = 7{,}96\times10^{-2}\ \text{J}/\text{m}^2\text{s}
> $$
>
> O raio da pupila é $r \sim 1\,\text{mm}$, então o número de fótons (suponha luz amarela, $\lambda = 5890\ \text{Å}$) que chega por segundo na retina é dado por
>
> $$
> \underbrace{\left(7{,}96\times10^{-2}\ \frac{\text{W}}{\text{m}^2}\right)\left(\pi(1\,\text{mm})^2\right)}_{\text{área da pupila}} = N \underbrace{\left(\frac{hc}{\lambda}\right)}_{\substack{\text{energia de}\\ \text{cada fóton}}}
> $$
>
> $$
> \boxed{N = 7{,}4\times10^{11}\ \text{fótons por segundo!}}
> $$

## Elétrons e a Dupla Fenda

Se fizermos a experiência dos dois orifícios com elétrons (ou átomos), cuja natureza-**PARTÍCULA** é absolutamente evidente, imaginamos que a interferência não poderá ser observada, uma vez que é preciso uma **ONDA** passando pelos 2 orifícios para haver interferência. (Isso é basicamente o que Davisson e Germer pensaram.)

**No entanto**, é obtido um padrão de interferência desde que o espaçamento dos orifícios seja $d \sim \lambda = h/p$.

Aqui $p$ é o momentum usual, $mv$, dos elétrons incidentes, e $\lambda = h/p$ é o comprimento de onda de **de Broglie**.

## Qual a ordem de grandeza de $\lambda$?

Um momentum típico de um elétron acelerado pela DDP de 1 Volt é:

*(diagrama: fonte de elétrons acelerados por uma diferença de potencial de 1 V, produzindo elétrons com velocidade $\vec{v}$ e energia cinética $K = 1\,\text{eV}$.)*

$$
\frac{p^2}{2m} = 1\,\text{eV} \quad \Longrightarrow \quad p = 5{,}4\times10^{-25}\ \text{kg}\cdot\text{m/s}
$$

$$
\lambda = \frac{h}{p} = 12{,}3\ \text{Å}
$$

Para ver a interferência, as fendas devem estar *muito* próximas ($d \sim 10\ \text{Å}$) (para a luz basta $d \sim 5000\ \text{Å}$).

*(diagrama: dois casos comparados — à esquerda, $d \sim \lambda \sim 12\,\text{Å}$ (comportamento ONDA), mostrando um padrão de interferência com franjas espaçadas de $2D\lambda/d$; à direita, $d \gg \lambda$, mostrando um único pico sem franjas visíveis.)*

No caso $d \gg \lambda$, você não consegue perceber as franjas de interferência, que ficam muito juntas.

**Obs:** Aqui você deve interpretar um máximo de interferência como um ponto do anteparo que recebe muitos elétrons.

**Obs:** A largura do envelope das franjas de interferência é determinada pela **LARGURA** dos orifícios, estou supondo que esta permanece a mesma.

As franjas de interferência muito próximas tornam a segunda situação ($d \gg \lambda$) indistinguível de uma distribuição de partículas de acordo com a curva envelope.

## O que seria esperado caso os elétrons se movessem como partículas, ao longo de trajetórias?

*(diagrama: elétrons incidem em uma barreira com dois orifícios $S_1$ e $S_2$; $I_1$ é a distribuição dos elétrons que passaram por $S_1$, $I_2$ a distribuição dos que passaram por $S_2$, e a curva $I_1 + I_2$ representa a soma das duas distribuições.)*

$I_1$ seria a distribuição das partículas que tivessem passado por $S_1$, e $I_2$ a distribuição das que tivessem passado por $S_2$. Como uma **PARTÍCULA** (diferente de uma **ONDA**) não pode passar pelos 2 orifícios, o resultado final deve ser a soma $I_1 + I_2$ (a curva tracejada), que é exatamente o envelope do caso $d \gg \lambda$ acima.

Elétrons e átomos podem exibir interferência e difração, apenas os orifícios e espaçamentos de orifícios devem ser **MUITO** pequenos. Para orifícios usuais não há como detectar os padrões de interferência, e o resultado pode ser entendido atribuindo-se uma natureza de **PARTÍCULA** aos elétrons.

No entanto, quando as condições são ajustadas com cuidado, podemos ver interferência e difração **EMBORA** os elétrons, como os fótons, cheguem ao anteparo como "pacotes".

> **Conclusão:** Assim como no caso dos fótons, os elétrons, prótons, átomos, etc., são governados por uma onda que sofre difração e interferência. Essa onda pode ser estudada e seu comportamento previsto (é o que faremos neste curso), mas seu conhecimento não permite prever onde os elétrons, átomos, etc., irão aparecer (exatamente como no caso dos fótons); trata-se de uma **ONDA DE PROBABILIDADE**! (sem ser muito rigoroso)

## Quando devo usar MQ? Ou: quando a natureza ondulatória se manifesta?

Sempre que a sua "partícula" (com licença de linguagem) estiver submetida a uma energia potencial (que reflete o ambiente com o qual ela interage) que varia apreciavelmente na escala de distância de seu comprimento de onda de de Broglie.

**Exemplo de difração:**

*(diagrama: dois casos comparados — à esquerda, $a \sim \lambda$ (comportamento ONDA), com fenda de largura $a$ produzindo um padrão de difração espaçado de $2D\lambda/a$; à direita, $a \gg \lambda$ (comportamento PARTÍCULA), com um único pico sem padrão de difração visível.)*
