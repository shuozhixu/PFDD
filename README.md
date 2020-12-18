# PFDD

In the phase-field dislocation model, each phase corresponds to a "state of slip". Individual dislocations are thus phase boundaries whose configurations are determined by minimizing the total system energy, which in its most general form contains the elastic energy, the lattice energy, the gradient energy, and the external energy.

There are many phase-field dislocation models, e.g., the [phase-field microelasticity](https://doi.org/10.1016/S1359-6454(01)00075-1) model and the [microscopic phase-field](https://doi.org/10.1016/j.actamat.2014.03.065) model. Below you will find a brief, historial overview of the phase-field dislocation dynamics (PFDD) model. In the current context, the name "PFDD" refers to a specifc model first developed by [Marisol Koslowski](https://scholar.google.com/citations?user=YKqLEyEAAAAJ&hl=en) and her students, postdocs, and colleagues. Note that (i) early PFDD papers did not use the name "PFDD", but they were considered to use the PFDD model, retrospectively, and (ii) some papers used the name "PFDD" for their models, but they were authored/co-authored by other groups, e.g., [Pi et al.](https://doi.org/10.1016/j.actamat.2017.04.019) Papers in the second case are not included in this overview.

Here is the very first PFDD paper:

- M. Koslowski, A.M. Cuiti&#241;o, M. Ortiz, [A phase-field theory of dislocation dynamics, strain hardening and hysteresis in ductile single crystals](https://doi.org/10.1016/S0022-5096(02)00037-6), J. Mech. Phys. Solids 50 (2002) 2597--2635

in which (i) the isotropic elasticity was assumed, (ii) the elastic tensor was assumed the same everywhere, (iii) the lattice energy was based on a simple 1D function, (iv) the lattice energy was assumed the same everywhere, (v) the gradient energy was omitted, (vi) the external energy invovled the stress-controlled loading only, (vii) the model was for FCC crystals only, and (viii) no numerical grid was used. These eight issues were addressed in the subsequent years.

As mentioned, the first PFDD paper did not use the name PFDD. The first paper that used the name PFDD was

- Lei Lei, Marisol Koslowski, [Mesoscale modeling of dislocations in molecular crystals](https://doi.org/10.1080/14786435.2010.533135), Philos. Mag. 91 (2011) 865-878

## (i)

Anisotropic elasticity was first implemented into PFDD in 2019:

- Shuozhi Xu, Lauren Smith, Jaber R. Mianroodi, Abigail Hunter, Bob Svendsen, Irene J. Beyerlein, [A comparison of different continuum approaches in modeling mixed-type dislocations in Al](http://dx.doi.org/10.1088/1361-651X/ab2d16), Modelling Simul. Mater. Sci. Eng. 27 (2019) 074004

Later that year, details in the formulation of anisotropic elasticity were presented:

- Shuozhi Xu, Yanqing Su, Irene J. Beyerlein, [Modeling dislocations with arbitrary character angle in face-centered cubic transition metals using the phase-field dislocation dynamics method with full anisotropic elasticity](http://dx.doi.org/10.1016/j.mechmat.2019.103200), Mech. Mater. 139 (2019) 103200

## (ii)

Elastic heterogeneity was introduced to PFDD, for a void in 2013:

- Lei Lei, Juan Luis Marin, Marisol Koslowski, [Phase-field modeling of defect nucleation and propagation in domains with material inhomogeneities](https://doi.org/10.1088/0965-0393/21/2/025009), Modelling Simul. Mater. Sci. Eng. 21 (2013) 025009

and for a secondary material in 2016:

- Yifei Zeng, Abigail Hunter, Irene Jane Beyerlein, Marisol Koslowski, [A phase field dislocation dynamics model for a bicrystal interface system: An investigation into dislocation slip transmission across cube-on-cube interfaces](https://doi.org/10.1016/j.ijplas.2015.09.001), Int. J. Plast. 79 (2016) 293--313

However, these two papers did not address issues (i), (iii), and (v).

## (iii)

In 2011, the lattice energy formulation was advanced such that it was based on a 2D function that approximates the generalized stacking fault energy (GSFE) surface in FCC crystals:

- A. Hunter, I.J. Beyerlein, T.C. Germann, M. Koslowski, [Influence of the stacking fault energy surface on partial dislocations in fcc metals with a three-dimensional phase field dislocations dynamics model](https://doi.org/10.1103/PhysRevB.84.144108), Phys. Rev. B 84 (2001) 144108

Then in 2019, the lattice energy was advanced again such that it was based on the GSFE surface that was entirely informed by atomic-level calculations without using any function:

- Shuozhi Xu, Jaber R. Mianroodi, Abigail Hunter, Irene J. Beyerlein, Bob Svendsen, [Phase-field-based calculations of the disregistry fields of static extended dislocations in FCC metals](http://dx.doi.org/10.1080/14786435.2019.1582850), Philos. Mag. 99 (2019) 1400--1428

In the paper above, effects of the two GSFE surfaces were studied and it was recommended that the one not using a function is more desirable.

The GSFE surface is used only for dissociated dislocations, e.g., those in FCC crystals and on basal planes in HCP crystals. For non-dissociated dislocations, e.g., those in BCC crystals and on non-basal planes in HCP crystals, GSFE curves should be used. In early PFDD models, the GSFE curve was approximated by a 1D function. That changed in 2020:

- Shuozhi Xu, Yanqing Su, Lauren T.W. Smith, Irene J. Beyerlein, [Frank-Read source operation in six body-centered cubic refractory metals](http://dx.doi.org/10.1016/j.jmps.2020.104017), J. Mech. Phys. Solids 141 (2020) 104017

in which the GSFE curve was informed entirely by atomic-level calculations without using any function.

## (iv)

In materials such as multi-principal element alloys, [the GSFE is not spatially uniform](http://dx.doi.org/10.1016/j.intermet.2020.106844). As a result, the lattice energy cannot be the same everywhere. This feature was added to PFDD in 2019:

- Yifei Zeng, Xiaorong Cai, Marisol Koslowski, [Effects of the stacking fault energy fluctuations on the strengthening of alloys](https://doi.org/10.1016/j.actamat.2018.09.066), Acta Mater. 164 (2019) 1--11

## (v)

In 2019, the gradient energy was added to the total energy in the PFDD model:

- Shuozhi Xu, Lauren Smith, Jaber R. Mianroodi, Abigail Hunter, Bob Svendsen, Irene J. Beyerlein, [A comparison of different continuum approaches in modeling mixed-type dislocations in Al](http://dx.doi.org/10.1088/1361-651X/ab2d16), Modelling Simul. Mater. Sci. Eng. 27 (2019) 074004

Similar to the GSFE surface, the gradient energy is intended for dissociated dislocations, e.g., those in FCC crystals and on basal planes in HCP crystals. Therefore, this feature is not used in BCC crystals or for non-basal slips in HCP crystals.

Note that including the gradient energy in the total energy is not necessarily desirable in all FCC crystals. In some FCC crystals, it may be better not to include it. An analysis was conducted in:

- Shuozhi Xu, Yanqing Su, Irene J. Beyerlein, [Modeling dislocations with arbitrary character angle in face-centered cubic transition metals using the phase-field dislocation dynamics method with full anisotropic elasticity](http://dx.doi.org/10.1016/j.mechmat.2019.103200), Mech. Mater. 139 (2019) 103200

In any case, if one decided to include the gradient energy, the formulation would ask for the values of two independent gradient energy coefficients per slip plane in FCC crystals. In [Xu et al. MSMSE (2019)](http://dx.doi.org/10.1088/1361-651X/ab2d16), the two coefficients were different. However, they may have the same value. The uniform coefficient was first used in the paper below, shortly after the preceding MSMSE paper was published:  

- Yanqing Su, Shuozhi Xu, Irene J. Beyerlein, [_Ab initio_-informed phase-field modeling of static dislocation core structures in equal-molar CoNiRu multi-principal element alloys](http://dx.doi.org/10.1088/1361-651X/ab3b62), Modelling Simul. Mater. Sci. Eng. 27 (2019) 084001

The two types of gradient energy coefficients were compared later:

- Shuozhi Xu, Jaber R. Mianroodi, Abigail Hunter, Bob Svendsen, Irene J. Beyerlein, [Comparative modeling of the disregistry and Peierls stress for dissociated edge and screw dislocations in Al](http://dx.doi.org/10.1016/j.ijplas.2020.102689), Int. J. Plast. 129 (2020) 102689

which recommended that the non-uniform cofficients be used whenever possible.

## (vi)

In 2015, the strain-controlled loading was implemented into PFDD:

- Lei Cao, Abigail Hunter, Irene J. Beyerlein, Marisol Koslowski, [The role of partial mediated slip during quasi-static deformation of 3D nanocrystalline metals](https://doi.org/10.1016/j.jmps.2015.02.019), J. Mech. Phys. Solids 78 (2015) 415--426

## (vii)

Another line of advancement is to extend PFDD from FCC crystals to other types of crystals. Three advancements were made in 2020. First, PFDD was extended to {110} slips in BCC crystals:

- Xiaoyao Peng, Nithin Mathew, Irene J. Beyerlein, Kaushik Dayal, Abigail Hunter, [A 3D phase field dislocation dynamics model for body-centered cubic crystals](https://doi.org/10.1016/j.commatsci.2019.109217), Comput. Mater. Sci. 171 (2020) 109217

in which the lattice energy also depended on the dislocation character angle, to take into account the difference in the glide resistance among dislocations with different character angles.

Soon after, PFDD was extended to {112} and {123} slips in BCC crystals:

- Shuozhi Xu, Yanqing Su, Lauren T.W. Smith, Irene J. Beyerlein, [Frank-Read source operation in six body-centered cubic refractory metals](http://dx.doi.org/10.1016/j.jmps.2020.104017), J. Mech. Phys. Solids 141 (2020) 104017

PFDD was also extended to HCP crystals, for slips on basal, prismatic, and pyramidal-II planes:

- C. Albrecht, A. Hunter, A. Kumar, I.J. Beyerlein, [A phase field model for dislocations in hexagonal close packed crystals](https://doi.org/10.1016/j.jmps.2019.103823), J. Mech. Phys. Solids 137 (2020) 103823

By Dec 2020, the PFDD model had not been used to study slips on pyramidal-I planes in HCP crystals, but doing so should be straightforward given the similarity between pyramidal-I and pyramidal-II slips.

## (viii)

In 2004, 2D numerical grids were introduced to PFDD:

- M. Koslowski, M. Ortiz, [A multi-phase field model of planar dislocation networks](https://doi.org/10.1088/0965-0393/12/6/003), Modelling Simul. Mater. Sci. Eng 12 (2004) 1087

Then in 2011, 3D numerical grids were used:

- Lei Lei, Marisol Koslowski, [Mesoscale modeling of dislocations in molecular crystals](https://doi.org/10.1080/14786435.2010.533135), Philos. Mag. 91 (2011) 865-878

However, in 3D grids, slips were not confined to pre-defined slip planes. 

The first paper in which all slips were confined to pre-defined slip planes in PFDD was published in 2019:

- Shuozhi Xu, Lauren Smith, Jaber R. Mianroodi, Abigail Hunter, Bob Svendsen, Irene J. Beyerlein, [A comparison of different continuum approaches in modeling mixed-type dislocations in Al](http://dx.doi.org/10.1088/1361-651X/ab2d16), Modelling Simul. Mater. Sci. Eng. 27 (2019) 074004

Later, effects of the confinement were studied in:

- Shuozhi Xu, Jaber R. Mianroodi, Abigail Hunter, Bob Svendsen, Irene J. Beyerlein, [Comparative modeling of the disregistry and Peierls stress for dissociated edge and screw dislocations in Al](http://dx.doi.org/10.1016/j.ijplas.2020.102689), Int. J. Plast. 129 (2020) 102689

which recommended that the confinement be used whenever possible.

## Note

Recent (as of Dec 2020) PFDD work combined several features mentioned above, e.g.,

- Lauren T.W. Smith, Yanqing Su, Shuozhi Xu, Abigail Hunter, Irene J. Beyerlein, [The effect of local chemical ordering on Frank-Read source activation in a refractory multi-principal element alloy](http://dx.doi.org/10.1016/j.ijplas.2020.102850), Int. J. Plast. 134 (2020) 102850

which used features (i), (iv), (vii), and (viii).

To sum up, it is always a good idea to use features (i) and (viii) in any PFDD work. Feature (iii) is highly recommended unless in the case of intensive high-throughput computing. Whether other features are used depends on the specific slip systems and material systems.