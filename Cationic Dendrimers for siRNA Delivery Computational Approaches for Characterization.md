# Cationic Dendrimers for siRNA Delivery: Computational Approaches for Characterization

Domenico Marson, Suzana Aulic, Maurizio Fermeglia, Erik Laurini and Sabrina Pricl

## Abstract 摘要

Nowadays, computer simulations have been established as a fundamental tool in the design and development of new dendrimer-based nanocarriers for drug and gene delivery. Moreover, the level of detail contained in the information that can be gathered by performing atomistic-scale simulations cannot be obtained with any other available experimental technique. In this chapter we describe the main computational toolbox that can be exploited in the different stages of novel dendritic nanocarrier production—from the initial conception to the stage of biological intermolecular interactions.

<span style=color:blue>在现代树枝状纳米载体的设计与开发中，计算机模拟已被确立为不可或缺的工具。原子尺度模拟所提供的信息细节超出了当前实验技术的能力范围。在本章中，我们将介绍在树枝状纳米载体生产的各个阶段——从最初的概念设计到生物分子相互作用研究——所能使用的核心计算工具和方法。</span>

## 1 Introduction 前言

Today computer simulations constitute an essential tool for the design and development of new dendrimer-based nanocarriers for both drug and gene delivery. Undoubtedly, this success is linked to the exponential increase in affordable computer power and to the optimization/development of highly scalable computer codes able to run in parallel even on consumer-grade graphical processing units (GPUs). Thus, for instance, under the magnifying lens of all-atom molecular dynamics (AA-MD) simulations researchers are now able to follow the exact time and space behavior of a given nanovector in solution at a molecular level, and to characterize its interactions with a specific target. Moreover, the same set of computational techniques allows performing in silico experiments dealing with, e.g., the interactions of dendrimers with biological membranes and proteins, and the eventual aggregation and clustering of dendrimers themselves. In essence, the analysis that can be performed with data obtained from AA-MD simulations is limited only by the creativity and coding proficiency of the investigator, and can be tailored to fit the specificity of the system under study.

<span style=color:blue>随着计算能力的快速提升以及高效并行计算代码的广泛应用，计算机模拟如今已成为设计和开发基于树枝状大分子的药物及基因递送纳米载体的核心工具。通过全原子分子动力学（AA-MD）模拟，研究人员能够在分子尺度上观察纳米载体在溶液中的动态行为，并深入解析其与目标分子的相互作用。这些计算技术还可以用来模拟树枝状分子与生物膜及蛋白的相互作用，甚至研究其自身的聚集行为。AA-MD模拟的分析潜力几乎无限，取决于研究人员的创新思维和编程能力，可以灵活适配于不同的研究系统。</span>

Based on our own experience in the field of computer-assisted cationic dendrimer-based nanovectors for siRNA delivery, in this chapter we will describe the main AA-MD computational toolbox that can be exploited in the different stages of novel dendritic nanocarrier production—from the initial conception to its structural and chemico-physical characterization to the stage of biological intermolecular interactions. Specifically, we will present a protocol for poly(amino amine) dendrimers (PAMAMs) as a proof-of-principle easily adaptable to other cationic dendrimer families. This protocol is subdivided in three main steps: (i) dendrimer and siRNA models building and optimization; (ii) AA-MD simulation of the dendrimer per se and in complex with its siRNA cargo, and (iii) simulation data analysis and correlation with experimental observations. We will further exploit the *Notes* sections to present some technical suggestions as well as some practical examples concerning the application of the computational techniques along with their biological relevance for the benefit of both computational and experimental scientists.

<span style=color:blue>基于我们在利用阳离子树枝状分子作为siRNA递送载体的研究经验，本章将全面介绍一个AA-MD模拟工具箱，涵盖从载体概念设计到结构与物理化学特性表征，再到与生物分子的相互作用研究的全过程。具体而言，我们将以聚（氨基胺）树枝状分子（PAMAM）为例，展示一套易于扩展的模拟流程。这套流程包括三大步骤：（1）构建并优化树枝状分子和siRNA的模型；（2）对单一树枝状分子及其与siRNA复合物进行AA-MD模拟；（3）分析模拟数据并将结果与实验数据进行比较。此外，我们将在“**注释**”部分分享技术提示和实际应用案例，帮助计算和实验领域的研究者更好地理解这些方法的生物学意义。</span>

## 2 Materials 材料

### 2.1 Forcefield and Software 力场与软件

AA-MD simulations try to mimic the behavior of individual atoms with the aid of a computer. Assuming all atoms as rigid spheres, and given the position in space of all atoms in a molecular system, the force experienced by each atom is computed applying a specific energy function, called a forcefield (FF). FFs can differ for the functional form and parameter sets used to calculate the potential energy of a given system of atoms. Newton’s laws are then used to integrate the FF over time, ultimately yielding the dynamic evolution (coordinates) of the molecular system under study.

<span style=color:blue>全原子分子动力学（AA-MD）模拟利用计算机来再现单个原子的行为。它假设原子为刚性球体，并基于分子体系中所有原子的已知空间位置，利用特定的能量函数（即力场，Forcefield, FF）计算每个原子所受的力。力场的功能形式和参数集因研究体系的不同而有所差异，决定了势能的计算方式。接着，通过应用牛顿定律对力场进行时间积分，模拟出分子体系的动态演化轨迹，即研究过程中各原子的动态坐标变化。</span>

While the underlying fundamental theories are highly similar, several different software (SW) are available to perform AA/CG-MD simulations. At the same time, a variety of FFs have been developed—from the most general ones to those custom-tailored to describe a particular system—and not all of them are compatible with all current SW. In the specific case of AA-MD simulations of cationic-dendrimer nanovectors, the most widely employed FFs are the Chemistry at Harvard Macromolecular Mechanics (CHARMM) general forcefield, the General AMBER Forcefield (GAFF) , the GROningen MOlecular Simulation (GROMOS) FF, and the Dreiding FF. Contextually, the principal simulation platforms adopted in the field are the Assisted Model Building with Energy Refinement (AMBER), the GROningen MAchine for Chemical Simulations (GROMACS), the Nanoscale Molecular Dynamics (NAMD) , and the Large-scale Atomic/Molecular Massively Parallel Simulator (LAMMPS). Provided the availability of a given FF , the SW choice is mainly driven by the proficiency of the simulator with the different software and the accessible computational platform. For instance, the speed of AMBER is unparalleled when GPUs are used for computation, while LAMMPS has the steepest learning curve but offers high scalability on CPU-based supercomputers and an impressive variety of methods and procedures for simulation/analysis customization.

<span style=color:blue>尽管基础理论高度相似，但用于全原子（AA）或粗粒化（CG）分子动力学（MD）模拟的软件（SW）种类繁多，各有特色。此外，现有的力场（FF）从通用型到专用型不等，但并非所有力场都适用于所有软件。针对阳离子树状大分子纳米载体的全原子分子动力学模拟，常用的力场包括CHARMM通用力场、GAFF、GROMOS力场和Dreiding力场。相应的主流模拟平台则有AMBER、GROMACS、NAMD和LAMMPS。软件的选择通常依赖于研究者对特定软件的熟练程度以及所使用的计算平台。例如，AMBER在GPU加速计算中的表现最为出色，而LAMMPS虽然学习难度较高，却在CPU架构的超级计算机上展现了强大的可扩展性，并且为模拟与分析提供了丰富的定制化选项和功能。</span>

The protocol reported in this chapter is based on the use of GAFF forcefield within the AMBER suite of programs. Our choice is based upon the following considerations: (i) the comprehensive availability of analysis tools within AMBER, (ii) the general agreement of the results obtained from simulations performed using GAFF FF with experimental data, (iii) its compatibility with AMBER’s highly performing forcefields for biological macromolecules, and (iv) the unrivaled speed of AMBER simulation software on GPUs. In the used AMBER family of forcefields the potential energy function used assumes the form:

<span style=color:blue>本章所报告的协议基于在AMBER软件套件中使用GAFF力场。我们选择这一方案的原因包括：（i）AMBER提供了全面的分析工具，（ii）使用GAFF力场进行的模拟结果与实验数据高度吻合，（iii）GAFF与AMBER中针对生物大分子的高效力场兼容，以及（iv）AMBER在GPU上的模拟速度无与伦比。在AMBER力场家族中，采用的势能函数形式为：</span>

