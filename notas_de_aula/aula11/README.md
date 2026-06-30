# (11ª aula) — Os Postulados da Mecânica Quântica (Seções 4.1 e 4.2)

Após a introdução à matemática dos espaços vetoriais, estamos prontos para começar a discutir a Mecânica Quântica.

Como vimos na aula anterior, a descrição da dinâmica de elétrons, prótons, átomos etc. deve ser feita de uma maneira diferente da usada para descrever o movimento de satélites, bolas de gude, piões etc.

Assim como no curso de Mecânica Clássica você aprendeu a descrever o movimento de objetos macroscópicos sob influência de forças externas (resolvendo $F=ma$ ou as equações de Lagrange), aqui você irá descrever o movimento de partículas MICROSCÓPICAS *(Note que aquelas que são inevitavelmente perturbadas pela medida.)* sob influência de forças.

Considere os 4 "postulados" abaixo, usados na Mecânica Clássica e na Mecânica Quântica para descrever uma partícula que se move em 1D sob a influência de forças (conservativas).

## Postulado I

**MECÂNICA CLÁSSICA:** O estado da partícula em qualquer tempo é especificado por $x(t)$ e $p(t)$.

**MECÂNICA QUÂNTICA:** O estado da partícula é especificado por um vetor $|\psi(t)\rangle$ no espaço vetorial das funções complexas em 1D.

> **Observação:** Veja a diferença: passamos de 2 funções do tempo para um vetor abstrato que evolui no tempo (daí a necessidade de se saber bem a matemática dos ESPAÇOS VETORIAIS).

## Postulado II

**MECÂNICA CLÁSSICA:** Toda variável dinâmica é uma função de $x$ e $p$: $\omega = \omega(x,p)$.

**MECÂNICA QUÂNTICA:** As variáveis $x$ e $p$ da Mecânica Clássica são representadas por OPERADORES HERMITIANOS $\hat{X}$ e $\hat{P} = \hbar \hat{K}$ (definidos na seção 1.10). O operador hermitiano associado a uma outra variável dinâmica é obtido da expressão clássica:

$$\hat{\Omega} = \omega(x \rightarrow \hat{X},\ p \rightarrow \hat{P})$$

> **Observação:** O operador momentum linear é $\hat{P} = \hbar \hat{K}$, onde $\hbar = \dfrac{h}{2\pi}$ e $\hat{K}$ é o operador definido na seção 1.10.

> **Observação:** "Variável dinâmica" pode ser o momento angular, a Hamiltoniana, o momento linear, a posição, a velocidade; QUALQUER COISA QUE POSSA SER ESCRITA EM FUNÇÃO DE $x$ E $p$.

> **Observação:** Como exemplo, a função Hamiltoniana do oscilador harmônico é
>
> $$H(x,p) = \frac{p^2}{2m} + \frac{1}{2}m\omega^2 x^2,$$
>
> o operador correspondente na Mecânica Quântica é
>
> $$\hat{H} = \frac{\hat{P}^2}{2m} + \frac{1}{2}m\omega^2 \hat{X}^2.$$

## Postulado III

**MECÂNICA CLÁSSICA:** Se a partícula está no estado $(x,p)$, a medida da variável $\omega$ resultará em $\omega(x,p)$. O estado da partícula NÃO é alterado pela medida.

**MECÂNICA QUÂNTICA:** Se a partícula está no estado $|\psi\rangle$, a medida de $\hat{\Omega}$ resultará em um dos AUTOVALORES do operador $\hat{\Omega}$. A PROBABILIDADE de se obter um dos autovalores na medida é proporcional a $\left|\hat{P}_{\omega_i}|\psi\rangle\right|^2$ (a norma ao quadrado da PROJEÇÃO de $|\psi\rangle$ no subespaço do autovalor $\omega_i$), onde $\hat{P}_{\omega_i}$ é o PROJETOR no subespaço do autovalor $\omega_i$. Após a medida que produziu $\omega_i$ como resultado, o estado da partícula passa a ser $\hat{P}_{\omega_i}|\psi\rangle$ (esse é o colapso do vetor de estado).

