# Stick-Based Methods for Aptamer-Mediated siRNA Targeted Delivery 基于"棒-桥“结构的适配体介导 siRNA 定向递送方法

Silvia Catuogno, Carla Lucia Esposito and Paloma H. Giangrande

## Abstract 摘要

Despite the therapeutic utility of small interfering RNA (siRNA) molecules, the development of a safe and reliable method to selectively target diseased organs and tissues is still a critical need for their translation to the clinic. Here we describe how nucleic acid-based aptamers against cell surface epitopes may be used to address this issue. We discuss the most recent examples and advances in the field of aptamer siRNA delivery and provide a fast and simple protocol for the design and generation of aptamer-siRNA chimeras. The described approach is based on the annealing of the targeting aptamer, and the antisense strand through “stick” complementary sequences elongated at their 3′ end, and the subsequent paring with the sense strand. Such a protocol allows a modular non-covalent generation of the constructs and permits an efficient delivery of the siRNA moiety into aptamer target cells.

<span style=color:blue>尽管小干扰 RNA (siRNA) 分子具有治疗应用前景，但开发一种安全可靠的方法选择性靶向患病器官和组织对于 siRNA 的临床转化仍然至关重要。本文我们将介绍如何利用针对细胞表面表位的核酸适配体来解决这一问题。我们讨论了适配体 siRNA 递送领域最新的例子和进展，并提供了一种快速简便的用于设计和生成适体-siRNA 嵌合体的方案。所述方法基于靶向适体和反义链通过其 3' 末端延伸的“棒”互补序列进行退火，然后与正义链配对。这种方法允许模块化非共价地构建 siRNA 载体，并有效地将 siRNA 部分递送至适体靶细胞。</span>

## 1 Introduction 

Small interfering RNAs (siRNAs) have emerged as highly powerful therapeutic options for the treatment of a wide range of human pathologies. Their mechanism of action lies in the inhibition of gene expression at a posttranscriptional level, through the recognition of specific sites in target genes and consequent target mRNA degradation. Restoration of normal expression levels of genes altered in a given disease by siRNAs represents a safe strategy for personalized gene therapy, and many have entered clinical trials. One main hurdle for clinical translation of therapeutic siRNAs is the development of suitable carriers, allowing selective delivery to diseased cells and tissues, as well as efficient siRNA intracellular processing. From this perspective, nucleic acid aptamers are very interesting molecules. Aptamers are single-stranded DNAs or RNAs that fold into unique three-dimensional shapes, which bind with high affinity specific target molecules, including proteins, carbohydrates, small peptides, or other compounds. Aptamer specificity for the target is very strong; indeed, they can distinguish between even very close molecules, including conformational isomers, molecules that differ for functional groups, or a single amino acid mutation. For their mode of action, aptamers are also known as “nucleic acid antibodies.” Compared to antibodies, aptamers show different advantageous properties, including rapid and simple production, and easy chemical synthesis and modifications to improve pharmacokinetic and pharmacodynamics properties. Interestingly, aptamers targeting cell surface receptors overexpressed in pathological states can be internalized into diseased cells in a receptor-dependent manner and can be used as carriers for selective delivery of various therapeutics. Therefore, the use of aptamers for therapeutic siRNA delivery has been widely explored in the last decade, and different conjugation strategies have been employed, including both covalent and non-covalent approaches.

<span style=color:blue> 小干扰 RNA (siRNA) 已成为治疗广泛人类疾病的强大选择。siRNA 的作用机制在于通过识别靶基因中的特定位点并降解靶 mRNA，从而在转录后水平抑制基因表达。利用 siRNA 恢复因疾病而改变的基因正常表达水平代表了一种安全的个性化基因治疗策略，许多 siRNA 已经进入临床试验阶段。然而，siRNA 临床转化的主要障碍之一在于合适载体的开发，这种载体需要能够选择性地将 siRNA 递送至患病细胞和组织，并有效地进行细胞内加工。从这个角度来看，核酸适配体是一种非常有趣的分子。适配体是单链 DNA 或 RNA，可以折叠成独特的立体结构，并能以高亲和力结合特异性靶标分子，包括蛋白质、碳水化合物、小肽或其他化合物。适配体对靶标的专一性非常强，甚至可以区分非常接近的分子，包括构象异构体、功能基团不同的分子或单个氨基酸突变的分子。由于其作用方式，适体也被称为“核酸抗体”。与抗体相比，适配体具有快速简便的生产、易于化学合成以及易于修饰以改善药代动力学和药效学性质等优点。有趣的是，靶向于病理状态下过表达的细胞表面受体的适体可以以依赖受体的方式被病变细胞内化，并可用作选择性递送各种治疗药物的载体。因此，在过去十年中，利用适配体进行治疗性 siRNA 递送的研究被广泛探索，并且采用了不同的结合策略，包括共价和非共价方法。</span>