```html
<math xmlns="http://www.w3.org/1998/Math/MathML" display="block">  <msub>    <mrow class="MJX-TeXAtom-ORD">      <mi>E</mi>    </mrow>    <mrow class="MJX-TeXAtom-ORD">      <mrow class="MJX-TeXAtom-ORD">        <mi mathvariant="normal">A</mi>        <mi mathvariant="normal">M</mi>        <mi mathvariant="normal">B</mi>        <mi mathvariant="normal">E</mi>        <mi mathvariant="normal">R</mi>      </mrow>    </mrow>  </msub>  <mo>=</mo>  <munder>    <mo movablelimits="false">∑<!-- ∑ --></mo>    <mrow class="MJX-TeXAtom-ORD">      <mi>i</mi>      <mo>∈<!-- ∈ --></mo>      <mrow class="MJX-TeXAtom-ORD">        <mi mathvariant="normal">b</mi>        <mi mathvariant="normal">o</mi>        <mi mathvariant="normal">n</mi>        <mi mathvariant="normal">d</mi>        <mi mathvariant="normal">s</mi>      </mrow>    </mrow>  </munder>  <msub>    <mrow class="MJX-TeXAtom-ORD">      <mi>k</mi>    </mrow>    <mrow class="MJX-TeXAtom-ORD">      <mi>l</mi>      <mo>,</mo>      <mi>i</mi>    </mrow>  </msub>  <msup>    <mrow class="MJX-TeXAtom-ORD">      <mrow>        <mo>(</mo>        <msub>          <mrow class="MJX-TeXAtom-ORD">            <mi>l</mi>          </mrow>          <mi>i</mi>        </msub>        <mo>−<!-- − --></mo>        <msub>          <mrow class="MJX-TeXAtom-ORD">            <mi>l</mi>          </mrow>          <mrow class="MJX-TeXAtom-ORD">            <mi>i</mi>            <mo>,</mo>            <mrow class="MJX-TeXAtom-ORD">              <mi mathvariant="normal">e</mi>              <mi mathvariant="normal">q</mi>            </mrow>          </mrow>        </msub>        <mo>)</mo>      </mrow>    </mrow>    <mn>2</mn>  </msup>  <mo>+</mo>  <munder>    <mo movablelimits="false">∑<!-- ∑ --></mo>    <mrow class="MJX-TeXAtom-ORD">      <mi>i</mi>      <mo>∈<!-- ∈ --></mo>      <mrow class="MJX-TeXAtom-ORD">        <mi mathvariant="normal">a</mi>        <mi mathvariant="normal">n</mi>        <mi mathvariant="normal">g</mi>        <mi mathvariant="normal">l</mi>        <mi mathvariant="normal">e</mi>        <mi mathvariant="normal">s</mi>      </mrow>    </mrow>  </munder>  <msub>    <mrow class="MJX-TeXAtom-ORD">      <mi>k</mi>    </mrow>    <mrow class="MJX-TeXAtom-ORD">      <mi>θ<!-- θ --></mi>      <mo>,</mo>      <mi>i</mi>    </mrow>  </msub>  <msup>    <mrow class="MJX-TeXAtom-ORD">      <mrow>        <mo>(</mo>        <msub>          <mrow class="MJX-TeXAtom-ORD">            <mi>θ<!-- θ --></mi>          </mrow>          <mi>i</mi>        </msub>        <mo>−<!-- − --></mo>        <msub>          <mrow class="MJX-TeXAtom-ORD">            <mi>θ<!-- θ --></mi>          </mrow>          <mrow class="MJX-TeXAtom-ORD">            <mi>i</mi>            <mo>,</mo>            <mrow class="MJX-TeXAtom-ORD">              <mi mathvariant="normal">e</mi>              <mi mathvariant="normal">q</mi>            </mrow>          </mrow>        </msub>        <mo>)</mo>      </mrow>    </mrow>    <mn>2</mn>  </msup>  <mo>+</mo>  <munder>    <mo movablelimits="false">∑<!-- ∑ --></mo>    <mrow class="MJX-TeXAtom-ORD">      <mi>i</mi>      <mo>∈<!-- ∈ --></mo>      <mrow class="MJX-TeXAtom-ORD">        <mi mathvariant="normal">t</mi>        <mi mathvariant="normal">o</mi>        <mi mathvariant="normal">r</mi>        <mi mathvariant="normal">s</mi>        <mi mathvariant="normal">i</mi>        <mi mathvariant="normal">o</mi>        <mi mathvariant="normal">n</mi>        <mi mathvariant="normal">s</mi>      </mrow>    </mrow>  </munder>  <mfrac>    <msub>      <mi>V</mi>      <mrow class="MJX-TeXAtom-ORD">        <mi>n</mi>        <mo>,</mo>        <mi>i</mi>      </mrow>    </msub>    <mn>2</mn>  </mfrac>  <mrow>    <mo>[</mo>    <mn>1</mn>    <mo>+</mo>    <mi>cos</mi>    <mo>⁡<!-- ⁡ --></mo>    <mrow>      <mo>(</mo>      <mi>n</mi>      <msub>        <mrow class="MJX-TeXAtom-ORD">          <mi>ω<!-- ω --></mi>        </mrow>        <mi>i</mi>      </msub>      <mo>−<!-- − --></mo>      <msub>        <mrow class="MJX-TeXAtom-ORD">          <mi>γ<!-- γ --></mi>        </mrow>        <mi>i</mi>      </msub>      <mo>)</mo>    </mrow>    <mo>]</mo>  </mrow>  <mo>+</mo>  <munder>    <mo movablelimits="false">∑<!-- ∑ --></mo>    <mrow class="MJX-TeXAtom-ORD">      <mtable rowspacing="4pt" columnspacing="1em">        <mtr>          <mtd>            <mi>i</mi>            <mo>,</mo>            <mi>j</mi>            <mo>∈<!-- ∈ --></mo>            <mrow class="MJX-TeXAtom-ORD">              <mi mathvariant="normal">a</mi>              <mi mathvariant="normal">t</mi>              <mi mathvariant="normal">o</mi>              <mi mathvariant="normal">m</mi>              <mi mathvariant="normal">s</mi>            </mrow>            <mo>,</mo>          </mtd>        </mtr>        <mtr>          <mtd>            <mrow class="MJX-TeXAtom-ORD">             </mrow>            <mtext> </mtext>            <mrow class="MJX-TeXAtom-ORD">              <mi mathvariant="normal">w</mi>              <mi mathvariant="normal">i</mi>              <mi mathvariant="normal">t</mi>              <mi mathvariant="normal">h</mi>            </mrow>            <mspace width="0.5em" />            <mi>i</mi>            <mo><</mo>            <mi>j</mi>          </mtd>        </mtr>      </mtable>    </mrow>  </munder>  <mrow>    <mo>{</mo>    <msub>      <mrow class="MJX-TeXAtom-ORD">        <mi>ϵ<!-- ϵ --></mi>      </mrow>      <mrow class="MJX-TeXAtom-ORD">        <mi>i</mi>        <mi>j</mi>      </mrow>    </msub>    <mrow>      <mo>[</mo>      <msup>        <mrow class="MJX-TeXAtom-ORD">          <mrow>            <mo>(</mo>            <mfrac>              <msub>                <mi>r</mi>                <mrow class="MJX-TeXAtom-ORD">                  <mi>m</mi>                  <mo>,</mo>                  <mi>i</mi>                  <mi>j</mi>                </mrow>              </msub>              <msub>                <mi>r</mi>                <mrow class="MJX-TeXAtom-ORD">                  <mi>i</mi>                  <mi>j</mi>                </mrow>              </msub>            </mfrac>            <mtext> </mtext>            <mo>)</mo>          </mrow>        </mrow>        <mrow class="MJX-TeXAtom-ORD">          <mn>12</mn>        </mrow>      </msup>      <mo>−<!-- − --></mo>      <mn>2</mn>      <msup>        <mrow class="MJX-TeXAtom-ORD">          <mrow>            <mo>(</mo>            <mfrac>              <msub>                <mi>r</mi>                <mrow class="MJX-TeXAtom-ORD">                  <mi>m</mi>                  <mo>,</mo>                  <mi>i</mi>                  <mi>j</mi>                </mrow>              </msub>              <msub>                <mi>r</mi>                <mrow class="MJX-TeXAtom-ORD">                  <mi>i</mi>                  <mi>j</mi>                </mrow>              </msub>            </mfrac>            <mo>)</mo>          </mrow>        </mrow>        <mn>6</mn>      </msup>      <mo>]</mo>    </mrow>    <mo>+</mo>    <mfrac>      <mrow>        <msub>          <mi>q</mi>          <mi>i</mi>        </msub>        <msub>          <mrow class="MJX-TeXAtom-ORD">            <mi>q</mi>          </mrow>          <mi>j</mi>        </msub>      </mrow>      <mrow>        <mn>4</mn>        <mi>π<!-- π --></mi>        <msub>          <mrow class="MJX-TeXAtom-ORD">            <mi>ϵ<!-- ϵ --></mi>          </mrow>          <mn>0</mn>        </msub>        <msub>          <mrow class="MJX-TeXAtom-ORD">            <mi>r</mi>          </mrow>          <mrow class="MJX-TeXAtom-ORD">            <mi>i</mi>            <mi>j</mi>          </mrow>        </msub>      </mrow>    </mfrac>    <mo>}</mo>  </mrow> </math>
```

while the first three terms represent the interactions between two (bonded), three (angular), and four (dihedral) atoms connected via covalent bonds. The parameters *k*<sub>*l*</sub>, *k*<sub>*θ*</sub>, and *V*<sub>*n*</sub> are force constants, *r*eqand *θ*~eq~ are equilibrium bond lengths and angles, respectively, and *n* and *γ* are the multiplicity and the phase factor for the dihedral angles. The last term in this FF equation contains a standard Lennard Jones (LJ) term for the van der Waals interactions (in which *r*<sub>*m*, *ij*</sub> and *ϵ* represent the minimum of the potential between two atoms *i* and *j* and the corresponding well depth, respectively), and a Coulombic energy term accounting for electrostatic interactions. In this term, *q*<sub>*i*</sub> and *q*<sub>*j*</sub> are the partial charges on the *i*th and *j*th atoms, and *ϵ*~0~ is the vacuum permittivity. The *r*<sub>*m*, *ij*</sub> and *ϵ*<sub>*ij*</sub> parameters for every couple of atoms in the system are computed from the self-interaction terms applying the Lorentz−Berthelot rules: *r*<sub>*m*, *ij*</sub> = (*r*<sub>*m*, *ii*</sub> + *r*<sub>*m*, *jj*</sub>)/2 and <math xmlns="http://www.w3.org/1998/Math/MathML">  <msub>    <mrow class="MJX-TeXAtom-ORD">      <mi>ϵ<!-- ϵ --></mi>    </mrow>    <mrow class="MJX-TeXAtom-ORD">      <mi>i</mi>      <mi>j</mi>    </mrow>  </msub>  <mo>=</mo>  <msqrt>    <msub>      <mi>ϵ<!-- ϵ --></mi>      <mrow class="MJX-TeXAtom-ORD">        <mi>i</mi>        <mi>i</mi>      </mrow>    </msub>    <msub>      <mrow class="MJX-TeXAtom-ORD">        <mi>ϵ<!-- ϵ --></mi>      </mrow>      <mrow class="MJX-TeXAtom-ORD">        <mi>j</mi>        <mi>j</mi>      </mrow>    </msub>  </msqrt> </math>.

