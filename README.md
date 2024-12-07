# `Mathematica` codes
This repository contains my `Mathematica` codes, organised by folders corresponding to the respective project.

## Tidal properties of neutron stars in scalar-tensor theories of gravity
This folder contains the codes used for the paper Tidal properties of neutron stars in scalar-tensor theories of gravity.

There are two Mathematica codes:
- Tidal properties of NS in ST- analytical calculation. This code starts from the scalar-tensor action written in the Einstein frame,
```math
\begin{align}
  S_{\rm ST}^{\rm (E)}=\int_{\mathcal{M}}d^4x\sqrt{-g}\left[K_R R_\ast- K_{\varphi} g^{\mu\nu}\partial_\mu\varphi\partial_\nu\varphi\right]+S_{\rm
  matter}\left[\psi_m,A^2(\varphi)g_{\mu\nu}\right]~.
\end{align}
 ``` 
  where
  - $g_{\mu\nu}$ is the metric in the Einstein frame,
  - $\varphi$ is the scalar field,
  - $A(\varphi)$ is the coupling function defining the theory,
  - $S_{\rm matter}\left[\psi_m,A^2(\varphi)g_{\mu\nu}\right]$ is the matter action containing matter fields $\psi_m$,
  - $K_R$, $K_{\varphi}$ are normalization constants.
    
  Using the [xAct package](https://josmar493.dreamhosters.com/), assuming a perfect-fluid energy-momentum tensor $T_{\mu\nu}$, it computes the scalar field equations of motion, the modified Einstein field equations, and the modified energy-momentum conservation,
```math
  \begin{align}
  &G_{\mu\nu}=\frac{1}{2K_R} T_{\mu\nu}+\frac{K_\varphi}{K_R} T^{\varphi}_{\mu\nu}~,\\
  &\Box\varphi=-\frac{1}{2K_\varphi}\frac{A'(\varphi)}{A(\varphi)} T,\\
  &\nabla^\mu T_{\mu\nu}=\frac{A'(\varphi)}{A(\varphi)} T \partial_\nu\varphi,
  \end{align}
```
  with $T_{\mu\nu}^{\varphi}$ the energy-momentum tensor of the scalar field. Then, it uses perturbation theory to split the metric and scalar field into a background piece and a perturbation,
  ```math
  \begin{align}
    g_{\mu\nu}&={g_{\mu\nu}}^{(0)}+\epsilon~\sum_{\ell,m}{h_{\mu\nu}^{\ell m}}(r)~Y_{\ell}^m(\theta,\phi)~,\\
    \varphi&=\varphi_0(r)+\epsilon~\sum_{\ell,m}\delta\varphi^{\ell m}(r)~Y_{\ell}^m(\theta,\phi),
\end{align}
  ```
and derives the equations of motion up to first order in the small parameter $\epsilon$. These equations are the starting point in the next notebook, where they are solved numerically and used to extract the Love numbers.
- [Tidal properties of NS in ST- numerical calculation](Tidal%20properties%20of%20neutron%20stars%20in%20scalar-tensor%20theories%20of%20gravity/Tidal%20properties%20of%20NS%20in%20ST-%20numerical%20calculation%20.nb). It imports the equations derived in the previous notebook and, using a piecewise
  polytropic approximation to tabulated equations of state, it solves the background and perturbation equations of motion. For the case study, although the code can work with any         functional form, we fix the coupling function to be the so-called Damour Esposito-Farèse (DEF) coupling,
   ```math
    \begin{align}
    A(\varphi)=e^{\frac{1}{2}\beta \varphi_0^2}
    \end{align}
    ```
and explore the cases $\beta=(-6,-4.5)$, and choose the cosmological scalar field values $\varphi_\infty=(10^{-3},1.5*10^{-3},10^{-6})$ (the second value is chosed for parameter space exploration, for instance for the dependence of the scalar-tensor Love number on the scalar field due to parity symmetry). Using these parameters, it solves the background equations of motion and extracts the mass-radius and charge-mass curves, in both Einstein and Jordan frames. 


