---
layout: post
author: "AG"
title: CoRe database second release
categories: [CoRe-Database,Papers]
tags: [BNS, GW, NR, NewSimulations, GWdata]
image: database_R02.png
link: https://arxiv.org/abs/2210.16366
---

 
In [2210.16366](https://arxiv.org/abs/2210.16366) we present the second data release of gravitational waveforms from
binary neutron star merger simulations performed by the Computational
Relativity (CoRe) collaboration. The current database consists of
254 different binary neutron star configurations and a total of 590 
individual numerical-relativity simulations using various grid resolutions. The
released waveform data contain the strain and the
Weyl curvature multipoles up to l=m=4. They 
span a significant portion of the mass, mass-ratio,
spin and eccentricity parameter space and include targeted
configurations to the events GW170817 and GW190425.
CoRe simulations are performed with
18 different equations of state, seven of which are finite
temperature models, and three of which account for non-hadronic
degrees of freedom. About half of the released data are computed
with high-order hydrodynamics schemes for tens of orbits to merger; 
the other half is computed with advanced microphysics. 
We showcase a standard waveform
error analysis and discuss the accuracy of the database in terms of
faithfulness. We present ready-to-use fitting formulas for
equation of state-insensitive relations at merger (e.g. merger frequency),
luminosity peak, and post-merger spectrum. 

Scripts and data used in this work are publicly available on [ZENODO](https://doi.org/10.5281/zenodo.7253784).

The simulation data can be found in our [CoRe Database](https://core-gitlfs.tpi.uni-jena.de/).

We also release the python package [watpy](https://git.tpi.uni-jena.de/core/watpy) to ease the management and analysis of the simulations in our database. 
Also installable through PyPI `pip install core-watpy`.
