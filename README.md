# ethanol_datasets

## Description

The dataset was generated from ab-initio molecular dynamics simulations. The dynamics was run using GFN2-xTB method [1,2] within ChemShell [3,4]. The total energy and atomic forces taken from the dynamics were recalculated at the PBE-D3(BJ)/6-31G*[5-8] level of theory. 

## Format

The data is stored in python compressed array format (.npz) with the total energy in kcal/mol and atomic forces in kcal/mol/Ang. The dataset contains five numpy arrays

```
import numpy as np
data = np.load('ethanol_500K.npz')
data['R']   # Cartesian coordinates of nuclei (Ang.)
data['E']   # Total energy (kcal/mol)
data['F']   # Atomic forces (kcal/mol/Ang.)
data['N']   # Number of atoms in each structure
data['Z']   # Nuclear charges
```

#### References

[1] Grimme, S.; Bannwarth, C.; Shushkov, P. A Robust and Accurate Tight-Binding Quantum Chemical Method for Structures, Vibrational Frequencies, and Noncovalent Interactions of Large Molecular Systems Parametrized for All spd-Block Elements (Z = 1–86). J. Chem. Theory Comput. 2017, 13, 1989–2009.

[2] Bannwarth, C.; Ehlert, S.; Grimme, S. GFN2-xTB–An Accurate and Broadly Parametrized Self-Consistent Tight-Binding Quantum Chemical Method with Multipole Electrostatics and
Density-Dependent Dispersion Contributions. J. Chem. Theory Comput. 2019, 15, 1652–1671.

[3] Metz, S.; Kästner, J.; Sokol, A. A.; Keal, T. W.; Sherwood, P. ChemShell—a modular soft-ware package for QM/MM simulations. WIREs Comput. Mol. Sci. 2014, 4, 101–110.

[4] Sherwood, P.; de Vries, A. H.; Guest, M. F.; Schreckenbach, G.; Catlow, C. A.; French, S. A.; Sokol, A. A.; Bromley, S. T.; Thiel, W.; Turner, A. J.; Billeter, S.; Terstegen, F.; Thiel, S.; Kendrick, J.; Rogers, S. C.; Casci, J.; Watson, M.; King, F.; Karlsen, E.; Sjøvoll, M.; Fahmi, A.; Schäfer, A.; Lennartz, C. QUASI: A general purpose implementation of the QM/MM approach and its application to problems in catalysis. J. Mol. Struc.-THEOCHEM 2003, 632, 1 – 28.

[5] Perdew, J. P.; Burke, K.; Ernzerhof, M. Generalized Gradient Approximation Made Simple. Phys. Rev. Lett. 1996, 77, 3865–3868.

[6] Grimme, S.; Antony, J.; Ehrlich, S.; Krieg, H. A consistent and accurate ab initio parametrization of density functional dispersion correction (DFT-D) for the 94 elements H-Pu. J. Chem.
Phys. 2010, 132, 154104.

[7] Grimme, S.; Ehrlich, S.; Goerigk, L. Effect of the damping function in dispersion corrected density functional theory. J. Comput. Chem. 2011, 32, 1456–1465.

[8] Rassolov, V. A.; Pople, J. A.; Ratner, M. A.; Windus, T. L. 6-31G* basis set for atoms K through Zn. J. Chem. Phys. 1998, 109, 1223–1229.
