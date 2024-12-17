# siRNA Therapeutics for Protein Misfolding Diseases of the Central Nervous System

Mark D. Zabel, Luke Mollnow and Heather Bender

## Abstract

Nanoparticles have been used to deliver siRNA to tissues and cells to silence specific genes in diverse organisms. Research and clinical application of nanoparticles like liposomes for drug delivery requires targeting them to specific anatomic regions or cell types, while avoiding off-target effects or clearance by the liver, kidney, or the immune system. Delivery to the central nervous system (CNS) presents additional challenges to cross the blood–brain barrier (BBB) to specific cell types like neurons, astrocytes, or glia. Here, we describe the generation of three different liposomal siRNA delivery vehicles to the CNS using the thin film hydration method. Utilizing cationic or anionic liposomes protects the siRNA from serum nucleases and proteases en route. To deliver the siRNA specifically to the CNS, the liposomes are complexed to a peptide that acts as a neuronal address by binding to nicotinic acetylcholine receptors (nAchRs). When injected intravenously or instilled intranasally, these liposome-siRNA-peptide complexes (LSPCs) or peptide addressed liposome-encapsulated therapeutic siRNA (PALETS) resist serum degradation, effectively cross the BBB, and deliver siRNA to AchR-expressing cells to suppress protein expression in the CNS.

<span style=color:blue>纳米颗粒已经被广泛应用于将siRNA递送到各种生物体的组织和细胞中，以实现特定基因的沉默。在药物递送领域，像脂质体这样的纳米颗粒的研究和临床应用要求能够靶向特定的解剖区域或细胞类型，同时避免脱靶效应和被肝脏、肾脏或免疫系统清除。特别是递送到中枢神经系统（CNS）面临着额外的挑战，因为需要克服血脑屏障（BBB），并靶向特定的细胞类型，如神经元、星形胶质细胞或胶质细胞。本文描述了使用薄膜水合法生成的三种不同脂质体siRNA递送载体，用于中枢神经系统的递送。这些阳离子或阴离子脂质体能够在递送过程中保护siRNA免受血清中的核酸酶和蛋白酶降解。为了特异性地递送siRNA到中枢神经系统，这些脂质体与一种能够与烟碱型乙酰胆碱受体（nAchRs）结合的肽复合，从而作为神经元的“地址”。当这些脂质体-siRNA-肽复合物（LSPCs）或肽定向脂质体包封的治疗性siRNA（PALETS）通过静脉注射或鼻内给药时，它们能够有效抵抗血清降解，成功穿越血脑屏障，并将siRNA递送到表达AchR的细胞，抑制中枢神经系统中的特定蛋白质表达。</span>

## 1 Introduction 前言

RNA interference (RNAi) is a biological process that diverse organisms use to help regulate the amount of messenger RNA (mRNA) available for translation. Dicer, an endogenous mammalian protein complex that mediates RNAi, cleaves double-stranded or short hairpin RNA (shRNA) into functional, small interfering RNA (siRNA). The RNA-induced silencing complex (RISC) guides siRNA to its complimentary mRNA target, which is then digested by Argonaute, an endonuclease present in the RISC. A concomitant reduction in protein expression ensues. Researchers have begun exploiting RNAi as a tool for silencing specific genes in biological systems. RNAi has shown potential efficacy in treating several diseases including hepatitis, cancer, ocular disorders, chronic pain, and neuropathologies induced by viruses and prions. Initial attempts to use RNAi in the central nervous system (CNS) primarily used intracranial injections of lentiviral vectors encoding shRNA. Lentivirus encoding shRNA against mRNA transcripts have demonstrated decreased expression of the cognate protein, but several aspects of this method limit its efficacy. Inadequate neuroinvasion by lentiviral vectors across the blood–brain barrier (BBB) necessitates their direct delivery to the CNS via stereotactic intracranial injection of shRNA lentivirus directly into the brain. Even then, lentiviral infection and shRNA expression was limited to a small area around the injection site, resulting in spatially limited knockdown of protein expression. This method also lacks desired temporal control of protein expression, since once brain cells are infected with lentivirus, it will likely irreversibly suppress protein expression in these cells. Moreover, despite improvements in lentiviral vector technology and construction, concerns over the oncogenic capacity of lentiviral delivery systems remain.

<span style=color:blue>RNA干扰（RNAi）是一种生物学过程，不同生物通过这种机制调节用于翻译的信使RNA（mRNA）的数量。Dicer是一个内源性蛋白复合物，负责切割双链RNA或短发夹RNA（shRNA），生成功能性的短小干扰RNA（siRNA）。RNA诱导沉默复合物（RISC）将siRNA引导至其互补的mRNA靶标，并通过Argonaute核酸内切酶将其切割，进而降低相关蛋白的表达。研究人员已经开始利用RNAi作为工具，在生物系统中沉默特定的基因。RNAi在治疗多种疾病中展示了潜在的疗效，包括肝炎、癌症、眼科疾病、慢性疼痛以及由病毒和朊病毒引起的神经病变。最初在中枢神经系统（CNS）中应用RNAi时，主要采用了通过颅内注射携带shRNA的慢病毒载体。携带shRNA的慢病毒能够有效减少目标蛋白的表达，但这种方法存在一些限制。由于慢病毒载体难以通过血脑屏障（BBB），它们通常需要通过立体定向颅内注射将shRNA慢病毒直接送入中枢神经系统。即便如此，慢病毒感染和shRNA表达仍然仅限于注射点周围的有限区域，导致蛋白质表达的下调范围非常有限。此外，这种方法也无法实现蛋白质表达的时间控制，因为一旦脑细胞感染了慢病毒，它将不可逆地抑制这些细胞中的蛋白质表达。尽管慢病毒载体技术和构建有了改进，但慢病毒递送系统的致癌性依然是一个值得关注的问题。</span>

Nonviral strategies to deliver siRNA molecules to cells include using cationic peptides capable of crossing plasma membranes. Conjugating siRNA to these cell-penetrating peptides via thiol linkages allows for efficient dissociation of siRNA-peptide complexes by reduction of the disulfide bond in the cytoplasm. While this delivery method holds therapeutic promise, it still does not solve two important problems of drug delivery to the brain: cell specificity and transport of its cargo across the blood–brain barrier (BBB). Kumar et al. developed a transvascular method to deliver siRNA across the BBB specifically to neuronal cells in the brain via intravenous (iv) injection. This method involves complexing siRNA to a short peptide derived from the rabies virus glycoprotein that binds specifically to acetylcholine receptors (AchRs) on neuronal cells. Adding nine d-Arginine residues to the carboxyl terminus of this peptide (RVG-9r) enabled it to electrostatically interact with siRNA and specifically deliver siRNA to neurons in mouse brains to suppress protein expression and protect against fatal viral encephalitis. This significant advance in siRNA delivery to the CNS was tempered by the lack of direct detection of siRNA in the brains of a majority of treated mice, suggesting that these naked complexes may have degraded significantly in the blood during transport. Efficient peptide-mediated delivery of siRNA to the brain after iv injection relies on protecting the complex from serum nuclease and protease degradation and immune activation en route. Alternatively or additionally, accessing more direct routes to the CNS may limit unwanted interception by these processes.

<span style=color:blue>非病毒递送策略中，使用能够穿越细胞膜的阳离子肽是一种常见方法。通过硫醇连接将siRNA与这些细胞穿透肽结合，能够在细胞质中通过还原二硫化物键有效释放siRNA和肽复合物。尽管这种递送方式展现了治疗潜力，但它依然未能解决药物递送到大脑的两个关键问题：细胞特异性和药物穿越血脑屏障（BBB）的运输。Kumar等人开发了一种跨血管递送siRNA的方法，能够通过静脉注射将siRNA特异性地递送到大脑的神经细胞。这一方法通过将siRNA与来自狂犬病毒糖蛋白的短肽结合，后者能够特异性地与神经细胞上的乙酰胆碱受体（AchRs）结合。通过在该肽的羧基末端添加九个d-精氨酸残基（RVG-9r），实现了与siRNA的静电结合，从而特异性地将siRNA递送到小鼠大脑的神经元中，抑制蛋白质的表达，并有效防止致命的病毒性脑炎。尽管这是向中枢神经系统（CNS）递送siRNA的一个重要进展，但大多数小鼠的大脑中未能直接检测到siRNA，表明这些复合物可能在血液运输过程中被显著降解。要实现静脉注射后肽介导的siRNA有效递送到大脑，必须保护复合物免受血清核酸酶和蛋白酶的降解以及免疫系统的激活。或者，通过更直接的路径进入CNS可能有助于减少这些过程对复合物的干扰。</span>