<span style=color:blue>前三项代表通过共价键连接的两个原子（键长）、三个原子（角度）和四个原子（二面角）之间的相互作用。力常数 k<sub>l</sub>、k<sub>θ</sub> 和 V<sub>n</sub> 分别对应键长、角度和二面角的力常数，req 和 θeq 分别表示平衡键长和角度，n 和 γ 是二面角的倍数和相位因子。该力场方程的最后一项包括标准的伦敦－琼斯（LJ）项，描述范德华力的相互作用（其中 r<sub>m, ij</sub> 和 ϵ 分别表示两个原子 i 和 j 之间的势能最小值及其深度），以及库伦能量项，描述静电相互作用。在这一项中，q<sub>i</sub> 和 q<sub>j</sub> 分别是 i 和 j 原子的部分电荷，ϵ0 是真空介电常数。每对原子的 r<sub>m, ij</sub> 和 ϵ<sub>ij</sub> 参数通过应用洛伦茨－伯特洛特规则从自相互作用项计算得到：r<sub>m, ij</sub> = (r<sub>m, ii</sub> + r<sub>m, jj</sub>)/2 和 <math xmlns="http://www.w3.org/1998/Math/MathML">  <msub>    <mrow class="MJX-TeXAtom-ORD">      <mi>ϵ<!-- ϵ --></mi>    </mrow>    <mrow class="MJX-TeXAtom-ORD">      <mi>i</mi>      <mi>j</mi>    </mrow>  </msub>  <mo>=</mo>  <msqrt>    <msub>      <mi>ϵ<!-- ϵ --></mi>      <mrow class="MJX-TeXAtom-ORD">        <mi>i</mi>        <mi>i</mi>      </mrow>    </msub>    <msub>      <mrow class="MJX-TeXAtom-ORD">        <mi>ϵ<!-- ϵ --></mi>      </mrow>      <mrow class="MJX-TeXAtom-ORD">        <mi>j</mi>        <mi>j</mi>      </mrow>    </msub>  </msqrt> </math></span>

### 2.2 Radius of Gyration and Asphericity 回转半径和非球面度

The radius of gyration *R*<sub>*g*</sub> provides a quantitative characterization of the real size of a dendrimer molecule, and is defined as:

<span style=color:blue>回转半径 *R*<sub>*g*</sub> 是用于定量表征树枝分子实际大小的重要指标，其定义为：</span>

```html
<math xmlns="http://www.w3.org/1998/Math/MathML" display="block">  <mrow>    <mo>⟨</mo>    <msubsup>      <mrow class="MJX-TeXAtom-ORD">        <mi>R</mi>      </mrow>      <mi>g</mi>      <mn>2</mn>    </msubsup>    <mo>⟩</mo>  </mrow>  <mo>=</mo>  <mfrac>    <mn>1</mn>    <mi>M</mi>  </mfrac>  <mrow>    <mo>⟨</mo>    <mtext> </mtext>    <msubsup>      <mrow class="MJX-TeXAtom-ORD">        <mo>∑<!-- ∑ --></mo>      </mrow>      <mrow class="MJX-TeXAtom-ORD">        <mi>i</mi>        <mo>=</mo>        <mn>1</mn>      </mrow>      <mi>n</mi>    </msubsup>    <msub>      <mrow class="MJX-TeXAtom-ORD">        <mi>m</mi>      </mrow>      <mi>i</mi>    </msub>    <msup>      <mrow class="MJX-TeXAtom-ORD">        <mrow>          <mo>(</mo>          <msub>            <mrow class="MJX-TeXAtom-ORD">              <mi>c</mi>            </mrow>            <mi>i</mi>          </msub>          <mo>−<!-- − --></mo>          <mi>C</mi>          <mo>)</mo>        </mrow>      </mrow>      <mn>2</mn>    </msup>    <mtext> </mtext>    <mo>⟩</mo>  </mrow> </math>
```

where *M* and *n* are the total mass and number of atoms of the dendrimer, *c*<sub>*i*</sub> and *m*<sub>*i*</sub> are the position and mass of the *i*th atom, *C* is the center of mass of the dendrimer, and the angular brackets denote an ensemble average over the sampled configurations. The radius of gyration is strictly related to the spatial distribution of the dendrimer atoms, and ultimately to its size in solution. As such, *R*<sub>*g*</sub> can be very useful to characterize the effect of some modification in the terminal units of a family of dendrimers of the same generation, or to study the effect of the protonation state on the structural configuration of a dendrimer. When computing *R*<sub>*g*</sub>, it is also possible to estimate the relevant radius of gyration tensor ***R***<sub>***g***</sub>. The eigenvalues of ***R***<sub>***g***</sub> are its principal moments *l*<sub>*x*</sub>, *l*<sub>*y*</sub>, and *l*<sub>*z*</sub> (with *l*<sub>*x*</sub> ≤ *l*<sub>*y*</sub> ≤ *l*<sub>*z*</sub>), from the knowledge of which the dendrimer asphericity *b* can also be calculated as:

<span style=color:blue>其中，M 是树枝分子的总质量，n 是原子数，c<sub>i</sub> 和 m<sub>i</sub> 分别是第 i 个原子的位置和质量，C 是树枝分子的质心。尖括号表示对采样配置进行的平均值计算。回转半径与树枝分子中原子的空间分布密切相关，因此可以反映其在溶液中的实际尺寸。因此，R<sub>g</sub> 是评估树枝分子末端单元修饰效果或质子化状态对树枝分子结构影响的重要工具。除了计算 R<sub>g</sub> 外，还可以进一步分析回转半径张量 R<sub>g</sub>，并从中得出其特征值 l<sub>x</sub>、l<sub>y</sub> 和 l<sub>z</sub>（其中 l<sub>x</sub> ≤ l<sub>y</sub> ≤ l<sub>z</sub>）。基于这些特征值，可以计算出树枝分子的非球度 b，其计算公式为：</span>

```html
<math xmlns="http://www.w3.org/1998/Math/MathML" display="block">  <mi>b</mi>  <mo>=</mo>  <msub>    <mrow class="MJX-TeXAtom-ORD">      <mi>l</mi>    </mrow>    <mi>z</mi>  </msub>  <mo>−<!-- − --></mo>  <mfrac>    <mn>1</mn>    <mn>2</mn>  </mfrac>  <mrow>    <mo>(</mo>    <msub>      <mrow class="MJX-TeXAtom-ORD">        <mi>l</mi>      </mrow>      <mi>x</mi>    </msub>    <mo>+</mo>    <msub>      <mrow class="MJX-TeXAtom-ORD">        <mi>l</mi>      </mrow>      <mi>y</mi>    </msub>    <mo>)</mo>  </mrow> </math>
```

As a useful descriptor of anisometry, *b* measures the deviation of a molecular geometry from a spherical form, in that for a perfectly spherical distribution of atoms *b* = 0, for prolate molecules *b* values are close to 0.25, whereas oblate molecules are characterized by values of *b* ≈ 1. As such, the evaluation of *b* can yield very insightful information about a dendrimer’s shape modification when, e.g., it forms a complex with siRNA.

<span style=color:blue>非球度 *b* 是分子几何形状偏离球形的度量。在球形分子中，*b* 的值为 0；对于棒状分子，*b* 接近 0.25，而扁平分子则具有接近 1 的 *b* 值。因此，*b* 的计算为研究树枝分子与 siRNA 形成复合物时形状变化提供了有价值的见解。</span>

### 2.3 Radial Monomer Density

While *b* and ***R***<sub>***g***</sub> are overall descriptors of a dendrimer shape , the radial monomer density *ρ*(*r*) is a tool to study the distributions of monomers and/or other different molecular elements within a dendrimeric structure. *ρ*(*r*) is defined as the number of atoms that are located within a spherical shell of radius *r* and thickness *Δr* from a reference center, usually taken as the dendrimer’s center of mass. This analysis tool can convey many fine details information about the structure of the dendrimer under investigation including, by way of example, the extent of compactness of the dendrimer interior, the relative spatial distribution of the different dendrimer sub-generations within the entire dendrimer shell, and, last but not least, the distributions of the dendrimer terminal units with respect to the dendrimer core, i.e., the degree of dendrimer back-folding. Importantly, the distribution of other molecules like water, ions, counterions, and siRNA fragments with respect to dendrimer core can also be described by behavior of the corresponding *ρ*(*r*).

<span style=color:blue>虽然 *b* 和 ***R***<sub>***g***</sub> 可以用来描述树枝分子的总体形状，但径向单体密度 *ρ*(*r*) 是用来研究树枝分子结构中不同单体或分子元素分布的工具。*ρ*(*r*) 定义为位于距参考中心半径 *r*、厚度为 *Δr* 的球壳内的原子数，通常参考中心为树枝分子的质心。这个分析方法可以提供关于树枝分子结构的丰富信息，例如树枝分子内部的紧密性、不同树枝分子亚代在分子壳中的空间分布，以及树枝分子末端单元与核心之间的分布（即树枝分子是否存在回折）。此外，水分子、离子、反离子以及 siRNA 片段等其他分子相对于树枝分子核心的分布，也可以通过 *ρ*(*r*) 的变化来进行描述。</span>

### 2.4 Solvent Accessible Surface Area and Interior Cavities 溶剂可接触的表面积和内部空腔

Water can play a key role both in the stabilization of the dendrimer structure and in its interactions with siRNA, mainly via the formation of an extensive network of hydrogen bonds. A measure of a dendrimer’s surface exposed to the solvent is given by its accessible surface area (*ASA*) . For any given molecule, *ASA* is typically calculated using the so-called *rolling ball* algorithm, which employs a sphere of a particular radius *r*<sub>*p*</sub> (e.g., a typical *r*<sub>*p*</sub> value is 1.4 Å, which approximates the radius of a water molecule) to “probe” the surface of the molecule. It is interesting to observe that, for a hypothetical spherical dendrimer without internal voids, the value of its *ASA* should increase with the square of the probe size *r*<sub>*p*</sub>

