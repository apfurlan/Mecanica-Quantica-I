# Aula 1 — Introdução à Mecânica Quântica

## Contexto Histórico: A Física Clássica

Você aprendeu em Mecânica Clássica a obter a trajetória de partículas submetidas a forças conhecidas. Para uma partícula de massa $m$, resolve-se a equação de Newton:

$$m \frac{d^2 \mathbf{r}}{dt^2} = \mathbf{F}(\mathbf{r}, \mathbf{v}, t)$$

Do ponto de vista clássico e fundamental, apenas dois tipos de força atuam sobre uma partícula: a **força gravitacional** e a **força eletromagnética**, expressas em termos de campos:

$$\mathbf{F}_G(\mathbf{r}, t) = -m \nabla \phi(\mathbf{r}, t)$$

$$\mathbf{F}_{EM}(\mathbf{r}, \mathbf{v}, t) = q \left[ \mathbf{E}(\mathbf{r}, t) + \mathbf{v} \times \mathbf{B}(\mathbf{r}, t) \right]$$

Os campos eletromagnéticos satisfazem as **Equações de Maxwell**:

$$\nabla \cdot \mathbf{E} = \frac{\rho}{\varepsilon_0}, \quad \nabla \times \mathbf{E} + \frac{1}{c}\frac{\partial \mathbf{B}}{\partial t} = 0$$

$$\nabla \cdot \mathbf{B} = 0, \quad \nabla \times \mathbf{B} - \frac{1}{c}\frac{\partial \mathbf{E}}{\partial t} = \frac{\mathbf{j}}{c\varepsilon_0}$$

Essas equações com as equações de Newton constituem a **Física Clássica**.

## Por que a Mecânica Quântica?

A MQ foi necessária por limitações fundamentais da MC ao tratar sistemas em escala atômica:

### 1. Espectros Atômicos

A Física Clássica não consegue explicar o espectro de emissão do hidrogênio (série de Balmer, 1885):

$$\frac{1}{\lambda} = R_H \left(\frac{1}{n_f^2} - \frac{1}{n_i^2}\right), \quad R_H = 1{,}097 \times 10^7\ \text{m}^{-1}$$

com $n_i, n_f$ inteiros. A explicação clássica preveria radiação contínua e colapso do elétron em espiral para o núcleo.

### 2. O Modelo de Rutherford e o Problema de Estabilidade

O modelo de Rutherford (1911): o átomo tem um núcleo pequeno e denso, com elétrons orbitando ao redor. Mas elétrons acelerados radiam energia (Maxwell), logo a órbita deveria ser instável.

### 3. Dualidade Onda-Partícula

- **Fóton (Einstein, 1905):** A luz, embora seja uma onda, se comporta como partícula com $E = h\nu$ ao interagir com a matéria (efeito fotoelétrico).
- **Elétron (de Broglie, 1924):** Partículas como o elétron exibem comportamento ondulatório com comprimento de onda $\lambda = h/p$.

### 4. O Problema da Medição

Na MQ, a medição perturba o sistema. Não é possível medir posição e momento simultaneamente com precisão arbitrária (Princípio da Incerteza de Heisenberg):

$$\Delta x \cdot \Delta p \geq \frac{\hbar}{2}$$

## Estrutura da Mecânica Quântica

Na MQ, o **estado** de um sistema é representado não por $({\mathbf{r}}(t), {\mathbf{p}}(t))$, mas por um vetor em um espaço vetorial chamado **espaço de Hilbert**, denotado $|\psi(t)\rangle$.

A evolução desse estado é governada pela **Equação de Schrödinger**:

$$i\hbar \frac{d}{dt} |\psi(t)\rangle = \hat{H} |\psi(t)\rangle$$

onde $\hat{H}$ é o **operador Hamiltoniano**.

> A ferramenta matemática central da MQ é a **Álgebra Linear** — o objeto que estudaremos nas próximas aulas.