> **Observação:** Em ambos os casos (tanto na Mecânica Clássica quanto na Mecânica Quântica) a "medida de $\omega$" se refere a uma MEDIDA IDEAL (a ser definida mais adiante). A Mecânica Quântica diz que, mesmo uma medida ideal perturba o estado de elétrons, prótons, etc.

> **Observação:** O postulado III da Mecânica Quântica diz exatamente como uma medida ideal perturba o estado da partícula.

> **Observação:** O postulado III diz que, conhecendo $|\psi\rangle$, só podemos saber a PROBABILIDADE do resultado da medida de $\hat{\Omega}$ resultar em $\omega_i$ (um dos autovalores).

Imagine que o operador $\hat{\Omega}$ tenha 3 autovalores $\{\omega_1, \omega_2, \omega_3\}$. Uma série de medidas de $\hat{\Omega}$ no mesmo estado $|\psi\rangle$ resultaria em algo como o diagrama abaixo, onde cada medida individual produz um dos três autovalores, de forma aparentemente aleatória, em função do número da medida:

```
ω3 :       ×    × × ×   ×
ω2 :    ×            × ×
ω1 :      × ×
       1  2  3  4  5  6  7  8 ... (# da medida)
```

NÃO HÁ COMO PREVER O RESULTADO DE UMA MEDIDA EM PARTICULAR, apenas podemos prever a DISTRIBUIÇÃO dos resultados de UMA SÉRIE DE MEDIDAS.

Lembre dos fótons ou elétrons formando as franjas de interferência do experimento de fenda dupla. Lá também é impossível prever onde um determinado fóton ou elétron irá aparecer, apenas é mais provável que ele apareça num máximo da figura de interferência do que em um mínimo.

No caso da variável $\hat{\Omega}$ acima, se $\left|\hat{P}_{\omega_3}|\psi\rangle\right|^2 > \left|\hat{P}_{\omega_1}|\psi\rangle\right|^2$, o resultado $\omega_3$ será mais obtido (em uma série de medidas) que o resultado $\omega_1$.

> **Observação:** É desse postulado que vem a QUANTIZAÇÃO. As variáveis clássicas $\omega(x,p)$ são funções contínuas que podem assumir qualquer valor real (talvez em algum intervalo limitado), no entanto, o operador associado $\hat{\Omega}$ pode ter um espectro discreto $\{\omega_1, \omega_2, \dots\}$ e, dessa forma, só admitir CERTOS VALORES como resultado da medida de $\hat{\Omega}$.

## Postulado IV

**MECÂNICA CLÁSSICA:** As variáveis $x$ e $p$ mudam com o tempo de acordo com

$$\dot{x} = \frac{\partial H}{\partial p}, \qquad \dot{p} = -\frac{\partial H}{\partial x},$$

onde $H(x,p)$ é a função Hamiltoniana.

**MECÂNICA QUÂNTICA:** O estado $|\psi(t)\rangle$ evolui no tempo de acordo com a Equação de Schrödinger

$$i\hbar \frac{d}{dt}|\psi(t)\rangle = \hat{H}|\psi(t)\rangle,$$

onde $\hat{H}$ é o operador Hamiltoniano obtido de $\hat{H} = H(x \rightarrow \hat{X},\ p \rightarrow \hat{P})$.

> **Observação:** Note o papel central desempenhado pela função Hamiltoniana na Mecânica Clássica e pelo operador Hamiltoniano na Mecânica Quântica. Por exemplo, para uma partícula de massa $m$ submetida a um potencial harmônico, usamos:
>
> $$H(x,p) = \frac{p^2}{2m} + \frac{1}{2}m\omega^2 x^2 \qquad \text{nas Eqs. de Hamilton,}$$
>
> $$\hat{H} = \frac{\hat{P}^2}{2m} + \frac{1}{2}m\omega^2 \hat{X}^2 \qquad \text{na Eq. de Schrödinger.}$$