<span style=color:blue>水分子在树枝分子结构的稳定性及其与 siRNA 相互作用中的作用至关重要，主要是通过形成一个广泛的氢键网络来实现的。树枝分子暴露在溶剂中的表面积可以通过其可接触表面积 (*ASA*) 来衡量。对于任何给定的分子，*ASA* 通常是通过所谓的 *滚动球* 算法计算的，该算法使用一个特定半径 *r*<sub>*p*</sub> 的球体（通常 *r*<sub>*p*</sub> 为 1.4 Å，接近水分子的半径）来“探测”分子的表面。有趣的是，对于一个假设的没有内部空隙的球形树枝分子，其 *ASA* 值应随着探针半径 *r*<sub>*p*</sub> 的平方而增加：</span>

```html
<math xmlns="http://www.w3.org/1998/Math/MathML" display="block">  <mi>A</mi>  <mi>S</mi>  <msub>    <mrow class="MJX-TeXAtom-ORD">      <mi>A</mi>    </mrow>    <mrow class="MJX-TeXAtom-ORD">      <mrow class="MJX-TeXAtom-ORD">        <mi mathvariant="normal">s</mi>        <mi mathvariant="normal">p</mi>        <mi mathvariant="normal">h</mi>        <mi mathvariant="normal">e</mi>        <mi mathvariant="normal">r</mi>        <mi mathvariant="normal">e</mi>      </mrow>    </mrow>  </msub>  <mo>=</mo>  <mn>4</mn>  <mi>π<!-- π --></mi>  <msup>    <mrow class="MJX-TeXAtom-ORD">      <mrow>        <mo>(</mo>        <msub>          <mrow class="MJX-TeXAtom-ORD">            <mi>r</mi>          </mrow>          <mi>d</mi>        </msub>        <mo>+</mo>        <msub>          <mrow class="MJX-TeXAtom-ORD">            <mi>r</mi>          </mrow>          <mi>p</mi>        </msub>        <mo>)</mo>      </mrow>    </mrow>    <mn>2</mn>  </msup> </math>
```

in which *r*<sub>*d*</sub> is the radius of the dendrimer. Accordingly, any deviation from linearity observed in a plot showing the square root of the calculated *ASA* as a function of *r*<sub>*p*</sub> is suggestive of the presence of internal voids in the corresponding dendrimer structure.

<span style=color:blue>其中 *r*<sub>*d*</sub> 为树枝分子的半径。因此，在绘制计算出的 *ASA* 平方根与 *r*<sub>*p*</sub> 的关系图时，若出现偏离线性的现象，则可能暗示该树枝分子结构中存在内部空隙。</span>

### 2.5 MM/PBSA

A relatively quick and not particularly computationally intensive procedure to estimate the free energy of binding (*ΔG*<sub>bind</sub>) between a dendrimer and its cargo is the Molecular Mechanics—Poisson-Boltzmann (Generalized Born) Surface Area (MM-PB(GB)SA) methodology. The framework of this theory is summarized by the following equations:

<span style=color:blue>一种相对快速且计算量不大的方法来估算树枝分子与其载体之间的结合自由能（*ΔG*<sub>bind</sub>）是分子力学—泊松-玻尔兹曼（广义本）表面积（MM-PB(GB)SA）方法。该方法的理论框架通过以下方程式总结：</span>

```html
<math xmlns="http://www.w3.org/1998/Math/MathML" display="block">  <mrow class="MJX-TeXAtom-ORD">    <mtext>Δ<!-- Δ --></mtext>  </mrow>  <msub>    <mrow class="MJX-TeXAtom-ORD">      <mi>E</mi>    </mrow>    <mrow class="MJX-TeXAtom-ORD">      <mrow class="MJX-TeXAtom-ORD">        <mi mathvariant="normal">M</mi>        <mi mathvariant="normal">M</mi>      </mrow>    </mrow>  </msub>  <mo>=</mo>  <mrow class="MJX-TeXAtom-ORD">    <mtext>Δ<!-- Δ --></mtext>  </mrow>  <msub>    <mrow class="MJX-TeXAtom-ORD">      <mi>E</mi>    </mrow>    <mrow class="MJX-TeXAtom-ORD">      <mrow class="MJX-TeXAtom-ORD">        <mi mathvariant="normal">c</mi>        <mi mathvariant="normal">o</mi>        <mi mathvariant="normal">v</mi>        <mi mathvariant="normal">a</mi>        <mi mathvariant="normal">l</mi>        <mi mathvariant="normal">e</mi>        <mi mathvariant="normal">n</mi>        <mi mathvariant="normal">t</mi>      </mrow>    </mrow>  </msub>  <mo>+</mo>  <mrow class="MJX-TeXAtom-ORD">    <mtext>Δ<!-- Δ --></mtext>  </mrow>  <msub>    <mrow class="MJX-TeXAtom-ORD">      <mi>E</mi>    </mrow>    <mrow class="MJX-TeXAtom-ORD">      <mrow class="MJX-TeXAtom-ORD">        <mi mathvariant="normal">v</mi>        <mi mathvariant="normal">d</mi>        <mi mathvariant="normal">W</mi>      </mrow>    </mrow>  </msub>  <mo>+</mo>  <mrow class="MJX-TeXAtom-ORD">    <mtext>Δ<!-- Δ --></mtext>  </mrow>  <msub>    <mrow class="MJX-TeXAtom-ORD">      <mi>E</mi>    </mrow>    <mrow class="MJX-TeXAtom-ORD">      <mrow class="MJX-TeXAtom-ORD">        <mi mathvariant="normal">e</mi>        <mi mathvariant="normal">l</mi>        <mi mathvariant="normal">e</mi>      </mrow>    </mrow>  </msub> </math>
```

```html
<math xmlns="http://www.w3.org/1998/Math/MathML" display="block">  <mrow class="MJX-TeXAtom-ORD">    <mtext>Δ<!-- Δ --></mtext>  </mrow>  <msub>    <mrow class="MJX-TeXAtom-ORD">      <mi>G</mi>    </mrow>    <mrow class="MJX-TeXAtom-ORD">      <mrow class="MJX-TeXAtom-ORD">        <mi mathvariant="normal">s</mi>        <mi mathvariant="normal">o</mi>        <mi mathvariant="normal">l</mi>        <mi mathvariant="normal">v</mi>      </mrow>    </mrow>  </msub>  <mo>=</mo>  <mrow class="MJX-TeXAtom-ORD">    <mtext>Δ<!-- Δ --></mtext>  </mrow>  <msub>    <mrow class="MJX-TeXAtom-ORD">      <mi>G</mi>    </mrow>    <mrow class="MJX-TeXAtom-ORD">      <mrow class="MJX-TeXAtom-ORD">        <mi mathvariant="normal">p</mi>        <mi mathvariant="normal">o</mi>        <mi mathvariant="normal">l</mi>        <mi mathvariant="normal">a</mi>        <mi mathvariant="normal">r</mi>      </mrow>    </mrow>  </msub>  <mo>+</mo>  <mrow class="MJX-TeXAtom-ORD">    <mtext>Δ<!-- Δ --></mtext>  </mrow>  <msub>    <mrow class="MJX-TeXAtom-ORD">      <mi>G</mi>    </mrow>    <mrow class="MJX-TeXAtom-ORD">      <mrow class="MJX-TeXAtom-ORD">        <mi mathvariant="normal">n</mi>        <mi mathvariant="normal">o</mi>        <mi mathvariant="normal">n</mi>        <mi mathvariant="normal">p</mi>        <mi mathvariant="normal">o</mi>        <mi mathvariant="normal">l</mi>        <mi mathvariant="normal">a</mi>        <mi mathvariant="normal">r</mi>      </mrow>    </mrow>  </msub> </math>
```

```html
<math xmlns="http://www.w3.org/1998/Math/MathML" display="block">  <mrow class="MJX-TeXAtom-ORD">    <mtext>Δ<!-- Δ --></mtext>  </mrow>  <msub>    <mrow class="MJX-TeXAtom-ORD">      <mi>H</mi>    </mrow>    <mrow class="MJX-TeXAtom-ORD">      <mrow class="MJX-TeXAtom-ORD">        <mi mathvariant="normal">b</mi>        <mi mathvariant="normal">i</mi>        <mi mathvariant="normal">n</mi>        <mi mathvariant="normal">d</mi>      </mrow>    </mrow>  </msub>  <mo>=</mo>  <mrow class="MJX-TeXAtom-ORD">    <mtext>Δ<!-- Δ --></mtext>  </mrow>  <msub>    <mrow class="MJX-TeXAtom-ORD">      <mi>E</mi>    </mrow>    <mrow class="MJX-TeXAtom-ORD">      <mi>M</mi>      <mi>M</mi>    </mrow>  </msub>  <mo>+</mo>  <mrow class="MJX-TeXAtom-ORD">    <mtext>Δ<!-- Δ --></mtext>  </mrow>  <msub>    <mrow class="MJX-TeXAtom-ORD">      <mi>G</mi>    </mrow>    <mrow class="MJX-TeXAtom-ORD">      <mrow class="MJX-TeXAtom-ORD">        <mi mathvariant="normal">s</mi>        <mi mathvariant="normal">o</mi>        <mi mathvariant="normal">l</mi>        <mi mathvariant="normal">v</mi>      </mrow>    </mrow>  </msub> </math>
```