Liposomes are widely used as delivery vehicles for gene therapy products in in vitro assays. They are also being investigated for in vivo use in animal and human models as delivery vehicles for siRNA. Complexing or encapsulating siRNA with liposomes has been shown to protect siRNA from degradation and improve delivery through the vasculature. Cationic liposomes are most commonly used because they electrostatically interact with the negatively charged phosphate backbone of RNA. Cationic liposomes also readily interact with the anionic phosphate head groups of cell membranes. Liposomes will transfer siRNA into cells either through direct fusion to the plasma membrane or through endocytosis. Anionic liposomes are used less frequently because they cannot penetrate the plasma membrane and repel the negative charge of the siRNA backbone. But anionic liposomes are less immunogenic than cationic ones and can effectively package and deliver DNA by first condensing nucleic acid with cations that shield its negative charge. Peptides with affinity for cell-specific receptors covalently or electrostatically bound to liposomes can target liposome-siRNA complexes to specific cell types to avoid off-target effects. Adding polyethylene glycol (PEG) to lipids increases bioavailability and circulation time in blood by decreasing immune clearance. PEGylated liposomes increased delivery of doxorubicin and cisplatin in experimental tumor models and were used in clinical trials to treat a variety of cancers, including AIDS-related Kaposi’s sarcoma and advanced malignant solid tumors, including those found in ovarian and breast cancer. Also, adding PEG groups reduces recognition by serum proteins and uptake of the liposomes by cells of the mononuclear phagocyte system.

<span style=color:blue>脂质体在体外实验中广泛作为基因治疗的递送载体，并且正在动物和人类模型中作为siRNA递送工具进行研究。将siRNA与脂质体复合或封装已经被证明能够保护siRNA免受降解，并改善其通过血管系统的递送。阳离子脂质体因其能够与RNA的负电荷磷酸骨架静电相互作用而最常被使用。此外，阳离子脂质体还能够与细胞膜上负电荷的磷酸头基相互作用。脂质体可以通过与细胞膜的直接融合或通过内吞作用将siRNA递送进入细胞。而阴离子脂质体较少使用，因为它们无法穿透质膜，且会排斥siRNA的负电荷骨架。但阴离子脂质体的免疫原性较低，且可以通过将核酸与阳离子进行凝聚来屏蔽其负电荷，从而有效地包装和递送DNA。通过共价结合或静电结合，将具有细胞特异性受体亲和力的肽与脂质体结合，能够将脂质体-siRNA复合物定向到特定细胞类型，从而避免靶外效应。向脂质体中添加聚乙二醇（PEG）能够减少免疫清除，从而提高其在血液中的生物利用度和循环时间。PEG化脂质体已被用来增加多柔比星和顺铂在肿瘤模型中的递送，并用于临床试验治疗多种癌症，包括艾滋病相关的卡波西肉瘤和晚期的恶性固体肿瘤，如卵巢癌和乳腺癌等。此外，PEG基团的添加还可以减少血清蛋白对脂质体的识别及其在单核吞噬细胞系统中的摄取。</span>

While protecting therapeutic agents from serum degradation represents a crucial step in transvascular delivery to target sites in the brain, liposomes alone do not provide cell specific delivery, nor do they ensure transport across the BBB. Coupling a monoclonal antibody against glial fibrillary acidic protein (GFAP) to PEGylated liposomes successfully targeted them to astrocytes in cell culture, but still failed to deliver them across the BBB to astrocytes in mouse brains. An effective, efficient delivery system must do all three: (1) provide a molecular address to the agent for delivery to neuronal cells, (2) gain access to the brain by crossing the BBB, and (3) protect the agent from serum degradation en route.

<span style=color:blue>虽然保护治疗剂免受血清降解是将其通过血管递送到大脑靶点的关键步骤，但仅使用脂质体无法实现细胞特异性递送，也无法确保其跨越血脑屏障（BBB）。例如，将抗星形胶质纤维酸性蛋白（GFAP）的单克隆抗体与PEG化脂质体结合，可以成功地将脂质体靶向到细胞培养中的星形胶质细胞，但依然未能有效地将脂质体送入小鼠大脑中的星形胶质细胞。一个真正有效且高效的递送系统需要同时满足三个要求：（1）为治疗剂提供分子地址，使其能够定向递送到神经细胞，（2）能够跨越血脑屏障进入大脑，（3）在运输过程中防止治疗剂在血清中降解。</span>

Intranasal instillation of therapeutic drugs targeting the CNS offers a compelling alternative to transvascular delivery. Administering drugs or stem cells into the nasal cavity shortens the route across the BBB to the CNS, further bypassing immune cells more commonly encountered systemically during transit through the vasculature. Mesenchymal stem cells intranasally delivered have been used to treat mouse models of neurodegeneration, including Alzheimer’s and Parkinson’s diseases, perinatal and ischemic brain damage and brain tumors. Combining specific delivery to brain cells with a more direct route to the CNS further refines therapeutic targeting for these and other brain pathologies.

<span style=color:blue>将治疗药物通过鼻腔给药递送到中枢神经系统（CNS）是一种有效的替代方案，相比通过血管递送，这种方法能够更直接地到达大脑。通过鼻腔给药，药物或干细胞可以缩短穿越血脑屏障（BBB）的距离，并且避免了在全身血液循环过程中常遇到的免疫细胞。间充质干细胞通过鼻腔递送已经被用于治疗小鼠神经退行性疾病模型，包括阿尔茨海默病、帕金森病、围产期和缺血性脑损伤以及脑肿瘤。通过将特定的脑细胞递送与更直接的中枢神经系统通道结合，进一步精细化了这些及其他脑部疾病的治疗靶向。</span>

Using siRNA as a therapeutic agent and prion diseases as models, we developed three therapeutic delivery systems via two delivery routes that address the primary issues with current neuropathology treatments. Liposome-siRNA-peptide complexes (LSPCs) are composed of cationic liposomes with siRNA and a targeting peptide (RVG-9r) electrostatically coating the outer surface of the liposome (Fig. 1). RVG-9r is a small modified peptide from the rabies virus glycoprotein that targets nicotinic acetylcholine receptors in the CNS to reduce siRNA off-target effects. Peptide addressed liposome encapsulated therapeutic siRNA (PALETS) are composed of either cationic or anionic liposomes with siRNA encapsulated inside the liposome, and RVG-9r either electrostatically or covalently bonded to lipid PEG groups. However, depending on the researcher’s preferences, the siRNA can also be electrostatically bound on the outside of the liposome.

<span style=color:blue>我们以朊病毒病为模型，使用siRNA作为治疗药物，开发了三种治疗递送系统，并通过两种递送途径解决了当前神经病理学治疗中的主要问题。脂质体-siRNA-肽复合物（LSPCs）由阳离子脂质体、siRNA和靶向肽（RVG-9r）组成，后者通过静电作用附着在脂质体的外表面（如图1所示）。RVG-9r是从狂犬病毒糖蛋白中改造的小肽，能够靶向中枢神经系统中的烟碱型乙酰胆碱受体，从而减少siRNA的离靶效应。肽靶向脂质体封装治疗性siRNA（PALETS）由阳离子或阴离子脂质体组成，siRNA封装在脂质体内，而RVG-9r则通过静电或共价方式与脂质体上的PEG基团连接。然而，根据研究人员的选择，siRNA也可以静电结合在脂质体的外表面。</span>