## Discussão dos postulados I, II e III

### Postulado I

O espaço vetorial da Mecânica Quântica é o espaço das funções complexas (em 1D, se a partícula se move em 1D, ou em 3D se ela se move em 3D). Esse espaço contém:

i) funções próprias ou normalizáveis

$$\langle \psi|\psi\rangle = \int_{-\infty}^{\infty} \psi^*(x)\psi(x)\, dx < \infty;$$

ii) funções impróprias, não normalizáveis, mas que não divergem no infinito.

Os estados físicos (possíveis de serem produzidos em laboratório) são NORMALIZÁVEIS. Os estados impróprios aparecem como autoestados de certos operadores.

A FUNÇÃO DE ONDA é

$$\psi(x,t) = \langle x|\psi(t)\rangle \qquad \text{(em 1D)}.$$

### Postulados II e III

Suponha que o operador $\hat{\Omega}$ associado a uma variável $\omega(x,p)$ foi construído. Pelo postulado II ele deve ser Hermitiano, portanto seus autovetores podem ser ortonormalizados.

- Vamos encontrar operadores com ESPECTRO DISCRETO (os autovalores vão poder ser associados a números inteiros chamados NÚMEROS QUÂNTICOS)

  $$\langle \omega_i|\omega_j\rangle = \delta_{ij} \qquad \text{(ortonormalização)}.$$

- Vamos encontrar também operadores com ESPECTRO CONTÍNUO *(São os autovetores associados à parte contínua do espectro que são impróprios.)* (os autovalores caem em uma faixa de números reais). Exemplos são os operadores $\hat{X}$ e $\hat{K}$.

  $$\langle \omega|\omega'\rangle = \delta(\omega - \omega') \qquad \text{(ortonormalização)}.$$

- Vamos encontrar operadores com uma parte do espectro discreta e outra parte contínua (espectros **mistos**).

Com autovetores ortonormalizados construímos os PROJETORES do postulado III.

Se o espectro de $\hat{\Omega}$ é discreto temos

$$\hat{I} = \sum_{i}\sum_{\alpha} |\omega_i,\alpha\rangle\langle\omega_i,\alpha|, \qquad \hat{P}_{\omega_i} = \sum_{\alpha} |\omega_i,\alpha\rangle\langle\omega_i,\alpha|,$$

onde o índice $i$ é o índice do autovalor e o índice $\alpha$ é o índice de eventuais degenerescências, e $\hat{P}_{\omega_i}$ é o projetor associado ao autovalor $\omega_i$.

A probabilidade de obtermos o autovalor $\omega_i$ ao medirmos $\hat{\Omega}$ no estado $|\psi\rangle$ é

$$P(\omega_i) = N \left|\hat{P}_{\omega_i}|\psi\rangle\right|^2 = N\langle\psi|\hat{P}_{\omega_i}^\dagger \hat{P}_{\omega_i}|\psi\rangle = N\langle\psi|\hat{P}_{\omega_i}|\psi\rangle,$$

onde usamos que $\hat{P}_{\omega_i}$ é Hermitiano e idempotente, e $N$ é a constante de proporcionalidade.

A soma das probabilidades associadas a todos os autovalores deve ser igual a 1. Isso determina $N$:

$$1 = \sum_i P(\omega_i) = N \sum_i \langle\psi|\sum_\alpha |\omega_i,\alpha\rangle\langle\omega_i,\alpha|\psi\rangle = N\langle\psi|\psi\rangle.$$

Finalmente,

$$P(\omega_i) = \frac{\langle\psi|\hat{P}_{\omega_i}|\psi\rangle}{\langle\psi|\psi\rangle}$$