```html
<math xmlns="http://www.w3.org/1998/Math/MathML" display="block">  <mrow class="MJX-TeXAtom-ORD">    <mtext>Δ<!-- Δ --></mtext>  </mrow>  <msub>    <mrow class="MJX-TeXAtom-ORD">      <mi>G</mi>    </mrow>    <mrow class="MJX-TeXAtom-ORD">      <mrow class="MJX-TeXAtom-ORD">        <mi mathvariant="normal">b</mi>        <mi mathvariant="normal">i</mi>        <mi mathvariant="normal">n</mi>        <mi mathvariant="normal">d</mi>      </mrow>    </mrow>  </msub>  <mo>=</mo>  <mrow class="MJX-TeXAtom-ORD">    <mtext>Δ<!-- Δ --></mtext>  </mrow>  <msub>    <mrow class="MJX-TeXAtom-ORD">      <mi>H</mi>    </mrow>    <mrow class="MJX-TeXAtom-ORD">      <mrow class="MJX-TeXAtom-ORD">        <mi mathvariant="normal">b</mi>        <mi mathvariant="normal">i</mi>        <mi mathvariant="normal">n</mi>        <mi mathvariant="normal">d</mi>      </mrow>    </mrow>  </msub>  <mo>−<!-- − --></mo>  <mi>T</mi>  <mrow class="MJX-TeXAtom-ORD">    <mtext>Δ<!-- Δ --></mtext>  </mrow>  <msub>    <mrow class="MJX-TeXAtom-ORD">      <mi>S</mi>    </mrow>    <mrow class="MJX-TeXAtom-ORD">      <mrow class="MJX-TeXAtom-ORD">        <mi mathvariant="normal">b</mi>        <mi mathvariant="normal">i</mi>        <mi mathvariant="normal">n</mi>        <mi mathvariant="normal">d</mi>      </mrow>    </mrow>  </msub> </math>
```

where *ΔE*<sub>MM</sub> represent the gas-phase molecular mechanical energy change, composed by *ΔE*<sub>covalent</sub> (the contribution of the covalent interactions energies: bonded, angles, torsions), *ΔE*<sub>vdW</sub> (the variation of the nonbonded van der Waals energy), and *ΔE*<sub>ele</sub> (the change in the electrostatic calculated from the Coulomb potential). *ΔG*<sub>solv</sub> represents the solvation free energy change, composed by its polar *ΔG*<sub>polar</sub> and nonpolar *ΔG*<sub>nonpolar</sub> contributions. The sum of *ΔE*<sub>MM</sub> and *ΔG*<sub>solv</sub> give the enthalpic contribution to the free energy (*ΔG*<sub>bind</sub>), while *TΔS*<sub>bind</sub> is the corresponding variation in conformational entropy upon binding (where *T* is the system temperature in Kelvin). The polar term  *ΔG*<sub>polar</sub>  is computed by replacing the solvent with a continuum medium with comparable dielectric constant (e.g., 78 for water) either using a Generalized Born (MM-**GB**SA)  pairwise approximation or by directly solving the Poisson-Boltzmann eq. (MM-**PB**SA). The nonpolar contribution to solvation *ΔG*<sub>nonpolar</sub>, arising both from van der Waals interactions between the dendrimer/siRNA complex and the solvent and from the formation of a cavity in the solvent due to the presence of the solute itself, is usually calculated according to the following empirical expression for non-small molecules like dendrimers:

<span style=color:blue>其中 ΔE<sub>MM</sub> 代表气相中的分子力学能量变化，由 ΔE<sub>covalent</sub>（共价键、角度、扭转等相互作用的贡献）、ΔE<sub>vdW</sub>（范德华力的能量变化）和 ΔE<sub>ele</sub>（由库仑势计算得到的静电能变化）组成。ΔG<sub>solv</sub> 代表溶剂化自由能的变化，包含了极性部分 ΔG<sub>polar</sub> 和非极性部分 ΔG<sub>nonpolar</sub> 的贡献。ΔE<sub>MM</sub> 和 ΔG<sub>solv</sub> 的总和给出了结合焓（ΔH<sub>bind</sub>），而 TΔS<sub>bind</sub> 是结合过程中构象熵的变化（其中 T 为系统温度，单位为开尔文）。极性项 ΔG<sub>polar</sub> 通过用具有相似介电常数的连续介质（如水的介电常数为78）替代溶剂来计算，通常使用广义本（MM-GBSA）对的近似方法，或通过直接求解泊松-玻尔兹曼方程（MM-PBSA）。溶剂化的非极性贡献 ΔG<sub>nonpolar</sub>，源自树枝分子/siRNA 复合物与溶剂的范德华相互作用及溶质引起的溶剂空腔的形成，通常通过以下经验公式计算，适用于较大分子如树枝分子：</span>

```html
<math xmlns="http://www.w3.org/1998/Math/MathML" display="block">  <mrow class="MJX-TeXAtom-ORD">    <mtext>Δ<!-- Δ --></mtext>  </mrow>  <msub>    <mrow class="MJX-TeXAtom-ORD">      <mi>G</mi>    </mrow>    <mrow class="MJX-TeXAtom-ORD">      <mrow class="MJX-TeXAtom-ORD">        <mi mathvariant="normal">n</mi>        <mi mathvariant="normal">o</mi>        <mi mathvariant="normal">n</mi>        <mi mathvariant="normal">p</mi>        <mi mathvariant="normal">o</mi>        <mi mathvariant="normal">l</mi>        <mi mathvariant="normal">a</mi>        <mi mathvariant="normal">r</mi>      </mrow>    </mrow>  </msub>  <mo>=</mo>  <mrow class="MJX-TeXAtom-ORD">    <mtext>Δ<!-- Δ --></mtext>  </mrow>  <msub>    <mrow class="MJX-TeXAtom-ORD">      <mi>G</mi>    </mrow>    <mrow class="MJX-TeXAtom-ORD">      <mrow class="MJX-TeXAtom-ORD">        <mi mathvariant="normal">d</mi>        <mi mathvariant="normal">i</mi>        <mi mathvariant="normal">s</mi>        <mi mathvariant="normal">p</mi>      </mrow>    </mrow>  </msub>  <mo>+</mo>  <mi>γ<!-- γ --></mi>  <mi>S</mi>  <mi>A</mi>  <mi>V</mi>  <mo>+</mo>  <mi>β<!-- β --></mi> </math>
```

where *ΔG*<sub>disp</sub> is the dispersion term due to the van der Waals interactions of the dendrimer/siRNA supramolecular assembly with the solvent, and can be computed via a solvent accessible surface integration. The rest of the equation accounts for the cavity formation via a combination of two empirical constants (*γ* and *β*) and a solvent accessible volume (*SAV*), i.e., the volume enclosed by the surface area of the solute. Finally, the entropic contribution to dendrimer/siRNA binding *ΔS*<sub>bind</sub> is usually estimated resorting to two most popular approaches: the normal mode analysis or the quasi harmonic approximation. As dendrimers are generally quite flexible molecules, a correct estimation of this last thermodynamic quantity may play a decisive role in the estimation of an ultimately realistic in silico *ΔG*<sub>bind</sub> value.

<span style=color:blue>其中 *ΔG*<sub>disp</sub> 是色散项，由树枝分子/siRNA 复合物与溶剂之间的范德华相互作用引起，通常通过溶剂可接触表面积积分计算得出。方程的其他部分则考虑了通过两个经验常数（*γ* 和 *β*）以及溶剂可接触体积（*SAV*）来描述溶剂中的空腔形成。最后，树枝分子/siRNA 结合的熵贡献 *ΔS*<sub>bind</sub> 通常通过两种常用方法估算：正常模式分析或准谐近似。由于树枝分子通常是高度柔性的分子，正确估算这一热力学量可能在获得一个更准确的计算自由能（*ΔG*<sub>bind</sub>）时起到关键作用。</span>

## 3 Methods 方法

### 3.1 Box and Simulation Input Parameters Creation 盒子与模拟输入参数创建

This procedure is used to create a solvated box and the corresponding input files (a topology PRMTOP and an initial coordinates INPCRD files) for the simulation with AMBER. The procedure is valid for creating the input parameter for the single dendrimer or siRNA alone, or the dendrimer-siRNA complex (from now on the name *solute* is used to indicate any of them in this section) starting from a coordinates PDB file (*see* Subheadings 3.3-3.5 for the creation of the file for the dendrimer, siRNA and complex, respectively). Open a *tleap* session with the following command:

<span style=color:blue>本过程用于创建溶剂化的盒子及相应的输入文件（拓扑文件 PRMTOP 和初始坐标文件 INPCRD），以便使用 AMBER 进行模拟。该方法适用于为单一树枝分子或 siRNA，或树枝分子-siRNA 复合物（以下称为*溶质*，本节中的任何一个）创建输入参数，起始于坐标 PDB 文件（*详见* 小节 3.3-3.5，对于树枝分子、siRNA 和复合物的文件创建）。打开 *tleap* 会话，输入以下命令：</span>

```shell
tleap -s
```
1. Load the required forcefield library files into AMBER’s tleap software. For parametrizing the dendrimer and the complex load the library and parameters created in Subheading 3.1 together with the general *leaprc.gaff* library file, while for the siRNA parameterization load the *leaprc.RNA.OL3* library file. The last command will load the recommended Amber FF for RNA simulations: the *f99* AMBER forcefield with its *bsc0* and *χOL3* updates . Load also the *leaprc.water.tip3p* library needed to solvate and add the Na+ and Cl− ions. Finally, load the 3D coordinates files of the solute and save the topology and initial coordinates files for further analysis. All of the above can be obtained by entering the following commands:

   <span style=color:blue>加载 AMBER 的 *tleap* 软件所需的力场库文件。对于树枝分子和复合物的参数化，加载小节 3.1 中创建的库和参数，并加载通用的 *leaprc.gaff* 库文件；对于 siRNA 的参数化，加载 *leaprc.RNA.OL3* 库文件。最后一条命令将加载适用于 RNA 模拟的 AMBER 力场：*f99* AMBER 力场及其 *bsc0* 和 *χOL3* 更新。还需要加载 *leaprc.water.tip3p* 库文件，用于溶剂化并添加 Na<sup>+ </sup>和 Cl<sup>− </sup>离子。接着，加载溶质的 3D 坐标文件，并保存拓扑和初始坐标文件以便后续分析。所有操作通过以下命令完成：</span>

   ```shell
   source leaprc.gaff
   source leaprc.RNA.OL3
   source leaprc.water.tip3p
   loadamberparams dendrimer.frcmod
   loadamberprep dendrimer.prepi
   a=loadpdb SOLUTE.pdb
   saveamberparm a SOLUTE.prmtop SOLUTE.inpcrd
   ```