A covalent aptamer-siRNA construct (AsiC) was first described in 2006 by McNamara et al. . This group covalently linked an antihuman prostate-specific membrane antigen (PSMA) aptamer to siRNAs targeting polo-like kinase 1 (PLK1) and B cell lymphoma 2 (BCL2) pro-survival genes and demonstrated selective internalization of the chimeric molecule into PSMA+ tumor cells and consequent tumor cell growth inhibition both in vitro and in vivo.

<span style=color:blue>2006 年，McNamara 等人首次描述了共价连接的适配体-siRNA 构建体 (AsiC)。该研究组将靶向人类前列腺特异性膜抗原 (PSMA) 的适体通过共价键连接到靶向细胞周期蛋白激酶 1 (PLK1) 和 B 细胞淋巴瘤 2 (BCL2) 抗凋亡基因的 siRNA 上，并证明了嵌合分子在 PSMA+ 肿瘤细胞中的选择性内化作用，以及体外和体内肿瘤细胞生长抑制的效果。</span>

From this first description, the covalent approach has been applied to generate a wide number of aptamer-siRNA conjugates.

<span style=color:blue>自从这一首次描述以来，共价连接方法已被用于生成多种适配体-siRNA 偶联物。</span>

For example, an aptamer targeting the epithelial cell adhesion molecule (EpCAM), a tumor-associated antigen overexpressed on epithelial cancers and tumor-initiating cells, has been covalently linked to PLK1-specific siRNA via a U-U-U linker. The conjugate has demonstrated the ability to downregulate PLK1 selectively in EpCAM+ cancer cells, inhibiting mammosphere formation, and tumor progression. The anti-EpCAM aptamer has also been linked to siRNA targeting survivin, demonstrating effectiveness in sensitizing breast cancer stem cells to doxorubicin. Further, a double EpCAM targeting chimera has also been described. Subramanian et al. conjugated the EpCAM binding aptamer to a siRNA targeting EpCAM mRNA. The resulting bifunctional conjugate reduced EpCAM expression and inhibited cell proliferation and tumor progression.

<span style=color:blue>例如，靶向上皮细胞粘附分子 (EpCAM) 的适配体（EpCAM 是肿瘤相关抗原，在上皮癌和肿瘤起始细胞中过表达）已通过 U-U-U 连接子共价连接到 PLK1 特异性 siRNA 上。该偶联物能够选择性地下调 EpCAM+ 癌细胞中的 PLK1 表达，抑制乳腺球体的形成和肿瘤进展。抗-EpCAM 适配体还被连接到靶向 survivin 的 siRNA 上，显示出增强乳腺癌干细胞对阿霉素耐药性的效果。此外，还描述了一种双重靶向 EpCAM 的嵌合体。Subramanian等人将 EpCAM 结合适体与靶向 EpCAM mRNA 的 siRNA 连接起来。所得的双功能偶联物降低了 EpCAM 的表达，并抑制了细胞增殖和肿瘤进展。</span>

Anticancer immunotherapeutic approaches based on aptamer-siRNA conjugates have also been successfully proposed. Recently, Rajagopalan and colleagues designed a chimera in which an anti-4-1BB aptamer was linked to a siRNA targeting interleukin 2 (IL-2) receptor alpha chain (CD-25). The chimera effectively reduced CD25 mRNA levels in 4-1BB+ cells and activated antitumor immunity to the attenuation of the IL-2 signaling pathway in CD8+ T cells.

<span style=color:blue>基于适配体-siRNA结合物的抗癌免疫治疗方法也已成功提出。最近，Rajagopalan及其同事设计了一种嵌合物，其中抗4-1BB的适配体与靶向白细胞介素2（IL-2）受体α链（CD-25）的siRNA共价连接。该嵌合物有效降低了4-1BB+细胞中CD25 mRNA水平，并通过抑制CD8+T细胞中IL-2信号传导途径的激活来激活抗肿瘤免疫。</span>

In addition to cancer therapy, different covalent aptamer-siRNA conjugates have been widely applied to the treatment of HIV infections.

<span style=color:blue>除了癌症治疗外，不同的共价连接适配体-siRNA 偶联物已被广泛应用于 HIV 感染的治疗。</span>

While covalent aptamer-siRNA conjugates have the advantage of being ready to use, their cost of synthesis is high. Therefore, less expensive and more advantageous non-covalent conjugation strategies have been developed. Ellington and colleagues proposed a strategy based on biotin-streptavidin interaction to conjugate anti-PSMA aptamers to biotinylated siRNAs against lamin A/C or glyceraldehyde 3-phosphate dehydrogenase (GAPDH).

