# (17ª aula) — Partícula sob Força Constante

## Partícula sob Força Constante

Um outro potencial que permite solução exata em 1D é $V(x) = -Fx$, o potencial de uma força constante.

Em Mecânica Clássica discutimos esse potencial quando estudamos o problema da queda livre, por exemplo.

## Mecânica Clássica

$$
H(x,p) = \frac{p^2}{2m} - Fx \qquad (F \text{ constante})
$$

$$
\dot{x} = \frac{p}{m} \qquad \text{e} \qquad \dot{p} = F
$$

são as equações de Hamilton.

Eliminando $p(t)$ encontramos a equação de Newton

$$
\ddot{x} = \frac{F}{m} \quad \Longrightarrow \quad
\begin{cases}
x(t) = x(0) + \dot{x}(0)\, t + \dfrac{1}{2}\dfrac{F}{m} t^2 \\[2mm]
p(t) = m\dot{x} = \underbrace{m\dot{x}(0)}_{p_0} + Ft
\end{cases}
$$

Trata-se do movimento uniformemente acelerado. A energia total é conservada e pode ter qualquer valor em $(-\infty, \infty)$.

$$
E = \frac{p_0^2}{2m} - Fx_0
$$

## Mecânica Quântica

Esse potencial é interessante pois a equação de autovalor do operador $\hat{H}$ é mais facilmente resolvida na base $|p\rangle$ do que na base $|x\rangle$.

Da forma do potencial antecipamos um espectro contínuo, com $E \in (-\infty, \infty)$, e com autovalores **NÃO-DEGENERADOS**.

*(Diagrama: reta $V(x) = -Fx$ decrescente no plano $x$–$V(x)$, com uma linha horizontal indicando um nível de energia $E$ não degenerado.)*

$$
\left( \frac{\hat{p}^2}{2m} - F\hat{x} \right) |E\rangle = E\, |E\rangle
$$

Tomando o produto interno com $\langle p|$:

$$
\frac{p^2}{2m}\psi_E(p) - i\hbar F \frac{d\psi_E}{dp} = E\, \psi_E(p)
$$

Uma EDO do 1º grau, com solução

$$
\langle p|E\rangle = \psi_E(p) = A \exp\left[ \frac{iEp}{F\hbar} - \frac{ip^3}{6mF\hbar} \right]
$$

O fato de só aparecer 1 constante arbitrária (pois a EDO era de 1ª ordem) indica que o autovalor é **NÃO DEGENERADO**, como sabíamos.

Impomos a normalização $\langle E|E'\rangle = \delta(E - E')$:

$$
\begin{aligned}
\langle E|E'\rangle &= \int_{-\infty}^{\infty} dp\, \langle E|p\rangle\langle p|E'\rangle \\
&= \int_{-\infty}^{\infty} dp\, A^2\, e^{i(E'-E)p/F\hbar} = A^2\, 2\pi\, \delta\!\left( \frac{E'-E}{F\hbar} \right) \\
&= A^2\, 2\pi F\hbar\, \delta(E-E')
\end{aligned}
$$

Escolhemos $A = \sqrt{\dfrac{1}{2\pi\hbar F}}$ para obter a normalização desejada.

$$
\boxed{\psi_E(p) = \frac{1}{\sqrt{2\pi\hbar F}} \exp\left[ \frac{iEp}{F\hbar} - \frac{ip^3}{6mF\hbar} \right]}
$$

## Operador de Evolução na Base $|p\rangle$

Podemos obter o operador de evolução na base $|p\rangle$:

$$
\begin{aligned}
\langle p| e^{-i\hat{H}t/\hbar} |p'\rangle &= \int_{-\infty}^{\infty} dE\, e^{-iEt/\hbar} \langle p|E\rangle\langle E|p'\rangle \qquad \left( \hat{1} = \int_{-\infty}^{\infty} dE\, |E\rangle\langle E| \right) \\
&= \int_{-\infty}^{\infty} dE\, e^{-iEt/\hbar} \frac{1}{2\pi\hbar F} \exp\left[ \frac{iE(p-p')}{F\hbar} - i\frac{p^3 - p'^3}{6mF\hbar} \right] \\
&= \frac{2\pi}{2\pi\hbar F}\, \delta\!\left( \frac{p-p'}{F\hbar} - \frac{t}{\hbar} \right) e^{-i\frac{p^3-p'^3}{6mF\hbar}} \\
&= \delta(p - p' - Ft)\, e^{-i\frac{p^3-p'^3}{6mF\hbar}}
\end{aligned}
$$

Esse "propagador" não é o propagador usual, que é $\langle x| e^{-i\hat{H}t/\hbar} |x'\rangle$. Ele é usado quando temos $\langle p|\Psi(0)\rangle = \Psi(p,0)$, a função de onda inicial no **ESPAÇO p**.

$$
|\Psi(t)\rangle = e^{-i\hat{H}t/\hbar} |\Psi(0)\rangle
$$

$$
\langle p|\Psi(t)\rangle = \int_{-\infty}^{\infty} dp'\, \langle p| e^{-i\hat{H}t/\hbar} |p'\rangle \langle p'|\Psi(0)\rangle
$$

$$
\Psi(p,t) = \int_{-\infty}^{\infty} dp'\, \langle p| \hat{U}(t) |p'\rangle\, \Psi(p',0)
$$

## Exemplo: Pacote Gaussiano Inicial

Por exemplo, para o pacote inicial

$$
\langle x|\Psi(0)\rangle = \Psi(x,0) = \left( \frac{1}{\pi\Delta^2} \right)^{1/4} e^{ip_0 x/\hbar}\, e^{-x^2/2\Delta^2}
$$

Temos

$$
\begin{aligned}
\Psi(p,0) = \langle p|\Psi(0)\rangle &= \int_{-\infty}^{\infty} dx\, \langle p|x\rangle\langle x|\Psi(0)\rangle \\
&= \int_{-\infty}^{\infty} dx\, \frac{e^{-ipx/\hbar}}{\sqrt{2\pi\hbar}}\, \Psi(x,0) \\
&= \left( \frac{\Delta^2}{\hbar^2\pi} \right)^{1/4} \exp\left[ -\frac{(p-p_0)^2\Delta^2}{2\hbar^2} \right]
\end{aligned}
$$

Esse pacote inicial evolui com o tempo para

$$
\begin{aligned}
\Psi(p,t) &= \int_{-\infty}^{\infty} dp'\, \underbrace{\delta(p-p'-Ft)\, e^{-i\frac{p^3-p'^3}{6mF\hbar}}}_{\langle p|\hat{U}(t)|p'\rangle}\, \underbrace{\left( \frac{\Delta^2}{\hbar^2\pi} \right)^{1/4} e^{-\frac{(p'-p_0)^2\Delta^2}{2\hbar^2}}}_{\Psi(p',0)} \\
&= \left( \frac{\Delta^2}{\hbar^2\pi} \right)^{1/4} \exp\left[ -i\frac{p^3 - (p-Ft)^3}{6mF\hbar} - \frac{(p-Ft-p_0)^2\Delta^2}{2\hbar^2} \right]
\end{aligned}
$$

Vemos que a distribuição de momenta se desloca rigidamente no eixo $p$:

$$
|\Psi(p,t)|^2 = \left( \frac{\Delta^2}{\hbar^2\pi} \right)^{1/2} e^{-(p-Ft-p_0)^2\Delta^2/\hbar^2}
$$

*(Diagrama: dois pacotes gaussianos no eixo $p$, um centrado em $p_0$ no instante inicial e outro centrado em $p_0+Ft$ posteriormente, ambos com a mesma largura $\hbar/\Delta$.)*

A incerteza $\Delta p$ permanece inalterada e $\langle p \rangle = p_0 + Ft$.

A função de onda $\Psi(x,t)$ pode ser obtida de $\Psi(p,t)$:

$$
\Psi(x,t) = \int_{-\infty}^{\infty} dp\, \frac{e^{ipx/\hbar}}{\sqrt{2\pi\hbar}}\, \Psi(p,t)
$$

obtemos

$$
\boxed{ |\Psi(x,t)|^2 = \left( \frac{1}{\pi\Delta^2(t)} \right)^{1/2} \exp\left[ -\frac{\left( x - \dfrac{p_0 t}{m} - \dfrac{Ft^2}{2m} \right)^2}{\Delta^2(t)} \right] }
$$

onde, como no caso da partícula livre (ver aula 14),

$$
\boxed{ \Delta(t) = \sqrt{ \Delta^2 + \frac{\hbar^2 t^2}{m^2 \Delta^2} } }
$$

O centro do pacote é acelerado e a largura cresce, como no caso da partícula livre.

*(Diagrama: pacote gaussiano estreito centrado em $x_0$ com largura $\Delta$ no instante inicial, e pacote mais largo e deslocado centrado em $x_0 + \dfrac{p_0 t}{m} + \dfrac{Ft^2}{2m}$ com largura $\Delta(t)$.)*

> **Obs:** Veja que no limite $F \to 0$ reobtemos os resultados da partícula livre.

> **Obs:** Veja que a presença da força não altera a rapidez com que o pacote se alarga, $\Delta(t)$ não depende de $F$.

## Comparação com a Força Harmônica

Para efeito de comparação, o mesmo $\Psi(x,0)$ evoluindo sob a ação de uma força harmônica se torna (usando o propagador (7.3.28))

$$
\boxed{ |\Psi(x,t)|^2 = \left( \frac{1}{\pi\delta^2(t)} \right)^{1/2} \exp\left[ -\frac{(x - \frac{p_0}{m\omega}\sin\omega t)^2}{\delta^2(t)} \right] }
$$

onde

$$
\delta(t) = \sqrt{ \Delta^2 \cos^2\omega t + \frac{\hbar^2 \sin^2\omega t}{m^2\omega^2\Delta^2} }
$$

O centro do pacote segue a trajetória clássica de uma partícula lançada da origem com velocidade $p_0/m$.

A largura do pacote, $\delta(t)$, oscila com o tempo ao invés de crescer monotonamente como no caso da força constante.

*(Diagrama, caso 1: $\Delta^2 > \hbar/m\omega$ — gráfico de $\delta(t)$ oscilando entre o valor mínimo $\hbar/m\omega\Delta$ e o valor máximo $\Delta$, com período relacionado a $\pi/\omega$ e $2\pi/\omega$.)*

*(Diagrama, caso 2: $\Delta^2 < \hbar/m\omega$ — gráfico análogo, mas com os valores mínimo e máximo trocados: mínimo $\Delta$ e máximo $\hbar/m\omega\Delta$.)*

**Caso 1:** a sequência de pacotes ao longo do tempo é

*(Diagrama: sequência de quatro pacotes gaussianos ao longo do tempo —*
*em $t=0$, pacote estreito centrado em $0$ com largura $\Delta$;*
*em $t=\pi/2\omega$, pacote largo centrado em $p_0/m\omega$ com largura $\hbar/m\omega\Delta$;*
*em $t=\pi/\omega$, pacote estreito centrado em $0$ com largura $\Delta$ (refletido);*
*em $t=3\pi/2\omega$, pacote largo centrado em $-p_0/m\omega$ com largura $\hbar/m\omega\Delta$.)*

No caso 2, o pacote se alarga ao atingir o ponto de retorno.

Se o estado inicial fosse $\Psi(x,0) = \left( \dfrac{1}{\pi\Delta^2} \right)^{1/4} e^{-(x-x_0)^2/2\Delta^2}$, uma "partícula" deslocada da origem em "repouso", obteríamos

$$
|\Psi(x,t)|^2 = \left( \frac{1}{\pi\delta^2(t)} \right)^{1/2} \exp\left[ -\frac{(x - x_0\cos\omega t)^2}{\delta^2(t)} \right]
$$

com o mesmo $\delta(t)$.

No caso $\Delta^2 > \hbar/m\omega$ temos a sequência

*(Diagrama: sequência de três pacotes gaussianos —*
*em $t=0$, pacote estreito centrado em $-x_0$ com largura $\Delta$;*
*em $t=\pi/2\omega$, pacote largo centrado em $0$ com largura $\hbar/m\omega\Delta$;*
*em $t=\pi/\omega$, pacote estreito centrado em $x_0$ com largura $\Delta$.)*