2. Now solvate the solute with TIP3P  water molecules (a simple planar three point model for water, commonly used for biological simulations) by creating a cubic solvent box with dimensions ranging at least 1.5 nm from the edges of each solute molecule. In MD simulations is important that the solute does not interact with its images belonging to the adjacent periodic boxes; thus, it is imperative to create a shell of solvent greater than the nonbonded cutoff used during the subsequent MD simulations (0.9 nm, as reported in the parameter *cut* in Table 1). Accordingly, type the following command:

   <span style=color:blue>接着，用 TIP3P 水分子（常用于生物学模拟的简单三点水模型）对溶质进行溶剂化，创建一个立方体溶剂盒，且盒子的尺寸需确保与溶质分子之间至少有 1.5 nm 的距离。为了避免在分子动力学模拟中溶质与其相邻周期盒子的镜像分子相互作用，必须确保溶剂壳的厚度超过模拟中非键合截断距离（如表 1 中 *cut* 参数报告的 0.9 nm）。输入以下命令：</span>

   ```shell
   solvatebox a TIP3PBOX 15.0
   ```


3. Now add the Na<sup>+ </sup>and  Cl<sup>− counterions needed to neutralize the solute and to reach a concentration 0.15 M of NaCl, representative of a physiological environment. Two *addions* commands needed to automatically neutralize the system with the required number of sodium or chlorine ions, as follows:

   <span style=color:blue>添加Na<sup>+ </sup>和 Cl<sup>− 反离子以中和溶质，并使 NaCl 的浓度达到 0.15 M，这一浓度常见于生理环境。输入两个 *addions* 命令，自动添加所需的钠离子和氯离子：</span>

   ```shell
   addions a Na+ 0
   addions a Cl- 0
   ```

4. While executing the *solvatebox* command, tleap will print the total volume (Vol) of the created simulation box, and this information can be used to compute the number of NaCl molecules needed to attain the physiological ionic strength (150 mM) using the following equation

   <span style=color:blue>执行 *solvatebox* 命令时，tleap 会输出创建的模拟盒的总体积（Vol）。这个信息可用于通过以下公式计算所需的 NaCl 分子数量，以达到生理离子强度（150 mM）：</span>

   ```html
   <math xmlns="http://www.w3.org/1998/Math/MathML" display="block">  <mrow class="MJX-TeXAtom-ORD">    <mi mathvariant="normal">N</mi>    <mi mathvariant="normal">u</mi>    <mi mathvariant="normal">m</mi>    <mi mathvariant="normal">F</mi>    <mi mathvariant="normal">o</mi>    <mi mathvariant="normal">r</mi>    <mi mathvariant="normal">P</mi>    <mi mathvariant="normal">h</mi>    <mi mathvariant="normal">y</mi>    <mi mathvariant="normal">s</mi>    <mi mathvariant="normal">C</mi>    <mi mathvariant="normal">o</mi>    <mi mathvariant="normal">n</mi>    <mi mathvariant="normal">c</mi>  </mrow>  <mo>=</mo>  <mrow class="MJX-TeXAtom-ORD">    <mi mathvariant="normal">V</mi>    <mi mathvariant="normal">o</mi>    <mi mathvariant="normal">l</mi>  </mrow>  <mo>×<!-- × --></mo>  <mn>0.15</mn>  <mo>×<!-- × --></mo>  <mn>6.022</mn>  <mo>×<!-- × --></mo>  <msup>    <mrow class="MJX-TeXAtom-ORD">      <mn>10</mn>    </mrow>    <mrow class="MJX-TeXAtom-ORD">      <mo>−<!-- − --></mo>      <mn>4</mn>    </mrow>  </msup> </math>
   ```

5. With a third *addions* command this computed number of sodium and chlorine ions is added to the simulation box. Thus, type:

   <span style=color:blue>使用第三个 *addions* 命令，将计算得出的钠离子和氯离子的数量添加到模拟盒中。输入：</span>

   ```shell
   addions a Na+ NumForPhysConc Cl- NumForPhysConc
   ```