<span style=color:blue>虽然共价连接的适配体-siRNA 构建体具有可以直接使用的优点，但其合成成本很高。因此，人们开发了更便宜、更具优势的非共价连接策略。Ellington及其同事提出了一种基于生物素-链亲和素相互作用的策略，将抗 PSMA 适配体与靶向层 lamin A/C 或甘油醛-3-磷酸脱氢酶 (GAPDH) 的生物素化 siRNA 偶联。</span>

An innovative conjugation strategy based on the use of a “universal sticky-bridge” to generate a dual-inhibitory construct for HIV treatment has been described. An aptamer targeting the HIV gp120 glycoprotein was linked by annealing to siRNAs to address the suppression of HIV replication. In this “sticky” approach, the aptamer and the siRNA sequences are extended with complementary portions that allow their connection by annealing. The sticky-bridge based strategy has been successfully used by the same group for the selective delivery of anti-STAT3 siRNAs to multiple myeloma cells and by other groups. In our laboratory, we used a similar approach to conjugate an anti-PDGFRβ aptamer (Gint4.T) to anti-STAT3 siRNAs for selective delivery in glioblastoma (GBM) cells. The construct resulted in an efficient reduction of cell viability and migration and tumor growth inhibition in vivo.

<span style=color:blue>已经描述了一种创新的连接策略，该策略基于使用“通用**棒-桥**”来生成用于 HIV 治疗的双重抑制构建体。靶向 HIV gp120 糖蛋白的配体通过退火与 siRNA 连接，以抑制 HIV 复制。这种“**棒-桥**”方法中，适配体和 siRNA 序列延伸出互补的部分，允许它们通过退火连接。“**棒-桥**”策略已由同一研究组成功用于将抗 STAT3 siRNA 选择性递送至多发性骨髓瘤细胞，并被其他研究组采用。在我们实验室，我们使用类似的方法将抗 PDGFRβ 适配体 (Gint4.T) 与抗 STAT3 siRNA 偶联，用于胶质母细胞瘤 (GBM) 细胞的选择性递送。该构建体导致细胞活力和迁移率有效降低，并能在体内抑制肿瘤生长。</span>

The great advantage of the sticky-bridge based approach compared with other conjugation strategies is the possibility of easily interchanging different siRNAs with the same aptamer, functioning as a “building block” system. Moreover, synthesis costs are greatly reduced in this approach.

<span style=color:blue>与其他连接策略相比，“棒-桥”方法的一大优势在于可以轻松地用不同的 siRNA 替换相同的适配体，起到“模块”系统的作用。此外，这种方法大大降低了合成成本。</span>

Here, we provide protocols for the generation of sticky-bridge based AsiCs and describe key elements necessary to control the correct annealing and function of the constructs.

<span style=color:blue>本文提供了基于棒-桥的 AsiC 的生成协议，并描述了控制构建体正确退火和功能所需的关键要素。</span>

## 2 Materials 材料

All solutions and RNAs are prepared using RNase-free ultrapure diethylpyrocarbonate (DEPC) treated water to assure absence of RNase activity.

<span style=color:blue>为了确保没有 RNase 活性，所有溶液和 RNA 都使用经过 RNase-free 超纯二乙基焦碳酸酯 (DEPC) 处理的水制备。</span>

### 2.1 Oligonucleotides 寡核苷酸

Synthetic RNA oligonucleotides may be obtained from commercial or institute facilities.
<span style=color:blue>合成 RNA 寡核苷酸可以从商业机构或研究所设施获得。</span>

The following RNAs (*see* **Note** **1**) were used for the described protocol.

<span style=color:blue>下表列出了用于所述方案的 RNA（见注释 1）。</span>

- Gint4.T-stick<span style=color:blue>Gint4.T-棒桥</span>:

  5′ UGUCGUGGGGCAUCGAGUAAAUGCAAUUCGACAXGUACAUUCUAGAUAGCC 3′.

- Human STAT3 Antisense strand stick <span style=color:blue>人STAT3反义链棒桥</span>(STAT3 AS-stick):

  5′ UUAGCCCAUGUGAUCUGACACCCUGAAGGCUAUCUAGAAUGUAC 3′.

- Human STAT3 sense strand<span style=color:blue>人STAT3正义链</span> (STAT3 SS):

  5′ CAGGGUGUCAGAUCACAUGGGCUAA 3′.

- Control aptamer<span style=color:blue> 对照适配体</span>(indicated as CtrlApt):

  5′ UUCGUACCGGGUAGGUUGGCUUGCACAUAGAACGUGUCA 3′.

