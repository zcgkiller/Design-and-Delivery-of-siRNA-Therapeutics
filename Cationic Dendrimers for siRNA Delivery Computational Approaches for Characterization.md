# Cationic Dendrimers for siRNA Delivery: Computational Approaches for Characterization

Domenico Marson, Suzana Aulic, Maurizio Fermeglia, Erik Laurini and Sabrina Pricl

## Abstract

Nowadays, computer simulations have been established as a fundamental tool in the design and development of new dendrimer-based nanocarriers for drug and gene delivery. Moreover, the level of detail contained in the information that can be gathered by performing atomistic-scale simulations cannot be obtained with any other available experimental technique. In this chapter we describe the main computational toolbox that can be exploited in the different stages of novel dendritic nanocarrier production—from the initial conception to the stage of biological intermolecular interactions.

## 1 Introduction

Today computer simulations constitute an essential tool for the design and development of new dendrimer-based nanocarriers for both drug and gene delivery. Undoubtedly, this success is linked to the exponential increase in affordable computer power and to the optimization/development of highly scalable computer codes able to run in parallel even on consumer-grade graphical processing units (GPUs). Thus, for instance, under the magnifying lens of all-atom molecular dynamics (AA-MD) simulations researchers are now able to follow the exact time and space behavior of a given nanovector in solution at a molecular level, and to characterize its interactions with a specific target. Moreover, the same set of computational techniques allows performing in silico experiments dealing with, e.g., the interactions of dendrimers with biological membranes and proteins, and the eventual aggregation and clustering of dendrimers themselves. In essence, the analysis that can be performed with data obtained from AA-MD simulations is limited only by the creativity and coding proficiency of the investigator, and can be tailored to fit the specificity of the system under study.

Based on our own experience in the field of computer-assisted cationic dendrimer-based nanovectors for siRNA delivery, in this chapter we will describe the main AA-MD computational toolbox that can be exploited in the different stages of novel dendritic nanocarrier production—from the initial conception to its structural and chemico-physical characterization to the stage of biological intermolecular interactions. Specifically, we will present a protocol for poly(amino amine) dendrimers (PAMAMs) as a proof-of-principle easily adaptable to other cationic dendrimer families. This protocol is subdivided in three main steps: (i) dendrimer and siRNA models building and optimization; (ii) AA-MD simulation of the dendrimer per se and in complex with its siRNA cargo, and (iii) simulation data analysis and correlation with experimental observations. We will further exploit the *Notes* sections to present some technical suggestions as well as some practical examples concerning the application of the computational techniques along with their biological relevance for the benefit of both computational and experimental scientists.

## 2 Materials

### 2.1 Forcefield and Software

AA-MD simulations try to mimic the behavior of individual atoms with the aid of a computer. Assuming all atoms as rigid spheres, and given the position in space of all atoms in a molecular system, the force experienced by each atom is computed applying a specific energy function, called a forcefield (FF). FFs can differ for the functional form and parameter sets used to calculate the potential energy of a given system of atoms. Newton’s laws are then used to integrate the FF over time, ultimately yielding the dynamic evolution (coordinates) of the molecular system under study.

While the underlying fundamental theories are highly similar, several different software (SW) are available to perform AA/CG-MD simulations. At the same time, a variety of FFs have been developed—from the most general ones to those custom-tailored to describe a particular system—and not all of them are compatible with all current SW. In the specific case of AA-MD simulations of cationic-dendrimer nanovectors, the most widely employed FFs are the Chemistry at Harvard Macromolecular Mechanics (CHARMM) general forcefield, the General AMBER Forcefield (GAFF) , the GROningen MOlecular Simulation (GROMOS) FF, and the Dreiding FF. Contextually, the principal simulation platforms adopted in the field are the Assisted Model Building with Energy Refinement (AMBER), the GROningen MAchine for Chemical Simulations (GROMACS), the Nanoscale Molecular Dynamics (NAMD) , and the Large-scale Atomic/Molecular Massively Parallel Simulator (LAMMPS). Provided the availability of a given FF , the SW choice is mainly driven by the proficiency of the simulator with the different software and the accessible computational platform. For instance, the speed of AMBER is unparalleled when GPUs are used for computation, while LAMMPS has the steepest learning curve but offers high scalability on CPU-based supercomputers and an impressive variety of methods and procedures for simulation/analysis customization.

The protocol reported in this chapter is based on the use of GAFF forcefield within the AMBER suite of programs. Our choice is based upon the following considerations: (i) the comprehensive availability of analysis tools within AMBER, (ii) the general agreement of the results obtained from simulations performed using GAFF FF with experimental data, (iii) its compatibility with AMBER’s highly performing forcefields for biological macromolecules, and (iv) the unrivaled speed of AMBER simulation software on GPUs. In the used AMBER family of forcefields the potential energy function used assumes the form:

$$ {E}_{\mathrm{AMBER}}=\sum \limits_{i\in \mathrm{bonds}}{k}_{l,i}{\left({l}_i-{l}_{i,\mathrm{eq}}\right)}^2+\sum \limits_{i\in \mathrm{angles}}{k}_{\theta, i}{\left({\theta}_i-{\theta}_{i,\mathrm{eq}}\right)}^2+\sum \limits_{i\in \mathrm{torsions}}\frac{V_{n,i}}{2}\left[1+\cos \left(n{\omega}_i-{\gamma}_i\right)\right]+\sum \limits_{\begin{array}{c}i,j\in \mathrm{atoms},\\ {}\ \mathrm{with}\kern0.5em i&lt;j\end{array}}\left\{{\epsilon}_{ij}\left[{\left(\frac{r_{m, ij}}{r_{ij}}\ \right)}^{12}-2{\left(\frac{r_{m, ij}}{r_{ij}}\right)}^6\right]+\frac{q_i{q}_j}{4\pi {\epsilon}_0{r}_{ij}}\right\} $$

while the first three terms represent the interactions between two (bonded), three (angular), and four (dihedral) atoms connected via covalent bonds. The parameters *k*<sub>*l*</sub>, *k*<sub>*θ*</sub>, and *V*<sub>*n*</sub> are force constants, *r*eqand *θ*~eq~ are equilibrium bond lengths and angles, respectively, and *n* and *γ* are the multiplicity and the phase factor for the dihedral angles. The last term in this FF equation contains a standard Lennard Jones (LJ) term for the van der Waals interactions (in which *r*<sub>*m*, *ij*</sub> and *ϵ* represent the minimum of the potential between two atoms *i* and *j* and the corresponding well depth, respectively), and a Coulombic energy term accounting for electrostatic interactions. In this term, *q*<sub>*i*</sub> and *q*<sub>*j*</sub> are the partial charges on the *i*th and *j*th atoms, and *ϵ*~0~ is the vacuum permittivity. The *r*<sub>*m*, *ij*</sub> and *ϵ*<sub>*ij*</sub> parameters for every couple of atoms in the system are computed from the self-interaction terms applying the Lorentz−Berthelot rules: *r*<sub>*m*, *ij*</sub> = (*r*<sub>*m*, *ii*</sub> + *r*<sub>*m*, *jj*</sub>)/2 and $$ {\epsilon}_{ij}=\sqrt{\epsilon_{ii}{\epsilon}_{jj}} $$.

