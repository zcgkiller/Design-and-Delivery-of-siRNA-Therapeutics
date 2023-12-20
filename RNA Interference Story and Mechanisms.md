# RNA Interference: Story and Mechanisms RNA 干扰：故事和机制

Mouldy Sioud

## Abstract 摘要

The discovery that gene expression can be silenced by exogenously introduced double-stranded RNAs into cells unveiled a hidden level of gene regulation by a variety of small RNA pathways, which are involved in regulating endogenous gene expression, defending against virus infections, and protecting the genome from invading transposons, both at the posttranscriptional and epigenetic levels. All endogenous RNA interference pathways share a conserved effector complex, which contains at least an argonaute protein and a short single-stranded RNA. Such argonaute-RNA complexes can repress the transcription of genes, target mRNA for site-specific cleavage, or block mRNA translation into proteins. This review outlines the history of RNAi discovery, function, and mechanisms of action. For comparison, it also touches on CRISPR interference.

<span style=color:blue>基因表达可被外源性引入的双链RNA静默，揭示了一种隐藏的基因调控水平，通过各种小RNA途径参与调控内源基因表达、抵御病毒感染，并在转录后和表观遗传水平上保护基因组免受侵入的跳跃子。所有内源RNA干扰途径共享一个保守的效应器复合物，其中至少包含一个靶向蛋白和一个短的单链RNA。这样的靶向蛋白-RNA复合物可以抑制基因的转录，使mRNA靶向特定位点剪切，或阻断mRNA翻译成蛋白质。本综述概述了RNAi发现、功能和作用机制的历史。为了比较，它还涉及CRISPR干扰。</span>

## 1 Introduction

RNA silencing is a highly conserved gene regulation mechanism in which small RNA molecules silence gene expression by either suppressing transcription (transcriptional gene silencing) or by triggering a sequence-specific degradation of target mRNA, a process known as posttranscriptional gene silencing or RNA interference (RNAi). Although Fire’s Nature paper is considered a key breakthrough in the history of RNAi technology, it should be noted that in 1990 researchers described for the first time that RNA could potentially suppress gene expression in plants. Indeed, Napoli and Jorgensen were the first to report an RNAi type of phenomenon in plants 1990. By overexpressing the gene for chalcone synthase, an enzyme responsible for the production of anthocyanin pigments, the authors wanted to generate more purple transgenic petunia flowers. Surprisingly, some of the transgenic petunia lost both endogenous and transgene expression. This phenomenon was described as “cosuppression” and can be induced by single copy transgene that integrates into the genome in multicopy arrays. Later in 1992, a similar phenomenon was observed by Romano and Macino in *Neurospora crassa*.

<span style=color:blue>RNA沉默是一种高度保守的基因调控机制，小RNA分子通过抑制转录（转录基因沉默）或触发目标mRNA的序列特异性降解，即被称为转录后基因沉默或RNA干扰（RNAi）的过程，来沉默基因表达。尽管Fire在自然杂志上的论文被认为是RNAi技术历史上的重要突破，但值得注意的是，在1990年，研究人员首次描述了RNA可能在植物中抑制基因表达的可能性。事实上，Napoli和Jorgensen于1990年首次报告了植物中RNAi类型的现象。通过过度表达编码花青素色素产生的酶——花翠素合酶的基因，作者希望产生更多紫色的转基因矮牵牛花。令人惊讶的是，一些转基因矮牵牛花失去了内源和转基因的表达。这种现象被描述为“共抑制”，可以由单拷贝转基因引入多拷贝基因组中而诱发。后来在1992年，Romano和Macino在*神经孢子菌*中观察到了类似的现象。</span>

In 1995, Guo and Kemphues were the first to report RNA silencing in animals. The authors reported that sense RNA was as effective as antisense RNA for suppressing the expression of *par-1* gene in worm. *Par-1*, a gene required for establishing polarity in *Caenorhabditis* (C) *elegans* . At that time, antisense was one of the most attractive strategy for inhibiting gene expression. As a control, the authors used the sense par-1 RNA that would not hybridize to par-1 transcript. Interestingly, the degradation of par-1 mRNA was still observed. Although the results were interesting, the mechanism of mRNA degradation remained unknown.

<span style=color:blue>在1995年，Guo和Kemphues首次报告了动物中的RNA沉默。作者报道说，对于抑制蠕虫中*par-1*基因表达，正义RNA和反义RNA一样有效。*Par-1*是在线虫（*Caenorhabditis* *elegans*）中建立极性所需的基因。那个时候，反义RNA是抑制基因表达最引人注目的策略之一。作为对照，作者使用了不与par-1转录本杂交的正义par-1 RNA。有趣的是，依然观察到了par-1 mRNA的降解。尽管结果很有趣，但mRNA降解的机制仍然是未知的。</span>

In 1998, Fire and Mello showed in the worm *C. elegans* that double-stranded RNA (dsRNA), but not single-stranded RNA (ssRNA), was involved in gene silencing and coined the term “RNA interference, RNAi”. The authors thought that the results of Guo and Kemphues showing that introduction of sense RNA leads to gene silencing could have been due to the contamination of the RNA preparation by dsRNA resulting from the activity of bacteriophage RNA polymerases. They purified the sense and antisense RNAs, then directly compared their effects on the *unc-22* gene, one of a set genes identified using classical genetics that affect muscle function in *C. elegans*. Overall, their data showed that exogenously introduced dsRNA reduces the expression of homologous mRNAs in *C. elegans*, and that RNAi may have a catalytic component. While these findings establish a new concept for the effects of RNA on gene silencing by highlighting a role for dsRNA, the mechanism of unwinding dsRNAs to promote the degradation of target mRNAs remained unresolved. It was later discovered that dsRNA molecules were processed into shorter intermediates dsRNAs and then into single-stranded RNAs that can ultimately base pair to the mRNA targets and induce their cleavage. These RNA intermediates were called small interfering (si) RNAs and proved to be the main effectors of RNAi induction in mammalian cells. In conclusion, in RNAi, a dsRNA is involved and may originate from viral infection (exogenously), inverted-repeat transgenes, or from transcription of nuclear genes (endogenously).