- Control aptamer stick<span style=color:blue>对照适配体棒桥</span> (used in the control construct):

  5′ GCCGCUAGAACCUUCUAAGCGAAUACAUUACCGCXXXXGUACAUUCUAGAUAGCC 3′.

RNAs are modified with 2′-F-pyrimidines (2′-FPy) (*see* **Note** **2**); X within the sequences indicates the ((CH~2~)~3~) carbon spacer (*see* **Note** **3**); stick sequences are underlined and consist of 2′-FPy and 2′-*O*-methyl-purines at all positions (*see* **Notes** **4** and **5**).

<span style=color:blue>RNA 用 2'-F-嘧啶 (2'-FPy) 修饰（见注释 2）；序列中的 X 表示 ((CH~2~)~3~) 碳间隔物（见注释 3）；衔接片段序列下划线标注，并且在所有位置都由 2'-FPy 和 2'-O-甲基嘌呤组成（见注释 4 和 5）。</span>

### 2.2 Construct Preparation 构建体制备

Construct preparation is performed in annealing buffer 1×: annealing buffer 10×: 200 mM 2-[4-(2-hydroxyethyl)piperazin-1-yl] ethanesulfonic acid (HEPES) buffer pH 7.5 (adjusted with NaOH), 1.5 mM NaCl, 20 mM CaCl~2~.

<span style=color:blue>构建体制备在退火缓冲液 1x 中进行：退火缓冲液 10x：200 mM 2-[4-(2-羟乙基)哌嗪-1-基] 乙磺酸 (HEPES) 缓冲液 pH 7.5 (用 NaOH 调节)，1.5 mM NaCl，20 mM CaCl~2~。</span>

### 2.3 Non-denaturing Polyacrylamide Gel for Annealing Control 退火控制的非变性聚丙烯酰胺凝胶

1. 10× Tris-borate–ethylenediaminetetraacetic acid (EDTA) buffer (TBE): 890 mM Tris base, 890 mM boric acid, 25 mM EDTA.

   <span style=color:blue>10×三硼酸-乙二胺四乙酸（TBE）缓冲液：890 mM Tris碱、890 mM 硼酸、25 mM EDTA。</span>

2. Non-denaturing polyacrylamide gel (12% final concentration): dilute 30% acrylamide/bis solution (37.5:1) in 1.5 ml 10× TBE (final concentration 1×) and water for a final volume of 15 ml.

   <span style=color:blue>非变性聚丙烯酰胺凝胶（最终浓度12%）：在1.5 ml 10× TBE（最终浓度1×）和适量水中稀释30%丙烯酰胺/双乙烯基溴化乙烯（37.5:1）溶液至15 ml。</span>

3. 10× gel loading buffer: 10 mM Tris–HCl (pH 7.6), 60 mM EDTA, 0.03% bromophenol blue (BBF), 60% glycerol.

   <span style=color:blue>10×凝胶加载缓冲液：10 mM Tris–HCl（pH 7.6）、60 mM EDTA、0.03% 溴酚蓝（BBF）、60% 甘油。</span>

4. GEL.DOC XR (Bio-Rad). 

5. Running buffer: 1× TBE. 

   <span style=color:blue>运行缓冲液：1× TBE。</span>

### 2.4 Cell Culture 细胞培养

1. PDGFRβ positive U87MG glioblastoma cells from ATCC (American Type Culture Collection, Manassas, VA). 

   <span style=color:blue>来自ATCC（美国类型培养物收藏中心，Manassas, VA）的PDGFRβ阳性U87MG胶质母细胞瘤细胞。</span>

2. Growth medium: DMEM supplemented with 10% fetal bovine serum (FBS). 

   <span style=color:blue>生长培养基：含有10%胎牛血清（FBS）的DMEM。</span>

3. Solution of trypsin and EDTA. 

   <span style=color:blue>胰蛋白酶和EDTA溶液</span>

### 2.5 Binding and Internalization Analysis by Quantitative Real-Time PCR (RT-qPCR) 运用RT-qPCR 分析结合和内化

1. Buffer for incubation of RNAs : medium without serum containing 100 mg/ml tRNA (Sigma-Aldrich; *see* **Note** **6**). 

   <span style=color:blue>用于RNA处理液的缓冲液：不含血清的培养基，含有100 mg/ml tRNA（Sigma-Aldrich；*见* **注** **6**）。</span>

2. Washing buffer for binding analyses: 1× PBS. 

   <span style=color:blue>用于结合分析的洗涤缓冲液：1×PBS。</span>

3. Washing buffer for internalization analyses: 1× PBS supplemented with 0.5 M NaCl. 

   <span style=color:blue>用于内吞分析的洗涤缓冲液：含有0.5 M NaCl的1×PBS。</span>

