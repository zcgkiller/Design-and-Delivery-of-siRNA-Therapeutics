# Non-covalent Encapsulation of siRNA with Cell-Penetrating Peptides

Martina Tuttolomondo and Henrik J. Ditzel

## Abstract

SiRNAs may act as selective and potent therapeutics, but poor deliverability in vivo is a limitation. Among the recently proposed vectors, cell-penetrating peptides (CPPs), also referred as protein transduction domains (PTDs), allow siRNA stabilization and increased cellular uptake. This chapter aims to guide scientists in the preparation and characterization of CPP-siRNA complexes, particularly the evaluation of novel CPPs variants for siRNA encapsulation and delivery. Herein, we present a collection of methods to determine CPP-siRNA interaction, encapsulation, stability, conformation, transfection, and silencing efficiency.

## 1 Introduction

RNA interference (RNAi) is a powerful tool and a potential therapeutic for reversibly silencing a specific gene. This approach may have a broad application in treatment of multiple severe and chronic diseases, including cancer, viral infections, and genetic disorders. Despite its efficiency when the target is reached, siRNA is poorly deliverable in vivo because of low stability in the bloodstream, poor cellular uptake, and difficulties in reaching its intracellular targets. To circumvent these limitations, the development of siRNA carriers is of broad interest. Viral vectors, cationic lipids, and nanoparticles of different materials have been designed to increase siRNA stability and subsequently improve tissue and cell penetration in vivo. Among these, cell-penetrating peptides (CPPs), also called protein transduction domains (PTDs) , are a promising category of siRNA vectors.

CPPs can be subdivided into two classes, the first requiring covalent conjugation with the cargo, and the second involving the formation of stable, non-covalent electrostatic complexes, the latter being more appropriate for charged cargos such as siRNAs. While covalent conjugation can result in inefficient delivery of siRNA to cells, electrostatic encapsulation offers many advantages such as low price, high ease of formulation, and excellent flexibility. Electrostatic complexation allows regulation of size and charge based on the siRNA/peptide molar ratio. Furthermore, the formation of a peptide shell around the nucleic acid molecule allows large amounts of siRNA to be encapsulated, stabilized, and protected in the biological fluids, and reduces the possibility of degradation or removal by immune cells and RNases when administered in vivo, thus increasing the half-life of the siRNA in the circulation.

In our previous work, we designed DMBT1-derived cell-penetrating peptides for the encapsulation of siRNA with successful administration to MCF7 cells and gene silencing in the absence of FBS.

Here, we present a collection of methods to characterize a candidate CPP and its complex with the siRNA, and to evaluate the encapsulation efficiency and vehicle capability. First, we present a UV-spectroscopy-based method to analyze the interaction between CPP and siRNA. Then, we provide detailed protocols for evaluating siRNA encapsulation, CPP-siRNA dissociation, and stability in FBS by classical agarose gel electrophoresis. Subsequently, a method to evaluate the secondary structure of CPP-siRNA complexes by circular dichroism, a method based on unequal absorption of left-handed and right-handed circularly polarized light, is presented. Two different methods to quantify the CPP-siRNA transfection efficiency by employing fluorescently labeled CPP and siRNA are presented, the former based on the 96-well plate-based format and the latter on confocal microscopy imaging associated with ImageJ analysis. Finally, we describe an alternative method for in vitro gene silencing evaluation by employing tdTomato-engineered fluorescent cells.

## 2 Materials

### 2.1 UV Spectrophotometry and Agarose Gel Electrophoresis for Interaction, Encapsulation, and Stability Assays

The following items are needed for the methods described in Subheadings 3.1-3.4 (*see* **Note** **1**).

1. 1 mM cell-penetrating peptide stock solution (*see* **Note** **2**): Dissolve the selected or designed cell-penetrating peptide in ultrapure RNAse free water or 0.1–2% DMSO depending on peptide solubility (*see* **Notes** **3** and **4**) to obtain a 1 mM solution. Aliquot and store at −20 °C. **Note** **5** details the peptide S-RRep-RGD used in our example. Depending on the tested molar ratio, dilutions of the stock solution may be needed. For peptide S-RRep-RGD, we prepared 0.1 and 0.01 mM solutions.
2. 0.1 mM siRNA stock solution targeting the gene of interest (*see* **Notes** **6**  and **7**): Dissolve the selected or designed siRNA in ultrapure RNAse free water to obtain a 0.1 mM solution. Aliquot and store at −20 °C.
3. A vial mixer with thermal control (optional, *see* **Note** **8**).
4. High-resolution agarose for Molecular Biology, powder.
5. 10× TAE buffer: 50 mM EDTA disodium salt, 2 M Tris base, 1 M glacial acetic acid. Add about 800 mL deionized water to a 1 l graduated cylinder or a glass beaker. Weigh 242 g Tris–base and transfer to the cylinder. Add 18.61 g of disodium EDTA to the solution (*see* **Note** **9**). Add 57.1 g of acetic acid to the solution. Add deionized water to a volume of 900 mL. Mix and adjust pH with NaOH. Add deionized water to 1000 mL. Store at room temperature. 
6. GelRed® Nucleic Acid Stain 10,000×, Biotium, or another appropriate stain for agarose gel (*see* **Note** **10**).
7. Loading solution: 30% glycerol in ultrapure water (*see* **Note** **11**).
8. Nucleic acid ladder for electrophoresis (*see* **Note** **12**).
9. Horizontal electrophoresis apparatus.
10. Gel imager or UV transilluminator.
11. NanoDrop One/Onec UV-Vis Spectrophotometer (Thermo Scientific™; this instrument is needed for the method described in Subheading 3.1, *see* **Note** **13).
12. 1000 mg/mL dextran sulfate sodium (DSS). This item is needed for the methods described in Subheadings 3.3 and 3.4.
13. Serum of interest. This assay can be performed with different sera, such as human, mouse, or fetal bovine serum (FBS), depending on the final application. In this example we used FBS. This item is needed for the method described in Subheading  3.4. 
14. 1 mg/mL proteinase K. This item is needed for the method described in Subheading 3.4. 

