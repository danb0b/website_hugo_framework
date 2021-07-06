---
title: Jacobians
bibliography: ../../project/bibliography.bib
csl: ../../project/ieee.csl
type: submodule
---

# Jacobians

## Jacobians

A Jacobian is a matrix that collects the partial derivatives of rates of change between two vectors.  These rates of change are related by 

$$\dot{a}=\mathbf{J}\dot{b}$$

$$\mathbf{J}=
\left[\begin{matrix}
j_{11} & j_{12} & \ldots & j_{1n}\\
j_{21} & j_{22} & \ldots & j_{2n}\\
\vdots & \vdots & \ddots & \vdots\\
j_{m1} & j_{m2} & \ldots & j_{mn}\\
\end{matrix}
\right]$$

where $j_{ij} = \frac{\partial \dot{a}_i}{\partial \dot{b}_j}$

## Physical Meaning

::: {.text-center}
![](../../sketches/gear-ratio.png){width="50%"}
:::

## How Jacobians are Used

::: {.text-center}
![](../../sketches/arm-traj.png){width="50%"}
:::

## How Jacobians are Used

::: {.text-center}
![](../../sketches/arm-traj2.png){width="50%"}
:::

## How Jacobians are Used

::: {.text-center}
![](../../sketches/arm-traj2.png){width="50%"}
:::

To calculate the speed of a Robot Arm as a function of its inputs

$$\dot{y}= \mathbf{J}\dot{q}$$

## Virtual Work

$$P_{in} = P_{out}$$
$$P_{in} = \tau^T \dot{q} = F^T \dot{y}=P_{out}$$
$$\tau^T \dot{q} = F^T \mathbf{J}\dot{q}$$
$$\tau^T  = F^T \mathbf{J}$$
$$\tau  = \mathbf{J}^T F$$

Relating forces felt at end-effector to torques felt by motors.

## Torques to Forces

::: {.text-center}
![](../../sketches/jtf.png){width="50%"}
:::

$$\tau  = \mathbf{J}^T F$$



<!---
::: {.columns}
::: {.column width=45%}

![](arm-traj.png)

:::
::: {.column width=45%}

![](arm-traj2.png)

:::
:::
-->