4. Recovering buffer: TRiZol (Invitrogen, Waltham, MA) containing a 0.5 pmol/ml of a reference sequence (as for example CL4 aptamer: 5′ GCCUUAGUAACGUGCUUUGAUGUCGAUUCGACAGGAGGC 3′) (*see* **Note** **7**). 

   <span style=color:blue>回收缓冲液：含有0.5 pmol/ml参考序列的TRiZol（Invitrogen, Waltham, MA）（例如CL4 aptamer：5′ GCCUUAGUAACGUGCUUUGAUGUCGAUUCGACAGGAGGC 3′）（*见* **注** **7**）。</span>

5. Reagents for RT-qPCR: MMuLV reverse transcriptase, 10× NTP mix (10 mM CTP, 10 mM UTP,10 mM ATP, 10 mM GTP, Invitrogen, Waltham, MA), SYBR Green Supermix; specific primers designed on aptamer and reference sequences (*see* **Note** **8**). 

   <span style=color:blue>RT-qPCR 试剂：MMuLV 逆转录酶，10× NTP 混匀液 (10 mM CTP，10 mM UTP，10 mM ATP，10 mM GTP，Invitrogen, Waltham, MA)，SYBR Green Supermix；设计在适配体和参考序列上的特异性引物（见注释 8）。</span>

### 2.6 Cell Lysis and Western Blotting for Functional Analysis 细胞裂解和功能分析的Western印迹

1. Buffer for cell extract : 50 mM Tris–HCl (pH 8.0) supplemented with 150 mM NaCl, 1% Nonidet P-40, 2 mg/ml aprotin, 1 mg/ml pepstatin, 2 mg/ml leupeptin, and 1 mM Na~2~VO~4~. 

   <span style=color:blue>用于细胞提取的缓冲液：50 mM Tris–HCl（pH 8.0）、150 mM NaCl、1% Nonidet P-40、2 mg/ml aprotinin、1 mg/ml pepstatin、2 mg/ml leupeptin和1 mM Na~2~VO~4~。</span>

2. Gel separating buffer (4×): 1.5 M Tris–HCl (pH 8.7), 0.4% sodium dodecyl sulfate (SDS). 

   <span style=color:blue>凝胶分离缓冲液（4×）：1.5 M Tris–HCl（pH 8.7）、0.4% SDS。</span>

3. Gel stacking buffer (4×): 0.5% Tris–HCl (pH 6.8), 0.4% SDS. 

   <span style=color:blue>凝胶堆积缓冲液（4×）：0.5% Tris–HCl（pH 6.8）、0.4% SDS。</span>

4. 30% Acrylamide/bis solution (37.5:1): to dilute in the appropriate buffer to the desired final concentration: 5% for the gel stacking gel and 10% for the separating gel (*see* **Note** **9**). 

   <span style=color:blue>30% 丙烯酰胺/双乙烯基溴化乙烯（37.5:1）溶液：根据所需的最终浓度在适当的缓冲液中稀释。凝胶堆积凝胶浓度为5%，分离凝胶为10%（*见* **注** **9**）。</span>

5. Gel running buffer (5×): 125 mM Tris, 960 mM glycine, 0.5% SDS.

   <span style=color:blue>凝胶运行缓冲液（5×）：125 mM Tris、960 mM甘氨酸、0.5% SDS。</span>

6. Sample loading buffer (Laemmli): 2% SDS, 5% β-mercaptoethanol, 0.001% BBF, 10% glycerol. 

   <span style=color:blue>样品加载缓冲液（Laemmli）：2% SDS、5% β-巯基乙醇、0.001% 溴酚蓝、10% 甘油。</span>

7. Molecular weight markers. 

   <span style=color:blue>分子量标记物</span>

8. Polyvinylidenedifluoride (PVDF) membrane and 3MM chromatography paper. 

   <span style=color:blue>聚偏氟乙烯（PVDF）膜和3MM色谱纸。</span>

9. Transfer buffer: 25 mM Tris, 190 mM glycine, 20% methanol, 0.05% SDS (*see* **Note** **10**). 

   <span style=color:blue>转移缓冲液：25 mM Tris、190 mM甘氨酸、20% 甲醇、0.05% SDS（*见* **注** **10**）。</span>

10. Antibody against siRNA target (blot shown in Fig. 3: anti-STAT3 antibody from Cell Signaling Technology Inc., Danvers, MA; anti-actin from Santa Cruz Biotechnology, Santa Cruz, CA). 

    <span style=color:blue>靶标的抗体（在图3中显示的blot中使用：来自Cell Signaling Technology Inc.的anti-STAT3抗体，Danvers, MA；来自Santa Cruz Biotechnology的anti-actin）。</span>

