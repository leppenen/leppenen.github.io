---
layout: default
title: Electrodynamics
---

<script>
window.MathJax = {
  tex: {
    tags: 'none'  // disable automatic numbering
  }
};
</script>
<script async src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js"></script>
<style>
.main {
  max-width: 1300px;  /* default is ~650px */
}
</style>



# Electrodynamics: Useful Basics 

## Maxwell Equations in SI 

$$\nabla \cdot {\boldsymbol E} = \frac{\rho}{\varepsilon_0} \tag{MW1} $$

$$ \nabla \cdot {\boldsymbol B} = 0 $$

$$ \nabla \times {\boldsymbol E} = -\frac{\partial {\boldsymbol B}}{\partial t} $$ 

$$ \nabla \times  {\boldsymbol B} = \mu_0 \left({\boldsymbol J} + \varepsilon_0 \frac{\partial {\boldsymbol E}}{\partial t}\right) $$

## Greens Function

### Electrostatic

$$ \Delta \varphi(\boldsymbol r) = -\delta(\boldsymbol r) $$


### Helmholtz equation

The Green’s function is the solution of the Helmholtz equation

$$ \bigl(\Delta + k^2\bigr)\,G_0(\boldsymbol r) = -\delta(\boldsymbol r). \tag{H1} $$

Use the 3D Fourier transform
$$
G_0(\boldsymbol r)=\frac{1}{(2\pi)^3}\!\int \mathrm{d}^3\boldsymbol q\; G_{\boldsymbol q}\,e^{i\boldsymbol q\cdot\boldsymbol r}. \tag{H2}
$$

Substitution gives


$$ (-q^2+k^2)\,G_{\boldsymbol q}=-1 \quad\Rightarrow\quad G_{\boldsymbol q}=\frac{1}{q^2-k^2-i\varepsilon}, \qquad \varepsilon\to0^+. \tag{H3} \label{eq:Gq1} $$

Choosing the outgoing-wave (radiation) condition $$ k\to k+i0^+ $$ and integrating over angles,

$$ G_0(\boldsymbol r)=\lim_{\varepsilon\to0^+}\frac{2}{(2\pi)^2 r}\! \int_{0}^{\infty}\!\mathrm{d}q\; q\,\frac{\sin(qr)}{q^2-k^2-i\varepsilon}. \tag{H4} \label{eq:GrInt1} $$

Using the Sokhotski–Plemelj formula

$$ \lim_{\varepsilon\to0^+}\frac{1}{q^2-k^2-i\varepsilon} =\mathcal{P}\!\left(\frac{1}{q^2-k^2}\right)+i\pi\,\delta(q^2-k^2) $$
$$ =\mathcal{P}\!\left(\frac{1}{q^2-k^2}\right)+\frac{i\pi}{2k}\,\delta(q-k), \tag{H5} $$

Eq.\eqref{eq:GrInt1} evaluates to

$$ G_0(\boldsymbol r)=\frac{2}{(2\pi)^2 r}\!\left[\mathcal{P}\!\int_{0}^{\infty}\!\frac{q\sin(qr)}{q^2-k^2}\,\mathrm{d}q+\frac{i\pi}{2}\sin(kr)\right]=\frac{e^{ikr}}{4\pi r}. \tag{H6} $$

> With the opposite sign in the imaginary part, $$ k\to k-i0^+ $$, one obtains the incoming spherical wave $$ e^{-ikr}/(4\pi r) $$.

---

### Green’s function of the 2D scalar field

The 2D Helmholtz Green’s function $$ G_{\mathrm{2D}}(\boldsymbol\rho) $$ satisfies

$$ \bigl(\Delta + k^2\bigr)\,G_{\mathrm{2D}}(\boldsymbol\rho)=-\delta(\boldsymbol\rho),  \qquad \boldsymbol\rho=(x,y). \tag{H7} $$

Fourier transform in 2D and switch to polar coordinates in $$ \boldsymbol q $$ -space:

$$ G_{\mathrm{2D}}(\boldsymbol\rho)=\frac{1}{(2\pi)^2}\!\int \mathrm{d}^2\boldsymbol q\; G_{\boldsymbol q}\,e^{i\boldsymbol q\cdot\boldsymbol\rho} $$
$$ =\frac{1}{2\pi}\lim_{\varepsilon\to0^+} \int_{0}^{\infty}\!\frac{q\,\mathrm{d}q}{q^2-k^2-i\varepsilon}\,J_0(q\rho), \tag{H8} $$

where we used 

$$ \int_0^{2\pi}\!e^{iq\rho\cos(\phi-\theta)}\,\mathrm{d}\phi=2\pi J_0(q\rho) $$.

Applying Sokhotski–Plemelj as in 3D case and the integral identity that could be calculated in Wolfram Mathematica

$$ \mathcal{P}\!\int_{0}^{\infty}\!\frac{q\,J_0(q\rho)}{q^2-k^2}\,\mathrm{d}q =-\frac{\pi}{2}\,Y_0(k\rho),$$

We obtain the standard result

$$ G_{\mathrm{2D}}(\boldsymbol\rho)=\frac{i}{4}\,H_0^{(1)}(k\rho) =\frac{1}{4}\!\left[iJ_0(k\rho)-Y_0(k\rho)\right]. \tag{H9} $$
