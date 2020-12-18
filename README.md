# PFDD

In the phase-field dislocation dynamics (PFDD) model, each phase corresponds to a "state of slip". Individual dislocations are thus phase boundaries whose configurations are determined by minimizing the total system energy, which in its most general form contains the elastic energy, the lattice energy, and the gradient energy.

Here is the very first PFDD paper:

- M. Koslowski, A.M. Cuiti&#241;o, M. Ortiz, [A phase-field theory of dislocation dynamics, strain hardening and hysteresis in ductile single crystals](https://doi.org/10.1016/S0022-5096(02)00037-6), J. Mech. Phys. Solids 50 (2002) 2597--2635

in which (i) the isotropic elasticity was assumed, (ii) the elastic tensor was assumed the same everywhere, (iii) the lattice energy was based on a simple 1D function, (iv) the lattice energy was assumed the same everywhere, (v) the gradient energy was omitted and (vi) the model was for FCC crystals only. These six issues were addressed in the subsequent years.

## (i)

Anisotropic elasticity was first implemented into PFDD in 2019:

- Shuozhi Xu, Lauren Smith, Jaber R. Mianroodi, Abigail Hunter, Bob Svendsen, Irene J. Beyerlein, [A comparison of different continuum approaches in modeling mixed-type dislocations in Al](http://dx.doi.org/10.1088/1361-651X/ab2d16), Modelling Simul. Mater. Sci. Eng. 27 (2019) 074004

and the differences between isotropic and anisotropic elasticity were systematically demonstrated in a later paper in the same year:

- Shuozhi Xu, Yanqing Su, Irene J. Beyerlein, [Modeling dislocations with arbitrary character angle in face-centered cubic transition metals using the phase-field dislocation dynamics method with full anisotropic elasticity](http://dx.doi.org/10.1016/j.mechmat.2019.103200), Mech. Mater. 139 (2019) 103200

## (ii)

Elastic heterogeneity was introduced to PFDD, for a void in 2013:

- Lei Lei, Juan Luis Marin, Marisol Koslowski, [Phase-field modeling of defect nucleation and propagation in domains with material inhomogeneities](https://doi.org/10.1088/0965-0393/21/2/025009), Modelling Simul. Mater. Sci. Eng. 21 (2013) 025009

and for a secondary material in 2016:

- Yifei Zeng, Abigail Hunter, Irene Jane Beyerlein, Marisol Koslowski, [A phase field dislocation dynamics model for a bicrystal interface system: An investigation into dislocation slip transmission across cube-on-cube interfaces](https://doi.org/10.1016/j.ijplas.2015.09.001), Int. J. Plast. 79 (2016) 293--313

However, these work did not address issues (i), (iii), and (v).

## (iii)

In 2011, the lattice energy formulation was advanced such that it was based on a 2D function that approximates the generalized stacking fault energy (GSFE) surface in FCC crystals:

- A. Hunter, I.J. Beyerlein, T.C. Germann, M. Koslowski, [Influence of the stacking fault energy surface on partial dislocations in fcc metals with a three-dimensional phase field dislocations dynamics model](https://doi.org/10.1103/PhysRevB.84.144108), Phys. Rev. B 84 (2001) 144108

Then in 2019, the lattice energy was advanced again such that it was directly based on the GSFE surface without any help of any function:

- Shuozhi Xu, Jaber R. Mianroodi, Abigail Hunter, Irene J. Beyerlein, Bob Svendsen, [Phase-field-based calculations of the disregistry fields of static extended dislocations in FCC metals](http://dx.doi.org/10.1080/14786435.2019.1582850), Philos. Mag. 99 (2019) 1400--1428

The GSFE surface is used only for FCC crystals and for basal slips in HCP crystals. For BCC crystals and non-basal slips in HCP crystals, GSFE curves should be used. In early PFDD models, the GSFE curve was approximated by a 1D function. That changed in 2020:

- Shuozhi Xu, Yanqing Su, Lauren T.W. Smith, Irene J. Beyerlein, [Frank-Read source operation in six body-centered cubic refractory metals](http://dx.doi.org/10.1016/j.jmps.2020.104017), J. Mech. Phys. Solids 141 (2020) 104017

in which the GSFE curve was used directly without any help of any function.

## (iv)

In materials such as multi-principal element alloys, [the GSFE is not spatially uniform](http://dx.doi.org/10.1016/j.intermet.2020.106844). As a result, the lattice energy cannot be the same everywhere. This feature was added to PFDD in 2019:

- Yifei Zeng, Xiaorong Cai, Marisol Koslowski, [Effects of the stacking fault energy fluctuations on the strengthening of alloys](https://doi.org/10.1016/j.actamat.2018.09.066), Acta Mater. 164 (2019) 1--11

## (v)

In 2019, the gradient energy was added to the total energy in the PFDD model:

- Shuozhi Xu, Lauren Smith, Jaber R. Mianroodi, Abigail Hunter, Bob Svendsen, Irene J. Beyerlein, [A comparison of different continuum approaches in modeling mixed-type dislocations in Al](http://dx.doi.org/10.1088/1361-651X/ab2d16), Modelling Simul. Mater. Sci. Eng. 27 (2019) 074004

## (iv)

Another line of advancement is to extend PFDD from FCC crystals to other crystals. Three advancements were made in 2020. First, PFDD was extended to {110} slips in BCC crystals:

- Xiaoyao Peng, Nithin Mathew, Irene J. Beyerlein, Kaushik Dayal, Abigail Hunter, [A 3D phase field dislocation dynamics model for body-centered cubic crystals](https://doi.org/10.1016/j.commatsci.2019.109217), Comput. Mater. Sci. 171 (2020) 109217

in which the lattice energy also depended on the dislocation character angle, to take into account the difference in the glide resistance among dislocations with different character angles.

Soon after, PFDD was extended to {112} and {123} slips in BCC crystals:

- Shuozhi Xu, Yanqing Su, Lauren T.W. Smith, Irene J. Beyerlein, [Frank-Read source operation in six body-centered cubic refractory metals](http://dx.doi.org/10.1016/j.jmps.2020.104017), J. Mech. Phys. Solids 141 (2020) 104017

PFDD was also extended to HCP crystals, for slips on basal, prismatic, and pyramidal-II planes:

- C. Albrecht, A. Hunter, A. Kumar, I.J. Beyerlein, [A phase field model for dislocations in hexagonal close packed crystals](https://doi.org/10.1016/j.jmps.2019.103823), J. Mech. Phys. Solids 137 (2020) 103823