11. Blocking and antibody incubation buffer: Tris-buffered saline supplemented with 0.1% Tween (T-TBS) and 5% nonfat dry milk. To prepare T-TBS, dilute 10× stock TBS solution (1.37 M NaCl, 27 mM KCl, 250 mM Tris–HCl pH 7.4) and add 0.1% Tween-20. 

    <span style=color:blue>阻断和抗体孵育缓冲液：含有0.1% Tween的三氯甲烷（T-TBS）和5%非脱脂奶的三氯甲烷。要准备T-TBS，稀释10×储存的TBS溶液（1.37 M NaCl、27 mM KCl、250 mM Tris–HCl pH 7.4）并加入0.1% Tween-20。</span>

12. Enhanced chemiluminescent (ECL) reagent . 

    <span style=color:blue>增强化学发光（ECL）试剂。</span>

13. Bio-Max ML film. 

    <span style=color:blue>Bio-Max ML胶片。</span>

### 2.7 Gene Expression by RT-qPCR

1. TRiZol (Life Technologies) for total cell RNA recovering. 

   <span style=color:blue>TRiZol（Life Technologies）用于总细胞RNA的回收。</span>

2. Reagents to measure mRNA level: cDNA synthesis kit and SYBR Green Supermix; specific primers for gene amplification. 

   <span style=color:blue>用于测量mRNA水平的试剂：cDNA合成试剂盒和SYBR Green Supermix；用于基因扩增的特异性引物。</span>

## 3 Methods 方法

### 3.1 Aptamer-siRNA Design 适配体-siRNA 设计

1. *Choice of an appropriate aptamer*. Choose the aptamer based on the cell system you want to target and on its ability to rapidly internalize within the cells overexpressing its target in a receptor-dependent manner. To generate the construct, extend the aptamer sequence at the 3′-end with the stick sequence. 

   <span style=color:blue>*选择合适的适配体*。根据您想要靶向的细胞系统以及其在受体依赖性方式下对其靶标的快速内化能力来选择适配体。为了生成构建物，将适配体序列在3'端延伸至棒-桥序列。</span>

2. *Choice of an appropriate siRNA*. Choose the siRNA based on experimentally tested sequences or by using siRNA tools available online (*see* **Note** **11**). The sequences reported here will be 19–21 nt in length. Extend the antisense strand at the 3′-end with the stick sequence. We recommend checking: (a) the correct annealing of the stick-antisense oligo to the corresponding siRNA sense strand by structure prediction (*see* **Note** **12**) and gel electrophoresis (*see* below Subheading 3.6, **Note** **13**); (b) the annealing with the stick-antisense sequence does not alter aptamer folding by using common structure prediction software (*see* **Note** **12**); (c) the therapeutic efficacy of the generated siRNA duplex upon cell transfection (*see* Subheading 3.7, **Note** **14**). The general aspects of aptamer attachment to different siRNA strands or the optimization of used siRNA sequences have been well discussed in several studies. 

   <span style=color:blue>*选择合适的siRNA*。根据实验测试的序列或使用在线siRNA工具来选择siRNA（详见**注11**）。这里报告的序列长度为19-21个核苷酸。将反义链在3'端延伸至棒-桥序列。我们建议检查：(a)通过结构预测（参见**注12**）和凝胶电泳（参见下文3.6节，**注13**）验证棒-桥-反义寡核苷酸与相应siRNA的正义链的正确退火；(b)使用常见的结构预测软件（参见**注12**）检查与棒-桥-反义序列的退火是否改变了适配体的折叠；(c)在细胞转染后检查生成的siRNA双链的治疗效力（参见3.7节，**注14**）。关于适配体如何附着到不同siRNA链或优化所用siRNA序列，已经在多项研究中得到了广泛讨论。</span>

### 3.2 Construct Preparation (Fig. 1) 构建体制备

1. Determine the concentration of each RNA oligo dissolved in sterile RNAse-free water (*see* **Note** **15**) spectrophotometrically, assuming that one A260 unit is equal to 40 mg/ml of RNA. 

   <span style=color:blue>将 RNA 寡核苷酸溶解于无菌 无RNAse酶水中，使用紫外分光光度计测定每种浓度（参见**注 15**），假设一个 A260 单位等于 40 mg/ml RNA。</span>