é a probabilidade de encontrar $\omega_i$, medindo $\hat{\Omega}$ no estado $|\psi\rangle$.

> **Observação:** Se $\hat{P}_{\omega_i}|\psi\rangle = |\psi\rangle$, o resultado da medida de $\hat{\Omega}$ resulta em $\omega_i$ em 100% das medidas ($|\psi\rangle$ pertence ao subespaço do autovalor $\omega_i$).

> **Observação:** Se
>
> $$|\psi\rangle = \frac{\alpha|\omega_1\rangle + \beta|\omega_2\rangle}{\sqrt{|\alpha|^2 + |\beta|^2}} \qquad \text{(normalizado)},$$
>
> a medida de $\hat{\Omega}$ resulta em:
>
> - $\omega_1$, com probabilidade $\dfrac{|\alpha|^2}{|\alpha|^2 + |\beta|^2}$,
> - $\omega_2$, com probabilidade $\dfrac{|\beta|^2}{|\alpha|^2 + |\beta|^2}$,
>
> e nenhum outro autovalor pode ser obtido.

> **Observação:** Quando expandimos $|\psi\rangle$ na base de autovetores de $\hat{\Omega}$, os coeficientes da expansão fornecem diretamente as probabilidades:
>
> $$|\psi\rangle = \sum_i \sum_\alpha \underbrace{\langle\omega_i,\alpha|\psi\rangle}_{c_{i,\alpha}} |\omega_i,\alpha\rangle \quad \Longrightarrow \quad P(\omega_i) = \frac{\sum_\alpha |c_{i,\alpha}|^2}{\langle\psi|\psi\rangle}.$$

**Exemplo:** Suponha

$$|\psi\rangle = \frac{1}{2}|\omega_1\rangle + \frac{1}{2}|\omega_2\rangle + \frac{1}{\sqrt{2}}|\omega_3\rangle,$$

onde $\{|\omega_i\rangle\}$ é uma base ortonormal. Verifique que $|\psi\rangle$ está normalizado:

$$\langle\psi|\psi\rangle = \left(\frac{1}{2}\right)^2 + \left(\frac{1}{2}\right)^2 + \left(\frac{1}{\sqrt{2}}\right)^2 = \frac{1}{4} + \frac{1}{4} + \frac{1}{2} = 1.$$

Os únicos resultados possíveis de serem obtidos medindo $\hat{\Omega}$ são:

- $\omega_1$, com prob. $1/4$,
- $\omega_2$, com prob. $1/4$,
- $\omega_3$, com prob. $1/2$,

($\omega_4, \omega_5$, etc., se existirem, não serão medidos).

## Complicações

**1) Em algumas situações a receita para se construir o operador $\hat{\Omega}$ é ambígua.**

Se $\omega(x,p) = xp$, devemos usar $\hat{\Omega}_1 = \hat{X}\hat{P}$ ou $\hat{\Omega}_2 = \hat{P}\hat{X}$? Na verdade, nenhum dos dois é Hermitiano:

$$\hat{\Omega}_1^\dagger = \hat{P}^\dagger \hat{X}^\dagger = \hat{P}\hat{X} \neq \hat{\Omega}_1 \qquad \text{(mesmo para } \hat{\Omega}_2\text{)}.$$

Usamos a combinação simétrica e Hermitiana:

$$\hat{\Omega} = \frac{1}{2}\left(\hat{X}\hat{P} + \hat{P}\hat{X}\right)$$

**2) O espectro de $\hat{\Omega}$ tem uma parte CONTÍNUA.**

Nesse caso não faz sentido perguntar qual a probabilidade de encontrar o valor $\omega$ (pertencente ao espectro contínuo) em uma medida de $\hat{\Omega}$, simplesmente porque nenhum aparelho de medida será capaz de selecionar um número real específico em uma faixa de valores possíveis.