<span style=color:blue>在1998年，Fire和Mello在线虫*C. elegans*中展示了双链RNA（dsRNA）参与基因沉默，而单链RNA（ssRNA）则不参与，并创造了术语“RNA干扰，RNAi”。作者认为Guo和Kemphues的结果表明引入正义RNA导致基因沉默可能是由于RNA制备中存在双链RNA的污染，这是由于噬菌体RNA聚合酶的活性导致的。他们纯化了正义和反义RNA，然后直接比较它们对*unc-22*基因的影响，这是使用经典遗传学鉴定的一组影响*C. elegans*肌肉功能的基因之一。总体而言，他们的数据显示，外源引入的dsRNA降低了*C. elegans*中同源mRNA的表达，并且RNAi可能具有催化组分。尽管这些发现通过突显dsRNA的作用为RNA对基因沉默的影响建立了一个新概念，但解开dsRNA的解旋机制以促进靶mRNA降解的方式仍然未解决。后来发现，dsRNA分子被加工成较短的中间体dsRNA，然后转化为可以最终与mRNA靶结合并诱导其剪切的单链RNA。这些RNA中间体被称为小干扰（si）RNA，证明它们是哺乳动物细胞中RNAi诱导的主要效应器。总之，在RNAi中，涉及dsRNA，可能源于病毒感染（外源）、反向重复转基因，或来自核基因的转录（内源）。</span>

## 2 The Interferon Response Hindered the Application of RNAi in Mammalian Cells 干扰素反应阻碍了RNAi在哺乳动物细胞中的应用

At the beginning, the use of RNAi was limited to flies, worms, and plants, as the introduction of long dsRNA into mammalian cells induces an interferon response that triggers a general inhibition of translation, abrogating the specificity of RNAi. However, in 2001 Tuschl and colleagues showed that duplexes of 21-nucleotide RNAs can bypass the interferon pathway and induce the degradation of their specific mRNA targets and thereby inhibiting the resulting protein expression. These experiments were performed in cancer cell lines that may lack the receptors that recognize small RNAs. In this respect, several groups were able to show that certain siRNA sequences are potent activators of the immune system . The activation of innate immunity by chemically made siRNAs is sequence-dependent and is normally mediated by Toll-like receptors (TLRs). We and others have demonstrated that the ribose sugar backbone are both necessary and sufficient for TLR7 and TLR8 recognition and that short ssRNA only requires several uridines in close proximity to render them effective immunostimulators. Fortunately, modifying siRNAs with as few as two 2′-OMe modifications at any position in the siRNA can eliminate the immunogenicity that can occur with unmodified siRNAs in immune cells. Other 2′-ribose modifications such as 2′-F and 2′-deoxy can also reduce immune activation; however, the effects are not as pronounced as 2′-OMe RNAs. Similarly, unmodified CRISPR guide RNAs induced type I interferon production in vitro in peripheral blood mononuclear cells , and that substitution of 2′OMe residues eliminated this response. Interestingly, 2′-modified RNAs can function as TLR antagonists.

<span style=color:blue>起初，RNAi的应用局限于果蝇、线虫和植物，因为引入长双链RNA到哺乳动物细胞中会诱导干扰素反应，触发翻译的普遍抑制，破坏RNAi的特异性。然而，2001年，Tuschl及其同事表明，21核苷酸RNA的双链可以绕过干扰素途径，诱导其特异mRNA靶的降解，从而抑制由此产生的蛋白质表达。这些实验是在可能缺乏识别小RNA的受体的癌细胞系中进行的。在这方面，几个研究小组能够表明，某些siRNA序列是免疫系统的强效激活剂。通过化学合成的siRNA引起的先天免疫的激活是依赖于序列的，通常由Toll样受体（TLRs）介导。我们和其他人已经证明，核糖糖骨架既是TLR7和TLR8识别的必要条件，也是充分条件，而短的单链RNA只需要靠近几个尿嘧啶就足以使它们成为有效的免疫刺激剂。幸运的是，在siRNA中进行至少两个2′-OMe修饰的修改可以消除未修饰的siRNA在免疫细胞中可能发生的免疫原性。其他2′-核糖修饰，如2′-F和2′-脱氧，也可以减少免疫激活；然而，效果不如2′-OMe RNAs显著。类似地，未修饰的CRISPR导向RNA在体外的外周血单核细胞中诱导I型干扰素的产生，而2′OMe残基的替代则消除了这种反应。有趣的是，2′-修饰的RNA可以作为TLR拮抗剂发挥作用。</span>

## 3 Molecular Mechanisms RNAi Induced by dsRNAs 双链RNA 诱导 RNAi 的分子机制

Early in vitro work by Hannon, Zamore, Tuschl, and colleagues showed that the RNAi active protein complex contains 25 nt-long small RNAs that were homologous to the target mRNAs. Shortly thereafter, several laboratories were able to identify enzymes and cofactors in RNAi pathways using genetic and biochemical methods. These efforts revealed that dsRNAs are cleaved by the enzyme Dicer, a RNase III family member, to generate 21–23-nt shorter RNA duplexes (Fig. 1). Dicer is a conserved protein among eukaryotes and can have multiple homologs with distinct functions. Like all RNase III enzymes, Dicer leaves 2-nt 3′-overhangs and 5′ phosphate groups. Some organisms, including mammals and nematodes, have only a single Dicer enzyme that functions in the biogenesis of both miRNAs and siRNAs whereas other organisms divide the labor among multiple Dicer proteins. For example, two distinct enzymes are involved in parallel pathways for small regulatory RNA biogenesis in *Drosophila*. Dicer-2 processes long-double-stranded precursors and generates siRNAs, while Dicer-1 processes pre-miRNAs into mature miRNAs.

<span style=color:blue>Hannon、Zamore、Tuschl等人在早期体外工作中表明，RNAi活性蛋白复合物包含与目标mRNA同源的25核苷酸长的小RNA。随后不久，几个实验室利用遗传学和生物化学方法成功识别了RNAi途径中的酶和辅因子。这些努力揭示了dsRNA由RNase III家族成员酶Dicer剪切，生成21-23核苷酸较短的RNA双链（图1）。Dicer是真核生物中的一个保守蛋白质，可以具有多个不同功能的同源物。与所有RNase III酶一样，Dicer留下2个核苷酸的3'端悬伸和5'磷酸基团。一些生物，包括哺乳动物和线虫，只有一个在miRNA和siRNA的生物发生中发挥作用的Dicer酶，而其他生物则在多个Dicer蛋白之间分工。例如，在果蝇中，两种不同的酶参与平行途径的小调控RNA的生物发生，Dicer-2处理长双链前体并生成siRNA，而Dicer-1将pre-miRNA处理成成熟的miRNA。</span>