2. To prepare constructs, anneal 5 μM antisense-stick siRNA strand to 5 μM of complementary siRNA guide (ratio 1:1) in 1× annealing buffer by incubating at 95 °C for 10 min, 55 °C for 10 min, and 37 °C for 20 min. Then, subject an equal amount of stick aptamer to short denaturation-renaturation steps (85 °C for 5 min, snap-cooling on ice for 2 min and warming up to 37 °C) and add it to the generated stick-siRNA duplex. Transfer the mixture at 37 °C for 30 min. 

   <span style=color:blue>为了制备构建体，将 5 μM 反义链棒-桥 siRNA 与 5 μM 互补 siRNA 正义链在 1× 退火缓冲液中以 1:1 的比例退火。 退火步骤为：95 °C 孵育 10 分钟，55 °C 孵育 10 分钟，37 °C 孵育 20 分钟。 然后，对等量的棒-桥适配体进行短暂的变性-复性步骤（85 °C 孵育 5 分钟，立即冰上急冻 2 分钟，然后升温至 37 °C），并将其添加到生成的棒桥-siRNA 双链中。 将混合物在 37 °C 孵育 30 分钟。</span>

3. After annealing procedures, immediately use or store the constructs at −20 °C (*see* **Note** **16**). 

   <span style=color:blue>退火程序完成后，构建体可以立即使用，也可以保存在 -20 °C 的冰箱里（参见**注 16**）</span>	

