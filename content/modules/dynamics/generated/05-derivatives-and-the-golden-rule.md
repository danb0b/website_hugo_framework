---
title: Derivatives and the Golden Rule
type: submodule
---

# Derivatives and the Golden Rule


$$
\frac{ {}^N{d\vec{v}}}{dt} = \frac{ {}^A{d\vec{v}}}{dt} + {}^N{\vec{w}}^{A} \times \vec{v}
$$

::: {style="text-align:center;"}
![double pendulum](../../../figures/dynamics/double_pendulum.png){height=3in}

![body moving through space](../../../figures/dynamics/body_in_space.png){height=3in}
:::


<!--
find the cartesian velocity of point q

$$\begin{aligned}
\vec{r}_1 &= x_1 \hat{n}_x + y_1 \hat{n}_y + z_1 \hat{n}_z \\
\vec{r}_2 &= x_2 \hat{n}_x + y_2 \hat{n}_y + z_2 \hat{n}_z \\
{}^N{\vec{\omega}}^{A} &= \omega_x \hat{n}_x + \omega_y \hat{n}_y + \omega_z \hat{n}_z
\end{aligned}$$



$$
\begin{array}{c|c c c}
  {}^N{R}^{A} & \hat{a}_x & \hat{a}_y & \hat{a}_z \\
  \hline
  \hat{n}_x &r_{11}&  r_{12}&r_{13} \\
  \hat{n}_y &r_{21}& r_{22} &r_{23} \\
  \hat{n}_z &r_{31}&r_{32}&r_{33}
 \end{array}
$$
-->

## Example


::: {style="text-align:center;"}
![pendulum](../../../figures/dynamics/pendulum.png){height="3in"}
:::


$$
\vec{r} = -l\hat{a}_y
$$
$$
\vec{v} =  \frac{ {}^N{d\vec{r}}}{dt} =\frac{ {}^{A} { d\vec{r}}}{dt} +  {}^{N}{\vec{\omega}}^{A} \times \vec{r}
$$
$$
\vec{v} = \frac{ {}^{N}{d\vec{r}}}{dt} = \dot{\theta}\hat{a}_z \times -l\hat{a}_y
$$
$$
\vec{v} = \frac{ {}^{N}{}{ d\vec{r}}{}{}}{dt}= l\dot{\theta}\hat{a}_x
$$
$$
\vec{a} = \frac{ {}^{N}{}{ d\vec{v}}{}{}}{dt} = \frac{ {}^{N}{}{d^2\vec{r}}{}{}}{dt^2}
$$
$$
\vec{a} =  \frac{ {}^{A}{}{d\vec{v}}{}{}}{dt} +  {}^{N}{}{\vec{\omega}}^{A}{} \times \vec{v}
$$
$$
\vec{a} = l\ddot{\theta}\hat{a}_x  + \dot{\theta}\hat{a}_z \times l\dot{\theta}\hat{a}_x
$$
$$
\vec{a} = l\ddot{\theta}\hat{a}_x  + l\dot{\theta}^2\hat{a}_y
$$

Frame A

* $ {}^{N}{}{\vec{\omega}}^{A}{} = \dot{\theta} \hat{n}_z= \dot{\theta} \hat{a}_z$