### 2.2 Radius of Gyration and Asphericity

The radius of gyration *R**g* provides a quantitative characterization of the real size of a dendrimer molecule, and is defined as:

$$ \left\langle {R}_g^2\right\rangle =\frac{1}{M}\left\langle\ {\sum}_{i=1}^n{m}_i{\left({c}_i-C\right)}^2\ \right\rangle $$

where *M* and *n* are the total mass and number of atoms of the dendrimer, *c*<sub>*i*</sub> and *m*<sub>*i*</sub> are the position and mass of the *i*th atom, *C* is the center of mass of the dendrimer, and the angular brackets denote an ensemble average over the sampled configurations. The radius of gyration is strictly related to the spatial distribution of the dendrimer atoms, and ultimately to its size in solution. As such, *R*<sub>*g*</sub> can be very useful to characterize the effect of some modification in the terminal units of a family of dendrimers of the same generation, or to study the effect of the protonation state on the structural configuration of a dendrimer. When computing *R**g*, it is also possible to estimate the relevant radius of gyration tensor ***R***<sub>***g***</sub>. The eigenvalues of ***R***<sub>***g***</sub> are its principal moments *l*<sub>*x*</sub>, *l*<sub>*y*</sub>, and *l*<sub>*z*</sub> (with *l*<sub>*x*</sub> ≤ *l*<sub>*y*</sub> ≤ *l*<sub>*z*</sub>), from the knowledge of which the dendrimer asphericity *b* can also be calculated as:

$$ b={l}_z-\frac{1}{2}\left({l}_x+{l}_y\right) $$

As a useful descriptor of anisometry, *b* measures the deviation of a molecular geometry from a spherical form, in that for a perfectly spherical distribution of atoms *b* = 0, for prolate molecules *b* values are close to 0.25, whereas oblate molecules are characterized by values of *b* ≈ 1. As such, the evaluation of *b* can yield very insightful information about a dendrimer’s shape modification when, e.g., it forms a complex with siRNA.

### 2.3 Radial Monomer Density

While *b* and ***R***<sub>***g***</sub> are overall descriptors of a dendrimer shape , the radial monomer density *ρ*(*r*) is a tool to study the distributions of monomers and/or other different molecular elements within a dendrimeric structure. *ρ*(*r*) is defined as the number of atoms that are located within a spherical shell of radius *r* and thickness *Δr* from a reference center, usually taken as the dendrimer’s center of mass. This analysis tool can convey many fine details information about the structure of the dendrimer under investigation including, by way of example, the extent of compactness of the dendrimer interior, the relative spatial distribution of the different dendrimer sub-generations within the entire dendrimer shell, and, last but not least, the distributions of the dendrimer terminal units with respect to the dendrimer core, i.e., the degree of dendrimer back-folding. Importantly, the distribution of other molecules like water, ions, counterions, and siRNA fragments with respect to dendrimer core can also be described by behavior of the corresponding *ρ*(*r*).

### 2.4 Solvent Accessible Surface Area and Interior Cavities