![485053_1_En_3_Fig1_HTML](https://raw.githubusercontent.com/zcgkiller/Pictures/main/Wechat/485053_1_En_3_Fig1_HTML.png)

<span style=font-family:kaiti>**Fig. 1** Stick-based conjugate. Schematic representation of constructs generated by stick-end annealing. 4XC3 indicates the 4X((CH2)3) carbon spacer <span style=color:blue>**图1** 基于棒桥末端退火的构建体。构建体的示意图。4XC~3~表示4X((CH~2~)~3~)碳间隔</span></span>

### 3.3 Control of the Correct Annealing by Gel Electrophoresis

1. Control the correct annealing on a 12% non-denaturing PAGE gel. Load unconjugated RNAs or annealed constructs (10–15 pmol each) on the gel and run it in 1× TBE (*see* **Note** **17**). 
2. Visualize gel bands by ethidium bromide staining and GEL.DOC XR gel camera. 
3. Monitor the correct annealing by the presence of a shifted band of migration as compared to the individual components (Fig.  2). 

![485053_1_En_3_Fig2_HTML](https://raw.githubusercontent.com/zcgkiller/Pictures/main/Wechat/485053_1_En_3_Fig2_HTML.png)

**Fig. 2** Electrophoresis of annealed AsiC. Representative gel electrophoresis to control the correct annealing of Gint4.T-STAT3 AsiC containing the anti-PDGFRβ aptamer (Gint4.T) conjugated to STAT3 siRNA by the stick-based approach. M, DNA base pair (bp) ladder

### 3.4 Cell Culture (For Binding and Internalization or Functional Activity Assays)

1. Seed cells in 6-well plates the day before treatments. 
2. For binding and internalization analysis, seed 2 × 105 cells per well. 
3. For functional activity assays, seed 1.4 × 105 cells/well (about 60% confluence). Treat cells with 400 nM aptamer or aptamer-siRNA construct (*see* **Notes** **18** and **19**) or transfect with 100 nM siRNA duplex as control using Lipofectamine 2000 according to manufacturer’s instructions. 
4. Following 3 days, process cells for functional analyses (either by RT-qPCR or by immunoblotting as detailed below). 

### 3.5 Binding and Internalization Analysis by RT-qPCR

1. Add RNAs (aptamers or constructs) to the cells at 200 nM for different incubation times (ranging from 15 min to 2 h) at 37 °C in the presence of 100 mg/ml tRNA used as a nonspecific competitor. At selected times, wash cells three times with PBS (to remove unbound sequences and recover total bound sequences) or with PBS 0.5 M NaCl (to remove cell surface-bound sequences and measure amount of internalized RNA). Then, recover RNAs with 1 ml/sample TRIzol containing 0.5 pmol/ml of the CL4 oligo used as reference control (*see* **Note** **20**) and extract. 
2. Determine the amount of recovered RNA by performing a two-step RT-qPCR protocol. In step 1, RNA is reverse transcribed using specific 3′ primers and the following protocol: heating step at 65 °C for 5 min, annealing step at 22 °C for 5 min, extension at 42 °C for 30 min followed by end extension at 48 °C for 30 min and enzyme inactivation at 95 °C for 5 min. In step 2, the RT products are PCR amplified with iQ SYBR Green Supermix (Bio-Rad) by heating at 95 °C for 2 min, followed by 40 cycles of heating at 95 °C for 30 s, annealing at 55 °C for 30 s, and extending at 60 °C for 30 s. A melt curve stage by heating at 60–95 °C is performed. 
3. Normalize data to the CL4 reference control. 

This experiment demonstrates that the siRNA conjugation to the aptamer does not abrogate aptamer binding and internalization properties.

### 3.6 AsiC Functional Activity Analyses by RT-qPCR

To demonstrate the aptamer ability to deliver a functional siRNA, analyze the levels of the siRNA target by RT-qPCR and immunoblotting (*see* Subheading  3.7) upon cell construct treatment.

1. For RT-qPCR, recover RNAs from transfected or treated cells in 1 ml of TRiZol and extract according to manufacturer’s instructions. 
2. Analyze the levels of the siRNA target by performing total RNA (1 μg) retrotranscription using a cDNA synthesis kit and subsequent amplification with SYBR Green Supermix and specific primers. Perform the amplification of a reference gene (i.e., actin, GAPDH) in parallel, and use the ΔΔCt method for relative quantization of gene expression. 

### 3.7 AsiC Functional Activity Analyses by Immunoblotting

1. For immunoblotting , prepare cell protein extracts from transfected or treated cells by washing cells in ice-cold PBS and lysing in lysis buffer. Determine protein concentration by using the Bradford assay and bovine serum albumin as standard. 
2. Run samples on SDS-polyacrylamide gels and transfer into PVDF membranes. 
3. Probe filters with primary antibodies against the siRNA target (STAT3 in the reported example in Fig. 3). Use antibodies against a reference protein (anti-actin in the reported example) to confirm equal loading. Visualize signals with peroxidase-conjugated secondary antibodies using the enhanced chemiluminescence system. 

An example of the results obtained with extracts from U87MG cells (PDGFRβ receptor-positive cells) treated with a chimera containing the anti-PDGFRβ internalizing aptamer conjugated to STAT3 siRNA by stick-end annealing (indicated as Gint4.T-STAT3) is shown in Fig. 3. As expected, the AsiC treatment results in a significant reduction of STAT3 levels as compared to cells left untreated or treated with a control aptamer or construct containing an unrelated aptamer. Notably, the extent of reduction is comparable to that obtained upon siSTAT3 duplex transfection.

![485053_1_En_3_Fig3_HTML](https://raw.githubusercontent.com/zcgkiller/Pictures/main/Wechat/485053_1_En_3_Fig3_HTML.png)

**Fig. 3** Functional analyses by immunoblotting. Cell extract from U87MG (PDGFRβ positive) cells left untreated (−) or treated with control construct (CtrlApt linked to siSTAT3), Gint4.T, control aptamer (CtrlApt), or Gint4.T-STAT3, or transfected with STAT3 siRNA duplex, were analyzed by immunoblotting with STAT3 or actin (used as loading control) antibodies

## 4 Notes

1. We recommend ordering HPLC-purification grade lyophilized RNAs. The RNAs are dissolved in sterile RNAse-free water before use. 
2. 2′F-Py RNAs are used to increase nuclease resistance. 
3. The carbon linker increases the distance of the stick sequence from the aptamer, reducing possible interferences with the correct aptamer folding. 
4. The sequence of the stick portion may vary based on the specific aptamer used. It is important that the stick portion: (a) does not alter the correct aptamer folding; (b) produces a duplex with the most favorable annealing in the construct. 
5. In addition to 2′-FPy, the stick portion contains 2′-*O*-methyl-purines to further increase the base pairing stability of the duplex. 
6. Alterative nonspecific competitors (e.g., polyinosinic acid) may be used. 
7. The reference control is an unrelated RNA that is used as an internal control to normalize any experimental errors between the analyzed samples. 
8. The same primers are used for the aptamer and the construct. 
9. Commercially available pre-casted gels may be used. 
10. Transfer buffer can be used up to three times, checking that the voltage is maintained at a constant rate. 
11. An example is the online tool available at www.Dharmacon.com. 
12. A prediction of bimolecular RNAs can be performed with common structure prediction software such as *RNAStructure*. 
13. The correct annealing can be monitored by the presence of a shifted band of migration as compared to the antisense stick and the sense strands on non-denaturing PAGE gel. 
14. The correct efficacy of the generated siRNA duplex can be monitored by analyzing the levels of the siRNA target by RT-qPCR and immunoblot following cell transfection with the duplex. 
15. Once dissolved, we recommend the solution be aliquoted and stored at −20 °C. 
16. When constructs are stored at −20 °C, we recommended avoiding freezing-refreezing cycles. 
17. The gel is run until the sample dye front settles to the bottom. 
18. Before treatment, constructs are warmed up to 37 °C, and the aptamers are subjected to the denaturation-renaturation steps (5 min 85 °C, 2 min snap-cooling on ice, warming up to 37 °C). 
19. To ensure a correct aptamer folding, denaturation-renaturation steps must be performed at low aptamer concentration (no more than 20 μM). 
20. We recommend preparing a unique solution of TRIzol with the reference control for all experimental points.