### 2.2 Circular Dichroism

1. Circular Dichroism Spectropolarimeter connected to a computer with the appropriate software.
2. Quartz cuvette for circular dichroism (a 55-μL, 3-mm path-length cuvette is preferred).
3. 50 μL CPP-siRNA complex solution prepared at the encapsulation molar ratio. Be sure the final peptide concentration is in the range 0.1–0.5 μM.
4. 50 μL CPP solution at the same concentration as the CPP-siRNA complex solution.

### 2.3 Quantitative 96-Well Microplate-Based and Semi-Quantitative-Imaging Confocal Microscopy Transfection Efficiency Assay

1. Target adherent cell line (we used the human breast cancer cell line MCF7).
2. Cell laboratory equipped with a flow bench and a cell incubator.
3. Cell medium (we used DMEM supplemented with 10% FBS, 10 mg/mL insulin, and 100 U/mL penicillin/streptomycin).
4. 1 mM FITC-labeled candidate CPP (we used SRCRP2–11: GRVEVLYRGSW).
5. 10 uM Silencer Cy3-labeled Negative Control No. 1 siRNA (Ambion, Thermo Fisher Scientific).
6. Trypsin or other suitable cell detaching reagent.
7. Sterile PBS.
8. 4% Paraformaldehyde solution (PFA, for the confocal microscopy-based assay).
9. Dark wall, clear-bottom 96-well plates (for the 96-well microplate-based assay).
10. Microplate fluorometer (for the 96-well microplate-based assay).
11. Nunc Lab-Tek 12-Chambered Coverglass (ThermoFisher, for the imaging protocol).
12. CellMask Deep Red plasma membrane stain (Thermo Fisher Scientific, for the imaging protocol).
13. ProLong Diamond Antifade Mountant with DAPI (Thermo Fisher Scientific, for the imaging protocol).
14. Single photon confocal laser scanning microscope equipped with a 20× numerical aperture 0.96 objective (for the imaging protocol).
15. Fiji ImageJ software (downloadable from https://imagej.net/Fiji, for the imaging protocol).

### 2.4 Silencing by tdTomato-siRNA Transfection of tdTomato-Positive Engineered Cells

1. tdTomato-positive target adherent cell line stably expressing tdTomato fluorescent protein (we used MCF7, *see* **Note** **14**). 
2. Cell laboratory equipped with a flow bench and a cell incubator.
3. Cultivation cell medium: DMEM supplemented with 10% FBS, 10 mg/mL insulin, 100 U/mL penicillin/streptomycin, and hygromycin 300 mg/mL).
4. Transfection cell medium: DMEM supplemented with 10 mg/mL insulin, 100 U/mL penicillin/streptomycin, and 0.5% ITS Liquid Media Supplement.
5. tdTomato-targeting siRNA: UUGGUGUCCACGUAGUAGUAG.
6. Non-targeting siRNA, ON-TARGETplus Non-targeting Pool (Dharmacon).
7. Lipofectamine RNAiMAX transfection reagent (Thermo Fisher Scientific).
8. Positive control cell-penetrating peptide TAT: GRKKRRQRRRPQ.
9. 1 mM candidate CPP (we used SRCRP2–11: GRVEVLYRGSW).
10. Trypsin or other suitable cell detaching reagent.
11. Sterile PBS.
12. Dark wall, clear-bottom 96-well plates.
13. Microplate fluorometer .

## 3 Methods

### 3.1 Evaluation of Candidate CPP-siRNA Interaction Using UV siRNA Peak Hypochromicity