Water can play a key role both in the stabilization of the dendrimer structure and in its interactions with siRNA, mainly via the formation of an extensive network of hydrogen bonds. A measure of a dendrimer’s surface exposed to the solvent is given by its accessible surface area (*ASA*) . For any given molecule, *ASA* is typically calculated using the so-called *rolling ball* algorithm [[40](clbr://internal.invalid/OEBPS/html/485053_1_En_16_Chapter.xhtml#CR40)], which employs a sphere of a particular radius *r*<sub>*p*</sub> (e.g., a typical *r*<sub>*p*</sub> value is 1.4 Å, which approximates the radius of a water molecule) to “probe” the surface of the molecule. It is interesting to observe that, for a hypothetical spherical dendrimer without internal voids, the value of its *ASA* should increase with the square of the probe size *r*<sub>*p*</sub>

$$ AS{A}_{\mathrm{sphere}}=4\pi {\left({r}_d+{r}_p\right)}^2 $$

in which *r*<sub>*d*</sub> is the radius of the dendrimer. Accordingly, any deviation from linearity observed in a plot showing the square root of the calculated *ASA* as a function of *r*<sub>*p*</sub> is suggestive of the presence of internal voids in the corresponding dendrimer structure.

### 2.5 MM/PBSA

A relatively quick and not particularly computationally intensive procedure to estimate the free energy of binding (*ΔG*~bind~) between a dendrimer and its cargo is the Molecular Mechanics—Poisson-Boltzmann (Generalized Born) Surface Area (MM-PB(GB)SA) methodology. The framework of this theory is summarized by the following equations:

$$ \varDelta {E}_{\mathrm{MM}}=\varDelta {E}_{\mathrm{covalent}}+\varDelta {E}_{\mathrm{vdW}}+\varDelta {E}_{\mathrm{ele}} $$

$$ \varDelta {G}_{\mathrm{solv}}=\varDelta {G}_{\mathrm{polar}}+\varDelta {G}_{\mathrm{nonpolar}} $$

$$ \varDelta {H}_{\mathrm{bind}}=\varDelta {E}_{MM}+\varDelta {G}_{\mathrm{solv}} $$

$$ \varDelta {G}_{\mathrm{bind}}=\varDelta {H}_{\mathrm{bind}}- T\varDelta {S}_{\mathrm{bind}} $$

where *ΔE*~MM~ represent the gas-phase molecular mechanical energy change, composed by *ΔE*~covalent~ (the contribution of the covalent interactions energies: bonded, angles, torsions), *ΔE*~vdW~ (the variation of the nonbonded van der Waals energy), and *ΔE*~ele~ (the change in the electrostatic calculated from the Coulomb potential). *ΔG*~solv~ represents the solvation free energy change, composed by its polar *ΔG*~polar~ and nonpolar *ΔG*~nonpolar~ contributions. The sum of *ΔE*<sub>*MM*</sub> and *ΔG*~solv~ give the enthalpic contribution to the free energy (*ΔH*~bind~), while *TΔS*~bind~ is the corresponding variation in conformational entropy upon binding (where *T* is the system temperature in Kelvin). The polar term *ΔG*~polar~ is computed by replacing the solvent with a continuum medium with comparable dielectric constant (e.g., 78 for water) either using a Generalized Born (MM-**GB**SA)  pairwise approximation or by directly solving the Poisson-Boltzmann eq. (MM-**PB**SA). The nonpolar contribution to solvation *ΔG*~nonpolar~, arising both from van der Waals interactions between the dendrimer/siRNA complex and the solvent and from the formation of a cavity in the solvent due to the presence of the solute itself, is usually calculated according to the following empirical expression for non-small molecules like dendrimers:

$$ \varDelta {G}_{\mathrm{nonpolar}}=\varDelta {G}_{\mathrm{disp}}+\gamma SAV+\beta $$

where *ΔG*~disp~ is the dispersion term due to the van der Waals interactions of the dendrimer/siRNA supramolecular assembly with the solvent, and can be computed via a solvent accessible surface integration. The rest of the equation accounts for the cavity formation via a combination of two empirical constants (*γ* and *β*) and a solvent accessible volume (*SAV*), i.e., the volume enclosed by the surface area of the solute. Finally, the entropic contribution to dendrimer/siRNA binding *ΔS*~bind~ is usually estimated resorting to two most popular approaches: the normal mode analysis or the quasi harmonic approximation. As dendrimers are generally quite flexible molecules, a correct estimation of this last thermodynamic quantity may play a decisive role in the estimation of an ultimately realistic in silico *ΔG*~bind~ value.

## 3 Methods

### 3.1 Box and Simulation Input Parameters Creation

This procedure is used to create a solvated box and the corresponding input files (a topology PRMTOP and an initial coordinates INPCRD files) for the simulation with AMBER. The procedure is valid for creating the input parameter for the single dendrimer or siRNA alone, or the dendrimer-siRNA complex (from now on the name *solute* is used to indicate any of them in this section) starting from a coordinates PDB file (*see* Subheadings [3.3](clbr://internal.invalid/OEBPS/html/485053_1_En_16_Chapter.xhtml#Sec11)–[3.5](clbr://internal.invalid/OEBPS/html/485053_1_En_16_Chapter.xhtml#Sec13) for the creation of the file for the dendrimer, siRNA and complex, respectively). Open a *tleap* session with the following command:

```shell
tleap -s
```
1. Load the required forcefield library files into AMBER’s tleap software. For parametrizing the dendrimer and the complex load the library and parameters created in Subheading [3.1](clbr://internal.invalid/OEBPS/html/485053_1_En_16_Chapter.xhtml#Sec9) together with the general *leaprc.gaff* library file, while for the siRNA parameterization load the *leaprc.RNA.OL3* library file. The last command will load the recommended Amber FF for RNA simulations: the *f99* AMBER forcefield with its *bsc0* and *χOL3* updates [[49](clbr://internal.invalid/OEBPS/html/485053_1_En_16_Chapter.xhtml#CR49), [50](clbr://internal.invalid/OEBPS/html/485053_1_En_16_Chapter.xhtml#CR50)]. Load also the *leaprc.water.tip3p* library needed to solvate and add the Na+ and Cl− ions. Finally, load the 3D coordinates files of the solute and save the topology and initial coordinates files for further analysis. All of the above can be obtained by entering the following commands:

   ```shell
source leaprc.gaff
source leaprc.RNA.OL3
source leaprc.water.tip3p
loadamberparams dendrimer.frcmod
loadamberprep dendrimer.prepi
a=loadpdb SOLUTE.pdb
saveamberparm a SOLUTE.prmtop SOLUTE.inpcrd
   ```

2. Now solvate the solute with TIP3P [[51](clbr://internal.invalid/OEBPS/html/485053_1_En_16_Chapter.xhtml#CR51)] water molecules (a simple planar three point model for water, commonly used for biological simulations) by creating a cubic solvent box with dimensions ranging at least 1.5 nm from the edges of each solute molecule. In MD simulations is important that the solute does not interact with its images belonging to the adjacent periodic boxes; thus, it is imperative to create a shell of solvent greater than the nonbonded cutoff used during the subsequent MD simulations (0.9 nm, as reported in the parameter *cut* in Table [1](clbr://internal.invalid/OEBPS/html/485053_1_En_16_Chapter.xhtml#Tab1)). Accordingly, type the following command:

   ```shell
   solvatebox a TIP3PBOX 15.0
   ```


3. 3.

   Now add the Na+ and Cl− counterions needed to neutralize the solute and to reach a concentration 0.15 M of NaCl, representative of a physiological environment. Two *addions* commands needed to automatically neutralize the system with the required number of sodium or chlorine ions, as follows:

   ```shell
   addions a Na+ 0
   addions a Cl- 0
   ```

4. 4.

   While executing the *solvatebox* command, tleap will print the total volume (Vol) of the created simulation box, and this information can be used to compute the number of NaCl molecules needed to attain the physiological ionic strength (150 mM) using the following equation

   $$ \mathrm{NumForPhysConc}=\mathrm{Vol}\times 0.15\times 6.022\times {10}^{-4} $$

5. With a third *addions* command this computed number of sodium and chlorine ions is added to the simulation box. Thus, type:

   ```shell
addions a Na+ NumForPhysConc Cl- NumForPhysConc
   ```

6. Finally, save both a topology and an initial coordinates file of the solvated system (required to carry on the subsequent simulations and analysis steps) by typing:

   ```shell
saveamberparm a SOLUTE.solvated.prmtop SOLUTE.solvated.inpcrd
   savepdb a SOLUTE.solvated.pdb
```
   
With the last command, a reference PDB file containing the model of the solvated simulation box is created.
   
**Table 1** List of input files for pmemd. A detailed description of the input parameters can be found in a recent AMBER manual available on line at https://ambermd.org/Manuals.php. The exclamation mark is used to indicate a comment block, as per FORTRAN 90 standard
   
![485053_1_En_16_Tab1a_HTML](https://raw.githubusercontent.com/zcgkiller/Pictures/main/Wechat/485053_1_En_16_Tab1a_HTML.png)
   
![485053_1_En_16_Tab1b_HTML](https://raw.githubusercontent.com/zcgkiller/Pictures/main/Wechat/485053_1_En_16_Tab1b_HTML.png)
   
![485053_1_En_16_Tab1c_HTML](https://raw.githubusercontent.com/zcgkiller/Pictures/main/Wechat/485053_1_En_16_Tab1c_HTML.png)

### 3.2 Simulation Protocol

This simulation protocol is valid for simulating either the dendrimer or the siRNA molecule alone, or the dendrimer-siRNA complex (i.e., any *solute*). Throughout all the following MD steps, electrostatic interactions are computed by means of the particle mesh Ewald (PME) algorithm.

1. Before starting any MD simulation, it is fundamental to perform an energy minimization process in order to fix steric clashes and optimize the initial model geometries according to the potential energy function. Also, the solvent box generated according to the protocol reported above needs to be optimized at the desired temperature and pressure conditions. Accordingly, first the solvation box has to be gradually heated to 300 K by performing MD simulations in the NVT ensemble (i.e., under constant number of atoms, volume and temperature conditions) to avoid the creation of air bubbles within the solvent, with positional restraint applied to the solute atoms. Then, while still applying positional restraint to the solute atoms, the system density must be equilibrated at 300 K and 1 atm by means of MD simulations in the NPT ensemble (i.e.*,* under constant number of atoms, pressure and temperature). The solute positional restraints have to be gradually removed in 10 runs of subsequent energy minimizations each performed reducing the force of the positional restraints . Finally, another run of heating in the NVT ensemble followed by density equilibration in the NPT ensemble with the solute free of positional restraint is run (*see* Table [1](clbr://internal.invalid/OEBPS/html/485053_1_En_16_Chapter.xhtml#Tab1) for examples of input files). The following pseudo-code can be used to carry on all of these steps:

   ```shell
pmemd -O -i min_sol.in -o min_sol.out -r min_sol.rst \
   -p complex.solvated.prmtop -c complex.solvated.inpcrd
pmemd -O -i heat_sol.in -o heat_sol.out -x heat_sol.nc -r heat_sol.rst \
   -p complex.solvated.prmtop -c min_sol.rst -ref min_sol.rst
pmemd -O -i NPT_sol.in -o NPT_sol.out -x NPT_sol.nc -r NPT_sol.rst \
   -p complex.solvated.prmtop -c heat_sol.rst -ref heat_sol.rst
set PREVIOUS=NPT_sol
   set N=1 ; while N<=11
pmemd -O -i minN.in -o minN.out -r minN.rst \
   -p complex.solvated.prmtop -c PREVIOUS.rst -ref PREVIOUS.rst
set PREVIOUS=minN
   increase N by 1
end
   pmemd -O -i heat_all.in -o heat_all.out -x heat_all.nc -r heat_all.rst \
-p complex.solvated.prmtop -c min10.rst -ref min10.rst
   pmemd -O -i NPT_all.in -o NPT_all.out -x NPT_all.nc -r NPT_all.rst \
-p complex.solvated.prmtop -c heat_all.rst -ref heat_all.rst
   ```

   In each pmemd command (*see* **Note** **1**) the option *-i* and *-o* specify the input and output (log of some energy and physico-chemical parameters of the simulation) files, option *-r* specifies the name of the restart file, option *-x* selects the output coordinates file, option *-p* selects the solvated complex topology file created by tleap, and options *-c* and *-ref* specify the files with the starting and reference coordinates of the system, respectively. 

2. Although a successful energy minimization should get rid of any steric clashes, there are some cases in which the resulting structure is still not perfect (one common example is the presence of intersecting aromatic rings). At least a visual inspection of the final produced configuration is recommended, which can be easily performed loading the produced NPT_all.rst file along with its complex.solvated.prmtop file into a molecular visualization program such as Chimera ([https://www.cgl.ucsf.edu/chimera/](https://www.cgl.ucsf.edu/chimera/))  or VMD ([https://www.ks.uiuc.edu/Research/vmd/](https://www.ks.uiuc.edu/Research/vmd/)) .

3. Once optimization of each system is achieved, productive MD simulations can be performed. The required input file is the md.in file reported in Table 1, and 15 subsequent simulations can be carried out with the following pseudo-code command:

   ```shell
Set PREVIOUS=NPT_all
   set N=1 ; while N<=15
pmemd -O -i md.in -o mdN.out -r mdN.rst \
   -p complex.solvated.prmtop -c PREVIOUS.rst -ref PREVIOUS.rst
set PREVIOUS=mdN
   increase N by 1
end
   ```

   Each of these simulations will run for 10 ns, the first 5 will be discarded as structural equilibration of the solute, and the last 10 produced files (100 ns in total) will be used for subsequent data analysis. 


### 3.3 Dendrimer Parametrization

1. Use any molecular editor software like Avogadro  ([https://avogadro.cc/](https://avogadro.cc/)) to create a 3D representation of the dendrimer (*see* **Note** **2**) and save it in PDB format. 

2. Use AMBER’s *antechamber* software to assign GAFF atom types to the dendrimer and compute its atomic partial charges via the AM1-BCC method, creating a forcefield library file (PREPIN file) for the dendrimer (*see* **Note** **3**). This can be achieved with the following command:

   ```shell
   antechamber -i dendrimer.pdb -fi pdb -o dendrimer.prepi -fo prepi \
   -at gaff -c bcc -nc NET_CHARGE
   ```

   where the options in order of appearance are: the name of the PDB file, the format, the name of the output file, its format, the forcefield to be applied, the method used to compute the partial charges, and finally the total charge of the dendrimer.

3. Use AMBER’s *parmchk2* software to create a file (FRCMOD file) for the eventually missing parameters to integrate the dendrimer forcefield library. Execute this command as:

   ```shell
parmchk2 -i dendrimer.prepi -f prepi -o dendrimer.frcmod
   ```

   where the options in order of appearance are: the name of the input PREPI file (created during the execution of the previous antechamber commands), the format of the input file, and the name of the output file. For PAMAM dendrimers , the parameter selected by *parmchk2* and reported in the FRCMOD file are accurate enough; however, the user is free to implement any parameter refinement at this stage.

4. Follow the steps in Subheadings 3.1 and 3.2 to perform the MD simulation of the dendrimer. The steps in Subheading 3.2 should be repeated three times to obtain the three different trajectories required for further analysis. 


### 3.4 siRNA Model Optimization

1. Use AMBER’s nab program to create an initial 3D structure of the desired siRNA sequence. This will ensure that the siRNA PDB file created will respect the naming conventions used in the AMBER forcefield. Firstly, create a text file called siRNA.nab with the following code:

   ```shell
molecule m;
   fd_helix( “arna”, “YOUR_RNA_SEQUENCE”, “rna”)
putpdb(“siRNA.pdb”, m, “-wwpdb”)
   ```

2. Run nab with the following commands to generate the siRNA.pdb file:

   ```shell
   nab siRNA.nab
   ./a.out
   ```
   
3. Follow the procedure reported in Subheadings 3.1 and 3.2 to obtain a solvated siRNA structure and an MD equilibrated siRNA trajectory in an aqueous environment. 


### 3.5 Complex Creation and Simulation

Electrostatic interactions are usually at the base of the formation of cationic dendrimer/siRNA complexes, and the intermolecular recognition does not depend on a specific sequence on the nucleic acid fragment (base-aspecific). Nonetheless, any information available from laboratory experiments, literature, or previous knowledge on the particular binding of the specific dendrimer to the given siRNA sequence studied should be taken into consideration when creating the relevant complex model.

1. Using Chimera or VMD extract the final equilibrated structure of the dendrimer from its last data collection trajectory.

2. With the same software, extract the final equilibrated structure of the siRNA from its last data collection trajectory.

3. Load both the extracted equilibrated 3D structures of the siRNA and the dendrimer into the visualization software, and place the dendrimer in close proximity of the siRNA yet avoiding visible clashes between their atoms.

4. Save the obtained starting 3D structure of the complex to a coordinates PDB file.

5. Follow all the steps in Subheadings 3.1 and 3.2 to obtain a solvated complex structure and perform data collection.

6. Repeat **steps 3**–**5** two more times, each time rotating the dendrimer and placing it to a different position in relation to the siRNA fragment. At the end of this section, three MD trajectories files will be obtained, each generated from the different dendrimer/siRNA complex starting structures and yet converging to the same equilibrium structure at the end of the corresponding simulation. Should this structural convergence not be achieved, the number of MD simulation must be increased (from 15 to 20 or more) until this condition is satisfied.


### 3.6 Dendrimer Analysis

The analysis of every MD simulation should always begin with a careful observation of the relevant trajectories, as some peculiar phenomena taking place during any phase of the calculation can be intuitively identified and, eventually, further investigated. All analysis steps reported here and in the subsequent section have to be repeated for the three replicate trajectories, and the relevant calculated properties or quantities must be reported as average values. As mentioned above for structural model convergence, also the properties of interest obtained from the different MD trajectories must converge to the same value, and if this is not the case, the simulation cannot be trusted. A possible solution for is to run the simulations longer until convergence is achieved. To enter AMBER’s analysis software cpptraj , just type cpptraj on the AMBER command line. Then, execute the following within cpptraj.

1. Load the equilibrated 100 ns-long dendrimer MD trajectory by typing:

   ```shell
parm dendrimer.prmtop
   for i=6;i&lt;16;i++
trajin MD$i.nc 1 last 10
   done
autoimage
   ```

2. Use the command *radgyr* with the *tensor* option to compute the dendrimer radius of gyration *R*<sub>*g*</sub> and the relevant gyration tensor ***R***<sub>*g*</sub>, from which the molecular asphericity *b* can be obtained (*see* Subheading 2.2 and **Note** **4**):

   ```shell
radgyr RgyrDendrimer :DENDRIMER_MASK out rgyr_dendrimer_alone.out tensor
   ```

3. Next*,* use the command *radial* with the *rawrdf* and *center2* options and selecting the dendrimer as *solute* to calculate any radial monomer density *ρ(r)* from the dendrimer center of mass (*see* Subheading [2.3](clbr://internal.invalid/OEBPS/html/485053_1_En_16_Chapter.xhtml#Sec5)). Set the maximum radius equal to (*R*<sub>*g*</sub> × 1.3 + 15) Å, in which *R*<sub>*g*</sub> is the value of the dendrimer radius of gyration calculated in the preceding step (2). Set spacing = 0.5 Å. This command must be three times, each time selecting i) the water oxygens, ii) the dendrimer terminal nitrogens, and iii) the whole dendrimer atoms, respectively, to obtain corresponding *ρ(r)* profiles around the center of mass of the dendrimer (*see* **Note** **5**). Accordingly, type:

   ```shell
   radial out radial_density.out 0.5 MAX_RADIUS \
   :WAT@O :DENDRIMER_MASK rawrdf center2
   radial out radial_density.out 0.5 MAX_RADIUS \
   :DENDRIMER_MASK@TERMINAL_NITROGEN :DENDRIMER_MASK rawrdf center2
   radial out radial_density.out 0.5 MAX_RADIUS \
   :DENDRIMER_MASK :DENDRIMER_MASK rawrdf center2
   ```
   
4. Now use the command *molsurf* selecting the dendrimer atoms to compute the relevant accessible surface area (*ASA)* (*see* Subheading 2.4). This command has to be issued multiple time, varying the *probe* option from 0.5 Å to 9.5 Å at 0.3 Å interval. The dendrimer interior cavities and voids can then be identified by plotting the square root of the *ASA* values thus obtained as a function of the probe radius used (*see* **Note** **6**). Accordingly, type:

   ```shell
   molsurf ASA_05 :DENDRIMER_MASK out ASA_05.out probe 0.5
   molsurf ASA_08 :DENDRIMER_MASK out ASA_08.out probe 0.8
   molsurf ASA_11 :DENDRIMER_MASK out ASA_11.out probe 1.1
   …
   molsurf ASA_95 :DENDRIMER_MASK out ASA_95.out probe 9.5
   ```

### 3.7 siRNA-Dendrimer Complex Structural Analysis

1. Load the equilibrated 100 ns-long dendrimer/siRNA complex MD trajectory into AMBER’s *cpptraj* software by issuing the same commands described in the previous step. 

2. Within *cpptraj,* select the dendrimer atoms and use the command *radgyr* with the *tensor* option to compute the *R*<sub>*g*</sub>, ***R***<sub>*g*</sub> and *b* of the siRNA-bound dendrimer over time. Compare these values with those obtained for the uncomplexed dendrimer in solution obtained at point 2 in Subheading 3.6.

3. Next use the command *radial* with the *rawrdf* and *center2* options and selecting the dendrimer as *solute*. Follow the same procedure described in **step 3** of Subheading 3.6 to set the corresponding values of the maximum radius and spacing. Issue this command 4 times, each time selecting different atoms as *solvent* (water atoms, the terminal nitrogen atoms, the whole dendrimer atoms and the siRNA atoms, respectively), to obtain the *ρ(r)* profiles for the selected atoms around the dendrimer center of mass (*see* **Note** **5**).


### 3.8 siRNA-Dendrimer Energy of Binding Analysis

1. Use AMBER’s MMPBSA.py script to compute the enthalpic contribution to free energy of binding . Select the last two equilibrated MD trajectories obtained for dendrimer, siRNA and their complex, respectively, and pick one every 10 MD frames. The corresponding total number of frames thus will be 200. In the *&pb* section set *inp* equal 1 (to separate the dispersion and cavity formation terms) and *indi* equal 3, as required when dealing with highly charged macromolecules. Also, turn on energy decomposition with *&dec*, to obtain the contribution of each dendrimer residue to siRNA binding (*see* **Note** [**7**](clbr://internal.invalid/OEBPS/html/485053_1_En_16_Chapter.xhtml#Sec17)). Then, move all trajectories and topology files to the same directory, and use the following command line:

   ```shell
MMPBSA -O -i mmpbsa_enth.in -o dH_dendrimer_siRNA.out \
   -sp complex.solvated.prmtop -cp complex.prmtop \
-rp siRNA.prmtop -srp siRNA.solvated.prmtop
   -lp dendrimer.prmtop -slp dendrimer.solvated.prmtop \
-y md14.complex.nc md15.complex.nc \
   -yr md14.siRNA.nc md15.siRNA.nc \
-yl md14.dendrimer.nc md15.dendrimer.nc
   ```

   where the options *-i* and *-o* specify the input and output files, the options *-sp*, *−slp*, *−srp* select the topology files of the solvated complex, dendrimer (ligand) and siRNA (receptor), respectively. Likewise, the options *-cp*, *−lp*, *−rp* and *-y*, *−yl*, *−yr* select the un-solvated topologies for the same systems and their corresponding solvated trajectories, respectively. The content of the mmpbsa_enth.in file is reported in Table 2.

2. Use AMBER’s MMPBSA.py script to compute the entropic contribution to free energy of binding. Select the same equilibrated trajectories used for enthalpy calculations, and pick one every 50 frames, for a total of 20 analyzed frames. Then, use the following command:

   ```shell
MMPBSA -O -i mmpbsa_entr_nmode.in -o TdS_dendrimer_siRNA.out \
   -sp complex.solvated.prmtop -cp complex.prmtop \
-rp siRNA.prmtop -srp siRNA.solvated.prmtop
   -lp dendrimer.prmtop -slp dendrimer.solvated.prmtop \
-y md14.complex.nc md15.complex.nc \
   -yr md14.siRNA.nc md15.siRNA.nc \
-yl md14.dendrimer.nc md15.dendrimer.nc
   ```

   The content of the mmpbsa_entr_nmode.in file is reported in Table 2.

3. As the last step, use the fundamental Gibbs equation, *ΔG*~bind~ = *ΔH*~bind~ − *TΔS*~bind~, to obtain the corresponding free energy of binding between the dendrimer and the siRNA (*see* Subheading 2.5, **Notes** **8** and **9**).


**Table 2** List of input files for energy of binding calculations. A detailed description of the input parameters can be found in a recent AMBER manual available on line at https://ambermd.org/Manuals.php

![485053_1_En_16_Tab2_HTML](https://raw.githubusercontent.com/zcgkiller/Pictures/main/Wechat/485053_1_En_16_Tab2_HTML.png)

## 4 Notes

1. The commands presented to perform energy minimization and MD simulations use the *pmemd* software of AMBER in its serial implementation, e.g., running on a single core. Given that powerful computational resources are commonly available to date, the single-core protocol was proposed in order to adopt a platform-agnostic approach. However, AMBER offers a parallel version of the software, pmemd.MPI, and also a GPU-based version called pmemd.cuda. Without entering in the technical details of the precision of the GPU-based code, our suggestion is to use it for every step of MD simulations whenever an appropriate hardware is available. To perform the energy minimization, however, the parallel pmemd.MPI version is always recommended. 

2. The regularly self-similar nature of dendrimers usually leads to a straightforward subdivision of their structure in a small number of repetitive moieties. Generally, for any dendrimer a central core unit, a repeating entity, and a terminal group can be identified, as shown in Fig. 1. Moreover, to build different dendrimer generations (G), successive layers of the repeating units can be simply added (Fig. 1). This dendrimer model building is also very practical as it allows for the fast FF parameterization of each individual dendrimer fragment. This procedure also offers further computational advantages: (i) it simplifies the process of computing the partial-charges, if needed (*see* **Note** **3**), (ii) it allows for the straightforward creation of different generations of the same dendrimer, and (iii) it offers an easier and more intuitive presentation of the final analysis for different properties. 

3. A more robust way of computing the partial charges is via the Restrained Electrostatic Potential (RESP) procedure, which can be easily carried out in an automated fashion via the R.E.D. server. The process involves first a geometry optimization of the studied molecule; next, the minimized structure is used to compute a Molecular Electrostatic Potential (MEP) on a three-dimensional grid employed to fit atom-centered charges. Both these steps involve heavy quantum chemistry computations, and so they cannot be performed on large molecules like, e.g., dendrimers with G > 1. If, however, the dendrimer structure has been subdivided into its fundamental units (*see* **Note** **2**), one can easily apply the RED-based automated RESP on each of these molecular building blocks. 

4. The radius of gyration *Rg* and asphericity *b* are two molecular descriptors (*see* Subheading 2.2) particularly helpful in the characterization of a dendrimer size and shape and its variation across generations or under the effect of a change in the surrounding medium (e.g., pH, ionic strength, temperature). Importantly, computational *R*g values can be directly compared with those obtained by different experimental techniques including dynamic light scattering (DLS) and small angle X-ray scattering (SAXS) (*see* Table 3). As an example, in our computational study on PAMAM dendrimers with generation ranging from G1 to G6, we could nicely show how the molecular size—expressed as the corresponding *R*<sub>*g*</sub> values—increased with increasing dendrimer generation and with decreasing pH (*see* Table 3 and Fig. 2). In particular, the molecular expansion detected at lower pH is ascribable to the enhanced charge-charge repulsion originating from the protonation of the tertiary amine nitrogens in the dendrimer inner shells. As the number of charged residues within the dendrimer structure protons increases, chloride ions will then begin to diffuse into the endosome in an attempt to restore the equilibrium potential, and this raises the osmotic pressure. This, in turn, causes the endosome to swell and expand until it passes a critical area strain, rupturing the lipid bilayer membrane and releasing the endosome contents into the cell (the so-called proton-sponge effect) . Considering that endosome entrapment and subsequent escape into the cytoplasm are fundamental stages in the process of nanovectors-assisted siRNA delivery, the ability of predicting related structural changes in the nanocarrier per se or in complex with its payload is of immediate paramount importance. 

5. The plots of the radial monomer density *ρ*(*r*) can be very informative about the internal structure of a dendrimer nanocarrier. First of all, as mentioned in the main text (*see* Subheading 2.3), when *ρ*(*r*) is calculated considering the distribution of all atoms around the dendrimer center of mass, it gives an indication about the compactness of the dendrimer interior. As an example, from Fig. 3 it can be observed that PAMAM dendrimers maintain the compact structure that characterizes these molecules when alone in solution (Fig. 3a and d, continuous lines) also once bound to siRNA (Fig. 3c and f). In other words, binding of a siRNA fragment to cationic PAMAMs does not reflect into a significant alternation of the nanocarrier molecular conformation. Also, another particularly instructive information can be gathered by analyzing the distributions of the dendrimer terminal units again with respect to the dendrimer’s center of mass. Indeed, although dendrimers are usually depicted as ordered branched structures, these molecular configurations are far from the actual conformation these compounds adopt in solution. Particularly, as the dendrimer generation G increases, some of the terminal units can be located within the dendrimer’s interion instead of pointing toward the solvent (a phenomenon known as back-folding) and, as such, cannot actively contribute to siRNA binding via electrostatic/hydrogen bond interactions. In this respect, our computational study of the distribution of the cationic PAMAM dendrimer terminal groups shows that the back-folding phenomenon becomes progressively more pronounced i) as the dendrimer generation increases and ii) as the pH of the solution changes from acidic to neutral (*see* Fig. 3b and e). The distribution of solvent molecules and of solution ion and counterions with respect to the dendrimer core can also be described with this technique. As can be seen for example in Fig.  3a and d, a considerable amount of water can permeate the dendrimer outer shell, water uptake clearly being dependent upon dendrimer generation. As it might be expected, water permeation is more pronounced at lower pH while, in neutral solutions, a greater effect of the dendrimer generation can be observed, dendrimers with higher G having less hydrated dendrimer branches (*see* Fig. 3a and d). In an entirely analogous fashion, the degree of molecular interpenetration between a siRNA fragment and its dendrimeric nanovector can also be investigated. As shown in Fig. 3c and f, a considerable overlap between siRNA and dendrimer *ρ*(*r*) profiles can be predicted; in other words, MD simulations thus reveal that the nucleic acid can reach deeper into the dendrimer structure, binding tightly to its carrier. 

6. Plotting the square root of calculated *ASA* as a function of *p*r (*see* Subheading 2.4) can help in identifying the maximum size a molecule can have to access the internal cavities of a dendrimer in solution. As an example, for G5 and G6 PAMAM dendrimers a deviation from linearity is observed for *p**r* < 6 Å (*see* Fig. 4). This evidence is in line with what is observed inspecting the corresponding siRNA-dendrimer complexes, for which only a few (smaller) base pairs can penetrate into the inner dendrimer structure. Moreover, such dendrimer interior void regions increase with decreasing pH (compare the two plots of Fig.4), in line with the observed dendrimer swelling in more acidic conditions. 

7. Undoubtedly, a fundamental aspect of the characterization cationic dendrimers in complex with siRNA therapeutics is the relative affinity between the nanovector and its cargo. One of the main advantages of the MM-PBSA computational approach (*see* Subheading 2.5) is that it can yield both quantitative and qualitative information about the nature of the underlying nanovector/siRNA interactions upon binding. Frequently, studies are carried on a homologous series of dendrimers in which the effect of the generation is interrogated. However, for any dendrimer structure the number of terminal units increase exponentially with the dendrimer generation branching point multiplicity. Therefore, in order to compare the affinity of different generations of homologous dendrimers for a given siRNA, a normalization of the binding energy components with respect to the number of charge-carrying groups of the dendrimer is typically done. This allows for a correct affinity ranking of different dendrimer generations for the nucleic acid fragment, ultimately leading to the identification of the most performing nanocarrier. As the synthesis of high G dendrimers is very complex, costly, and time consuming, the preliminary in silico identification of the lowest yet most effective generation is of obvious utmost importance. Notably, the procedure described in **Note** **1** according to which a dendrimer molecule is partitioned into its main building blocks (core, branching units, and terminal groups, Fig. 1) allows to exploit another feature of the MM-PBSA methodology, i.e., the so-called per-residue free energy decomposition, which can ultimately lead to an even more precise way to compare siRNA binding by different dendrimer generations. This method identifies the number of dendrimer branches mostly involved in siRNA interactions, *N*<sub>*eff*</sub>. Summing all the energetic contribution afforded by each siRNA binding-effective dendrimer branch yields the effective free energy of binding $$ \varDelta {G}_{\mathrm{bind}}^{\mathrm{eff}} $$ of the relevant siRNA/dendrimer complex (*see* Fig. 5). An example of the application of this computational procedure can be found in the study focused on the interaction between a triethanolamine (TEA)-core G5 PAMAM dendrimer and a series of siRNAs bearing overhangs of different nature and length. As can be seen in Fig. 5, for this G5 TEA-core PAMAM nanovector the number of dendrimer terminal groups effective in binding the nucleic acid—*N*eff—is found to increase with the length of the siRNA overhangs (i.e., from 2 to 7 base pairs). Accordingly, the corresponding $$ \varDelta {G}_{\mathrm{bind}}^{\mathrm{eff}} $$ values becomes progressively more negative, i.e., more favorable. As far as the nature of the siRNA overhangs is concerned, the MM/PBSA analysis also reveals that (i) the rigid nature of the adenine overhangs reflects into a less unfavorable entropic contribution to binding for the systems featuring these overhangs, and (ii) those siRNA bearing the longest adenine overhangs exhibit the highest affinity for the G5 TEA-core PAMAM nanocarrier in the entire series of nucleic acid fragments analyzed.

8. Another computational technique that can be used to rank the binding affinity of different dendrimers toward their siRNA cargoes and gather more details on their binding mutual binding mechanisms is the application of the constant velocity steered molecular dynamic (CV-SMD) method. During a CV-SMD simulation, a force is applied between two different groups of atoms or molecules (e.g., the dendrimer and the siRNA) along the vector joining their centers of mass. This force acts modifying the distance between the selected two groups of atoms, pulling them apart. As the velocity at which the two groups are pulled away must remain constant during the simulation, the corresponding force required to move the groups at each timestep under such condition is recorded. The peak force needed to separate two molecular entities such as a dendrimer and a siRNA fragment can be identified from the time profiles of the pulling force during the CV-SMD unbinding simulation. This value is characteristic for every intermolecular complex, and, being strictly related to the binding strength, it can be used to rank the affinities between, e.g., different dendrimer generations and/or dendrimers of different chemistries and siRNAs. This approach also gives a dynamic perspective of a supramolecular complex unbinding process, and the time at which the peak force is attained can be correlated with other important property as the siRNA release from its nanovectors (*see* **Note** **9**). 

9. In the same study reported in **Note** **7**, we also applied the CV-SMD approach (*see* **Note** **8**) to study the unbinding of the G5 TEA-core PAMAM from the siRNA molecules decorated with different overhangs. The peak forces extracted from the time profiles of the force during the CV-SMD unbinding simulations are found in strong correlation with the respective $$ \varDelta {G}_{\mathrm{bind}}^{\mathrm{eff}} $$ obtained from the corresponding classical MD simulations (*R*<sub>*2*</sub> = 0.95, Fig. 6): the more negative (favorable) the $$ \varDelta {G}_{\mathrm{bind}}^{\mathrm{eff}} $$ value, the larger the force needed to perform the unbinding event. In other words, while a great nanovector affinity for its siRNA cargo can be desirable in phases of siRNA delivery as complexation, protection, and transport within the bloodstream, it can ultimately constitute an obstacle in the later stage of siRNA release. Accordingly, a fine balance between affinity and ability to discharge its payload endows a cationic dendrimer nanovector with the best properties in gene silencing applications . Another important and unique information yielded by this technique is the time at which the force peak is reached. As again seen in Fig. 6, for the TEA-core G5 PAMAM dendrimer in complex with the more flexible thymine overhangs of length 5 and 7 the force is at its maximum value already after ~150 ps, while it takes more than 2 ns for the corresponding complexes with siRNAs bearing adenine overhangs to attain the same condition. This indicates that those siRNA decorated with the more flexible thymine overhangs, which are endowed with a somewhat lower affinity for the dendrimer nanocarrier compared to the alternative nucleic acid fragments bearing the more rigid adenine ones, also dissociate at earlier time points. This peculiar combination of easier nanocarrier detachment and yet sufficient dendrimer binding affinity ultimately constitute an optimal compromise for the 7 base pair-long thymine overhang siRNA/G5 TEA-core PAMAM dendrimer nanovector complex, in agreement with the corresponding experimental evidence as the most efficient gene silencing delivery complex in the entire series.


![485053_1_En_16_Fig1_HTML](https://raw.githubusercontent.com/zcgkiller/Pictures/main/Wechat/485053_1_En_16_Fig1_HTML.png)

**Fig. 1** Schematic representation of a PAMAM dendrimer, subdivided into its fundamental building blocks: light green, core, orange, repeating units, purple, terminal groups

**Table 3** Radius of gyration values [Å] for PAMAM dendrimers obtained from MD simulations at two different pH values (standard deviation in parenthesis). Experimental values obtained from SAXS experiments are given for comparison

| Generation | pH 5^a^      | pH 7.4^a^    |         | SAXS^b^ |          |
| :--------- | ------------ | ------------ | ------- | ------- | -------- |
| G1         | 10.19 (0.34) | 09.85 (0.30) |         |         |          |
| G2         | 13.88 (0.37) | 14.44 (0.41) |         |         |          |
| G3         | 17.96 (0.17) | 16.25 (0.38) | 15.8^c^ | 16.5^d^ | 15.09^d^ |
| G4         | 21.00 (0.22) | 19.00 (0.21) | 17.1    | 17.6    | 18.06    |
| G5         | 24.23 (0.18) | 22.43 (0.29) | 24.1    | 25.3    | 23.07    |
| G6         | 28.90 (0.10) | 27.21 (0.11) | 26.3    | 27.5    | 27.5     |

a *See* reference [[9](clbr://internal.invalid/OEBPS/html/485053_1_En_16_Chapter.xhtml#CR9)]

b *See* references [[66](clbr://internal.invalid/OEBPS/html/485053_1_En_16_Chapter.xhtml#CR66), [67](clbr://internal.invalid/OEBPS/html/485053_1_En_16_Chapter.xhtml#CR67)]

c In CH~3~OH from sphere model

d In CH~3~OH from Guinier plot. Adapted from [[9](clbr://internal.invalid/OEBPS/html/485053_1_En_16_Chapter.xhtml#CR9)], with the permission of John Wiley and Sons

![485053_1_En_16_Fig2_HTML](https://raw.githubusercontent.com/zcgkiller/Pictures/main/Wechat/485053_1_En_16_Fig2_HTML.png)

**Fig. 2**

Log-log plot of *R*g calculated as a function of the PAMAM dendrimer molecular weight (*M*w). Adapted from [[9](clbr://internal.invalid/OEBPS/html/485053_1_En_16_Chapter.xhtml#CR9)], with the permission of John Wiley and Sons

![../images/485053_1_En_16_Chapter/485053_1_En_16_Fig3_HTML.png](clbr://internal.invalid/OEBPS/images/485053_1_En_16_Chapter/485053_1_En_16_Fig3_HTML.png)

**Fig. 3** Panels **a**, **b**, **d**, **e**: radial monomer distribution for G1 to G6 PAMAM dendrimers (continuous line), water (broken lines) and terminal nitrogens (dotted-broken lines) from MD simulations of each dendrimer in solution. Panels **c** and **f**: radial monomer distribution for G4 to G6 PAMAM dendrimers (continuous line) in complex with siRNA (dotted-broken lines) and water (broken lines). Results are from simulations at pH 5 (upper raw) and pH 7.4 (lower raw). Color code: red, G1; light green, G2; dark green, G3; blue, G4; purple, G5; dark red, G6. Adapted from [[9](clbr://internal.invalid/OEBPS/html/485053_1_En_16_Chapter.xhtml#CR9)], with the permission of John Wiley and Sons

![485053_1_En_16_Fig4_HTML](https://raw.githubusercontent.com/zcgkiller/Pictures/main/Wechat/485053_1_En_16_Fig4_HTML.png)

**Fig. 4** Square root of the *ASA* as a function of the probe radius for PAMAM dendrimers G4 (blue circles), G5 (purple squares), and G6 (dark red triangles) at pH 5.0 (**a**) and pH 7.4 (**b**). Adapted from [[9](clbr://internal.invalid/OEBPS/html/485053_1_En_16_Chapter.xhtml#CR9)], with the permission of John Wiley and Sons

![485053_1_En_16_Fig5_HTML](https://raw.githubusercontent.com/zcgkiller/Pictures/main/Wechat/485053_1_En_16_Fig5_HTML.png)

**Fig. 5** G5 PAMAM dendrimer branches effectively interacting (*N*eff) involved in siRNA binding, as well as enthalpic ($$ \varDelta {H}_{\mathrm{bind}}^{\mathrm{eff}} $$), entropic ($$ - T\varDelta {S}_{\mathrm{bind}}^{\mathrm{eff}} $$) and total effective free energy ($$ \varDelta {G}_{\mathrm{bind}}^{\mathrm{eff}}=\varDelta {H}_{\mathrm{bind}}^{\mathrm{eff}}- T\varDelta {S}_{\mathrm{bind}}^{\mathrm{eff}} $$), components of binding of the siRNA molecules with different overhangs toward the dendrimeric carrier. Adapted from [[13](clbr://internal.invalid/OEBPS/html/485053_1_En_16_Chapter.xhtml#CR13)], with the permission of the American Chemical Society

![485053_1_En_16_Fig6_HTML](https://raw.githubusercontent.com/zcgkiller/Pictures/main/Wechat/485053_1_En_16_Fig6_HTML.png)

**Fig. 6** (**a**) Time profile of the force of siRNA unbinding from their G% PAMAM dendrimer complexes. Color legend: blue, siRNA(T5/T5); green, siRNA(T7/T7)); yellow, siRNA(A7/A7)); red, siRNA(A5/A5)); black, siRNA(T2/T2). (**b**) Correlation between the CV-SMD peak force and the effective binding free energy $$ \varDelta {G}_{\mathrm{bind}}^{\mathrm{eff}}\Big) $$ for the corresponding siRNA and G5 dendrimer complexes. Adapted from [[13](clbr://internal.invalid/OEBPS/html/485053_1_En_16_Chapter.xhtml#CR13)], with the permission of the American Chemical Society.