6. Finally, save both a topology and an initial coordinates file of the solvated system (required to carry on the subsequent simulations and analysis steps) by typing:

   <span style=color:blue>最后，保存溶剂化系统的拓扑文件和初始坐标文件（以便后续的模拟和分析步骤）：</span>

   ```shell
   saveamberparm a SOLUTE.solvated.prmtop SOLUTE.solvated.inpcrd
   savepdb a SOLUTE.solvated.pdb

With the last command, a reference PDB file containing the model of the solvated simulation box is created.

<span style=color:blue>此命令将生成一个包含溶剂化模拟盒的参考 PDB 文件。</span>

**Table 1** List of input files for pmemd. A detailed description of the input parameters can be found in a recent AMBER manual available on line at https://ambermd.org/Manuals.php. The exclamation mark is used to indicate a comment block, as per FORTRAN 90 standard

![485053_1_En_16_Tab1a_HTML](https://raw.githubusercontent.com/zcgkiller/Pictures/main/Wechat/485053_1_En_16_Tab1a_HTML.png)

![485053_1_En_16_Tab1b_HTML](https://raw.githubusercontent.com/zcgkiller/Pictures/main/Wechat/485053_1_En_16_Tab1b_HTML.png)

![485053_1_En_16_Tab1c_HTML](https://raw.githubusercontent.com/zcgkiller/Pictures/main/Wechat/485053_1_En_16_Tab1c_HTML.png)


### 3.2 Simulation Protocol 模拟方案

This simulation protocol is valid for simulating either the dendrimer or the siRNA molecule alone, or the dendrimer-siRNA complex (i.e., any *solute*). Throughout all the following MD steps, electrostatic interactions are computed by means of the particle mesh Ewald (PME) algorithm.

<span style=color:blue>此模拟方案适用于模拟单独的树枝分子或 siRNA 分子，或者树枝分子-siRNA 复合物（即任意*溶质*）。在所有后续的分子动力学（MD）步骤中，静电相互作用采用粒子网格 Ewald（PME）算法进行计算。</span>

1. Before starting any MD simulation, it is fundamental to perform an energy minimization process in order to fix steric clashes and optimize the initial model geometries according to the potential energy function. Also, the solvent box generated according to the protocol reported above needs to be optimized at the desired temperature and pressure conditions. Accordingly, first the solvation box has to be gradually heated to 300 K by performing MD simulations in the NVT ensemble (i.e., under constant number of atoms, volume and temperature conditions) to avoid the creation of air bubbles within the solvent, with positional restraint applied to the solute atoms. Then, while still applying positional restraint to the solute atoms, the system density must be equilibrated at 300 K and 1 atm by means of MD simulations in the NPT ensemble (i.e.*,* under constant number of atoms, pressure and temperature). The solute positional restraints have to be gradually removed in 10 runs of subsequent energy minimizations each performed reducing the force of the positional restraints . Finally, another run of heating in the NVT ensemble followed by density equilibration in the NPT ensemble with the solute free of positional restraint is run (*see* Table [1](clbr://internal.invalid/OEBPS/html/485053_1_En_16_Chapter.xhtml#Tab1) for examples of input files). The following pseudo-code can be used to carry on all of these steps:
   
   <span style=color:blue>在开始任何 MD 模拟之前，进行能量最小化是至关重要的，这可以修正立体冲突并根据势能函数优化初始模型的几何结构。同时，按照前述协议生成的溶剂盒，也需要在期望的温度和压力条件下进行优化。因此，首先需要通过在 NVT 集合中（即在恒定原子数、体积和温度的条件下）进行 MD 模拟，将溶剂盒逐步加热至 300 K，以避免溶剂中形成气泡，并对溶质的原子施加位置约束。随后，继续对溶质原子施加位置约束，通过在 NPT 集合中（即在恒定原子数、压力和温度的条件下）进行 MD 模拟，使系统在 300 K 和 1 atm 的条件下达到密度平衡。在此过程中，溶质的位置约束需要逐步去除，方法是进行 10 次能量最小化，每次减少位置约束的强度。最后，再次进行 NVT 集合的加热，并在 NPT 集合中进行密度平衡，这时溶质不再受到位置约束（*参见* 表 [1]() 中的输入文件示例）。以下伪代码可以用来执行这些步骤：</span>
   
   
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

In each pmemd command (*see* **Note** **1**) the option *-i* and *-o* specify the input and output (log of some energy and physico-chemical parameters of the simulation) files, option *-r* specifies the name of the restart file, option *-x* selects the output coordinates file, option *-p* selects the solvated complex topology file created by tleap, and options *-c* and *-ref* specify the files with the starting and reference coordinates of the system, respectively. 

<span style= color:blue>在每个 *pmemd* 命令中（*参见* **注释** **1**），选项 *-i* 和 *-o* 用于指定输入文件和输出文件（包含能量及物理化学参数的日志），选项 *-r* 用于指定重启文件的名称，选项 *-x* 用于选择输出的坐标文件，选项 *-p* 用于选择由 *tleap* 生成的溶剂化复合物拓扑文件，选项 *-c* 和 *-ref* 分别指定系统的起始和参考坐标文件。</span>

2. Although a successful energy minimization should get rid of any steric clashes, there are some cases in which the resulting structure is still not perfect (one common example is the presence of intersecting aromatic rings). At least a visual inspection of the final produced configuration is recommended, which can be easily performed loading the produced NPT_all.rst file along with its complex.solvated.prmtop file into a molecular visualization program such as Chimera (https://www.cgl.ucsf.edu/chimera/)  or VMD (https://www.ks.uiuc.edu/Research/vmd/) .

   <span style=color:blue>尽管能量最小化应能去除大部分立体冲突，但在某些情况下，最终结构可能仍存在缺陷（例如，芳香环之间可能存在交叉）。建议至少进行目视检查，检查方法是将生成的 *NPT_all.rst* 文件及其 *complex.solvated.prmtop* 文件加载到分子可视化程序中（如 Chimera（https://www.cgl.ucsf.edu/chimera/）或 VMD（https://www.ks.uiuc.edu/Research/vmd/））进行查看。</span>

3. Once optimization of each system is achieved, productive MD simulations can be performed. The required input file is the md.in file reported in Table 1, and 15 subsequent simulations can be carried out with the following pseudo-code command:

   <span style=color:blue>一旦系统优化完成，就可以进行正式的 MD 模拟。所需的输入文件是表 1 中的 *md.in* 文件，可以使用以下伪代码命令执行 15 次后续模拟：</span>

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

   <span style=color:blue>每次模拟的运行时间为 10 ns，其中前 5 次用于溶质的结构平衡，将被丢弃；接下来的 10 个文件（共 100 ns）将用于后续的数据分析。</span>


### 3.3 Dendrimer Parametrization

1. Use any molecular editor software like Avogadro  (https://avogadro.cc/) to create a 3D representation of the dendrimer (*see* **Note** **2**) and save it in PDB format. 

   <span style=color:blue>使用任何分子编辑软件（例如 Avogadro，网址：https://avogadro.cc/）创建树枝状分子的三维结构，并以 PDB 格式保存。</span>

2. Use AMBER’s *antechamber* software to assign GAFF atom types to the dendrimer and compute its atomic partial charges via the AM1-BCC method, creating a forcefield library file (PREPIN file) for the dendrimer (*see* **Note** **3**). This can be achieved with the following command:

   <span style=color:blue>使用 AMBER 的 *antechamber* 软件为树枝状分子分配 GAFF 原子类型，并通过 AM1-BCC 方法计算其部分电荷，生成树枝状分子的力场库文件（PREPIN 文件）(*参见* **注释** **3**)。此操作可以通过以下命令完成：</span>

   ```shell
   antechamber -i dendrimer.pdb -fi pdb -o dendrimer.prepi -fo prepi \
   -at gaff -c bcc -nc NET_CHARGE
   ```

   where the options in order of appearance are: the name of the PDB file, the format, the name of the output file, its format, the forcefield to be applied, the method used to compute the partial charges, and finally the total charge of the dendrimer.

   <span style=color:blue>其中，选项依次表示：PDB 文件的名称、文件格式、输出文件名称、格式、使用的力场、部分电荷计算方法，以及树枝状分子的总电荷。</span>

3. Use AMBER’s *parmchk2* software to create a file (FRCMOD file) for the eventually missing parameters to integrate the dendrimer forcefield library. Execute this command as:

   <span style=color:blue>使用 AMBER 的 *parmchk2* 软件创建一个 FRCMOD 文件，补充可能缺失的力场参数，以完成树枝状分子力场库的整合。可以执行以下命令：</span>

   ```shell
   parmchk2 -i dendrimer.prepi -f prepi -o dendrimer.frcmod
   ```

   where the options in order of appearance are: the name of the input PREPI file (created during the execution of the previous antechamber commands), the format of the input file, and the name of the output file. For PAMAM dendrimers , the parameter selected by *parmchk2* and reported in the FRCMOD file are accurate enough; however, the user is free to implement any parameter refinement at this stage.

   <span style=color:blue>各选项的顺序为：输入的 PREPI 文件名称（在上一步 *antechamber* 生成），输入文件格式和输出文件名称。对于 PAMAM 树枝状分子，*parmchk2* 选择的参数已足够准确并已报告在 FRCMOD 文件中，但用户可在此阶段对参数进行改进。</span>

4. Follow the steps in Subheadings 3.1 and 3.2 to perform the MD simulation of the dendrimer. The steps in Subheading 3.2 should be repeated three times to obtain the three different trajectories required for further analysis. 

   <span style=color:blue>按照子章节 3.1 和 3.2 中描述的步骤执行树枝状分子的 MD 模拟。在子章节 3.2 中的步骤需要重复三次，以获得三条不同的轨迹用于后续分析。</span>


### 3.4 siRNA Model Optimization siRNA 模型优化

1. Use AMBER’s nab program to create an initial 3D structure of the desired siRNA sequence. This will ensure that the siRNA PDB file created will respect the naming conventions used in the AMBER forcefield. Firstly, create a text file called siRNA.nab with the following code:

   <span style=color:blue>利用 AMBER 的 *nab* 程序生成目标 siRNA 序列的初始三维结构。此方法确保生成的 siRNA PDB 文件符合 AMBER 力场的命名规则。首先，创建一个名为 **siRNA.nab** 的文本文件，并写入以下代码：</span>

   ```shell
   molecule m;
   fd_helix( “arna”, “YOUR_RNA_SEQUENCE”, “rna”)
   putpdb(“siRNA.pdb”, m, “-wwpdb”)
   ```

2. Run nab with the following commands to generate the siRNA.pdb file:

   <span style=color:blue>通过以下命令运行 *nab* 程序，生成 **siRNA.pdb** 文件：</span>

   ```shell
   nab siRNA.nab
   ./a.out
   ```

3. Follow the procedure reported in Subheadings 3.1 and 3.2 to obtain a solvated siRNA structure and an MD equilibrated siRNA trajectory in an aqueous environment. 

   <span style=color:blue>按照子章节 3.1 和 3.2 的流程，对 siRNA 结构进行溶剂化处理，并通过分子动力学模拟生成在水环境中达到平衡的 siRNA 轨迹。</span>


### 3.5 Complex Creation and Simulation 复合物的创建与模拟

Electrostatic interactions are usually at the base of the formation of cationic dendrimer/siRNA complexes, and the intermolecular recognition does not depend on a specific sequence on the nucleic acid fragment (base-aspecific). Nonetheless, any information available from laboratory experiments, literature, or previous knowledge on the particular binding of the specific dendrimer to the given siRNA sequence studied should be taken into consideration when creating the relevant complex model.

<span style=color:blue>复合物创建与模拟主要依赖于阳离子型树枝状分子和siRNA的静电相互作用，这种结合通常不特异于核酸片段的特定序列。但在构建复合物模型时，应充分参考实验、文献或先前研究中的任何特定结合信息。</span>

1. Using Chimera or VMD extract the final equilibrated structure of the dendrimer from its last data collection trajectory.<span style=color:blue>通过 **Chimera** 或 **VMD** 提取树枝状分子在最后一次模拟轨迹中的平衡结构。</span>

2. With the same software, extract the final equilibrated structure of the siRNA from its last data collection trajectory.<span style=color:blue>同样方法提取 siRNA 的最终平衡结构。</span>

3. Load both the extracted equilibrated 3D structures of the siRNA and the dendrimer into the visualization software, and place the dendrimer in close proximity of the siRNA yet avoiding visible clashes between their atoms.<span style=color:blue>在可视化工具中加载上述提取的三维结构，将树枝状分子放置于siRNA附近，确保两者没有原子间的直接碰撞。</span>

4. Save the obtained starting 3D structure of the complex to a coordinates PDB file.<span style=color:blue>将调整后的初始复合物结构保存为 PDB 格式。</span>

5. Follow all the steps in Subheadings 3.1 and 3.2 to obtain a solvated complex structure and perform data collection.<span style=color:blue>按照 **3.1** 和 **3.2** 的溶剂化与模拟流程，对复合物进行结构优化和数据收集。</span>

6. Repeat **steps 3**–**5** two more times, each time rotating the dendrimer and placing it to a different position in relation to the siRNA fragment. At the end of this section, three MD trajectories files will be obtained, each generated from the different dendrimer/siRNA complex starting structures and yet converging to the same equilibrium structure at the end of the corresponding simulation. Should this structural convergence not be achieved, the number of MD simulation must be increased (from 15 to 20 or more) until this condition is satisfied.<span style=color:blue>更换树枝状分子的初始位置（通过旋转和重新摆放），重复**步骤3至5**两次。此过程将生成三个不同初始结构的分子动力学轨迹文件，预期轨迹应在模拟后期收敛到一致的平衡结构。若未能达到预期的结构收敛，建议将模拟次数从15次增加至20次或更多，以保证可靠的结果。</span>


### 3.6 Dendrimer Analysis 树枝状分子分析

The analysis of every MD simulation should always begin with a careful observation of the relevant trajectories, as some peculiar phenomena taking place during any phase of the calculation can be intuitively identified and, eventually, further investigated. All analysis steps reported here and in the subsequent section have to be repeated for the three replicate trajectories, and the relevant calculated properties or quantities must be reported as average values. As mentioned above for structural model convergence, also the properties of interest obtained from the different MD trajectories must converge to the same value, and if this is not the case, the simulation cannot be trusted. A possible solution for is to run the simulations longer until convergence is achieved. To enter AMBER’s analysis software cpptraj , just type cpptraj on the AMBER command line. Then, execute the following within cpptraj.

<span style=color:blue>对每次分子动力学 (MD) 模拟的分析都应从仔细观察相关轨迹开始，因为计算过程中的某些特殊现象可以直观地被识别出来，并在需要时进行进一步研究。本节及后续部分中描述的所有分析步骤需针对三个独立轨迹重复进行，并将计算的属性或量值作为平均值报告。如同结构模型的收敛性要求，不同MD轨迹计算出的目标属性也必须收敛至相同值，否则模拟结果将不可被信赖。一种可能的解决办法是延长模拟时间，直至达到收敛。在进入AMBER的分析软件cpptraj时，只需在AMBER命令行中输入 `cpptraj`，然后按以下步骤执行分析。</span>

1. Load the equilibrated 100 ns-long dendrimer MD trajectory by typing:<span style=color:blue>加载平衡态的100 ns树枝状分子MD轨迹，输入以下命令</span>

   ```shell
   parm dendrimer.prmtop
   for i=6;i&lt;16;i++
   trajin MD$i.nc 1 last 10
   done
   autoimage
   ```

2. Use the command *radgyr* with the *tensor* option to compute the dendrimer radius of gyration *R*<sub>*g*</sub> and the relevant gyration tensor ***R***<sub>*g*</sub>, from which the molecular asphericity *b* can be obtained (*see* Subheading 2.2 and **Note** **4**):<span style=color:blue>**计算树枝状分子的回转半径 (\*R\*<sub>\*g\*</sub>) 及相关的回转张量 (\*R\*<sub>\*g\*</sub> tensor)**，使用 *radgyr* 命令和 *tensor* 选项。由此结果可以进一步计算分子的非球形度 *b* (详见子章节 **2.2** 及**注释4**)</span>

   ```shell
   radgyr RgyrDendrimer :DENDRIMER_MASK out rgyr_dendrimer_alone.out tensor
   ```

3. Next*,* use the command *radial* with the *rawrdf* and *center2* options and selecting the dendrimer as *solute* to calculate any radial monomer density *ρ(r)* from the dendrimer center of mass (*see* Subheading 2.3). Set the maximum radius equal to (*R*<sub>*g*</sub> × 1.3 + 15) Å, in which *R*<sub>*g*</sub> is the value of the dendrimer radius of gyration calculated in the preceding step (2). Set spacing = 0.5 Å. This command must be three times, each time selecting i) the water oxygens, ii) the dendrimer terminal nitrogens, and iii) the whole dendrimer atoms, respectively, to obtain corresponding *ρ(r)* profiles around the center of mass of the dendrimer (*see* **Note** **5**). Accordingly, type:<span style=color:blue>**计算树枝状分子的径向单体密度 \*ρ(r)\***，使用 *radial* 命令，同时选择 *rawrdf* 和 *center2* 选项，树枝状分子被选为 *solute*。径向分布的计算半径范围应设为 (*R*<sub>*g*</sub> × 1.3 + 15) Å，其中 *R*<sub>*g*</sub> 为先前步骤计算得到的回转半径，间隔设为0.5 Å。每次分别选定以下三种情况执行命令：</span>

   ```shell
   radial out radial_density.out 0.5 MAX_RADIUS \
   :WAT@O :DENDRIMER_MASK rawrdf center2
   radial out radial_density.out 0.5 MAX_RADIUS \
   :DENDRIMER_MASK@TERMINAL_NITROGEN :DENDRIMER_MASK rawrdf center2
   radial out radial_density.out 0.5 MAX_RADIUS \
   :DENDRIMER_MASK :DENDRIMER_MASK rawrdf center2
   ```

4. Now use the command *molsurf* selecting the dendrimer atoms to compute the relevant accessible surface area (*ASA)* (*see* Subheading 2.4). This command has to be issued multiple time, varying the *probe* option from 0.5 Å to 9.5 Å at 0.3 Å interval. The dendrimer interior cavities and voids can then be identified by plotting the square root of the *ASA* values thus obtained as a function of the probe radius used (*see* **Note** **6**). Accordingly, type:<span style=color:blue>**计算树枝状分子的可及表面积 (\*ASA\*)**，使用 *molsurf* 命令，选择树枝状分子的所有原子作为输入，设置不同的探针半径，从0.5 Å至9.5 Å，间隔为0.3 Å。通过绘制得到的 *ASA* 值的平方根与探针半径的关系图，可以识别树枝状分子内部的孔隙和空腔 (详见子章节 **2.4** 及**注释6**)。输入以下命令：</span>

   ```shell
   molsurf ASA_05 :DENDRIMER_MASK out ASA_05.out probe 0.5
   molsurf ASA_08 :DENDRIMER_MASK out ASA_08.out probe 0.8
   molsurf ASA_11 :DENDRIMER_MASK out ASA_11.out probe 1.1
   …
   molsurf ASA_95 :DENDRIMER_MASK out ASA_95.out probe 9.5
   ```


### 3.7 siRNA-Dendrimer Complex Structural Analysis siRNA-树枝状分子复合体的结构分析

1. Load the equilibrated 100 ns-long dendrimer/siRNA complex MD trajectory into AMBER’s *cpptraj* software by issuing the same commands described in the previous step. <span style=color:blue>**加载平衡态的100 ns树枝状分子/siRNA复合体MD轨迹**，按照 **3.6** 节中描述的相同命令，在 AMBER 的 *cpptraj* 软件中加载树枝状分子/siRNA复合体的轨迹。</span>

2. Within *cpptraj,* select the dendrimer atoms and use the command *radgyr* with the *tensor* option to compute the *R*<sub>*g*</sub>, ***R***<sub>*g*</sub> and *b* of the siRNA-bound dendrimer over time. Compare these values with those obtained for the uncomplexed dendrimer in solution obtained at point 2 in Subheading 3.6.<span style=color:blue>**计算复合状态下树枝状分子的回转半径、回转张量及非球形度**，在 *cpptraj* 中选择树枝状分子原子，使用 *radgyr* 命令及 *tensor* 选项，计算树枝状分子结合siRNA后的 *R*<sub>*g*</sub>、***R***<sub>*g*</sub> 和非球形度 *b* 的时间变化。将这些值与 **3.6** 节中未结合状态下的树枝状分子数据进行比较。</span>

3. Next use the command *radial* with the *rawrdf* and *center2* options and selecting the dendrimer as *solute*. Follow the same procedure described in **step 3** of Subheading 3.6 to set the corresponding values of the maximum radius and spacing. Issue this command 4 times, each time selecting different atoms as *solvent* (water atoms, the terminal nitrogen atoms, the whole dendrimer atoms and the siRNA atoms, respectively), to obtain the *ρ(r)* profiles for the selected atoms around the dendrimer center of mass (*see* **Note** **5**).<span style=color:blue>**计算复合体的径向密度分布 </span>\*ρ(r)\***，使用 *radial* 命令及 *rawrdf* 和 *center2* 选项，将树枝状分子作为 *solute*，按 **3.6** 节步骤3中描述的方法设置最大半径和间距。重复命令4次，分别选定以下原子作为 *solvent*：水原子；树枝状分子的末端氮原子；树枝状分子的所有原子；siRNA原子。通过这些命令，获得不同选定原子围绕树枝状分子质心的 *ρ(r)* 分布。</span>



### 3.8 siRNA-Dendrimer Energy of Binding Analysis siRNA-树枝状分子结合自由能分析

1. Use AMBER’s MMPBSA.py script to compute the enthalpic contribution to free energy of binding . Select the last two equilibrated MD trajectories obtained for dendrimer, siRNA and their complex, respectively, and pick one every 10 MD frames. The corresponding total number of frames thus will be 200. In the *&pb* section set *inp* equal 1 (to separate the dispersion and cavity formation terms) and *indi* equal 3, as required when dealing with highly charged macromolecules. Also, turn on energy decomposition with *&dec*, to obtain the contribution of each dendrimer residue to siRNA binding (*see* **Note 7**). Then, move all trajectories and topology files to the same directory, and use the following command line:<span style=color:blue>**计算结合焓 (\*ΔH\*)**，使用 AMBER 的 *MMPBSA.py* 脚本计算结合自由能中的焓贡献。选择树枝状分子、siRNA及其复合体的最后两个平衡MD轨迹，每隔10帧选择一个，总共200帧。在 *&pb* 部分设置 *inp=1* （分离分散和空腔形成项）和 *indi=3*（针对高电荷大分子）。同时启用 *&dec* 能量分解功能，获取每个树枝状分子残基对siRNA结合的贡献。将所有轨迹和拓扑文件移动到同一目录下，输入以下命令：</span>

   ```shell
   MMPBSA -O -i mmpbsa_enth.in -o dH_dendrimer_siRNA.out \
   -sp complex.solvated.prmtop -cp complex.prmtop \
   -rp siRNA.prmtop -srp siRNA.solvated.prmtop
   -lp dendrimer.prmtop -slp dendrimer.solvated.prmtop \
   -y md14.complex.nc md15.complex.nc \
   -yr md14.siRNA.nc md15.siRNA.nc \
   -yl md14.dendrimer.nc md15.dendrimer.nc
   ```

   where the options *-i* and *-o* specify the input and output files, the options *-sp*, *−slp*, *−srp* select the topology files of the solvated complex, dendrimer (ligand) and siRNA (receptor), respectively. Likewise, the options *-cp*, *−lp*, *−rp* and *-y*, *−yl*, *−yr* select the un-solvated topologies for the same systems and their corresponding solvated trajectories, respectively. The content of the mmpbsa_enth.in file is reported in Table 2.<span style=color:blue>*-i* 和 *-o* 指定输入和输出文件。*-sp*, *-slp*, *-srp* 分别指定溶剂化复合体、树枝状分子（配体）及siRNA（受体）的拓扑文件。*-cp*, *-lp*, *-rp* 和 *-y*, *-yl*, *-yr* 分别指定非溶剂化拓扑文件及对应的溶剂化轨迹。*mmpbsa_enth.in* 文件的内容详见 **表2**。</span>

2. Use AMBER’s MMPBSA.py script to compute the entropic contribution to free energy of binding. Select the same equilibrated trajectories used for enthalpy calculations, and pick one every 50 frames, for a total of 20 analyzed frames. Then, use the following command:<span style=color:blue>**计算结合熵 (\*TΔS\*)**，使用相同轨迹，选择焓计算所用的平衡轨迹，每隔50帧选择一个，总共分析20帧。输入以下命令：</span>

   ```shell
   MMPBSA -O -i mmpbsa_entr_nmode.in -o TdS_dendrimer_siRNA.out \
   -sp complex.solvated.prmtop -cp complex.prmtop \
   -rp siRNA.prmtop -srp siRNA.solvated.prmtop
   -lp dendrimer.prmtop -slp dendrimer.solvated.prmtop \
   -y md14.complex.nc md15.complex.nc \
   -yr md14.siRNA.nc md15.siRNA.nc \
   -yl md14.dendrimer.nc md15.dendrimer.nc
   ```

   The content of the mmpbsa_entr_nmode.in file is reported in Table 2.<span style=color:blue>*mmpbsa_entr_nmode.in* 文件的内容详见 **表2**。</span>

3. As the last step, use the fundamental Gibbs equation, *ΔG*<sub>bind</sub> = *ΔH*<sub>bind</sub> − *TΔS*<sub>bind</sub>, to obtain the corresponding free energy of binding between the dendrimer and the siRNA (*see* Subheading 2.5, **Notes** **8** and **9**).<span style=color:blue>**计算结合自由能 (*ΔG*<sub>bind</sub> = *ΔH*<sub>bind</sub> − *TΔS*<sub>bind</sub>)**，使用基本吉布斯自由能方程：</span>



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