![485053_1_En_1_Fig1_HTML](https://raw.githubusercontent.com/zcgkiller/Pictures/main/Wechat/485053_1_En_1_Fig1_HTML.png)

**Fig. 1** <span style=font-family:kaiti>Schematic representation of gene silencing by double-stranded RNAs. The RNAi pathway is experimentally activated by introducing double-stranded RNA (dsRNA) to silence specific genes. Long dsRNA is cut into 19–21 bp siRNA fragments by Dicer and then into a multi-protein complex termed RNA-induced silencing complex (RISC) where the sense strand with high 5′-end stability is eliminated by the nuclease argonaute 2 (Ago2), resulting in strand separation. Synthetic siRNAs are directly loaded into the Ago2 RISC complex. Subsequent to strand separation, the sense strand guides the RISC to recognize and cleave complementary mRNA sequences. Gene silencing is a result of nucleolytic degradation of the targeted mRNA by Argonaute 2, an RNase H enzyme. Cleaved mRNA molecules are rapidly degraded by cellular nucleases. Following dissociation, the RISC is able to recycle and cleave additional mRNA molecules. Unlike chemically made siRNAs, hairpin RNAs (hsiRNAs) produced from plasmid vectors in cell nucleus are processed by Dicer in the cytoplasm before entering the RNAi pathway.<span style=color:blue>Hannon、Zamore、Tuschl等人在早期体外工作中表明，RNAi活性蛋白复合物包含与目标mRNA同源的25核苷酸长的小RNA。随后不久，几个实验室利用遗传学和生物化学方法成功识别了RNAi途径中的酶和辅因子。这些努力揭示了dsRNA由RNase III家族成员酶Dicer剪切，生成21-23核苷酸较短的RNA双链（图[1](javascript:void(0))）。Dicer是真核生物中的一个保守蛋白质，可以具有多个不同功能的同源物。与所有RNase III酶一样，Dicer留下2个核苷酸的3'端悬伸和5'磷酸基团。一些生物，包括哺乳动物和线虫，只有一个在miRNA和siRNA的生物发生中发挥作用的Dicer酶，而其他生物则在多个Dicer蛋白之间分工。例如，在果蝇中，两种不同的酶参与平行途径的小调控RNA的生物发生，Dicer-2处理长双链前体并生成siRNA，而Dicer-1将pre-miRNA处理成成熟的miRNA。</span></span>

In the next step, the siRNA duplexes are loaded onto an Argonaute protein , which along with Dicer and the trans-activation response RNA binding protein (TRBP) form the effector RNA-induced silencing complex (RISC). Subsequent to strand separation based on asymmetric unwinding, the antisense strand guides the activated RISC to the complementary site in the target mRNA, resulting in mRNA cleavage (Fig.1). In mammals, the catalytic activity of RISC is mediated by Ago2 protein. This slicer activity of the Ago-2 is very precise and cleaves in a position 10 and 11, counting from the 5′end, generating products with a 5′-monophosphate and a 3′-hydroxyl termini. Once the target mRNA is degraded by cellular nucleases, the RISC complex is recycled and free to cleave additional targets. Eukaryotic Argonaute protein consists of three conserved domains: PAZ, MID, and PWI. The PAZ domain binds the 3′end of the single-stranded RNA. The Mid domain folds into a binding pocked that anchors the 5′ phosphate of the small RNA. Therefore, it is a strict requirement for the siRNAs to be 5′ phosphorylated to enter into the RISC pathway, and siRNAs that lack a 5′ phosphate are rapidly phosphorylated by an endogenous kinase prior to loading into the RISC complex. Analysis of the crystal structure of a siRNA guide strand associated with an Ago2 PIWI domain identified a seed sequence (nucleotides 2–8) that directs target mRNA recognition by RISC. It should be noted that the interactions between the small RNA and Ago2 protein are mediated by the sugar-phosphate backbone; as a result, the nucleotides of the guide RNA are free to base-pair with target mRNA. In humans, there are four Argonaute proteins and only Ago2 is catalytically active. In flies and humans, the passenger strand cleaved by Ago2 is removed from the RISC-loading complex by the endonuclease C3PO, known as translin. Although the mechanisms of gene silencing by dsRNAs are well studied, additional factors may contribute to strand selection by RISC and cleavage activity. Moreover, competition of coding and non-coding RNAs for Argonaute binding can influence gene silencing.

<span style=color:blue>在下一步中，siRNA双链被加载到一个Argonaute蛋白上，该蛋白与Dicer和转录激活反应RNA结合蛋白（TRBP）一起形成效应器RNA诱导沉默复合物（RISC）。在基于不对称解旋的基础上进行链分离后，反义链将激活的RISC引导到目标mRNA中的互补位点，导致mRNA的剪切（图1）。在哺乳动物中，RISC的催化活性由Ago2蛋白介导。Ago-2的这种切割活性非常精确，在从5'端计数的位置10和11处切割，生成具有5'磷酸基团和3'羟基末端的产物。一旦目标mRNA被细胞核酸酶降解，RISC复合物将被循环利用，并可以自由地剪切其他目标。真核生物Argonaute蛋白包含三个保守结构域：PAZ、MID和PWI。PAZ结域结合单链RNA的3'端。Mid结域折叠成一个结合口袋，锚定小RNA的5'磷酸基团。因此，siRNA必须5'磷酸化才能进入RISC途径，缺乏5'磷酸基团的siRNA在加载到RISC复合物之前将被内源激酶迅速磷酸化。通过分析与Ago2 PIWI结域相关的siRNA引导链的晶体结构，确定了一个种子序列（核苷酸2-8），该序列指导RISC对目标mRNA的识别。应注意，小RNA和Ago2蛋白之间的相互作用是通过糖磷酸骨架介导的；因此，引导RNA的核苷酸可以自由与目标mRNA形成碱基对。在人类中，有四种Argonaute蛋白，只有Ago2具有催化活性。在果蝇和人类中，被Ago2切割的载体链被内切酶C3PO，也称为translin，从RISC加载复合物中移除。尽管dsRNA通过的基因沉默机制得到了深入研究，但额外的因素可能影响RISC的链选择和剪切活性。此外，编码和非编码RNA竞争Argonaute结合可能影响基因沉默。</span>

## 4 MicroRNAs: Masters of Gene Regulation MicroRNA：基因调控大师

Although researchers demonstrated RNAi functionality using exogenous dsRNAs, RNAi is also induced by the endogenously present single-stranded hairpin microRNAs (miRNAs) (miRNAs) in cells. To date, miRNAs are the most abundant species of noncoding RNAs in mammalian cells, and they have fundamental roles in regulating gene expression at the posttranscriptional level. In some cases, RNAi can also confer resistance to virus or other pathogen infection. Notably, the first miRNAs were discovered through forward genetic screens in worms. Indeed, Ambros and colleagues described in 1993 a new mechanism of gene regulation in *C. elegans* through small non-protein-coding RNA lin-4, which was found to have complementary sequence to the 3′ untranslated region of lin-14 mRNA. In both plants and animals, cloning was the initial strategy of large-scale miRNA discovery. Additionally, several groups developed bioinformatics approaches for miRNA identification. According the miRBase database (release 22.1, http://www.mirbase.org), there is currently 2656 human mature miRNA sequences that have the capacity to regulate more than two-thirds of protein-coding genes in humans and are involved in every cellular process known so far.

<span style=color:blue>尽管研究人员通过外源性dsRNA展示了RNAi的功能，但RNAi也可由细胞内存在的单链发夹式微小RNA（miRNA）诱导。迄今为止，miRNA是哺乳动物细胞中最丰富的非编码RNA物种，它们在调控基因在转录后水平的表达中发挥着基础性作用。在某些情况下，RNAi还可以赋予对病毒或其他病原体感染的抗性。值得注意的是，最早的miRNA是通过在线虫中进行正向遗传筛选而发现的。事实上，Ambros和同事于1993年通过对*C. elegans*中的小非蛋白编码RNA lin-4进行描述，揭示了一种通过与lin-14 mRNA的3'非翻译区相互配对的基因调控新机制。在植物和动物中，克隆是大规模miRNA发现的最初策略。此外，几个团队开发了用于miRNA鉴定的生物信息学方法。根据miRBase数据库（版本22.1，http://www.mirbase.org），目前有2656个人类成熟miRNA序列，它们有能力调控人类超过三分之二的编码蛋白基因，并参与到目前为止已知的每一个细胞过程中。</span>

In contrast to siRNAs, most miRNA genes are transcribed in the nucleus by RNA polymerase II, and the primary transcripts known as primary miRNAs (pri-miRNAs) are capped and polyadenylated. Before their export to the cytoplasm for further processing and silencing, nuclear pri-miRNAs must be recognized and cleaved (Fig. 2). These respective tasks are carried out by the proteins Drosha and DGCR8 (known as Pasha in invertebrates), which together constitute the microprocessor complex. As with Dicer, Drosha proteins belong to the RNase III family. The endonucleolytic activity results in the cleavage of the stem structure of pri-miRNAs and the release of the pre-miRNAs, which have a hairpin-like structure. Thereafter, Drosha-generated pre-miRNAs are exported from the nucleus to the cytoplasm by the nuclear export protein Exportin-5, which binds miRNA hairpin duplex along with GTP-bound form of the cofactor Ran, and releases it in the cytoplasm after hydrolysis of GTP. In the cytoplasm, pre-miRNAs are cleaved further by Dicer to generate 22-nt miRNA duplexes containing mismatches and having a two nucleotides 3′ overhang. Subsequently, the miRNA duplex assembles with Ago2 protein to form the effector RISC complex after which the mature miRNA strand is selected (Fig.2). Depending on the homology to mRNAs, miRNA can lead either to mRNA cleavage (complete homology) or to repression of translation (partial homology). In flies and mammals few miRNAs are reported to lead to cleavage of their targets, whereas in plants most miRNAs exhibit complete homology with their corresponding target mRNA genes , resulting in target cleavage. Plant miRNA genes are generally not located within protein-coding genes but comprise their own RNA polymerase II-dependent transcriptional units. This contrasts with animal miRNAs, which sometimes appear to be processed from introns of protein-coding genes. In plants, many predicted miRNA targets encode regulatory proteins, suggesting that plant miRNAs are master regulators. Notably, miRNAs and siRNAs have much in common. Both are 20–24-nucleotides long and processed from longer RNA precursors by Dicer-like ribonucleases, and both are incorporated into ribonucleoprotein silencing complexes in which the small RNAs, through their base-pairing potential, guide target gene repression. However, the fundamental difference between the two small RNA classes is the nature of their precursors; siRNAs are processed from long, double-stranded RNAs, whereas miRNAs are processed from single RNA molecules that include imperfect stem-loop secondary structures as illustrated in Fig.2.

<span style=color:blue>与siRNA不同，大多数miRNA基因在细胞核中由RNA聚合酶II转录，其初级转录本被称为初级miRNA（pri-miRNA），并且具有帽子和聚腺苷酸尾。在它们被导入细胞质进行进一步处理和沉默之前，核内的pri-miRNA必须被识别和切割（图2）。这些任务由蛋白质Drosha和DGCR8（在无脊椎动物中称为Pasha）共同完成，它们一起构成了微处理器复合物。与Dicer一样，Drosha蛋白属于RNase III家族。内切活性导致pri-miRNA的茎结构切割，并释放出具有发夹状结构的pre-miRNA。此后，由Drosha生成的pre-miRNA通过核出口蛋白Exportin-5从细胞核输出到细胞质，该蛋白与miRNA发夹复合物以及辅因子Ran的GTP结合形式结合，并在GTP水解后在细胞质中释放。在细胞质中，pre-miRNA由Dicer进一步切割，生成含有错配并具有两个核苷酸的3'悬垂的22核苷酸miRNA双链。随后，miRNA双链与Ago2蛋白组装形成效应器RISC复合物，之后选择成熟的miRNA链（图2）。根据与mRNA的同源性，miRNA可能导致mRNA的剪切（完全同源）或抑制翻译（部分同源）。在果蝇和哺乳动物中，少数miRNA被报道导致其目标的剪切，而在植物中，大多数miRNA与其相应的目标mRNA基因具有完全同源性，导致目标剪切。植物miRNA基因通常不位于编码蛋白质的基因内，而是包含它们自己的RNA聚合酶II依赖的转录单元。这与动物miRNA形成对比，后者有时似乎是从编码蛋白质的基因内部处理出来的。在植物中，许多预测的miRNA靶基因编码调控蛋白质，这表明植物miRNA是主要的调控因子。值得注意的是，miRNA和siRNA有很多共同之处。它们都是20-24核苷酸长，由Dicer-like核糖核酸酶从较长的RNA前体中加工而来，都被整合到核糖核蛋白沉默复合物中，在这个复合物中，通过它们的碱基配对潜力，引导目标基因的沉默。然而，这两类小RNA之间的根本差异在于它们的前体的性质；siRNA是从长的双链RNA中加工而来的，而miRNA是从包含不完美的发夹状二级结构的单链RNA分子中加工而来，如图2所示。</span>

![485053_1_En_1_Fig2_HTML](https://raw.githubusercontent.com/zcgkiller/Pictures/main/Wechat/485053_1_En_1_Fig2_HTML.png)

**Fig. 2** <span style=font-family:kaiti>Schematic representation of miRNA silencing pathway. miRNAs are encoded in the genome and are transcribed to yield primary transcripts (pri-miRNAs), which are processed by Drosha with the aid of its partner DGCR8 protein (Pasha) to generate short precursor miRNAs (pre-miRNAs). These precursor miRNAs are then exported from the nucleus to the cytoplasm, where they are further processed by Dicer to yield miRNA duplexes that were unwound to single-stranded mature miRNA and then loaded into the miRNA-induced silencing complex (miRISC). Unwinding of the complex seems to occur so rapidly after duplex formation due to the Ago2 presence in the complex with Dicer and TRBP. The loaded strand RNA guides the RISC complex to recognize target mRNA sequences. A perfect homology allows Ago-cleavage of mRNA, whereas central mismatches promote repression of mRNA translation.<span style=color:blue>miRNA沉默途径的示意图。miRNA编码在基因组中，经转录产生初级转录本（pri-miRNA），由Drosha在其合作伙伴DGCR8蛋白（Pasha）的帮助下加工，生成短的前体miRNA（pre-miRNA）。然后，这些前体miRNA从细胞核导出到细胞质，在那里它们被Dicer进一步加工，生成miRNA双链，这些双链解开成为单链成熟miRNA，然后加载到miRNA诱导沉默复合物（miRISC）中。由于Ago2与Dicer和TRBP一起存在于复合物中，复合物形成后迅速解开。加载的链RNA引导RISC复合物识别目标mRNA序列。完全同源允许Ago切割mRNA，而中央错配促使抑制mRNA的翻译。</span></span>

## 5 piRNAs: Guardians of the Germline piRNA：种系的守护者

The Piwi-interacting RNAs (piRNAs) are the most recently discovered class of small non-coding RNAs, and they bind to the PIWI subclade of Argonaute proteins. One well-characterized Piwi/piRNA function is the silencing of retrotransposons, both at the posttranscriptional and epigenetic levels, as well as of other genetic elements in germlines, particularly those during spermatogenesis. Fly piRNAs were initially termed repeat-associated small interfering RNAs (rasiRNAs) because they were found to map to transposons and repetitive elements. Unlike rasiRNAs in flies, the majority of piRNAs in mammals arise from un-annotated regions of the genome devoid of transposons. Currently there are about 23,500 piRNAs identified in the human genome, a number that is quite comparable to that of protein-coding mRNAs (around 20,000), suggesting that piRNAs may have several important roles in gene regulation that remain to be investigated.

<span style=color:blue>与PIWI亚家族的Argonaute蛋白结合的Piwi相互作用RNA（piRNA）是最近发现的一类小非编码RNA。一个经过充分表征的Piwi/piRNA功能是沉默转座子，包括在转录后和表观遗传水平上，以及在生殖细胞系中的其他遗传元素，特别是在精子形成过程中。果蝇piRNA最初被称为重复相关小干扰RNA（rasiRNAs），因为发现它们与转座子和重复元件映射相关。与果蝇中的rasiRNA不同，哺乳动物中大多数piRNA来自基因组中没有转座子的未注释区域。目前已经在人类基因组中鉴定了大约23,500个piRNA，这个数量与编码蛋白质的mRNA数量（约为20,000个）相当，表明piRNA可能在基因调控中有几个重要的作用，这些作用有待进一步研究。</span>

Unlike miRNA and siRNA, piRNAs are typically longer, with a length of 26–31, originate from single-stranded RNA precursors, and do not require Dicer for maturation (Fig. 3). Most piRNAs are transcribed by RNA polymerase II as long transcripts which are then exported to the cytoplasm and processed into smaller sequences (mature piRNAs). In *D. melanogaster*, the nuclear export of piRNA precursors is mediated by UAP-56 that has been previously implicated in mRNA splicing and export. Another factor that has been important in the context of piRNAs biogenesis is the mitochondrial surface protein Zucchini. This protein has endonuclease activity for single-stranded RNA and likely processes the piRNA precursors, possibility at the 5′end. After 5′ processing, the 5′U/piRNA is incorporated into the MID domain of the Piwi protein, followed by 3′end processing, which likely involves an unknown trimmer activity as well as the action of methyl-transferase Pimet. Mature piRNAs are 5′ monophosphated and 2′-*O*-methyl modified in the 3′ terminal, a unique and specific feature of all piRNAs.

<span style=color:blue>与miRNA和siRNA不同，piRNA通常较长，长度为26-31个核苷酸，起源于单链RNA前体，成熟过程中不需要Dicer（图3）。大多数piRNA由RNA聚合酶II转录为长转录本，然后被导出到细胞质并加工成较小的序列（成熟piRNA）。在*D. melanogaster*中，piRNA前体的核导出是由UAP-56介导的，这在先前已涉及到mRNA剪接和导出。在piRNA的生物发生背景中另一个重要因素是线粒体表面蛋白Zucchini。这个蛋白对单链RNA具有内切酶活性，可能在5'端处理piRNA前体。在5'处理后，5'U/piRNA被整合到Piwi蛋白的MID结域中，然后进行3'端处理，这可能涉及未知的修剪活性以及甲基转移酶Pimet的作用。成熟的piRNA在3'末端是5'磷酸化和2' -*O*- 甲基修饰的，这是所有piRNA的独特和特定特征。</span>

![485053_1_En_1_Fig3_HTML](https://raw.githubusercontent.com/zcgkiller/Pictures/main/Wechat/485053_1_En_1_Fig3_HTML.png)

**Fig. 3** <span style=font-family:kaiti>Mechanisms of piRNA biogenesis in *D. melanogaster.* The piwi-interacting RNA pathway is involved in defense against transposable elements in the germline. Antisense precursor piRNAs are synthesized from repetitive elements by RNA polymerase II and then exported from the nucleus to nuage granules, where piRNA biogenesis is believed to occur. These piRNA precursors are cleaved by the endonuclease Zucchini, located in the outer membrane of mitochondria, generating the 5′end of the future piRNAs. Then they are trimmed to short fragments, and their 3′ ends are 2′-methylated and then loaded onto aubergine (Aub), which cleaves complementary transposon transcripts to generate sense piRNA fragments. Argonaute 3 (Ago3) uses the sense piRNA fragments to bind and cleave additional complementary antisense transposon transcripts to generate more antisense piRNAs, thus creating a feedback loop known as the ping-pong cycle. This amplification step generates new piRNAs that are identical in sequence to the piRNA that initiated the cycle.<span style=color:blue>*D. melanogaster*中piRNA生物发生的机制。Piwi相互作用RNA通路参与了生殖细胞中对抗转座元件的防御。反义前体piRNA是由RNA聚合酶II从重复元件中合成的，然后从细胞核导出到核仁颗粒，在那里piRNA的生物发生被认为发生。这些piRNA前体由位于线粒体外膜的内切酶Zucchini剪切，生成未来piRNA的5'端。然后，它们被修剪成短片段，它们的3'端被2'甲基化，然后加载到茄子（Aub）上，Aub切割互补的转座子转录本，生成反义piRNA片段。Argonaute 3（Ago3）使用反义piRNA片段结合并切割额外的互补的反义转座子转录本，生成更多的反义piRNA，从而创建一个被称为ping-pong循环的反馈循环。这一放大步骤生成了与启动循环的piRNA序列相同的新piRNA。</span>

The *D. melanogaster* genome encodes three Piwi proteins, Piwi, Aubergine (Aub), and Ago3, all of which are required for male and female fertility. As shown in Fig. 3, Piwi and Aub show a strong preference for sequences with a 5′uridine (U) within the antisense to transposons, whereas Ago3 shows enrichment for adenine (A) at position 10 within the sense to transposons, suggesting that Ago3 piRNAs are generated by a new mechanism known as the “ping-pong cycle” of amplification. In this cycle, Aub-bound piRNAs recognize a complementary transposon and induce endonuclease cleavage of the target. Such slicing generates the 5′ end of new sense piRNAs. This cytoplasmic loop, which is also found in zebrafish, links piRNA amplification to posttranscriptional target silencing. Additionally, mature piRNAs in the cytoplasm form a complex with Piwi proteins and migrate back into the nucleus, reaching their target transcripts and mobilizing the silencing machinery to block the transcription of transposable elements via DNA methylation (Fig. 3). Although the role of piRNAs in silencing transposon repeat elements is well established, recent reports have shown that piRNAs can also regulate gene expression and perfect sequence homology between the piRNA and its target mRNA is not required for efficient repression by deadenylation. Apart from the gonads, piRNAs and PIWI proteins may be expressed in various somatic cell types, albeit typically at lower levels than those observed in the germline . Similar to miRNAs , a higher number of piRNAs are expressed in tumors compared to normal tissues.

<span style=color:blue>*D. melanogaster*基因组编码了三种Piwi蛋白，Piwi、Aubergine（Aub）和Ago3，所有这些蛋白都对雄性和雌性的生育能力都是必需的。如图3所示，Piwi和Aub对反义转座子序列中的5'尿嘧啶（U）显示强烈的偏好，而Ago3在转座子的正义序列中的位置10处富集腺嘌呤（A），这表明Ago3 piRNA是通过一种被称为“ping-pong循环”的放大新机制生成的。在这个循环中，Aub结合的piRNA识别互补的转座子并诱导目标的内切酶切割。这种切割生成新的正义piRNA的5'端。这种细胞质循环也存在于斑马鱼中，将piRNA的放大与转录后靶基因沉默相连接。此外，细胞质中的成熟piRNA与Piwi蛋白形成复合物，并迁移到细胞核，达到它们的目标转录本并动员沉默机器通过DNA甲基化阻止转座元件的转录（图3）。尽管piRNA在沉默转座子重复元件方面的作用得到了充分确认，但最近的报告显示，piRNA也可以调控基因表达，而piRNA与其靶mRNA之间的完全序列同源性对于通过脱腺苷酸化实现的高效抑制并非必需。除了生殖细胞外，piRNA和PIWI蛋白可能在各种体细胞类型中表达，尽管通常表达水平低于生殖细胞中观察到的水平。与miRNA类似，与正常组织相比，肿瘤中表达的piRNA数量较高。</span>

## 6 CRISPR Interference CRISPR干扰

As indicated above, RNAi plays an essential role in many plant biological processes, including developmental timing and patterning, transposon control, DNA methylation, and chromatin modification. Although its role in human immunity is not known yet, RNAi constitutes the primary natural plant immune system against viruses. The plant RNAi defense system is highly specific because it will only target nucleic acids that are identical in sequence to the triggering dsRNAs. In addition to viral infections, RNAi protects the genome from genetics parasites such as transposons and retrotransposons. These mobile nucleic acid elements can cause diseases and alter the genome in a number of different ways.

<span style=color:blue>如上所述，RNAi在许多植物生物过程中起着重要作用，包括发育时机和模式、转座子控制、DNA甲基化和染色质修饰。尽管它在人类免疫中的作用尚不清楚，RNAi构成了植物对抗病毒的主要天然免疫系统。植物RNAi防御系统非常特异，因为它只会针对与触发的双链RNA序列完全相同的核酸。除了对抗病毒感染外，RNAi还保护基因组免受转座子和逆转座子等遗传寄生物的侵害。这些可移动的核酸元素可以以多种方式引起疾病并改变基因组。</span>

By analogy to RNAi-mediated plant protection against pathogen attack, the *C*lustered *R*egularly *I*nterspaced *S*hort *P*alindromic *R*epeats (CRISPR) loci and CRISPR-associated (Cas) proteins provide acquired immunity against viruses and other mobile genetic elements in bacteria and archaea. These CRISPR sequences are part of the bacteria’s immune system and provide endogenous adaptive immunity in approximately 40% of bacterial genomes and 70% of sequenced archaeal species. Immunological memories of phages and plasmids are stored in the CRISPR array as short spacer sequences that intercalate between repeats and specify the targets of CRISPR-Cas immunity. The locus consists of CRISPR-associated (Cas) genes in operons in addition to the spacer-repeat array. These repeats were initially discovered in the 1980s in *E. coli*, but their function was not uncovered until 2007 by Barrangou and colleagues, who demonstrated that the *Streptococcus thermophilus* strains that survived initial phage challenge were resistant to subsequent phage challenge and had incorporated sequences from the phage genome into their CRISPR arrays. When a new infection occurs, the spacer-repeat array is expressed as a long precursor pre-CRISPR RNA (pre-crRNA), and the transcript is processed into individual spacer repeat units as crRNAs, while the *cas* genes are transcribed and translated into proteins. Additionally, the *Cas* genes are transcribed into proteins. Such crRNAs associate with and direct Cas nucleases (e.g., Cas9) to cleave foreign nucleic acids complementary to the spacer sequence. Cleavage of the viral or plasmid target DNA prevents infection (Fig. 4). Target recognition requires base pairing between the crRNA and the target and a PAM sequence adjacent to the crRNA-binding region. The requirement of a PAM site prevents cleavage of the CRISPR loci, which lacks a PAM site. The PAM sequences allow the discrimination between self and non-self, a crucial characteristic of all immune systems.

<span style=color:blue>类似于RNAi介导的植物对抗病原体攻击的情况，*C*lustered *R*egularly *I*nterspaced *S*hort *P*alindromic *R*epeats (CRISPR) 序列和CRISPR相关（Cas）蛋白为细菌和古细菌提供了对抗病毒和其他可移动基因元件的获得性免疫。这些CRISPR序列是细菌免疫系统的一部分，在约40%的细菌基因组和70%的已测序的古细菌物种中提供内源性适应性免疫。噬菌体和质粒的免疫记忆以短的间隔序列的形式存储在CRISPR阵列中，这些序列插入在重复之间，指定CRISPR-Cas免疫的目标。该位点由CRISPR相关（Cas）基因和间隔-重复阵列之外的操纵子组成。这些重复最初是在1980年代在大肠杆菌中发现的，但其功能直到2007年由Barrangou等人揭示，他们证明了在初次噬菌体挑战后幸存的*Streptococcus thermophilus*菌株对随后的噬菌体挑战具有抗性，并且已经将噬菌体基因组的序列整合到其CRISPR阵列中。当发生新的感染时，间隔-重复阵列被表达为长的前体前CRISPR RNA（pre-crRNA），并且该转录本被加工成个体间隔重复单元，即crRNA，同时*cas*基因被转录并翻译成蛋白质。此外，*Cas*基因也被转录成蛋白质。这样的crRNA与并指导Cas核酸酶（例如Cas9）结合，切割与间隔序列互补的外源性核酸。对病毒或质粒靶DNA的切割防止感染（图4）。目标识别需要crRNA与目标之间的碱基配对以及与crRNA结合区域相邻的PAM序列。PAM位点的要求防止了对CRISPR序列的切割，因为它缺乏PAM位点。PAM序列允许在自身和非自身之间进行区分，这是所有免疫系统的关键特征。</span>

![485053_1_En_1_Fig4_HTML](https://raw.githubusercontent.com/zcgkiller/Pictures/main/Wechat/485053_1_En_1_Fig4_HTML.png)

**Fig. 4** <span style=font-family:kaiti>Schematic representation of CRISPR-Cas systems. When a phage infects a bacterium, it injects its DNA into the bacterium which responds by producing Cas enzymes to cut the phage DNA into small fragments and then incorporate them into its own genome at the CRISPR locus. During the second infection, the bacterium that survived the first infection activates the CRISPR locus to generate small RNA molecules and Cas protein enzymes. After RNA processing, each small RNA molecule associates with the Cas effector protein and guides the enzyme to cleave the invading phage DNA, thus blocking the infection. Cas genes code for important endonuclease enzymes in this pathway One of these, Cas9, is a nuclease that cuts nucleic acid (DNA or RNA).<span style=color:blue>CRISPR-Cas系统的示意图。当噬菌体感染细菌时，它将其DNA注入细菌体内，细菌体通过产生Cas酶来切割噬菌体DNA成小片段，然后将它们整合到自己的基因组中的CRISPR位点。在第二次感染期间，幸存第一次感染的细菌激活CRISPR位点以生成小RNA分子和Cas蛋白酶。经过RNA加工后，每个小RNA分子与Cas效应蛋白结合，并引导酶切割入侵的噬菌体DNA，从而阻止感染。Cas基因在这一途径中编码重要的内切酶酶。其中之一，Cas9，是一个切割核酸（DNA或RNA）的核酸酶。</span></span>

## 7 A Versatile Genome Editing Technology 多功能基因组编辑技术

CRISPR/Cas9 genome editing is a relatively new nucleic acid-based technique that relies on high-performing nucleic acids to produce highly efficient and specific alterations to the genome. The technology has been adapted for genome editing applications in eukaryotic cells and is an emerging tool because it allows for some more flexibility compared to other gene-editing tools. Moreover, the technique is incredibly precise, cheap, and easy. The CRISPR-Cas system described so far falls into two major classes, which are further divided into a total of six types. Class 1 uses a multi-subunit effector complex and consists of CRISPR type I, II, and IV. Class 2 employs a single effector nuclease and consists of CRISPR type II, V, and VI. CRISPR type II is known by Cas9 nuclease, a multidomain protein that is able to bind crRNA and cleave corresponding target DNA and thus represents the most convenient format to use in eukaryotic cells. Indeed, in a landmark 2012 paper, Doudna, Chapentier, and Jinek showed that they could use CRISPR-Cas 9 system to introduce specific mutations in any genome. When loaded with both crRNA and tracrRNA (or an artificial chimera of the two), the wild-type Cas9 can site-specifically introduce double-stranded DNA breaks (DSBs). The resulting DSB will either generate nonspecific mutations knocking out a gene through the error-prone NHEJ (non-homologous end joining) pathway. Alternatively, if a donor template with homology to the target locus is supplied, the DSB may be repaired by the homology-directed repair (HDR) pathway allowing for precise replacement mutations to be made. By directing the cells toward one of these repair mechanisms, CRISPR/Cas9 can be used to generate knockouts or knock-ins in cells. In addition to gene editing, the technology was also adapted for mRNA targeting (knockdown) with high specificity. This system relies on an enzyme called Cas13a, which complexes with guide RNA, which binds to complementary messenger RNA. The better the match between the guide RNA and the messenger RNA, the more effective the Cas13a’s gene silencing action.

<span style=color:blue>CRISPR/Cas9基因编辑是一种相对较新的基于核酸的技术，依赖于高效的核酸，以对基因组进行高效且特异性的改变。这项技术已经被改编用于真核细胞的基因编辑应用，因为与其他基因编辑工具相比，它具有更大的灵活性，而且这项技术非常精确、廉价和简便。到目前为止，已经描述的CRISPR-Cas系统分为两个主要类别，进一步分为共计六个类型。第一类使用多亚基效应复合物，包括CRISPR类型I、II和IV。第二类采用单亚基效应核酸酶，包括CRISPR类型II、V和VI。CRISPR类型II以Cas9核酸酶而闻名，这是一种能够结合crRNA并切割相应目标DNA的多域蛋白，因此在真核细胞中使用最方便。事实上，在2012年的一篇具有重要意义的论文中，Doudna、Chapentier和Jinek展示了他们可以使用CRISPR-Cas9系统在任何基因组中引入特定突变。当同时装载crRNA和tracrRNA（或两者的人工嵌合体）时，野生型Cas9可以特异性地引入双链DNA断裂（DSBs）。产生的DSB将通过错误倾向的NHEJ（非同源末端连接）途径生成非特异性突变，使基因失活。另外，如果提供了与目标位点同源的供体模板，DSB可以通过同源定向修复（HDR）途径修复，从而实现精确的替代突变。通过引导细胞朝着这些修复机制之一，CRISPR/Cas9可用于在细胞中生成敲除或敲入。除了基因编辑，该技术还被改编用于具有高特异性的mRNA靶向（敲低）。该系统依赖于一种名为Cas13a的酶，它与引导RNA形成复合物，引导RNA结合到互补的信使RNA上。引导RNA与信使RNA之间的匹配程度越好，Cas13a的基因沉默作用就越有效。</span>

In contrast to previous tools for genome editing such as zinc-finger nucleases and transcription activator-like effector nucleases, CRISPR does not require engineering of new enzymes for each new target. With respect to specificity, high-fidelity Cas9 variants including eSpCas9, SpCas9-HF1, HypaCas9, and xCas9 were developed. These Cas9 protein variants combined with the use of chemically modified gRNAs have increased the specificity of genome editing. Although RNAi was adopted as gene silencing technique first, CRISPR has surpassed RNAi in popularity due to several advantages including specificity and versatility. Drs Emmanuelle Chapentier and Jennifer Doudna who developed the CRISPR technology are awarded the Nobel Prize in Chemistry 2020.

<span style=color:blue>与先前的基因编辑工具（如锌指核酸酶和转录激活因子核酸酶）不同，CRISPR不需要为每个新目标设计新的酶。在特异性方面，高保真度的Cas9变体，包括eSpCas9、SpCas9-HF1、HypaCas9和xCas9，已经被开发出来。这些Cas9蛋白变体与化学修饰的gRNA的使用提高了基因组编辑的特异性。尽管RNAi最初被采用作为基因沉默技术，但由于CRISPR具有特异性和多功能性等几个优势，它已经超过了RNAi在流行度上。Emmanuelle Chapentier博士和Jennifer Doudna博士开发的CRISPR技术荣获2020年诺贝尔化学奖。</span>

## 8 Conclusions 结论

Analysis of RNAi in a variety of organisms revealed that RNAi is a widespread natural phenomenon that is conserved across fungi, plants, and animals. The process is induced not only by exogenous siRNAs but also by several endogenous small RNA species such as microRNAs and piwi-interacting RNAs. While miRNAs participate actively in all cellular processes, piwi-interacting RNAs (piRNAs) have a major function in the repression of transposable elements in the germline. Recently, CRISPR/Cas9 technology has evolved as the most powerful approach to generate genetic models both for fundamental and preclinical research. Not only can scientists use such technology to silence genes by knocking them out, they can also introduce desired genes into the genome. The choice remains with the user to perform knockout, knock-ins, or knockdown experiments, making CRISPR interference extremely versatile.

<span style=color:blue>对各种生物体中RNAi的分析揭示了RNAi是一种广泛存在的自然现象，在真菌、植物和动物中都是保守的。这一过程不仅由外源siRNA诱导，还由一些内源小RNA种类，如microRNA和piwi相互作用RNA引发。虽然microRNA在所有细胞过程中都积极参与，但piwi相互作用RNA（piRNA）主要在生殖细胞中抑制转座元件方面发挥作用。最近，CRISPR/Cas9技术已经发展成为生成基因模型的最强大方法，既用于基础研究又用于临床前研究。科学家不仅可以利用这种技术通过基因敲除来沉默基因，还可以将所需的基因引入基因组。用户可以选择进行基因敲除、基因插入或基因沉默实验，使CRISPR干扰具有极大的灵活性。</span>