1. Switch on the thermomixer to the needed temperature. In our case, for peptide SRCRP2–11, 37 °C is preferred.
2. Prepare 5 μL siRNA solution at 10 μM (1:10 dilution of the stock siRNA solution at 0.1 mM).
3. Prepare 6 samples of 10 μL candidate CPP in a range of concentrations (e.g., 70, 140, 210, 280, and 350 μM, *see* Table [1](clbr://internal.invalid/OEBPS/html/485053_1_En_19_Chapter.xhtml#Tab1)).
4. Add 10 μL of 10 μM siRNA solution to each sample of one of the peptide solution series (CPP-siRNA samples) and 10 μL of ultrapure water to the other series (corresponding peptide samples). Finally, add 10 μL ultrapure water to the remaining 10 μL of 10 μM siRNA solution (free siRNA sample).
5. Incubate the samples in the thermomixer for 30 min at the encapsulating temperature.
6. Analyze at NanoDrop by using the custom function UV-Vis spectra in the range 190–290 nm and following the manufacturer’s instructions.
7. In the peptide-siRNA sample, the peak at 260 nm (siRNA) will be lower in comparison to the free siRNA sample (hypochromicity) and, in some cases, also shifted toward the red (bathochromic shift). The hypochromicity of the 260 nm peak confirms peptide-siRNA interaction (*see* Fig. [1a](clbr://internal.invalid/OEBPS/html/485053_1_En_19_Chapter.xhtml#Fig1)). The hypochromicity can be shown as absorbance decrease by plotting the absorbance at 260 nm against the peptide-siRNA molar ratio (*see* Fig. [1b](clbr://internal.invalid/OEBPS/html/485053_1_En_19_Chapter.xhtml#Fig1)). The peptide-siRNA interaction is usually observed at a peptide-siRNA molar ratio lower than that of encapsulation.

**Table 1** Preparation of peptide-siRNA mixtures for hypochromicity encapsulation assay

|                |                           | 1. Mix peptide and siRNA working solutions to obtain 20 μL final mixed solution2. Incubate for 30 min at the encapsulation temperature |                               |                                |                                                 |
| :------------- | :------------------------ | :----------------------------------------------------------- | :---------------------------- | :----------------------------- | :---------------------------------------------- |
|                |                           | 10 μL peptide working solution                               | 10 μL siRNA working solution  |                                |                                                 |
| #              | Peptide:siRNA molar ratio | Volume of 0.01 mM peptide (μL)                               | Volume of 0.1 mM peptide (μL) | Volume of ultrapure water (μL) | Volume of 0.01 mM siRNA or ultrapure water (μL) |
| 1 (siRNA only) | 0:1                       | –                                                            | –                             | 10                             | 10                                              |
| 2              | 7:1                       | 7                                                            | –                             | 3                              | 10                                              |
| 3              | 14:1                      | –                                                            | 1.4                           | 8.6                            | 10                                              |
| 4              | 21:1                      | –                                                            | 2.1                           | 7.9                            | 10                                              |
| 5              | 28:1                      | –                                                            | 2.8                           | 7.2                            | 10                                              |
| 6              | 35:1                      | –                                                            | 3.5                           | 6.5                            | 10                                              |

![485053_1_En_19_Fig1_HTML](https://raw.githubusercontent.com/zcgkiller/Pictures/main/Wechat/485053_1_En_19_Fig1_HTML.png)

**Fig. 1** (**a**) UV spectra analysis showing hypochromicity of the tdTomato1 siRNA peak at 260 nm after the addition of peptide SRCRP2–11. (**b**) Hypochromicity can be highlighted by plotting the absorbance at 260 nm against the peptide-siRNA molar ratio. Data were reused from [[15](clbr://internal.invalid/OEBPS/html/485053_1_En_19_Chapter.xhtml#CR15)]

### 3.2 Determination of the Optimal Encapsulation Molar Ratio for the Candidate CPP-siRNA Complex

1. Switch on the thermomixer to the needed temperature. In the case of peptide S-RRep-RGD, 37 °C is preferred.
2. Prepare a 4% agarose gel in 1× TAE buffer (*see* **Note** **15**). After agarose dissolution, add 10 μL of GelRed® to the gel and mix. Since the gel is warm and cooling down will provoke fast polymerization, we recommend adding the stain under a flow bench for safety. Pour the gel in the cassette with a comb and wait until polymerization. High-percentage agarose gels require only 15–20 min to polymerize.
3. Prepare samples of mixed peptide and siRNA solutions. For each sample, maintain a constant siRNA concentration and increase the amount of peptide to obtain increasing peptide:siRNA molar ratios. If the approximate encapsulation molar ratio is unknown, select a wide range of molar ratios, such as 1:1–200:1. We suggest preparing the peptide working solutions in 10 μL, then separately preparing the siRNA working solutions in 10 μL. In the example provided (*see* Fig. 2 and Table 1), 6 samples of 60 μL at 0.01 mM were prepared and finally the working solutions were mixed to obtain a final volume of 20 μL. Thus, equal volumes of peptide and siRNA solution will be mixed and the reaction will be even, ensuring regular complex size and small polydispersion index. In the provided example, we tested 5 samples in the molar ratio range between 1:1 and 1:30 and prepared the samples by mixing the peptide solution and siRNA working solutions according to Table 2. Incubate the samples for 30 min at the encapsulation temperature, for peptide S-RRep-RGD, 37 °C.
4. Prepare the agarose gel cassette. Add the appropriate volume of 6× glycerol loading solution to each sample based on the final volume (in our example 4 μL), pipette up and down, and load the ladder and the samples in the wells. We suggest loading the ladder in a well both to the left and right of the samples to have a horizontal reference to evaluate the shift. Perform electrophoresis at 7 V/cm for 30 min.
5. Image with an UV transilluminator or gel imager. If the peptide efficiently encapsulates the siRNA, a complete shift of the band should be observed at a specific molar ratio (encapsulation molar ratio). Figure [2](clbr://internal.invalid/OEBPS/html/485053_1_En_19_Chapter.xhtml#Fig2) shows the result obtained for S-RRep-RGD. In this case, the peptide efficiently encapsulated BrafMut siRNA at a peptide-siRNA molar ratio of 30:1. This assay is imperative to establish the encapsulation capability and the encapsulation molar ratio of newly tested cell-penetrating peptides or cell-penetrating peptide-siRNA combinations.

![485053_1_En_19_Fig2_HTML](https://raw.githubusercontent.com/zcgkiller/Pictures/main/Wechat/485053_1_En_19_Fig2_HTML.png)

**Fig. 2** Gel shift for encapsulation assay of BrafMut siRNA with peptide S-RRep-RGD. The agarose gel percentage was 4%. Each lane contains 10 pmol of siRNA and increasing amounts of peptide in a range between 10 and 300 pmol. The electrophoresis was performed in TAE at 7 V/cm for 30 min. Complete encapsulation was observed at peptide-siRNA molar ratio of 30:1

**Table 2** Preparation of peptide-siRNA mixtures for gel shift encapsulation assay

|      |                           | 3. Mix peptide and siRNA working solutions to obtain 20 μL final mixed solution4. Incubate for 30 min at the encapsulation temperature |                               |                                |                              |
| :--- | :------------------------ | :----------------------------------------------------------- | :---------------------------- | :----------------------------- | :--------------------------- |
|      |                           | 10 μL peptide working solution                               | 10 μL siRNA working solution  |                                |                              |
| #    | Peptide:siRNA molar ratio | Volume of 0.01 mM peptide (μL)                               | Volume of 0.1 mM peptide (μL) | Volume of ultrapure water (μL) | Volume of 0.01 mM siRNA (μL) |
| 1    | 0:1                       | –                                                            | –                             | 10                             | 10                           |
| 2    | 1:1                       | 1                                                            | –                             | 9                              | 10                           |
| 3    | 5:1                       | 5                                                            | –                             | 5                              | 10                           |
| 4    | 10:1                      | –                                                            | 1                             | 9                              | 10                           |
| 5    | 20:1                      | –                                                            | 2                             | 8                              | 10                           |
| 6    | 30:1                      | –                                                            | 3                             | 7                              | 10                           |

### 3.3 Dextran Sulfate Sodium Competition Assay for Cell-Penetrating Peptide-siRNA Complexes

This method is useful to evaluate whether the interaction forces between the peptide and the siRNA rely on electrostatic bonds .

1. Prepare multiple samples of peptide-siRNA complexes at the encapsulation molar ratio previously determined. Follow the procedure described in Subheading 3.2. For peptide Rep6, the peptide-siRNA encapsulation molar ratio is 25:1, as shown in Fig. 3a. Prepare the mixtures according to Table 3. We prepared 9 samples of peptide-siRNA complexes to be treated with increasing concentrations of DSS. One sample of untreated peptide-siRNA complexes and one with only free siRNA were used as controls. 
2. Prepare dilutions of DSS in the desired range of concentrations. In our example, we prepared DSS solutions at 5, 25, 50, 100, 150, 300, 800 mg/mL from a stock solution of 1000 mg/mL.
3. Add 1 μL of DSS at serial dilution of increasing concentrations to the samples of peptide-siRNA complex. Table 3 shows the suggested sample setting and corresponding final concentrations of DSS , considering 1 μL in 20 μL will correspond to a 1:20 dilution.
4. Incubate for 30 min at 37 °C.
5. Proceed with agarose gel electrophoresis, as described in Subheading 3.2, **steps 4** and **5**.
6. Figure 3b shows the result obtained for Rep6. If the interaction between the peptide and the siRNA is electrostatic, DSS should interfere with peptide-siRNA interaction, resulting in decreased siRNA shift in the agarose gel or siRNA release. 

![485053_1_En_19_Fig3_HTML](https://raw.githubusercontent.com/zcgkiller/Pictures/main/Wechat/485053_1_En_19_Fig3_HTML.png)

**Fig. 3** Dextran sulfate sodium competition assay showing tdTomato1 siRNA encapsulation (**a**) and release (**b**) from Rep6-tdTomato1 siRNA complexes after addition of DSS

**Table 3** Preparation of peptide-siRNA mixtures for stability DSS competition assay

|      |                           | Step 1                                                       | Step 2                                   |                              |                                       |                            |
| :--- | :------------------------ | :----------------------------------------------------------- | :--------------------------------------- | :--------------------------- | :------------------------------------ | :------------------------- |
|      |                           | 1. Mix peptide and siRNA working solutions to obtain 20 μL final mixed solution2. Incubate for 30 min at the encapsulation temperature | 3. Add DSS4.Incubate for 30 min at 37 °C |                              |                                       |                            |
|      |                           | 10 μL peptide working solution                               | 10 μL siRNA working solution             | 1 μL DSS working solution    |                                       |                            |
| #    | Peptide:siRNA molar ratio | Volume of 0.1 mM peptide (μL)                                | Volume of ultrapure water (μL)           | Volume of 0.01 mM siRNA (μL) | Concentration of DSS working solution | Final concentration of DSS |
| 1    | 0:1siRNA no DSS           | –                                                            | 10                                       | 10                           | –                                     | –                          |
| 3    | 25:1siRNA/peptide no DSS  | 2.5                                                          | 6.5                                      | 10                           | –                                     | –                          |
| 4    | 25:1                      | 2.5                                                          | 6.5                                      | 10                           | 5 mg/mL                               | 0.25 mg/mL                 |
| 5    | 25:1                      | 2.5                                                          | 6.5                                      | 10                           | 25 mg/mL                              | 1.25 mg/mL                 |
| 6    | 25:1                      | 2.5                                                          | 6.5                                      | 10                           | 50 mg/mL                              | 2.5 mg/mL                  |
| 7    | 25:1                      | 2.5                                                          | 6.5                                      | 10                           | 150 mg/mL                             | 7.5 mg/mL                  |
| 8    | 25:1                      | 2.5                                                          | 6.5                                      | 10                           | 300 mg/mL                             | 15 mg/mL                   |
| 9    | 25:1                      | 2.5                                                          | 6.5                                      | 10                           | 800 mg/mL                             | 40 mg/mL                   |
| 10   | 25:1                      | 2.5                                                          | 6.5                                      | 10                           | 1000 mg/mL                            | 50 mg/mL                   |

### 3.4 Stability Assay of Cell-Penetrating Peptide-siRNA Complexes

Here, we describe one of the classical agarose gel electrophoresis approaches for evaluation of serum stability . As recently reported, we also designed a sensitive method for evaluation of siRNA stability in serum that can be applied to other siRNA delivery systems. A detailed protocol for the latter assay is described in Chapter [10](https://github.com/zcgkiller/Design-and-Delivery-of-siRNA-Therapeutics/blob/main/Preparation%20and%20Characterization%20of%20siRNA-Loaded%20Liposomes.md).

1. Switch on the thermomixer to the needed temperature. In the case of Rep6, a temperature of 37 °C is preferred. 
2. Prepare a 4% agarose gel, as described in Subheading 2.1.
3. Prepare samples of mixed peptide and siRNA solutions at the encapsulation peptide:siRNA molar ratio. To test the stability in a range of serum concentrations, prepare replicates of the cell-penetrating peptide-siRNA complexes as needed as well as a similar number of samples containing the siRNA without peptide. Table 4 shows an experimental setting suggested to test a single peptide. We suggest testing at least 3 percentages of FBS for the selected candidate CPP and leave 1 untreated, e.g., prepare 4 samples for each series with and without peptide, according to Table 4.
4. Add FBS to the samples in a range of volume depending on the chosen range of percentages (as from Table 4), and incubate for 2 h at 37 °C.
5. Add 1 μL of 1 mg/mL proteinase K and 50 mg/mL DSS working solution (*see* **Note** **16**), and incubate for 10 min at 37 °C.
6. Proceed with agarose gel electrophoresis as described in Subheading 3.2, **steps 4** and **5**.
7. Figure 4a shows the stability of several DMBT1 variants in 10% FBS at 37 °C for 1 h. If the peptide efficiently protects the siRNA, the intensity of the siRNA band released from the peptide should not be weaker than that of the free untreated siRNA band, confirming that the peptide efficiently protects the siRNA from FBS RNAses. As a negative control, the free FBS-treated siRNA band will be weakened because of RNAse degradation. Bands can be analyzed by ImageJ using the gel analysis tool, as shown in Fig. 4b. 

**Table 4** Preparation of peptide-siRNA mixtures for stability assay in FBS

|      |                                          | Step 1—encapsulation of siRNA                                | Step 2—FBS treatment                   | Step 3—release of siRNA                                      |                             |                    |      |
| :--- | :--------------------------------------- | :----------------------------------------------------------- | :------------------------------------- | :----------------------------------------------------------- | :-------------------------- | :----------------- | ---- |
|      |                                          | 5. Mix peptide and siRNA working solutions to obtain 20 μL final mixed solution6. Incubate for 30 min at the encapsulation temperature | 7. Add FBS8. Incubate for 2 h at 37 °C | 9. Add 1 mg/mL proteinase K and 50 mg/mL DSS10. Incubate for 10 min at 37 °C |                             |                    |      |
|      |                                          | 10 μL peptide working solution                               | 10 μL siRNA working solution           | Volume of FBS (μL)                                           | Volume of proteinase K (μL) | Volume of DSS (μL) |      |
| #    | Peptide:siRNA molar ratioAnd sample name | Volume of 0.1 mM peptide (μL)                                | Volume of ultrapure water (μL)         | Volume of 0.01 mM siRNA(μL)                                  |                             |                    |      |
| 1    | 0:1siRNA untreated                       | –                                                            | 10                                     | 10                                                           | –                           | 1                  | 1    |
| 2    | 0:1siRNA +5% FBS                         | –                                                            | 9                                      | 10                                                           | 1                           | 1                  | 1    |
| 3    | 0:1siRNA +10% FBS                        | –                                                            | 8                                      | 10                                                           | 2                           | 1                  | 1    |
| 4    | 0:1siRNA +25% FBS                        | –                                                            | 5                                      | 10                                                           | 5                           | 1                  | 1    |
| 5    | 30:1siRNA-peptide untreated              | 3                                                            | 7                                      | 10                                                           | –                           | 1                  | 1    |
| 6    | 30:1siRNA-peptide +5% FBS                | 3                                                            | 7                                      | 10                                                           | 1                           | 1                  | 1    |
| 7    | 30:1siRNA-peptide 10% FBS                | 3                                                            | 7                                      | 10                                                           | 2                           | 1                  | 1    |
| 8    | 30:1siRNA-peptide 25% FBS                | 3                                                            | 7                                      | 10                                                           | 5                           | 1                  | 1    |

![485053_1_En_19_Fig4_HTML](https://raw.githubusercontent.com/zcgkiller/Pictures/main/Wechat/485053_1_En_19_Fig4_HTML.png)

**Fig. 4** (**a**) Agarose gel electrophoresis showing the stability of several DMBT1-derived peptide variants encapsulating tdTomato1 siRNA and incubated in 10% FBS for 1 h at 37 °C. (**b**) ImageJ analysis of the agarose gel shown in **a**

### 3.5 Circular Dichroism

1. Start the machine according to manufacturer’s instructions.
2. Place the CPP sample in the cuvette and measure the circular dichroism. Repeat the procedure for the CPP-siRNA sample.
3. Retrieve spectra raw data and plot the circular dichroism (mdeg) against the wavelength (nm) to obtain spectra (Fig. 5a).
4. Use the provided spectra fingerprints (Fig. 5b) to evaluate the conformation of the CPP and the CPP-siRNA complex. Data for Fig. 5b were retrieved from the PCDDB website (www.pcddb.cryst.bbk.ac.uk). In our example, the SRCRP2–11-siRNA complex exhibits a beta-helix conformation (Fig. 5a). Several short CPPs exhibit a random coiled conformation before the addition of siRNA. For CPP-siRNA complexes, ordered structures, such as alpha- or beta-helix, are more likely to approach and cross the cell membrane compared to random coiled complexes.

![485053_1_En_19_Fig5_HTML](https://raw.githubusercontent.com/zcgkiller/Pictures/main/Wechat/485053_1_En_19_Fig5_HTML.png)

**Fig. 5** (**a**) Circular dichroism spectra of peptide SRCRP2–11, tdTomato1 siRNA, and Peptide SRCRP2–11-tdTomato siRNA complex. Data were reused from [[15](clbr://internal.invalid/OEBPS/html/485053_1_En_19_Chapter.xhtml#CR15)]. (**b**) Circular dichroism spectra of different protein secondary structures can be used as fingerprints for the identification of peptide-siRNA complex structure. Data were retrieved from PCDDB

### 3.6 Quantitative 96-Well Plate-Based Transfection Efficiency Assay

1. Culture the target cell line according to the usual protocols.
2. Prepare a scheme of the 96-well microplate wells to be seeded with samples and controls solutions based on the number of tested conditions and replicates (*see* Fig. 6a for the plate scheme provided in this example, *see* **Note** **16**).
3. When cells reach 80% confluence, trypsinize and transfer the cells to the 96-well microplate at 20,000 cell/well according to the desired plate scheme and keep the plate in the cell incubator overnight.
4. Prepare FITC-CPP-CY3-siRNA complex solutions at various molar ratios (e.g., 10:1–180:1). Vary the peptide concentration (e.g., 10–180 μM) and keep a constant siRNA concentration (1 μM). For the suggested ranges, the final concentration of the peptide in the wells will correspond to 1–18 mM, and the final concentration of siRNA in all wells will be 100 nM (*see* Table [5](clbr://internal.invalid/OEBPS/html/485053_1_En_19_Chapter.xhtml#Tab5) for the volume calculation corresponding to the provided example).
5. Prepare a 9:1 in volume mixture of cell medium:FITC-CPP-Cy3-siRNA solution. For each well, 90 μL of cell medium and 10 μL of FITC-CPP-Cy3-siRNA solution will be needed. For 3 replicates, mix 270 μL of cell medium and 30 μL of FITC-CPP-Cy3-siRNA for each condition. Add 100 μL of the prepared cell medium-FITC-CPP-Cy3-siRNA mixture to each well according to the microplate scheme. Add 100 μL of cell-medium to the untreated cell sample wells. Add 100 μL PBS to the surrounding empty wells.
6. Leave the 96-well microplate in the cell incubator for at least 2 h. In our sample, we incubated overnight. This assay can be performed at different time intervals by preparing multiple plates.
7. Remove cell medium from all wells and wash 3 times with PBS to remove the residual labeled complexes. Add 100 μL of cell-medium to each well.
8. Use a microplate fluorometer to read the fluorescence from FITC (pick of excitation 495 nm, pick of emission 521 nm, related to the peptide) and Cy3 (pick of excitation 550 nm, pick of emission 570 nm, related to the siRNA, *see* **Note** **18**).
9. Figure 6b shows the graph obtained for our provided example. In the case of peptide SRCRP2–11, we observed that the optimal molar ratio allowing maximum transfection efficiency is approximately 60:1.

![485053_1_En_19_Fig6_HTML](https://raw.githubusercontent.com/zcgkiller/Pictures/main/Wechat/485053_1_En_19_Fig6_HTML.png)

**Fig. 6** (**a**) MCF7 cells internalization of Cy3-labeled siRNA at fixed concentration after addition of increasing amounts of FITC-SRCRP2–11 peptide. Values are the average of three experiments, with error bars indicating SEMs. Asterisks indicate the level of significance, based on the Student t test (**p* = 0.0021–0.04332, ***p* = 0.0002–0.0021, ****p* = 0.0001–0.0002, *****p* < 0.0001). (**b**) Microplate sample setting for 96-well-based internalization assay. Data were reused from [[15](clbr://internal.invalid/OEBPS/html/485053_1_En_19_Chapter.xhtml#CR15)]

**Table 5** Preparation of FITC-CPP-Cy3-siRNA complexes for 96-well microplate-based transfection efficiency assay (math for 3 replicates +1 sample excess)

|      |                           | 1. Mix peptide and siRNA working solutions to obtain 40 μL final mixed solution2. Incubate for 30 min at the encapsulation temperature |                                  |                                |                           |
| :--- | :------------------------ | :----------------------------------------------------------- | :------------------------------- | :----------------------------- | :------------------------ |
|      |                           | 20 μL FITC-peptide working solution                          | 20 μL Cy3-siRNA working solution |                                |                           |
| #    | Peptide:siRNA molar ratio | Volume of 0.1 mM peptide (μL)                                | Volume of 1 mM peptide (μL)      | Volume of ultrapure water (μL) | Volume of 1 μM siRNA (μL) |
| 1    | 0:1                       | –                                                            | –                                | 20                             | 20                        |
| 2    | 10:1                      | 4                                                            | –                                | 16                             | 20                        |
| 3    | 30:1                      | 12                                                           | –                                | 6                              | 20                        |
| 4    | 60:1                      | –                                                            | 2.4                              | 17.6                           | 20                        |
| 5    | 120:1                     | –                                                            | 4.8                              | 15.2                           | 20                        |
| 6    | 180:1                     | –                                                            | 7.2                              | 12.8                           | 20                        |

### 3.7 Confocal Microscopy-Based Semi-Quantitative-Imaging Transfection Efficiency Assay

1. Culture cell lines according to standard protocols.
2. When 80% confluence is reached, trypsinize, transfer to a Nunc Lab-Tek 12-Chambered Coverglass at 30,000 cells/well, and culture overnight.
3. Transfect with FITC-CPP alone, FITC-CPP-Cy3-siRNA and FITC-CPP-Cy3-siRNA complexes at the optimal final concentration/molar ratio as established in the previous assay and incubate for at least 2 h.
4. Remove cell medium from all wells and wash 3 times with PBS to remove the residual labeled peptide and siRNA.
5. Stain cells with CellMask Deep Red plasma membrane stain according to the manufacturer’s protocol. Wash 3 times with PBS.
6. Fix cells by adding 100 μL of 4% PFA solution and incubate for 10 min at room temperature. Wash 3 times with PBS.
7. Disassemble the slide chambers according to the manufacturer instructions.
8. Mount the slides with ProLong Diamond Antifade Mountant with DAPI and a cover glass.
9. Image using a single photon laser scanning confocal microscope (*see* Fig. 7a for an example of the imaging).
10. Setting of channels (abs/em):
    - DAPI (nuclei): 358/461 nm.
    - CellMask™ Deep Red Plasma membrane Stain (cell membrane): 649/666 nm.
    - FITC (peptide): 493/522 nm.
    - Cy3: 554/568 nm.
11. Import the image files in Fiji software: from the drop-down menu click on “File” – “Open,” then find the directory of your multi-channel image.
12. Convert to 8-bit image: click on “Image” – “Type” – “8-bit.”
13. Split the channels to single images: click on “Image” – “Color” – “Arrange channels,” write the name for the channel combination. Click on “Image” – “Color” – “Split channels” (*see* Figs. 7c-f).
14. Click on the image of the cell membrane (CellMask™ Deep Red channel). Click on “Image” – “Adjust” – “Threshold.” Choose a threshold that includes the signal from FITC and excludes the background (*see* Fig. 7g). Choose the “Wand tool” from the toolbar and select one group of cells. Add this selection to the ROI (region of interest) manager: click on “Edit” – “Selection” – “Add to manager.” Rename the ROI “Group of cells 1.” Do the same with the remaining cells and group of cells (*see* **Note** **19**).
15. Set the measurements for ImageJ to calculate the areas: click on “Analyze” – “Set measurements” and check “Area.”
16. Click on the image of the internalized peptide (FITC channel) and set the threshold: click on “Image” – “Adjust” – “Threshold.” Choose a threshold that includes the signal from FITC and excludes the background (*see* Fig. 7i). Click on the ROI manager and select all the ROIs created from the cell membrane image. Click “More…” and select “OR (combine).”
17. Measure the FITC signal inside the ROIs (peptide internalized by the cells): click on “Analyze” – “Analyze Particles.” Check “Pixel units. Set “Show” to “Outlines.” Check “Display Results” and “Summarize” and uncheck “Clear Results.” Click on “ok.” The window “Summary” will show the total area of FITC signal. A separate window will show the areas analyzed in the image.
18. Repeat **steps 15** and **16** for the image of the internalized siRNA (Cy3 channel) to establish how much siRNA has entered the cells (*see* Fig. 7j).
19. Analyze the nuclear internalization: Create a threshold for the nuclei (*see* Fig. 7h).
20. Select each nucleus and add each selection to the ROI manager. Rename the selections “Nucleus1, Nucleus2 etc.” These latter steps are similar to those used for the cells (**step 13**).
21. Repeat **steps 15** and **16** for FITC and Cy3 by using the merge of nuclei ROI as selection (*see* Fig. 7h).
22. Analyze data and create a graph (*see* Fig. 7b).

![485053_1_En_19_Fig7_HTML](https://raw.githubusercontent.com/zcgkiller/Pictures/main/Wechat/485053_1_En_19_Fig7_HTML.png)

**Fig. 7** Internalization of FITC-SRCRP2–11-Cy3 siRNA Complexes by MCF7 Breast Cancer Cells. (**a**, **c**–**f**) Confocal microscopy images of MCF7 cells treated with FITC-SRCRP2–11 peptide. (**a**) Merge of CellMask (**c**), DAPI (**d**), FITC (**e**), and Cy3 (**f**) channels. Colors indicate the following: red, CellMask Deep Red plasma membrane staining of plasma membranes; blue, DAPI staining of nuclei; green, FITC-peptide; yellow, Cy3-siRNA. (**b**) Image J analysis of confocal microscopy images representing the nuclear and cytoplasmatic FITC-peptide and Cy3-siRNA fluorescence intensity. (**g**) Threshold of **c**. (**h**) Threshold of **d**. (**i**) Threshold of **e**. (**j**) Threshold of **f**. Data were reused from [[15](clbr://internal.invalid/OEBPS/html/485053_1_En_19_Chapter.xhtml#CR15)]

### 3.8 Exploiting tdTomato-Transfected Fluorescent Cells for the Evaluation of siRNA-Driven Gene Silencing

The use of a cell line stably expressing a fluorescent gene is an alternative to the classical methods for the evaluation of gene silencing such as RT-qPCR or Western blot. The MCF7 cell line used here has been engineered to stably express the fluorescent protein tdTomato. A tdTomato-targeting siRNA can be combined with the candidate CPP and administered to the cells to evaluate tdTomato gene knockdown proportional to the decrease of fluorescence. Figure 8a shows a scheme of the method.

1. Maintain the tdTomato-positive cell line in culture with cultivation cell medium until 80% confluence is reached. 
2. Prepare a scheme of the 96-well microplate wells to be seeded with candidate CPP-siRNA complex solution and controls based on the number of tested conditions and replicates (*see* Fig. 8b).
3. On the day of transfection, prepare the candidate CPP-tdTomato siRNA complexes as described in Subheading 3.2 in 10 μL PBS/well at the established encapsulation molar ratios. The final well siRNA concentration used in our example is 100 nM. However, to better distinguish between the vector capability of several peptide variants, it is recommended that the final well siRNA concentration be decreased to 20–50 nM. Prepare CPP-non-targeting siRNAs as a negative control, use Lipofectamine- and TAT-encapsulated tdTomato siRNA as positive controls. Remember to include 3 wells for the untreated cells. All solutions should be prepared in the volume needed for at least 3 replicates (e.g., 30 μL).
4. Add 10 μL of CPP-siRNA complexes or controls to each well of an empty 96-well plate in triplicates according to the plate scheme (*see* Fig. 8b).
5. Trypsinize cells and resuspend them in transfection medium at 110,000 cells/mL in order to obtain 10,000 cells in 90 μL. The volume of transfection medium to be prepared will be 90 × number of wells to be transfected. Add 90 μL of cell suspension to each well of the pretreated 96-well plate. The final cell density will be 10,000 cells/well.
6. Incubate the 96-well plate for at least 96 h at 37 °C in humidified 5% CO~2~.
7. Read the fluorescence from the plate using a microplate fluorometer close to the excitation and emission peaks at 554/581 nm. The decreased fluorescence from tdTomato-positive cells compared to the untreated samples will be proportional to the gene silencing (*see* Fig. 8c). 

![485053_1_En_19_Fig8_HTML](https://raw.githubusercontent.com/zcgkiller/Pictures/main/Wechat/485053_1_En_19_Fig8_HTML.png)

**Fig. 8** (**a**) Schematic representation of the tdTomato-silencing assay in MCF7 cells. (**b**) Microplate sample setting for tdTomato-silencing assay. (**c**) tdTomato gene silencing by SRCRP2–11-R-peptide-tdTomato1 siRNA complexes in MCF7 cells. Values are the average of two experiments, with error bars indicating SEMs. Asterisks indicate the level of significance, based on the Student t test (\**p* = 0.0021–0.04332, \*\**p* = 0.0002–0.0021, \*\*\**p* = 0.0001–0.0002, \*\*\*\**p* < 0.0001). Data were reused from [[15](clbr://internal.invalid/OEBPS/html/485053_1_En_19_Chapter.xhtml#CR15)]

## 4 Notes

1. All steps should be performed in an RNase-free area, requiring use of commercially available sprays to clean benches, gloves, pipettes, and equipment.
2. Cell-penetrating peptides can be selected from a database (e.g., CPPsite 2.0: http://crdd.osdd.net/raghava/cppsite), from the literature or designed using online tools (e.g., CellPPD: http://crdd.osdd.net/raghava/cellppd). The selected or designed cell-penetrating peptides can be purchased from a peptide synthesis services (e.g., ThermoFisher, GenScript, ProteoGenix, and many others) and customized synthesis will ensure the peptide is at least 97% pure. Alternatively, peptides can be synthesized and prepared in any laboratory using a solid-phase peptide synthesizer (e.g., ABI433 automatic peptide synthesizers, Weiterstadt, Germany) or by manual synthetic cycles if the required expertise and laboratory equipment is available.
3. Ultrapure RNase-free water should be used to solubilize the peptides. The most common alternative is Diethyl pyrocarbonate (DEPC)-treated water; however, the ultrapure water has more natural characteristics. We observed decreased pH in water after DEPC treatment, probably due to dissolution of CO2 derived from the degradation of DEPC after autoclaving. Moreover, even after autoclaving, DEPC is not completely degraded, and residual DEPC can still carboxymethylate Tyr and His residues of peptides.
4. Dissolution conditions should be checked for the selected peptides. If the peptide is newly designed, solubility tests should be performed. If the peptide is produced by a peptide synthesis service, solubility tests can be ordered prior receiving the product. Amphipathic peptides may require sonication to be completely dissolved. Incomplete dissolution of the peptide may affect the efficacy as a vector.
5. In this chapter, we employ our previously designed DMBT1-derived cell-penetrating peptides and variants thereof as an example: SRCRP2–11 (GRVEVLYRGSW), SRCRP2–11-R (GRVRVLYRGSW), Rep6 (GRRRRLYRGSWGRRRRLYRRSR), S-RRep-RGD (Stearyl-GRVRRLRGDGWGRVRVLRGDGW-amide). The peptides SRCRP2–11, SRCRP2–11-R, and Rep6 were dissolved in water at 1 mM, while peptide S-RRep-RGD was dissolved in 10% DMSO at 1 mM.
6. The siRNA sequence should be designed based on the targeted gene. If the siRNA is synthetized in-house, it is possible to use an online tool such as siDirect2.0 software (available at http://siDirect2.RNAi.jp/). If using an oligonucleotide synthesis service, it is possible to order a predesigned or validated siRNA or to design custom siRNA sequences by using online tools provided by the chosen company.
7. For many cell-penetrating peptides, we have observed that siRNA encapsulation is not dependent on the siRNA sequence. Different siRNA sequences may slightly change the exact encapsulation molar ratio. For better accuracy, the suggested encapsulation assay should be performed at increasing molar ratios when working with a new CPPs-siRNA combination. For the experiments shown in this chapter, we used tdTomato1 (UUGGUGUCCACGUAGUAGUAG) and BrafMut (GGTCTAGCTACAGAGAAATCTCGAT) siRNAs.
8. The encapsulation conditions could be different for different peptides. Most peptides spontaneously encapsulate siRNA with no need for mixing or heating, although a vial mixer with thermal control may be needed for variants that have shown a faster reaction and higher encapsulation efficiency when mixing and incubating at 37 °C. The best conditions should be checked in the literature for known CPPs or tested experimentally for novel variants.
9. EDTA will not be completely dissolved until the pH is adjusted.
10. GelRed® Nucleic Acid Stain 10,000× (Biotium) can be replaced with another nucleic acid stain. Although the common EtBr may be suitable for this assay, the purchase of safer reagents provided by several companies is advised.
11. The suggested custom-made loading solution does not include a dye in the formulation since we observed that most dyes would run on top of the siRNA band, reducing the detection efficiency.
12. The nucleic acid ladder can be purchased from several companies and can be DNA- or RNA-based. The ladder should contain fragments in the size range of the chosen siRNA. The use of FastRuler Ultra Low Range DNA Ladder (Thermo Scientific) that contains DNA fragments between 10 bp and 200 bp is advised. This DNA ladder achieves a good resolution of all fragments in a short time with no need to run the fragments until the bottom of the gel.
13. The protocol can also be adapted for a common UV-Vis spectrophotometer by correcting the needed volume of reagents accordingly.
14. Our group can provide a MCF7-tdTomato-positive cell line stably expressing the fluorescent protein. Alternatively, it is possible to generate a tdTomato-positive adherent cell-line of interest by following the method described by Tuttolomondo et al. and Ebbesen et al. .
15. To achieve the best resolution of the DNA fragment ladder, a high agarose gel percentage is recommended. The gel can be prepared using the preferred technique, but using a plate heater or microwave will require longer dissolution time for the agarose than an autoclave. Considering the long dissolution time, adding excess TAE buffer to compensate for the evaporation and to check that the final volume of the gel is correct is advised.
16. Proteinase K will inactivate the RNases contained in the serum and stop the reaction, and concurrently fasten the release of siRNA in combination with DSS by cleaving the peptide.
17. Samples should be centered in the microplate and surrounded by PBS-filled wells to allow equal evaporation of medium from all wells, and at least 3 replicates for each condition is advised.
18. Depending on the instrument, it is possible that increasing the exposure time or changing other machine settings will optimize the reading output.
19. The use of ROI is needed to exclude the signal from artifacts outside the cells. ROIs can also be used to analyze the amount of peptide-siRNA nanocomplex internalized by nuclei or stained vesicles.