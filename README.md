# PFDD

In the phase-field dislocation model, each phase corresponds to a "state of slip". Individual dislocations are thus phase boundaries whose configurations are determined by minimizing the total system energy, which in its most general form contains the elastic energy, the lattice energy, the gradient energy, and the external energy.

There are many phase-field dislocation models, e.g., the [phase-field microelasticity](https://doi.org/10.1016/S1359-6454(01)00075-1) model and the [microscopic phase-field](https://doi.org/10.1016/j.actamat.2014.03.065) model. Below you will find a brief, historical overview of the phase-field dislocation dynamics (PFDD) model. In the current context, the name "PFDD" refers to a specific model first developed by [Marisol Koslowski](https://scholar.google.com/citations?user=YKqLEyEAAAAJ&hl=en) and later advanced by her students, postdocs, and colleagues. Note that (i) early PFDD papers did not use the name "PFDD", but they were retrospectively considered to use the PFDD model, and (ii) some papers used the name "PFDD" for their models, but they were authored/co-authored by other groups, e.g., [Pi et al.](https://doi.org/10.1016/j.actamat.2017.04.019) Papers in the second category are not included in this overview.

Here is the very first PFDD paper:

- M. Koslowski, A.M. Cuiti&#241;o, M. Ortiz, [A phase-field theory of dislocation dynamics, strain hardening and hysteresis in ductile single crystals](https://doi.org/10.1016/S0022-5096(02)00037-6), J. Mech. Phys. Solids 50 (2002) 2597--2635

in which (i) the isotropic elasticity was assumed, (ii) the elastic tensor was assumed the same everywhere, (iii) the lattice energy was based on a simple 1D function, (iv) the lattice energy was assumed the same everywhere, (v) the gradient energy was omitted, (vi) the external energy involved the stress-controlled loading only, (vii) the model was for FCC crystals only, and (viii) no numerical grid was used. These eight issues were addressed in subsequent years.

As mentioned, the first PFDD paper did not use the name PFDD. The first paper that used the name PFDD was

- Lei Lei, Marisol Koslowski, [Mesoscale modeling of dislocations in molecular crystals](https://doi.org/10.1080/14786435.2010.533135), Philos. Mag. 91 (2011) 865--878

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

Note that the two papers above did not address issues (i), (iii), or (v). In 2022, issues (i), (ii), and (iii) were addressed in the same model:

- Shuozhi Xu, Justin Y. Cheng, Zezhou Li, Nathan A. Mara, Irene J. Beyerlein, [Phase-field modeling of the interactions between an edge dislocation and an array of obstacles](https://doi.org/10.1016/j.cma.2021.114426), Comput. Methods Appl. Mech. Eng. 389 (2022) 114426

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

In materials such as multi-principal element alloys, [the GSFE is not spatially uniform](http://dx.doi.org/10.1016/j.intermet.2020.106844). As a result, the lattice energy cannot be the same everywhere. The feature of spatially varying lattice energy was added to PFDD in 2019:

- Yifei Zeng, Xiaorong Cai, Marisol Koslowski, [Effects of the stacking fault energy fluctuations on the strengthening of alloys](https://doi.org/10.1016/j.actamat.2018.09.066), Acta Mater. 164 (2019) 1--11

The spatial variation in the lattice energy inevitably generated a large amount of data, leading to difficulties in relating the inputs and outputs analytically yet providing an opportunity to use machine learning:

- Pau Cutrina Vilalta, Somayyeh Sheikholeslami, Katerine Saleme Ruiz, Xin C. Yee, Marisol Koslowski, [Machine learniing for predicting the critical yield stress of high entropy alloys](https://doi.org/10.1115/1.4048873), J. Eng. Mater. Tech. 143 (2021) 021005

In 2020, the feature of character angle-dependent lattice energy was added to PFDD, for BCC metals:

- Xiaoyao Peng, Nithin Mathew, Irene J. Beyerlein, Kaushik Dayal, Abigail Hunter, [A 3D phase field dislocation dynamics model for body-centered cubic crystals](https://doi.org/10.1016/j.commatsci.2019.109217), Comput. Mater. Sci. 171 (2020) 109217

The rational was that the Peierls stress differs greatly between edge and screw dislocations in BCC metals.

## (v)

In 2019, the gradient energy was added to the total energy in the PFDD model:

- Shuozhi Xu, Lauren Smith, Jaber R. Mianroodi, Abigail Hunter, Bob Svendsen, Irene J. Beyerlein, [A comparison of different continuum approaches in modeling mixed-type dislocations in Al](http://dx.doi.org/10.1088/1361-651X/ab2d16), Modelling Simul. Mater. Sci. Eng. 27 (2019) 074004

Originally the gradient energy was intended only for dissociated dislocations, e.g., those in FCC crystals and on basal planes in HCP crystals. Later, it was found that inlcuding the gradient energy may result in a match between the PFDD-based dislocation core width and the atomistic-based one in BCC metals:

- Hyojung Kim, Nithin Mathew, Darby J. Luscher, Abigail Hunter, [Phase field dislocation dynamics (PFDD) modeling of non-Schmid behavior in BCC metals informed by atomistic simulations](http://dx.doi.org/10.1016/j.jmps.2021.104460), J. Mech. Phys. Solids 152 (2021) 104460

Note that including the gradient energy in the total energy is not necessarily desirable in all FCC crystals. In some FCC crystals, it may be better not to include it. An analysis of edge and screw dislocations in eight FCC crystals was conducted in:

- Shuozhi Xu, Yanqing Su, Irene J. Beyerlein, [Modeling dislocations with arbitrary character angle in face-centered cubic transition metals using the phase-field dislocation dynamics method with full anisotropic elasticity](http://dx.doi.org/10.1016/j.mechmat.2019.103200), Mech. Mater. 139 (2019) 103200

In any case, if one decided to include the gradient energy, the formulation would ask for the values of two independent gradient energy coefficients per slip plane in an FCC crystal. In [Xu et al. MSMSE (2019)](http://dx.doi.org/10.1088/1361-651X/ab2d16), the two coefficients were different. However, they may have the same value. The uniform coefficient was first used in the paper below, shortly after the preceding MSMSE paper was published:  

- Yanqing Su, Shuozhi Xu, Irene J. Beyerlein, [_Ab initio_-informed phase-field modeling of static dislocation core structures in equal-molar CoNiRu multi-principal element alloys](http://dx.doi.org/10.1088/1361-651X/ab3b62), Modelling Simul. Mater. Sci. Eng. 27 (2019) 084001

The two types of gradient energy coefficients, i.e., non-uniform and uniform, were compared later in:

- Shuozhi Xu, Jaber R. Mianroodi, Abigail Hunter, Bob Svendsen, Irene J. Beyerlein, [Comparative modeling of the disregistry and Peierls stress for dissociated edge and screw dislocations in Al](http://dx.doi.org/10.1016/j.ijplas.2020.102689), Int. J. Plast. 129 (2020) 102689

which recommended that the non-uniform coefficients be used whenever possible.

## (vi)

In 2015, the strain-controlled loading was implemented into PFDD:

- Lei Cao, Abigail Hunter, Irene J. Beyerlein, Marisol Koslowski, [The role of partial mediated slip during quasi-static deformation of 3D nanocrystalline metals](https://doi.org/10.1016/j.jmps.2015.02.019), J. Mech. Phys. Solids 78 (2015) 415--426

## (vii)

Another line of advancement is to extend PFDD from FCC crystals to other types of crystals. Three advancements were made in 2020. First, PFDD was extended to {110} slips in BCC crystals:

- Xiaoyao Peng, Nithin Mathew, Irene J. Beyerlein, Kaushik Dayal, Abigail Hunter, [A 3D phase field dislocation dynamics model for body-centered cubic crystals](https://doi.org/10.1016/j.commatsci.2019.109217), Comput. Mater. Sci. 171 (2020) 109217

Soon after, PFDD was extended to {112} and {123} slips in BCC crystals:

- Shuozhi Xu, Yanqing Su, Lauren T.W. Smith, Irene J. Beyerlein, [Frank-Read source operation in six body-centered cubic refractory metals](http://dx.doi.org/10.1016/j.jmps.2020.104017), J. Mech. Phys. Solids 141 (2020) 104017

PFDD was also extended to HCP crystals, for slips on basal, prismatic-I, and pyramidal-II planes:

- C. Albrecht, A. Hunter, A. Kumar, I.J. Beyerlein, [A phase field model for dislocations in hexagonal close packed crystals](https://doi.org/10.1016/j.jmps.2019.103823), J. Mech. Phys. Solids 137 (2020) 103823

As of March 2022, the PFDD model had not been used to study slips on pyramidal-I planes in HCP crystals, but doing so should be straightforward.

## (viii)

In 2004, 2D orthogonal numerical grids were introduced to PFDD:

- M. Koslowski, M. Ortiz, [A multi-phase field model of planar dislocation networks](https://doi.org/10.1088/0965-0393/12/6/003), Modelling Simul. Mater. Sci. Eng 12 (2004) 1087--1097

Then in 2011, 3D orthogonal numerical grids were used:

- Lei Lei, Marisol Koslowski, [Mesoscale modeling of dislocations in molecular crystals](https://doi.org/10.1080/14786435.2010.533135), Philos. Mag. 91 (2011) 865--878

which studied a 3D problem. In the above paper (and many others that were not referenced here), slips were not confined to pre-defined slip planes in a 3D grid. 

The first paper in which all slips were confined to pre-defined slip planes in PFDD was published in 2019:

- Shuozhi Xu, Lauren Smith, Jaber R. Mianroodi, Abigail Hunter, Bob Svendsen, Irene J. Beyerlein, [A comparison of different continuum approaches in modeling mixed-type dislocations in Al](http://dx.doi.org/10.1088/1361-651X/ab2d16), Modelling Simul. Mater. Sci. Eng. 27 (2019) 074004

Later, effects of the confinement were studied in:

- Shuozhi Xu, Jaber R. Mianroodi, Abigail Hunter, Bob Svendsen, Irene J. Beyerlein, [Comparative modeling of the disregistry and Peierls stress for dissociated edge and screw dislocations in Al](http://dx.doi.org/10.1016/j.ijplas.2020.102689), Int. J. Plast. 129 (2020) 102689

which recommended that the confinement be used whenever possible.

One may wonder: wouldn't the confinement reduce a 3D model to a 2D model? This is indeed the case for a 2D problem, i.e., when only one slip plane is involved in the system. However, the 3D model, even confined, can be used for a 3D problem, i.e., when multiple slip planes, either parallel or non-parallel, are involved. Clearly, the 3D model is advantageous to the 2D model which cannot simulate a 3D problem.

In 2021, 3D non-orthogonal numerical grids were developed for FCC and BCC crystals:

- Xiaoyao Peng, Abigail Hunter, Irene J. Beyerlein, Ricardo A. Lebensohn, Kaushik Dayal, Enrique Martinez, [Non-orthogonal computational grids for studying dislocation motion in phase field approaches](https://doi.org/10.1016/j.commatsci.2021.110834), Comput. Mater. Sci. 200 (2021) 110834

Such non-orthogonal grids made screw dislocation cross-slip possible:

- Lauren T. W. Fey, Abigail Hunter, Irene J. Beyerlein, [Phase-field dislocation modeling of cross-slip](https://doi.org/10.1007/s10853-021-06716-1), J. Mater. Sci. (2022)

## Note

Recent PFDD work combined several features mentioned above, e.g.,

- Lauren T.W. Smith, Yanqing Su, Shuozhi Xu, Abigail Hunter, Irene J. Beyerlein, [The effect of local chemical ordering on Frank-Read source activation in a refractory multi-principal element alloy](http://dx.doi.org/10.1016/j.ijplas.2020.102850), Int. J. Plast. 134 (2020) 102850

which used features (i), (iv), (vii), and (viii).

To sum up, it is always a good idea to use feature (i) in any PFDD work. Feature (iii) is highly recommended unless in the case of intensive high-throughput computing. Whether other features are used depends on the specific slip systems, material systems, and/or loading conditions.

## Code development

The PFDD code was parallelized in 2011:

- Abigail Hunter, Faisal Saied, Chinh Le, Marisol Koslowski [Large-scale 3D phase field dislocation dynamics simulations on high-performance architectures](http://dx.doi.org/10.1177/1094342010382534), Int. J. High Perform. Comput. Appl. 25 (2011) 223-235

and was then accelerated by GPU in 2018:

- Adnan Eghtesad, Kai Germaschewski, Irene J. Beyerlein, Abigail Hunter, Marko Knezevic, [Graphics processing unit accelerated phase field dislocation dynamics: Application to bi-metallic interfaces](https://doi.org/10.1016/j.advengsoft.2017.09.010), Adv. Eng. Software 115 (2018) 248-267

## Reference

For the progress in the PFDD method between 2016 and early 2022, please read:

- Shuozhi Xu, Recent progress in the phase-field dislocation dynamics method, Comput. Mater. Sci. (2022)