![485053_1_En_20_Fig1_HTML](https://raw.githubusercontent.com/zcgkiller/Pictures/main/Wechat/485053_1_En_20_Fig1_HTML.png)

**Fig. 1** Schematic representation of (**a**) LSPCs and (**b**) PALETS

For anionic PALETS , we use the cation protamine sulfate to neutralize the negative charge of and condense the siRNA to facilitate encapsulation within anionic liposomes. We also compared intravenous injection vs. intranasal instillation for delivery efficiency, therapeutic efficacy, and immune stimulation. LSPCs and PALETS decrease surface PrPC up to 70% in neuronal cells, and PALETS result in a decrease of the total number of PrPC expressing cells. Intranasal instillation doubled the response rate (60 vs. 33%) and halved the seroconversion rate (40 vs. 78%) compared to IV injection.

<span style=color:blue>在阴离子PALETS中，我们使用阳离子原白蛋白硫酸盐来中和siRNA的负电荷，并将其凝聚以促进其在阴离子脂质体中的封装。我们还比较了静脉注射与鼻腔滴注在递送效率、治疗效果和免疫刺激方面的不同。LSPCs和PALETS能够使神经元细胞表面PrPC减少最多70%，而PALETS还会导致PrPC表达细胞的总数减少。与静脉注射相比，鼻腔滴注的反应率提高了两倍（60%比33%），而血清转化率减少了一半（40%比78%）。</span>

## 2 Materials 材料

### 2.1 LSPC and PALETS Reagents, Supplies, and Equipment LSPC 和 PALETS 试剂、耗材和设备

1. siRNA : Design siRNA using siRNA scales or similar siRNA design software and synthesize, pre-anneal, and lyophilize (*see* **Note** **1**). Resuspend in sterile RNAse-free water to 40 μM according to manufacturer’s directions. Store in single-use aliquots at −70 °C (*see* **Note** **2**).<span style=color:blue>**siRNA**: 使用siRNA设计软件或类似的工具设计siRNA，并合成、预先退火并冻干（*参见* **备注** **1**）。根据生产商的指示，将其溶解在无RNA酶水中，浓度为40 μM。将其分装为单次使用的样品并储存于−70°C（*参见* **备注** **2**）。</span>

2. Peptides: RVG-9r and control RVM-9r peptides (Table 1) were synthesized and purified by high-performance liquid chromatography by ChemPeptide. Resuspend in sterile phosphate-buffered saline (PBS), pH 7.4 to 400 μM, or approximately 2 mg/mL. For example, resuspend 100 mg of peptide in 50 mL PBS. Store at −70 °C in single-use aliquots (typically 400 μL, *see* **Note** **2**).<span style=color:blue>**肽类**: RVG-9r和对照肽RVM-9r（见表1）由ChemPeptide合成并通过高效液相色谱法纯化。将其溶解在无菌磷酸盐缓冲盐水（PBS），pH 7.4，浓度为400 μM或约2 mg/mL。例如，将100 mg肽溶解在50 mL PBS中。将其分装为单次使用的样品（通常为400 μL），并储存于−70°C（*参见* **备注** **2**）。</span>

3. 10% Sterile sucrose: Weigh 1 g of sucrose and mix into 9 mL of sterile deionized water, pH 7.0.<span style=color:blue>**10%无菌蔗糖**: 称取1 g蔗糖并混入9 mL无菌去离子水中，pH 7.0。</span>

4. Liposomes : Lipids required to construct PALETS include N-[1-(2,3-Dioleoyloxy)propyl]-N,N,N trimethylammonium chloride (DOTAP), 1,2-Distearoyl-sn-glycero-3-phosphoethanolamine (DSPE), and DSPE-.polyethylene glycol 2000 (DSPE-PEG). Cholesterol, chloroform, and methanol are required to mix and assemble liposomes. Use nitrogen gas (N2) to evaporate lipid solvents. Store lipids at −70 °C.<span style=color:blue>**脂质体**: 构建PALETS所需的脂质包括N-[1-(2,3-二油氧基)丙基]-N,N,N-三甲基氯化铵（DOTAP），1,2-二硬脂酰-sn-甘油-3-磷酸乙醇胺（DSPE），以及DSPE-聚乙二醇2000（DSPE-PEG）。需要胆固醇、氯仿和甲醇用于混合和组装脂质体。使用氮气（N2）蒸发脂质溶剂。脂质应储存在−70°C。</span>

5. A horn sonicator that accommodates individual 0.6 mL, 1.0 mL, or 2.0 mL microcentrifuge tubes or a 48- or 96-well plate.<span style=color:blue>**超声波破碎仪**：用于容纳单独0.6 mL、1.0 mL或2.0 mL的微量离心管或48孔、96孔板。</span>

6. An extruder to create uniformly sized liposomes (1, 0.45, or 0.2 μm).<span style=color:blue>**挤出器**：用于制造均匀尺寸的脂质体（1、0.45或0.2 μm）。</span>

7. 15 mL glass flasks to mix and lyophilize lipids and 1–5 mL glass vials to rehydrate and store liposomes.<span style=color:blue>**15 mL玻璃烧瓶**：用于混合和冻干脂质，以及1–5 mL玻璃小瓶用于再水化和储存脂质体。</span>

8. Sterile 1× phosphate-buffered saline (PBS), pH 7.4.<span style=color:blue>**无菌1×磷酸盐缓冲盐水（PBS），pH 7.4**。</span>

9. Fluorochrome labeling kit for LSPC detection. We recommend far-red dyes like DyLight 649 or Alexa 647 to avoid confounding autofluorescence.<span style=color:blue>**LSPC检测的荧光染料标记试剂盒**：推荐使用远红色染料如DyLight 649或Alexa 647，以避免自发荧光的干扰。</span>

10. 3 Kd molecular weight cutoff centrifugal filter<span style=color:blue>**3 KDa分子量截断离心滤器**。</span>

**Table 1** Delivery peptide sequences

| RVG-9r<sup>a</sup> | YTIWMPENPRPGTPCDIFTNSRGKRASNGGGGrrrrrrrrr |
| ------------------ | ----------------------------------------- |
| RVM-9r<sup>b</sup> | MNLLRKIVKNRRDEDTQKSSPASAPLDGGGGrrrrrrrrr  |

<sup>a</sup> Lower case r denotes d-Arginine racemer

<sup>b</sup> Control

### 2.2 LSPC Delivery Supplies LSPC 给药所需耗材

1. Mice: Choose mouse lines and strains appropriate for the experimental design. Various strains of wild-type mice can be purchased from Charles River or Jackson labs (*see* **Note** **3**).<span style=color:blue>**小鼠**: 选择适合实验设计的小鼠品系。可以从Charles River或Jackson实验室购买各种野生型小鼠品系（*参见* **备注** **3**）。</span>

2. 26–30 Gauge insulin syringes.<span style=color:blue>**26–30号胰岛素注射器**。</span>

3. Heat lamp.<span style=color:blue>**加热灯**。</span>

4. Rodent anesthesia machine dispensing Isofluorane (*see* **Note** **4**).<span style=color:blue>**啮齿动物麻醉机，分配异氟烷**（*参见* **备注** **4**）。</span>

5. Sterile gauze.<span style=color:blue>**无菌纱布**。</span>

6. Hyaluronidase.<span style=color:blue>**透明质酸酶**。</span>

7. Live, whole animal imaging system.<span style=color:blue>**活体动物成像系统**。</span>

8. 45 μm Nylon mesh filters<span style=color:blue>**45 μm尼龙网状过滤器**。</span>

9. Flow Cytometer.<span style=color:blue>**流式细胞仪**。</span>

10. Droplet Digital or other quantitative PCR machine.<span style=color:blue>**滴度数字或其他定量PCR仪**。</span>

11. Optimal Cutting Temperature (OCT) or similar tissue freezing and embedding media.<span style=color:blue>**最佳切割温度（OCT）或类似组织冷冻嵌入介质**。</span>

12. Cryostat machine for sectioning tissues.<span style=color:blue>**冷冻切片机**。</span>

13. Liquid nitrogen.<span style=color:blue>**液氮**。</span>

14. Ice-cold acetone.<span style=color:blue>**冰冷的丙酮**。</span>

15. Fluorescent antibodies and 4′,6-diamidino-2-phenylindole (DAPI), Hoechst or other nuclear dye to stain tissues.<span style=color:blue>**荧光抗体和4′,6-二氨基-2-苯基吲哚（DAPI）、Hoechst或其他核染料用于组织染色**。</span>

16. Fluorescent mounting media , glass slides, and cover slips.<span style=color:blue>**荧光封片介质、玻璃载玻片和盖玻片**。</span>

17. Fluorescent microscope.<span style=color:blue>**荧光显微镜**。</span>


## 3 Methods 方法

### 3.1 Preparing Liposomes 制备脂质体

#### 3.1.1 DOTAP LSPCs

1. Prepare cationic LSPCs by mixing N-[1-(2,3-Dioleoyloxy)propyl]-N,N,N trimethylammonium chloride and cholesterol at 1:1 molar ratio in a 1:1 chloroform:methanol (C:M) solution. Weigh and mix 20 μmoles of cholesterol and 20 μmoles of DOTAP to a final concentration of 8 mM (a total of 40 μmole) C:M solution in a round-bottom, 15-mL glass flask.<span style=color:blue>**制备阳离子LSPCs**：将N-[1-(2,3-二油氧基)丙基]-N,N,N-三甲基氯化铵（DOTAP）和胆固醇以1:1的摩尔比混合，在1:1的氯仿:甲醇（C:M）溶液中。称取20微摩尔的胆固醇和20微摩尔的DOTAP，最终浓度为8 mM（总共40微摩尔）。将其溶解在15 mL的圆底玻璃烧瓶中，加入C:M溶液。</span>

2. Evaporate the C:M solvent using N2 gas. Remove any excess solvent by placing the tube in a vacuum desiccator and drying overnight to a thin film (*see* **Note** **5**).<span style=color:blue>**蒸发溶剂**：使用氮气（N2）蒸发C:M溶剂。将玻璃烧瓶放入真空干燥器中，放置过夜以去除多余溶剂，形成薄膜（*参见* **备注** **5**）。</span>

3. Rehydrate liposomes to a final stock concentration of 8 μM in sterile 10% sucrose. Keep the thin lipid film and the 10% sucrose at 55 °C throughout the rehydration procedure. Add 1 mL of 10% sucrose every 10 min and swirl the lipid solution every 3 min for a total of 5 mL across 50 min.<span style=color:blue>**重新水化脂质体**：将脂质体溶液重新水化至最终浓度为8 μM，使用无菌10%蔗糖溶液。保持薄脂质膜和10%蔗糖溶液在55°C下进行重新水化过程。每10分钟加入1 mL的10%蔗糖溶液，并每3分钟轻轻搅拌一次，持续50分钟，直到总量达到5 mL。</span>

4. Size either through an extruder using 1, 0.45, and 0.2 μm pore filters or sonication .<span style=color:blue>**粒度大小化**：使用1、0.45和0.2 μm的孔径滤膜通过挤出法或超声处理法进行粒度大小化。</span>

5. Store at 4 °C in glass vials for several months.<span style=color:blue>**存储**：将脂质体储存在4°C的玻璃瓶中，可保存数月。</span>


#### 3.1.2 DOTAP PALETS

1. Prepare cationic PALETS by mixing DOTAP, cholesterol, and DSPE-PEG at a 55:40:5 molar ratio in a 1:1 C:M solution. Weigh out 22 μmoles of DOTAP, 16 μmoles of cholesterol, and 2 μmoles of DSPE-PEG to a final concentration of 8 mM (total of 40 μmole) C:M solution in a round-bottom, 15-mL glass flask.<span style=color:blue>**制备阳离子PALETS**：将DOTAP、胆固醇和DSPE-PEG以55:40:5的摩尔比混合，使用1:1的C:M溶液。称取22微摩尔的DOTAP、16微摩尔的胆固醇和2微摩尔的DSPE-PEG，最终浓度为8 mM（总共40微摩尔）。将其溶解在15 mL的圆底玻璃烧瓶中，加入C:M溶液。</span>

2. Evaporate the solvent using the same above procedure as DOTAP LSPCs.<span style=color:blue>**蒸发溶剂**：按照DOTAP LSPCs的上述方法蒸发溶剂。</span>

3. Rehydrate DOTAP PALETS using 5 mL of sterile (*see* **Note** **6**) 1× PBS. Keep both the PBS and the lipid solutions above 65 °C (*see* **Note** **7**) while rehydrating. Add 1 mL of 1× PBS every 10 min for a total of 5 mL across 50 min. Swirl the solution every 3 min. <span style=color:blue>**重新水化DOTAP PALETS**：使用5 mL的无菌1×PBS进行水化（*参见* **备注** **6**）。在水化过程中，保持PBS和脂质溶液的温度都高于65°C（*参见* **备注** **7**）。每10分钟加入1 mL的1×PBS，直到总量达到5 mL，持续50分钟。每3分钟轻轻搅拌一次。</span>

4. Size using the procedure described in Subheading 3.1.1. <span style=color:blue>**粒度大小化**：按照第3.1.1节的方法进行粒度大小化。</span>

5. Store at 4 °C for several months. <span style=color:blue>**存储**：将脂质体储存在4°C的玻璃瓶中，可保存数月。</span>


#### 3.1.3 DSPE PALETS

1. To prepare DSPE PALETS , use the same above procedure as DOTAP PALETS. Use a 55:40:5 molar ratio (*see* **Note** **8**) of DSPE:cholesterol:DSPE-PEG lipids in a 1:1 C:M solution by weighing out 22 μmoles of DSPE, 16 μmoles of cholesterol, and 2 μmoles of DSPE-PEG to a final concentration of 8 mM (total of 40 μmoles). <span style=color:blue>**制备DSPE PALETS**：使用与DOTAP PALETS相同的方法。将DSPE、胆固醇和DSPE-PEG以55:40:5的摩尔比混合，使用1:1的C:M溶液。称取22微摩尔的DSPE、16微摩尔的胆固醇和2微摩尔的DSPE-PEG，最终浓度为8 mM（总共40微摩尔）。</span>

2. Perform solvent evaporation, rehydration, and sizing as described for the DOTAP PALETS procedure (*see* Subheading 3.1.2).<span style=color:blue>**蒸发溶剂**、**重新水化**和**粒度大小化**：按照DOTAP PALETS的步骤进行操作（*参见* 第3.1.2节）。</span>


### 3.2 Resuspending Liposomes 重悬脂质体

1. Before use, dilute liposomes (LSPCs and PALETS) 1:100 in sterile 1× PBS. For example, briefly mix stock liposomes by inverting the tube and add 2 μL of liposomes to 198 μL of sterile 1× PBS. Mix by pipetting and put 80 μL of diluted liposome solution into screw cap microcentrifuge tubes.<span style=color:blue>**重悬脂质体**：使用前，将脂质体（LSPCs和PALETS）以1:100的比例稀释在无菌1×PBS中。例如，将脂质体存储液轻轻倒置混匀后，取2 μL的脂质体溶液，加入198 μL的无菌1×PBS中，混合均匀后，将80 μL稀释后的脂质体溶液转移至螺旋瓶微量离心管中。</span>

2. Place into the tube holder of the sonicator. Sonicate liposomes for 40 s at 20% power (*see* **Note** **9**).<span style=color:blue>**超声处理**：将微量离心管放入超声仪的管架中，以20%的功率进行40秒的超声处理（*参见* **备注** **9**）。</span>


The liposomes can be used immediately or stored for several weeks in glass vials at 4 °C (*see* **Note** **10**).<span style=color:blue>脂质体可以立即使用，或在4°C的玻璃瓶中储存数周（*参见* **备注** **10**）。</span>

### 3.3 Preparing LSPCs and PALETS 制备LSPCs和PALETS

Complex siRNA, liposomes, and peptides using filter barrier tips and sterile technique in a cell culture hood. The following preparation will produce enough LSPCs/PALETS to treat one mouse.<span style=color:blue>使用滤芯屏障移液管和无菌操作，在细胞培养工作台中将siRNA、脂质体和肽复合。以下制备方法可产生足够的LSPCs/PALETS以用于治疗一只小鼠。</span>

#### 3.3.1 LSPCs

1. Thaw 100 μL of stock siRNA and 80 μL stock peptide on ice.<span style=color:blue>**解冻siRNA和肽**：将100 μL的siRNA存储液和80 μL的肽存储液在冰上解冻。</span>

2. Add 50 μL of the diluted and sonicated liposomes (sonicate first if necessary, *see* **Note** **9**) to 100 μL of 20 μM siRNA and mix gently by pipetting.<span style=color:blue>**加入脂质体和siRNA**：将50 μL的稀释并经过超声处理的脂质体（如有需要，先进行超声处理，*参见* **备注** **9**）加入到100 μL的20 μM siRNA溶液中，轻轻吸管混合。</span>

3. Incubate at 4 °C for 10 min (Fig. 1).<span style=color:blue>**孵育**：将混合液在4°C下孵育10分钟（见图1）。</span>

4. Add 80 μL of peptide, mix gently by pipetting and incubate at 4 °C for 10 min (*see* **Note** **11**).<span style=color:blue>**加入肽**：将80 μL肽溶液加入混合物中，轻轻吸管混合，并在4°C下孵育10分钟（*参见* **备注** **11**）。</span>


#### 3.3.2 DOTAP PALETS

1. Thaw 100 μL of stock siRNA and 80 μL stock peptide on ice.<span style=color:blue>**解冻siRNA和肽**：将100 μL的siRNA存储液和80 μL的肽存储液在冰上解冻。</span>

2. Lyophilize 50 μL of diluted DOTAP PALETS liposomes in a glass vial using a benchtop lyophilizer for 15 min.<span style=color:blue>**冻干脂质体**：将50 μL的稀释DOTAP PALETS脂质体溶液在玻璃瓶中使用台式冻干机冻干15分钟。</span>

3. Add 100 μL of stock siRNA to the lyophilized single-use aliquot of liposome to encapsulate the siRNA within the liposome. Incubate for 5 min.<span style=color:blue>**封装siRNA**：将100 μL的siRNA存储液加入冻干的脂质体单次使用分装液中，使siRNA封装在脂质体内，孵育5分钟。</span>

4. Optional: Covalently link RVG-9r to DSPE-PEG groups (*see* **Note** **12**). Add 10 μL of a 60 mM 1-ethyl-3-(3-dimethylaminopropyl)carbodiimide hydrochloride (EDC) solution to the liposome/siRNA solution. Add 10 μL of a 150 mM N-hydroxysulfosuccinimide (sulfo-NHS) solution to the liposome/siRNA solution. Incubate the EDC/sulfo-NHS liposome/siRNA solution for 10 min.<span style=color:blue>**选择性共价连接RVG-9r肽**：可选步骤：按照以下方案将RVG-9r肽与DSPE-PEG基团共价连接（*参见* **备注** **12**）。向脂质体/siRNA溶液中加入10 μL的60 mM 1-乙基-3-(3-二甲氨基丙基)氯化碳二亚胺（EDC）溶液，再加入10 μL的150 mM N-羟基磺基琥珀酰亚胺（sulfo-NHS）溶液。将EDC/sulfo-NHS脂质体/siRNA溶液孵育10分钟。</span>

5. Add 80 μL of stock RVG-9r and incubate for either 10 min if not covalently modifying or for 2 h if covalently linking to PEG groups.<span style=color:blue>**加入RVG-9r肽**：将80 μL的RVG-9r肽存储液加入，若不进行共价修饰则孵育10分钟；若要与PEG基团共价连接，则孵育2小时。</span>


#### 3.3.3 DSPE PALETS

1. Thaw 100 μL of stock siRNA and 80 μL of stock peptide on ice.<span style=color:blue>**解冻siRNA和肽**：将100 μL的siRNA存储液和80 μL的肽存储液在冰上解冻。</span>

2. Lyophilize 50 μL of diluted DSPE PALETS liposomes in a glass vial using a benchtop lyophilizer for 15 min.<span style=color:blue>**冻干脂质体**：将50 μL的稀释DSPE PALETS脂质体溶液在玻璃瓶中使用台式冻干机冻干15分钟。</span>

3. Incubate 100 μL of stock siRNA solution with 1.4 μL of a 26.6 μM solution of protamine sulfate (*see* **Note** **13**) for 10 min at room temperature.<span style=color:blue>**制备siRNA与protamine复合物**：将100 μL的siRNA溶液与1.4 μL的26.6 μM protamine sulfate溶液（*参见* **备注** **13**）在室温下孵育10分钟。</span>

4. Add the siRNA/protamine to the single-use aliquot of lyophilized DSPE PALETS liposomes. Incubate for 10 min at 4 °C.<span style=color:blue>**加入siRNA/protamine混合物**：将siRNA/protamine混合物加入冻干的DSPE PALETS脂质体单次使用分装液中，4°C下孵育10分钟。</span>

5. Add 80 μL of stock RVG-9r and incubate for 10 min on ice.<span style=color:blue>**加入RVG-9r肽**：将80 μL的RVG-9r肽存储液加入，冰上孵育10分钟。</span>

6. Optional: Covalently link the RVG-9r to the DSPE PEG liposomes using the above protocol in Subheading 3.1.2 (*see* **Note** **12**).<span style=color:blue>**选择性共价连接RVG-9r肽**：可选步骤：按照第3.1.2节的方案，将RVG-9r与DSPE-PEG脂质体共价连接（*参见* **备注** **12**）。</span>


### 3.4 Injecting LSPCs or PALETS 注射LSPCs或PALETS

1. Warm mice in their cage by placing it four to six inches below a heat lamp for 5–10 min (*see* **Note** **14**).<span style=color:blue>**加温小鼠**：将小鼠放置在笼子中，并将笼子放置在距离热灯约4–6英寸的位置，持续加热5-10分钟（*参见* **备注** **14**）。</span>

2. While warming the mice, turn on the anesthesia machine such that oxygen flows at a rate of 3–4 L/min. Turn on the isoflurane at 3 L/min.<span style=color:blue>**准备麻醉**：在加温过程中，开启麻醉机，设置氧气流量为3–4 L/min，氟烷流量设置为3 L/min。</span>

3. Place mice in anesthesia chamber until mice lose consciousness.<span style=color:blue>**麻醉小鼠**：将小鼠放入麻醉室，直到小鼠失去意识。</span>

4. When the tail vasculature is clearly visible, place a single mouse in the anesthesia chamber until its respiration visibly slows to 1–2 breaths per second (*see* **Note** **15**).<span style=color:blue>**观察尾部血管**：当尾部血管清晰可见时，将小鼠放回麻醉室，直到小鼠呼吸频率明显减慢至1–2次/秒（*参见* **备注** **15**）。</span>

5. Meanwhile, load ~250 μL of LSPCs into a sterile insulin syringe (*see* **Note** **16**).<span style=color:blue>**装载脂质体溶液**：此时，将约250 μL的LSPCs或PALETS溶液装入无菌胰岛素注射器中（*参见* **备注** **16**）。</span>

6. Place the mouse on a flat surface with its face in the nose cone attached to the anesthesia machine (*see* **Note** **17**).<span style=color:blue>**固定小鼠位置**：将小鼠放置在平坦的表面上，面部放置在麻醉机的鼻罩中（*参见* **备注** **17**）。</span>

7. Starting with the mouse laying on its ventral side (dorsal side up), locate one of the two lateral veins . Starting as far posterior as possible, rotate the tail slightly and insert the needle with the bevel up at a shallow 10–15° angle 1–2 mm into the vein. Slowly press the plunger to inject the LSPC or PALETS solution (*see* **Note** **18**).<span style=color:blue>**注射脂质体溶液**：从小鼠腹侧开始（背面朝上），定位尾部的两条侧血管。尽可能从尾部远端开始，稍微旋转尾巴，将针头以10–15°的浅角度插入血管，针尖朝上，深度为1–2毫米。缓慢按压活塞注射LSPC或PALETS溶液（*参见* **备注** **18**）。</span>


### 3.5 Instilling LSPCs or PALETS 鼻内灌注LSPCs或PALETS

1. Place mice in anesthesia chamber and turn on the anesthesia machine such that oxygen flows at a rate of 3–4 L/min until mice lose consciousness.<span style=color:blue>**麻醉小鼠**：将小鼠放入麻醉室，并开启麻醉机，设置氧气流量为3–4 L/min，直到小鼠失去意识。</span>

2. Instill 100 U of Hyaluronidase in 30 μL PBS into each naris of the nose. Wait 30 min, then re-anesthetize the mice (*see* **Note**  **19**).<span style=color:blue>**鼻内灌注透明质酸酶**：向每只小鼠的两个鼻孔内分别灌注30 μL PBS中含有100单位的透明质酸酶，等待30分钟后重新麻醉小鼠（*参见* **备注** **19**）。</span>

3. Place ~1 cm diameter of sterile gauze into the caudal oropharynx.<span style=color:blue>**准备无菌纱布**：将约1厘米直径的无菌纱布放置在小鼠口咽部的后端。</span>

4. Instill up to 100 μL of LSPCs or PALETS into each naris, sealing the pipette tip against the nasal cavity and applying modest pressure to drive the LSPCs or PALETS across the cribriform plate.<span style=color:blue>**灌注LSPCs或PALETS**：向每只小鼠的鼻孔内灌注最多100 μL的LSPCs或PALETS，将移液管尖端封住鼻腔，并施加适度压力将LSPCs或PALETS推动过筛板。</span>


### 3.6 Monitoring LSPC and PALET Trafficking 监测LSPC和PALET运输

1. To monitor LSPC trafficking and determine delivery kinetics, label peptides with DyLight 649 or similar fluorochrome (Alexa dyes, for example) according to manufacturer’s directions.<span style=color:blue>**标记肽**：为了监测LSPC的运输并确定递送动力学，可以使用DyLight 649或类似的荧光染料（例如Alexa染料）对肽进行标记，按照制造商的说明操作。</span>

2. Use a 3 Kd molecular weight cutoff centrifugal filter to exchange labeling buffer for storage buffer (10 mg/mL bovine serum albumin in sterile PBS).<span style=color:blue>**交换缓冲液**：使用3 Kd分子量切割离心滤器将标记缓冲液更换为储存缓冲液（10 mg/mL的牛血清白蛋白在无菌PBS中）。</span>


#### 3.6.1 Monitoring LSPCs and PALETS in Live Mice 监测LSPCs和PALETS在活体小鼠中的表现

1. Inject or instill fluorochrome-labeled LSPCs or PALETS in live mice.<span style=color:blue>**注射或灌注标记LSPCs或PALETS**：将标记了荧光染料的LSPCs或PALETS注射或灌注到活体小鼠中。</span>

2. Visualize fluorochrome-labeled LSPCs or fluorochrome-labeled PALETS using a live animal imager. <span style=color:blue>**活体成像**：使用活体动物成像仪可视化标记了荧光染料的LSPCs或PALETS。</span>


#### 3.6.2 Visualizing LSPCS and PALETS in the CNS CNS中可视化LSPCs和PALETS

1. LSPC localization can be observed in the CNS by fluorescent microscopy. Euthanize injected mice and remove and snap-freeze their brains in OCT in liquid nitrogen.<span style=color:blue>**大脑定位观察**：通过荧光显微镜可以观察LSPC在CNS中的定位。安乐死注射的小鼠，取出其大脑并在液氮中快速冷冻。</span>

2. Using a cryostat cooled to −20 °C, cut 8 μm-thick brain sections and mount them on glass slides.<span style=color:blue>**切片和封片**：使用冷冻切片机将大脑切成8 μm厚的切片，并将切片安装在玻璃载玻片上。</span>

3. Fix in ice-cold acetone for 10 min and air dry overnight. Slides can be stained with additional markers (the protein knockdown target, for example) or DAPI before mounting in anti-fade mounting media.<span style=color:blue>**固定和染色**：将切片浸泡在冰冷的丙酮中10分钟，然后在空气中晾干过夜。切片可用其他标记物（例如蛋白质敲降靶标）或DAPI染色，然后用抗褪色封片介质封片。</span>

4. isualize LSPCs in brain sections using a microscope capable of detecting the fluorochromes used (Fig. 2a-t).<span style=color:blue>**显微观察**：使用能够检测所用荧光染料的显微镜可视化LSPCs在大脑切片中的分布（见图2a-t）。</span>


![485053_1_En_20_Fig2_HTML](https://raw.githubusercontent.com/zcgkiller/Pictures/main/Wechat/485053_1_En_20_Fig2_HTML.png)

**Fig. 2** LSPC delivery to PrPC-expressing cells in vivo (11). FVB mice were intravenously injected with liposomes alone (panels **a–e**) or LSPCs containing DyLight 488-labeled peptides and Alexa 488-labeled siRNAs as follows: PrP siRNA-control RVM-9r (**f–j**), Control siRNA -RVG-9r (K-O), or PrP siRNA-RVG-9r (**p–t**). Mice were sacrificed 24 h later, dissected, and their brains snap frozen and 8 μm sections thereof stained with DyLight 649-labeled anti-PrP antibody (**a**, **f**, **k,** and **p**) and DAPI (**c**, **h**, **m**, and **r**) and visualized by fluorescence microscopy. Panels **e**, **j**, **o**, and **t** depict magnifications of the boxed areas in panels **d**, **i**, **n**, and **s**. Inset in panel **p** depicts a serial section stained with an irrelevant isotype control antibody. Scale bars, 50 μm

#### 3.6.3 Quantifying LSPC and PALETS Delivery 定量LSPC和PALETS递送

Quantitative analysis of LSPC delivery can be performed on brain and kidney cells isolated from injected mice by flow cytometry and digital droplet PCR.<span style=color:blue>可以通过流式细胞术和数字滴度PCR对注射小鼠的脑和肾细胞进行定量分析。</span>

1. Sacrifice mice and remove their brains and kidneys.<span style=color:blue>**取样**：安乐死小鼠并取出其大脑和肾脏。</span>

2. Strain the organs through a 45 μm nylon mesh to produce a single cell suspension for flow cytometry.<span style=color:blue>**制备单细胞悬液**：将脏器通过45 μm尼龙滤网过滤，获得单细胞悬液用于流式细胞术分析。</span>

3. Stain cells for 30–60 min with additional cell markers of interest (the protein knockdown target) and 1 μg/mL DAPI for 10 min and analyze by flow cytometry according to protocols specific for the PCR machine used (*see* **Note** **20** and Fig. 3).<span style=color:blue>**细胞标记**：使用感兴趣的附加细胞标记物（例如蛋白质敲降靶标）以及1 μg/mL的DAPI在细胞中染色30-60分钟，然后根据所用PCR机器的特定协议进行流式细胞术分析（*参见* **备注** **20** 和图3）。</span>


![485053_1_En_20_Fig3_HTML](https://raw.githubusercontent.com/zcgkiller/Pictures/main/Wechat/485053_1_En_20_Fig3_HTML.png)

**Fig. 3** LSPCs target the majority of neuronal cells and deliver PrPC siRNA to the brain when injected intravenously. (**a**) Flow cytometry of primary neuronal cells labeled with BAR-224, an anti-PrPC antibody, and RVG-9r reveals that 98% of cells in the brain display PrPC and nAchRs on their surfaces. Ninety-six percent of those cells express both PrPC and nAchRs. A smaller proportion of kidney cells (78%) express both PrPC and nAchRs. (**b**) In vivo live imaging revealed that RVG-9r increased LSPC delivery to the brain 2 min to 10 days after intravascular injection compared to siRNA and peptide complexes without liposomes (SPCs). We controlled for background fluorescence using PBS-injected mice. (**c**) Flow cytometry analysis 24 h after fluorescent LSPC injection revealed siRNA delivery to 47% of brain cells and 15% of kidney cells (black histograms) compared to PBS-injected controls (gray histograms). Data are representative of at least seven independent experiments

#### 3.6.4 Quantifying siRNA Knockdown 定量siRNA敲降效果

1. Isolate RNA from cells using an mRNA isolation kit.<span style=color:blue>**提取RNA**：使用mRNA提取试剂盒从细胞中提取RNA。</span>

2. Analyze 1–100 ng of cDNA obtained from the RNA RT-PCR using a digital droplet PCR system according to protocols specific for the PCR machine used (*see* **Note** **21**).<span style=color:blue>**RT-PCR分析**：使用数字滴度PCR系统，根据所用PCR机器的特定协议分析从RNA反转录得到的1–100 ng的cDNA（*参见* **备注** **21**）。</span>

3. Analyze protein expression by Flow Cytometry according to protocols specific for the PCR machine used (*see* **Note** **21**).<span style=color:blue>**蛋白质表达分析**：通过流式细胞术分析蛋白质表达，按照PCR机器特定的协议进行分析（*参见* **备注** **21**）。</span>


## 4 Notes

1. We have used siRNA prepared for us by several biotechnology companies, but have observed optimal knockdown using siRNA prepared from Qiagen. Additionally, Qiagen can label siRNA with Alexa fluorochromes to monitor LSPC trafficking for determining delivery kinetics (*see* **Note** **15**).<span style=color:blue>**siRNA来源**：我们曾使用多家生物技术公司提供的siRNA，但发现使用Qiagen公司提供的siRNA能够实现最佳的基因敲降效果。此外，Qiagen还可以为siRNA标记Alexa荧光染料，以监测LSPC的运输过程，从而确定递送动力学（*参见* **备注** **15**）。</span>

2. We typically treat cages of five mice at a time and therefore aliquot 1 mL of 200 μM stock siRNA, enough to treat five mice. Aliquots should be adjusted to meet researchers’ experimental requirements.<span style=color:blue>**siRNA分配**：我们通常一次处理5只小鼠，因此将1 mL的200 μM siRNA储备液分装，足够用于处理5只小鼠。分装量应根据研究者的实验需求进行调整。</span>

3. White mice (FVB, C3H, CD-1, for example) tend to be much easier to inject intravenously in the tail than brown or black mice (129sv, C57/Bl6).<span style=color:blue>**小鼠品种选择**：白色小鼠（例如FVB、C3H、CD-1）通常比棕色或黑色小鼠（例如129sv、C57/Bl6）更容易进行尾静脉注射。</span>

4. The machine should have an incubating chamber and a nose cone. We recommend isoflurane, but alternative anesthesia, such as ketamine, can be used. While tail vein injections can be done using physical restraint, we strongly recommend using chemical restraint to avoid sudden movements from the mouse that can compromise the injection and waste valuable time and reagents.<span style=color:blue>**麻醉设备要求**：麻醉机应具有孵育舱和鼻罩。我们推荐使用氟烷麻醉，但也可以使用其他麻醉剂，如酮胺。虽然尾静脉注射可以通过物理约束完成，但我们强烈建议使用化学麻醉，以避免小鼠突然的运动影响注射操作，并浪费宝贵的时间和试剂。</span>

5. Desiccation time may vary. Most importantly, the lipids must be completely dry. For faster desiccation, the solution can be split into several tubes.<span style=color:blue>**干燥时间**：干燥时间可能有所不同。最重要的是脂质必须完全干燥。为了加快干燥过程，可以将溶液分装到多个管中。</span>

6. Rehydration medium depends on lipid composition and experimental requirements. Lipid mixtures with anionic lipids, such as DSPE-PEG, have improved rehydration with the addition of a salt buffer, such as PBS. If injecting either LSPCs or PALETS in vivo, a biologically safe hydration solution needs to be chosen.<span style=color:blue>**再水化介质**：再水化介质应根据脂质组成和实验需求选择。含有阴离子脂质（如DSPE-PEG）的脂质混合物，在加入盐缓冲液（如PBS）后，其再水化效果有所改善。如果在体内注射LSPCs或PALETS，则需要选择生物安全的水合溶液。</span>

7. It may be possible to use different cationic and anionic lipids in these formulations depending on researchers’ requirements. If other lipids are used, other than what is listed above, rehydration should always be performed above the gel-liquid phase transition (Tm) temperature to ensure proper mixing of lipids.<span style=color:blue>**脂质选择**：根据研究者的需求，这些配方中可以使用不同的阳离子和阴离子脂质。如果使用其他脂质（例如，非上述列举的脂质），则在重构时必须保持温度高于凝胶-液体相变（Tm）温度，以确保脂质混合均匀。</span>

8. At increasing molar concentrations, DSPE lipid molecules become more attracted to itself than to other types of lipids. The result is insoluble DSPE complexes that cannot be rehydrated or formed into liposomes. Therefore, DSPE should never be used above a 55% molar ratio.<span style=color:blue>**DSPE脂质的使用限制**：随着摩尔浓度的增加，DSPE脂质分子对自身的吸引力大于对其他脂质的吸引力，导致不溶解的DSPE复合物，无法进行再水化或形成脂质体。因此，DSPE的摩尔比不能超过55%。</span>

9. Do not sonicate more than 100 μL per tube using this sonicator. Other sonicators may be used, but volumes may have to be increased significantly if a probe sonicator is used. Horn sonicators produce the best, most consistent results with the small volumes used here.<span style=color:blue>**超声处理限制**：每次超声处理时，不要超过100 μL的体积。其他类型的超声波仪器也可以使用，但如果使用探头超声波仪器，体积可能需要显著增加。角超声波仪器在处理小体积时能提供最稳定的效果。</span>

10. If used later, sonicate liposomes again prior to complexation.<span style=color:blue>**二次超声处理**：如果以后需要使用，超声脂质体时，必须在复合前再次进行超声处理。</span>

11. LSPCs are ready to use in 10 min, but are stable for several hours at room temperature.<span style=color:blue>**LSPCs稳定性**：LSPCs在10分钟内即可准备好使用，但在室温下可稳定保存几个小时。</span>

12. The covalent linkage of the peptide to the PEG groups is optional. If using DOTAP PALETS, the positive charge of RVG-9r may be able to bind to the negatively charged COO− groups of the PEG lipids. If using DSPE PALETS, the positively charged RVG-9r can bind to the negatively charged DSPE lipids.<span style=color:blue>**肽与PEG的共价连接**：将肽与PEG基团共价连接是可选的。如果使用DOTAP PALETS，RVG-9r的正电荷可能会与PEG脂质的负电荷（COO−基团）结合。如果使用DSPE PALETS，则RVG-9r的正电荷可以与DSPE脂质的负电荷结合。</span>

13. This protocol uses protamine sulfate to condense the siRNA so that it can be encapsulated within DSPE PALETS. However, other small positively charged cations can also be used, such as Ca2+, depending on the application.<span style=color:blue>**Protamine硫酸盐的使用**：本协议使用Protamine硫酸盐来凝聚siRNA，使其能够包裹在DSPE PALETS中。然而，也可以使用其他小型阳离子，如Ca2+，具体取决于应用需求。</span>

14. This step is crucial for successful tail vein injections, especially in dark-colored mice. The cage should reach an ambient temperature between 32 and 35 °C. The lateral tail veins and/or the ventral artery should be clearly visible before proceeding. This usually coincides with salivation, so look for moisture around the mouth and nose. Monitor mice under the heat lamp every 2 min for signs of distress or hyperthermia. Do not leave a mouse cage under the heat lamp for more than fifteen consecutive minutes.<span style=color:blue>**加热小鼠的重要性**：此步骤对于成功的尾静脉注射至关重要，尤其是在深色小鼠中。笼子应加热至32–35°C的环境温度，尾部的侧静脉和/或腹动脉应在注射前清晰可见。通常这会伴随小鼠流涎，因此应观察小鼠口鼻周围的湿润迹象。每2分钟检查一次小鼠是否有不适或过热的迹象。不要让小鼠笼子长时间放在热灯下，避免超过连续15分钟。</span>

15. This should take 1–3 min. Isoflurane is very safe and accidental overdoses are very rare. Distressed mice can be given pure oxygen to help revive them if necessary.<span style=color:blue>**麻醉剂的使用时间**：此过程应该在1-3分钟内完成。氟烷非常安全，意外过量的情况非常少见。如果小鼠感到不适，可以给予纯氧帮助其复苏。</span>

16. If bubbles appear, hold the syringe vertically with the needle pointing up and flick the syringe until the bubbles dislodge and float to the top of the syringe, toward the needle. Carefully keeping the needle tip above the syringe barrel, place it on the inside of the tube containing the LSPCs or PALETS and gently push the syringe plunger until the bubbles are evacuated (i.e., when a small amount of liquid emerges from the needle). Load additional LSPC/PALETS mixture into the syringe to 250 μL if necessary.<span style=color:blue>**去除气泡**：如果注射器中出现气泡，将注射器竖直放置，针头朝上，并轻轻敲击注射器，使气泡浮到注射器顶部，靠近针头。小心地将针头保持在注射器管内，轻轻推动注射器活塞，直到气泡被排出（即，注射器中少量液体从针头处排出）。如果需要，将LSPC/PALETS混合液补充到250 μL。</span>

17. Mice can be placed in physical restraints at this time if desired, but we recommend simultaneous chemical restraint.<span style=color:blue>**化学麻醉和物理约束**：此时可以将小鼠放置在物理约束中，但我们推荐同时使用化学麻醉。</span>

18. Curling the tail over a finger can help orient the tail in a position that facilitates inserting the needle at the shallow 10–15° angle required for entering the vein. You should, but not always, feel the needle entering the vein lumen. You should feel little or no resistance on the plunger if you are in the lumen, and you will often see the vein blanche as the solution displaces the blood. If you feel resistance or see the tail swell just anterior to the injection site, stop immediately. You are most likely not in the vein. Apply direct pressure to the injection site for a few seconds, then attempt the injection again further anterior to the previous site. If this fails after multiple attempts, or if the vasculature is no longer visible, stop. Allow the mouse to recover, proceed to the next mouse, and try injecting the former mouse after attempting the others.<span style=color:blue>**尾巴定位技巧**：用手指轻轻弯曲尾巴可以帮助将尾巴定位到适当位置，从而使针头以10–15°的浅角度插入静脉。你应该能够感受到针头进入静脉腔，通常注射活塞几乎没有阻力，且会看到血管因溶液注入而变白。如果感觉到阻力或看到注射部位前端尾巴肿胀，请立即停止操作。很可能针头未进入静脉，停止操作并对注射部位进行短暂按压，再尝试将针头插入更靠前的位置。如果多次尝试仍然失败，或者血管不可见，立即停止操作。让小鼠恢复后，可以继续处理其他小鼠，然后再尝试进行注射。</span>

19. Hyaluronidase administration prior to instilling LSPCs or PALETS into the nose is highly recommended to transiently break down connective tissue matrices to facilitate efficient delivery to the brain via the olfactory bulb. Blocking the oropharynx during intranasal instillation helps build pressure in the nasal cavity that facilitates delivery by providing moderate pressure to force cells across the cribriform plate.<span style=color:blue>**透明质酸酶的使用**：在进行鼻内注射LSPCs或PALETS前，强烈推荐使用透明质酸酶来暂时分解结缔组织基质，从而促进通过嗅球向大脑的高效递送。在进行鼻内灌注时，通过封堵口咽部可以在鼻腔内建立压力，有助于通过筛板的输送。</span>

20. We observed LSPC delivery in as little as 2 min using this technique (Fig. 3) and detected LSPCs up to 10 days after injection. We observed similar pharmacokinetics and pharmacodynamics using PALETS and intranasal instillation.<span style=color:blue>**LSPC递送动力学**：我们观察到，通过该技术，LSPC在2分钟内即可递送到目标区域（见图 3），并且在注射后最多可检测到LSPC存在10天。我们观察到，使用PALETS和鼻内灌注时，具有类似的药代动力学和药效学表现。</span>

21. Flow cytometric analysis of brain cells reveals that DOTAP LSPCs and DSPE PALETS decrease cell surface PrPC levels compared to untreated controls (Fig. 4a), and DOTAP PALETS decrease the number of PrPC-positive cells. Protein analysis in the kidneys shows that DOTAP LSPCs decrease both PrPC expression and PrPC + cells and DSPE PALETS reduce the amount of cell surface PrPC (Fig. 4b). DOTAP PALETS had no apparent effect on either parameter (Fig. 4b). Longitudinal mRNA and protein expression analyses revealed that mice treated with LSPCs (Fig. 5a, b) expressed less PrPC in their brains and kidneys over 21 days than mice treated with PALETS (Fig. 5c, d).<span style=color:blue>**流式细胞术分析**：流式细胞术分析显示，DOTAP LSPCs和DSPE PALETS可以减少脑细胞表面的PrPC水平（见图4a），而DOTAP PALETS则减少了PrPC阳性细胞的数量。肾脏中的蛋白质分析表明，DOTAP LSPCs减少了PrPC表达和PrPC阳性细胞的数量，而DSPE PALETS则降低了细胞表面PrPC的量（见图4b）。DOTAP PALETS对这两个参数没有明显影响（见图4b）。纵向的mRNA和蛋白质表达分析表明，与PALETS组小鼠相比，LSPC处理的小鼠在21天内的大脑和肾脏中PrPC表达较低（见图5a，b与5c，d）。</span>


![485053_1_En_20_Fig4_HTML](https://raw.githubusercontent.com/zcgkiller/Pictures/main/Wechat/485053_1_En_20_Fig4_HTML.png)

**Fig. 4** Analysis of PrPC protein levels in the brain after LSPCs or PALETS treatment. FVB mice were intravenously injected with either 1× PBS (untreated control, black squares), DOTAP LSPCs (green circles), DOTAP PALETS (red circles), or DSPE PALETS (blue triangles). Mice were sacrificed 4 days after treatment and their brains and kidneys were harvested. Asterisks to the right of symbols indicate statistically significant differences in percentage of PrP^C^ + cells. Asterisks on top of symbols indicate statistically significant differences in PrP^C^ expression. Asterisks in the center indicate statistical significance for both parameters. Error bars indicate 95% confidence intervals of the mean. Some error bars do not extend past symbols. \**p* < 0.05, \*\**p* < 0.01. (**a**) DOTAP LSPCs and DSPE PALETS decrease the amount of cell surface PrP^C^ in the brain, while DOTAP PALETs decrease the number of PrP^C^-positive cells in the brain. (**b**) DOTAP LSPCs decrease both PRP^C^ expression and the number of PrP^C^ + cells in the kidney. DSPE PALETS decreased the amount of cell surface PrP^C^, while DOTAP PALETS did not affect either parameter

![485053_1_En_20_Fig5_HTML](https://raw.githubusercontent.com/zcgkiller/Pictures/main/Wechat/485053_1_En_20_Fig5_HTML.png)

**Fig. 5** Longitudinal analysis of PrPC mRNA and protein levels in the brain after LSPCs or PALETS treatment. LSPCs significantly repressed PrPC mRNA (**a**) and protein (**b**) expression more and longer than PALETS (**c** and **d**) in both brain (squares) and kidneys (circles). Error bars indicate 95% confidence intervals of the mean. \**p* < 0.01, \*\**p* < 0.01, \*\*\**p* < 0.001
