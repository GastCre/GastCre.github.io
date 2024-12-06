# `Mathematica` codes
This repository contains my `Mathematica` codes, organised by folders corresponding to the respective project.

## Tidal properties of neutron stars in scalar-tensor theories of gravity
This folder contains the codes used for the paper Tidal properties of neutron stars in scalar-tensor theories of gravity.

There are two Mathematica codes:
- Tidal properties of NS in ST- analytical calculation. This code starts from the scalar-tensor action written in the Einstein frame,
  ```math
  S_{\rm ST}^{\rm (E)}=\int_{\mathcal{M}}d^4x\sqrt{-g}\left[K_R R_\ast- K_{\varphi} g^{\mu\nu}\partial_\mu\varphi\partial_\nu\varphi\right]+S_{\rm matter}\left[\psi_m,A^2(\varphi)g_{\mu\nu}\right]~.
  ```
  where
  - $g_{\mu\nu}$ is the metric in the Einstein frame,
  - $\varphi$ is the scalar field,
  - $A(\varphi)$ is the coupling function defining the theory,
  - $S_{\rm matter}\left[\psi_m,A^2(\varphi)g_{\mu\nu}\right]$ is the matter action containing matter fields $\psi_m$.
    
  Using xAct, assuming a perfect-fluid energy-momentum tensor $T_{\mu\nu}$, it computes the scalar field equations of motion, the modified Einstein field equations, and the modified energy-momentum conservation,
  ```math
  $$G_{\mu\nu}=\frac{1}{2K_R} T_{\mu\nu}+\frac{K_\varphi}{K_R} T^{\varphi}_{\mu\nu}~,$$
  $$\Box\varphi=\frac{1}{2K_\varphi}\alpha(\varphi) T,$$
  $$\nabla^\mu T_{\mu\nu}=-\alpha T \partial_\nu\varphi.$$```
  
it contains the analytical derivations with the xAct package and generates the equations of motion.
- [Tidal properties of NS in ST- numerical calculation](Tidal%20properties%20of%20neutron%20stars%20in%20scalar-tensor%20theories%20of%20gravity/Tidal%20properties%20of%20NS%20in%20ST-%20numerical%20calculation%20.nb): it contains the numerical calculations, including the main results of our paper.