*(Diagrama: reta numérica do eixo $\omega$ marcando os pontos $\omega_a$ e $\omega_b$, com uma chave indicando a "faixa de autovalores do operador $\hat{\Omega}$" entre eles.)*

Perguntamos qual a probabilidade de, medindo $\hat{\Omega}$, encontrar um resultado em uma FAIXA $[\omega_1,\omega_2]$ dentro do espectro contínuo.

Exatamente como no caso do espectro discreto, a probabilidade é obtida de um projetor:

$$\hat{P}_{[\omega_1,\omega_2]} = \int_{\omega_1}^{\omega_2} |\omega\rangle\langle\omega|\, d\omega,$$

que projeta um estado no subespaço gerado pelos autovetores de $\hat{\Omega}$ com autovalor entre $\omega_1$ e $\omega_2$.

> **Observação:** Estou supondo que os autovetores de $\hat{\Omega}$ estão normalizados no sentido da função delta de Dirac, $\langle\omega|\omega'\rangle = \delta(\omega-\omega')$.

$$P([\omega_1,\omega_2]) = \frac{\left|\hat{P}_{[\omega_1,\omega_2]}|\psi\rangle\right|^2}{\langle\psi|\psi\rangle} = \frac{\displaystyle\int_{\omega_1}^{\omega_2} \langle\psi|\omega\rangle\langle\omega|\psi\rangle\, d\omega}{\langle\psi|\psi\rangle}$$

Caso $\langle\psi|\psi\rangle = 1$, interpretamos $|\langle\omega|\psi\rangle|^2$ como DENSIDADE DE PROBABILIDADE, com dimensão de $[\omega]^{-1}$.

> **Observação:** Apenas quando os autovetores impróprios estão normalizados no sentido da função delta de Dirac os projetores se escrevem como $\displaystyle\int d\omega\, |\omega\rangle\langle\omega|$.

A probabilidade de obter QUALQUER RESULTADO POSSÍVEL deve ser 1. De fato (admitindo $\langle\psi|\psi\rangle=1$):

$$P([\omega_a,\omega_b]) = \underbrace{\int_{\omega_a}^{\omega_b} d\omega\, |\langle\omega|\psi\rangle|^2}_{\text{integral sobre todos os valores possíveis de }\omega \text{ (conjunto completo dos autovalores de }\hat{\Omega}\text{)}}$$

$$= \int_{\omega_a}^{\omega_b} d\omega\, \langle\psi|\omega\rangle\langle\omega|\psi\rangle$$

$$= \langle\psi|\hat{I}|\psi\rangle = 1.$$

> **Observação:** Aqui usei $\hat{I} = \displaystyle\int_{\omega_a}^{\omega_b} d\omega\, |\omega\rangle\langle\omega|$, válida se $\langle\omega|\omega'\rangle = \delta(\omega-\omega')$.

**Exemplo:** Qual a probabilidade de encontrar o elétron, no estado (normalizado) $|\psi\rangle$, entre $x=a$ e $x=b$?

$$P([a,b]) = \int_a^b dx\, |\langle x|\psi\rangle|^2 = \int_a^b dx\, |\psi(x)|^2,$$

onde $|x\rangle$ são os autovetores do operador $\hat{X}$ associados à faixa de autovalores da medida, e $|\psi(x)|^2$ é o quadrado da função de onda.

**3)** Veremos o exemplo de um operador, o spin, que não tem uma variável clássica associada. Nesse caso o experimento irá nos dizer como construir o operador quântico.

## Colapso do vetor de estado

O postulado III diz que, após medir $\hat{\Omega}$ e encontrar o resultado $\omega_i$ (no caso discreto), ou um resultado na faixa $[\omega_1,\omega_2]$ (no caso contínuo), o vetor de estado da partícula passa a ser a projeção de $|\psi\rangle$ no subespaço associado ao resultado da medida *(Salvo pela necessária renormalização do vetor de estado.)*:

$$\hat{P}_{\omega_i}|\psi\rangle = \sum_\alpha |\omega_i,\alpha\rangle\langle\omega_i,\alpha|\psi\rangle \qquad \text{(caso discreto)}$$

$$\hat{P}_{[\omega_1,\omega_2]}|\psi\rangle = \int_{\omega_1}^{\omega_2} d\omega\, |\omega\rangle\langle\omega|\psi\rangle \qquad \text{(caso contínuo)}$$

As "medidas" a que se referem os postulados são medidas idealmente precisas e não perturbadoras do estado do sistema. Na prática elas quase sempre envolvem a interação com a radiação eletromagnética.

## Medida ideal de momentum

*(Diagrama: uma partícula de momentum bem definido $p$ é atingida por um fóton de frequência $\omega$ (ANTES); depois do espalhamento Compton, a partícula tem momentum $p'$ e o fóton espalhado tem frequência $\omega'$ (DEPOIS).)*

Para esse espalhamento Compton ser uma medida ideal de momentum, ele não pode alterar o momentum da partícula, pois, de acordo com o postulado, se a partícula tem um momentum bem definido (está no estado $|\psi\rangle = |p\rangle$) *(Na verdade, uma faixa estreita em torno de $p$, pois o operador $\hat{P} = \hbar\hat{K}$ tem espectro contínuo.)*, uma medida de momentum só pode resultar em $p$ e o estado do sistema NÃO IRÁ SE ALTERAR (pois já é um dos autovetores do operador $\hat{P}$).

O momentum do fóton é $\dfrac{\hbar\omega}{c}$ (sua energia $\div\, c$):

$$p - \frac{\hbar\omega}{c} = p' + \frac{\hbar\omega'}{c} \qquad \text{(cons. momentum)}$$

$$\underbrace{\sqrt{p^2c^2 + m^2c^4}}_{\text{energia inicial da partícula (relativística)}} + \hbar\omega = \sqrt{p'^2c^2 + m^2c^4} + \hbar\omega' \qquad \text{(cons. energia)}$$

Aqui você mede $\omega$ e $\omega'$ e, dessas equações, obtém $p$ e $p'$.

Uma medida ideal deve usar um fóton de frequência $\omega$ que permita $p \approx p'$ (i.e., que não altere o valor de $p$, mas que ainda permita determiná-lo).

É fácil ver que se $\omega \to 0$, $p' \to p$ (momentum da partícula não é alterado). Isso seria uma medida ideal de momentum.

UMA MEDIDA IDEAL É AQUELA QUE NÃO ALTERA O ESTADO DO SISTEMA QUANDO ESSE ESTADO É UM DOS AUTOVETORES DO OPERADOR $\hat{\Omega}$.

Uma medida ideal de posição no estado $|p\rangle$ (autovetor do operador $\hat{P}$) altera o estado, pois $|p\rangle$ não é autoestado do operador $\hat{X}$.

Isso é o que o postulado III diz, mas por que deve ser assim? Porque uma medida ideal de posição usa fótons de momentum arbitrariamente grande *(Correspondentes a uma radiação com comprimento de onda muito pequeno.)* e que alteram completamente um estado como $|p\rangle$ (mas não alterariam um estado de posição definida como $|x\rangle$).

UMA MEDIDA IDEAL DE $\hat{\Omega}$ DEIXA APENAS OS AUTOVETORES DO OPERADOR $\hat{\Omega}$ INALTERADOS. OUTROS VETORES SÃO ALTERADOS.

"Medida", no nosso curso, será sempre "medida ideal" no sentido acima.

"Medida Ideal" para a Mecânica Clássica deixa QUALQUER estado $(x,p)$ inalterado, pois para objetos clássicos é possível encontrar uma radiação eletromagnética que permite determinar a posição e o momentum da partícula sem alterar nenhum dos dois (para átomos, elétrons, etc. isso não é possível).
