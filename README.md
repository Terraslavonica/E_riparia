# Genome assembly and search for genetic markers of adaptation of shore flies (Diptera, Ephydridae) to extreme habitats
Dipteran insects characterized by the huge taxonomic diversity (more than 160 thousand species at the time of 2013 (Zhang, 2013)), the diversity of ecological niches, and adaptation to various extreme environmental conditions. At the same time, the mechanisms of these adaptations are poorly studied, especially at the genomics level. Now the NCBI Genome database contains only 165 dipteran genomes (for comparison, for 40 thousand vertebrates we have more than 1000 sequenced genomes). Different species of the large family Ephydridae (shore flies), about 2000 species, are adapted to the most adverse environmental conditions from saline and alkaline impoundment and hot springs to oil puddles (Kadavy et al., 2020), but the genomes of only two species of this curious family - [*Ephydra gracilis*](https://www.ncbi.nlm.nih.gov/assembly/GCA_001014675.1) and [*E. hians*](https://www.ncbi.nlm.nih.gov/assembly/GCA_001015075.1/) (syn. *Cirrula hians*) - were sequenced. The genome of the third fly from family Ephydridae - *E. riparia* - were sequenced at the department of biological evolution at Lomonosov Moscow State University.


## Goal:
The goal of this project is to assemble de novo the *E. riparia* genome and compare it with the genomes of two sequenced species of shore flies to identify candidate genes that allow flies to adapt to extreme environmental conditions.


## Objectives:
1. To study the articles dedicated to the adaptation of organisms to extreme environmental conditions and stress factors.
2. Assemble *de novo* the genome of *E. riparia*.
3. Annotate the shore flies’ genomes.
4. Identify genes that may be associated with the adaptation of the shore flies to extreme habitats and compare the genomes of those three species of shore flies (task for summer internship).
5. Analyze the fly’s digestive microbiome based on the reads that was classified as bacterial and fungal contamination (additional task for summer internship).


## Materials and methods:
Full genome of *E. riparia* were sequenced on the Illumina platform. We got 94.4M paired reads with the length about 150 bp.
Raw reads were filtered by Trimmomatic and cleaned of bacterial and fungal contamination by Kraken2 protein and nucleotide databases. After that 67% of reads left. 
*E. riparia* genome was assembled by SPAdes, SOAPdenovo and Platanus. The quality was assessed by QUAST and BUSCO (dipteran database).
We masked the repeats and low complexity regions by WindowMasker and made structural genomes annotation by Augustus.
Now we continue the functional annotation of the shore flies’ genomes by KEGG and eggNOG-mapper databases. More details are available in the [laboratory journal](https://docs.google.com/document/d/147rQTXeOp-6CRlvWNGPbjIMCVoK0hkg7_j6raF1Ku7M/edit?usp=sharing).


## Results:
(1) We studied the articles dedicated to the adaptation of organisms to extreme environmental conditions and stress factors. Studying populations that adapt to life in extreme habitats is of great interest for evolutionary studies (Rane et al., 2019a, b), because extreme conditions (physical and chemical stress factors) create a particularly interesting evolutionary context associated with solving the problems of maintaining the basic vital functions of the body in difficult conditions (Bang et al., 2018; Riesch et al., 2015; Waterman, 1999).

There are many levels of protection against stress factors, ranging from transcription regulation, post-transcriptional modification mechanisms, activation of certain metabolic pathways (Davies et al., 2014), ending with the compartmentalization of the body and the role of insect Malpighian tubules in fluid secretion, osmoregulation, and neuroendocrine regulation of ion transport (Beyenbach, 2003; O'Donnell et al., 2003; Coast, 2007; Spring et al., 2009; Wieczorek et al., 2009; Maddrell, 2009).

In response to increased salt concentrations and osmotic stress, the body reacts by activating signalling cascades such as p38 and JNK MAPK (Kyriakis et al., 1994; Stronach, Perrimon, 1999; Inoue et al., 2001; Craig et al., 2004; Davies et al., 2014; Reidl et al., 2016). The p38 kinase cascade is an ancient stress response system found in yeast, plants, and animals (Brewster et al., 1993; Han S.-J. et al., 1998; Han Z.S. et al., 1998; Berman, 2001; Solomon et al., 2004; Xu et al., 2013). JNK MAPK (mitogen-activated protein kinase) is a signalling system that facilitates the transmission of a signal from the external environment to the nucleus to change the transcription of desired genes (Stronach, Perrimon, 1999; Nebreda, Porras, 2000).

LEA-proteins are included in the group of hydrophilins (and are usually characterized by a high content of glycerin amino acids in their composition) found in archaea, eubacteria and in the eukaryotic domain. Their role has not been fully understood, but they undoubtedly play an important role in the acclimation and adaptive response to stress (Imai et al., 1996; Xu et al., 1996; Swire-Clark, Marcotte, 1999; Battaglia et al., 2008; Olvera-Carrillo et al., 2011; Deinlein et al., 2014; Huang et al., 2016), including osmotic stress, because a deletion in the corresponding gene in E. coli leads to the appearance of an osmosis sensitive phenotype (Garay-Arroyo et al., 2000).

Heat shock proteins (hsp) are proteins whose expression increases during and after exposure to a wide range of stress factors. These proteins can also control other proteins important in response to stress, many of which have not been studied (Jensen et al., 2008; Muthusamy et al., 2017).

Aquaporins are a family of membrane proteins that regulate the movement of water molecules and other small molecules through plant vacuoles and plasma membranes. These proteins are inevitably associated with the tolerance of biotic and abiotic stresses by organisms (Maurel et al., 2015; Zargar et al., 2017; Mishra, Tanna, 2017; Pawłowicz, Masajada, 2019). For example, the transcription level of the GoPIP1 gene (related to aquaporins) was significantly increased when Galega orientalis was treated with 200 mM NaCl or 20% polyethylene glycol (PEG) 6000. (Li et al., 2015). It has been shown that aquaporins are extremely important in the regulation of many physiological processes in hematophagous arthropods, including in response to stress (Benoit et al., 2014).

The above are only examples of mechanisms and groups of proteins associated with a response to stress. A significant amount of proteins related to the response to stress continues to be discovered and studied. Thus, in a recent work by Das and colleagues in the genome of the bacterium Staphylococcus sp. living in saltwater, 10 proteins were found that contribute to resistance to great salinity, up to 20% NaCl in a laboratory environment (Das et al., 2020).

Thus, after the functional annotation of the shore flies’ genomes we will search the genes that can contribute to adaptation to extreme habitats and stressful conditions. It might be genes encoding LEA-proteins, heat shock proteins, aquaporins, metal-transport proteins, proteins that are the part of the signalling cascades p38 and JNK MAPK, etc.

(2) We assembled the *E. riparia* genome. The genome, about 600M bp, was assembled by SPAdes program into scaffold with average coverage 11.2x, with N50 equal 3.5K bp and L50 – 53K contigs. In assembly we detected 53% of genes typical for Diptera by BUSCO. Comparing with assemblies of close relatives, [*E. gracilis*](https://www.ncbi.nlm.nih.gov/assembly/GCA_001014675.1) (410M bp, cov. 9.4x, N50 2.1K, L50 46K, BUSCO 81%) and [*E. hians*](https://www.ncbi.nlm.nih.gov/assembly/GCA_001015075.1/) (399M bp, cov. 27.0x, N50 1.8K, L50 53K, BUSCO 37%), we can conclude that *E. riparia* assembly is good enough for further analyses. More details  are available in the [laboratory journal](https://docs.google.com/document/d/147rQTXeOp-6CRlvWNGPbjIMCVoK0hkg7_j6raF1Ku7M/edit?usp=sharing) (items 8-16).

(3) We got a lot of annotated genes and metabolic pathway from functional annotation by KEGG and eggNOG-mapper databases. More details  are available in the [laboratory journal](https://docs.google.com/document/d/147rQTXeOp-6CRlvWNGPbjIMCVoK0hkg7_j6raF1Ku7M/edit?usp=sharing) (items 17-19).


## References:
1.	Adler, M., Anjum, M., Andersson, D. I., & Sandegren, L. (2016). Combinations of mutations in envZ, ftsI, mrdA, acrB and acrR can cause high-level carbapenem resistance in *Escherichia coli*. Journal of Antimicrobial Chemotherapy, 71(5), 1188–1198. https://doi.org/10.1093/jac/dkv475
2.	Bang, C., Dagan, T., Deines, P., Dubilier, N., Duschl, W. J., Fraune, S., Hentschel, U., Hirt, H., Hülter, N., Lachnit, T., Picazo, D., Pita, L., Pogoreutz, C., Rädecker, N., Saad, M. M., Schmitz, R. A., Schulenburg, H., Voolstra, C. R., Weiland-Bräuer, N., Ziegler, M., … Bosch, T. (2018). Metaorganisms in extreme environments: do microbes play a role in organismal adaptation? Zoology (Jena, Germany), 127, 1–19. https://doi.org/10.1016/j.zool.2018.02.004
3.	Battaglia, M., Olvera-Carrillo, Y., Garciarrubio, A., Campos, F., & Covarrubias, A. A. (2008). The enigmatic LEA proteins and other hydrophilins. Plant physiology, 148(1), 6–24. https://doi.org/10.1104/pp.108.120725
4.	Benoit, J. B., Hansen, I. A., Szuter, E. M., Drake, L. L., Burnett, D. L., & Attardo, G. M. (2014). Emerging roles of aquaporins in relation to the physiology of blood-feeding arthropods. Journal of comparative physiology. B, Biochemical, systemic, and environmental physiology, 184(7), 811–825. https://doi.org/10.1007/s00360-014-0836-x
5.	Beyenbach, K. W. (2003). Transport mechanisms of diuresis in Malpighian tubules of insects. J. Exp. Biol. 206, 3845-3856.
6.	Brewster JL, de Valoir T, Dwyer ND, Winter E, Gustin MC. (1993) An Osmosensing Signal Transduction Pathway in Yeast. Science. 259:1760–1763.
7.	Coast, G. (2007). The endocrine control of salt balance in insects. Gen. Comp. Endocrinol. 152, 332-338.
8.	Craig CR, Fink JL, Yagi Y, Ip YT, Cagan RL. (2004) A *Drosophila* p38 orthologue is required for environmental stress responses. EMBO Rep. 5:1058–1063.
9.	Das, P., Behera, B. K., Chatterjee, S., Das, B. K., & Mohapatra, T. (2020). De novo transcriptome analysis of halotolerant bacterium Staphylococcus sp. strain P-TSB-70 isolated from East coast of India: In search of salt stress tolerant genes. PloS one, 15(2), e0228199. https://doi.org/10.1371/journal.pone.0228199
10.	Davies, S. A., Cabrero, P., Overend, G., Aitchison, L., Sebastian, S., Terhzaz, S., & Dow, J. A. (2014). Cell signalling mechanisms for insect stress tolerance. The Journal of experimental biology, 217(Pt 1), 119–128. https://doi.org/10.1242/jeb.090571
11.	Deinlein, U., Stephan, A. B., Horie, T., Luo, W., Xu, G., & Schroeder, J. I. (2014). Plant salt-tolerance mechanisms. Trends in plant science, 19(6), 371–379. https://doi.org/10.1016/j.tplants.2014.02.001
12.	Garay-Arroyo, A., Colmenero-Flores, J. M., Garciarrubio, A., & Covarrubias, A. A. (2000). Highly hydrophilic proteins in prokaryotes and eukaryotes are common during conditions of water deficit. The Journal of biological chemistry, 275(8), 5668–5674. https://doi.org/10.1074/jbc.275.8.5668
13.	Herbst, D. B. (1999). Biogeography and physiological adaptations of the brine fly genus Ephydra (Diptera: Ephydridae) in saline waters of the Great Basin. Great Basin Naturalist, 59(2), 127–135.
14.	Huang Z, Zhong X-J, He J, Jin S-H, Guo H-D, Yu X-F, et al. (2016) Genome-Wide Identification, Characterization, and Stress-Responsive Expression Profiling of Genes Encoding LEA (Late Embryogenesis Abundant) Proteins in Moso Bamboo (Phyllostachys edulis). PLoS ONE 11(11): e0165953. doi:10.1371/journal. pone.0165953
15.	Han SJ, Choi KY, Brey PT, Lee WJ. (1998) Molecular cloning and characterization of a *Drosophila* p38 mitogen-activated protein kinase. J Biol Chem. 273:369–374. 
16.	Han ZS, Enslen H, Hu X, Meng X, Wu IH, et al. (1998) A conserved p38 mitogen-activated protein kinase pathway regulates *Drosophila* immunity gene expression. Mol Cell Biol. 18:3527–3539.
17.	Imai R, Chang L, Ohta A, Bray EA, and Takagi M (1996) A lea-class gene of tomato confers salt and freezing tolerance when expressed in Saccharomyces cerevisiae. Gene. 170, 243±248. PMID:8666253
18.	Inoue H, Tateno M, Fujimura-Kamada K, Takaesu G, Adachi-Yamada M. (2001) A Drosophila MAPKKK, D-MEKK1, mediates stress responses through activation of p38 MAPK. EMBO J. 20:5421–5430.
19.	Jensen, L.T., Nielsen, M.M., Loeschcke, V. (2008). New candidate genes for heat resistance in *Drosophila melanogaster* are regulated by HSF.  Cell Stress Chaperones 13(2): 177--182.
20.	Kadavy, D. R., Hornby, J. M., Haverkost, T., Nickerson, K. W. (2000). Natural antibiotic resistance of bacteria isolated from larvae of the oil fly, *Helaeomyia petrolei*. Applied and environmental microbiology, 66(11), 4615–4619. https://doi.org/10.1128/aem.66.11.4615-4619.2000
21.	Khan, A. R., Pervez, M. T., Babar, M. E., Naveed, N., & Shoaib, M. (2018). A Comprehensive Study of De Novo Genome Assemblers: Current Challenges and Future Prospective. Evolutionary bioinformatics online, 14, 1176934318758650. https://doi.org/10.1177/1176934318758650
22.	Kyriakis JM, Banerjee P, Nikolakaki E, Dai T, Rubie EA, et al. (1994) The stress-activated protein kinase subfamily of c-Jun kinases. Nature. 369:156–160.
23.	Li, J., Ban, L., Wen, H., Wang, Z., Dzyubenko, N., Chapurin, V., Gao, H., & Wang, X. (2015). An aquaporin protein is associated with drought stress tolerance. Biochemical and biophysical research communications, 459(2), 208–213. https://doi.org/10.1016/j.bbrc.2015.02.052
24.	Maddrell, S. (2009). Insect homeostasis: past and future. J. Exp. Biol. 212, 446-451.
25.	Mahajan, S., & Bachtrog, D. (2017). Convergent evolution of Y chromosome gene content in flies. Nature communications, 8(1), 785. https://doi.org/10.1038/s41467-017-00653-x
26.	Maurel, C., Boursiac, Y., Luu, D. T., Santoni, V., Shahzad, Z., & Verdoucq, L. (2015). Aquaporins in Plants. Physiological reviews, 95(4), 1321–1358. https://doi.org/10.1152/physrev.00008.2015
27.	Mishra, A., & Tanna, B. (2017). Halophytes: Potential Resources for Salt Stress Tolerance Genes and Promoters. Frontiers in plant science, 8, 829. https://doi.org/10.3389/fpls.2017.00829
28.	Muthusamy, S. K., Dalal, M., Chinnusamy, V., & Bansal, K. C. (2017). Genome-wide identification and analysis of biotic and abiotic stress regulation of small heat shock protein (HSP20) family genes in bread wheat. Journal of plant physiology, 211, 100–113. https://doi.org/10.1016/j.jplph.2017.01.004
29.	Nebreda AR, Porras A. p38 MAP kinases: beyond the stress response. Trends Biochem Sci. 2000;25:257–260.
30.	O′Donnell, M. J., Ianowski, J. P., Linton, S. M. and Rheault, M. R. (2003). Inorganic and organic anion transport by insect renal epithelia. Biochim. Biophys. Acta 1618, 194-206.
31.	Olvera-Carrillo, Y., Luis Reyes, J., & Covarrubias, A. A. (2011). Late embryogenesis abundant proteins: versatile players in the plant adaptation to water limiting environments. Plant signaling & behavior, 6(4), 586–589. https://doi.org/10.4161/psb.6.4.15042
32.	Pawłowicz, I., & Masajada, K. (2019). Aquaporins as a link between water relations and photosynthetic pathway in abiotic stress tolerance in plants. Gene, 687, 166–172. https://doi.org/10.1016/j.gene.2018.11.031
33.	Rane, R. V., Ghodke, A. B., Hoffmann, A. A., Edwards, O. R., Walsh, T. K., & Oakeshott, J. G. (2019a). Detoxifying enzyme complements and host use phenotypes in 160 insect species. Current opinion in insect science, 31, 131–138. https://doi.org/10.1016/j.cois.2018.12.008
34.	Rane, R. V., Pearce, S. L., Li, F., Coppin, C., Schiffer, M., Shirriffs, J., Sgrò, C. M., Griffin, P. C., Zhang, G., Lee, S. F., Hoffmann, A. A., & Oakeshott, J. G. (2019b). Genomic changes associated with adaptation to arid environments in cactophilic *Drosophila* species. BMC genomics, 20(1), 52. https://doi.org/10.1186/s12864-018-5413-3
35.	Riedl, C. A., Oster, S., Busto, M., Mackay, T. F., & Sokolowski, M. B. (2016). Natural variability in *Drosophila* larval and pupal NaCl tolerance. Journal of insect physiology, 88, 15–23. https://doi.org/10.1016/j.jinsphys.2016.02.007
36.	Riesch, R., Plath, M., Schlupp, I., Tobler, M., & Brian Langerhans, R. (2014). Colonisation of toxic environments drives predictable life-history evolution in livebearing fishes (Poeciliidae). Ecology letters, 17(1), 65–71. https://doi.org/10.1111/ele.12209
37.	Solomon A, Bandhakavi S, Jabbar S, Shah R, Beitel GJ, et al. Caenorhabditis elegans OSR-1 regulates behavioral and physiological responses to hyperosmotic environments. Genetics. 2004;167:161–170.
38.	Spring, J. H., Robichaux, S. R. and Hamlin, J. A. (2009). The role of aquaporins in excretion in insects. J. Exp. Biol. 212, 358-362.
39.	Stronach BE, Perrimon N. Stress signaling in *Drosophila*. Oncogene. 1999;18:6172–6182.
40.	Swire-Clark, G. A., & Marcotte, W. R., Jr (1999). The wheat LEA protein Em functions as an osmoprotective molecule in *Saccharomyces cerevisiae*. Plant molecular biology, 39(1), 117–128. https://doi.org/10.1023/a:1006106906345
41.	Van Breugel, F., Dickinson, M. H., & Meinwald, J. (2017). Superhydrophobic diving flies (*Ephydra hians*) and the hypersaline waters of Mono Lake. Proceedings of the National Academy of Sciences of the United States of America, 114(51), 13483–13488. https://doi.org/10.1073/pnas.1714874114
42.	Vicoso B, Bachtrog D (2015) Numerous Transitions of Sex Chromosomes in Diptera. PLoS Biol 13(4): e1002078. doi:10.1371/journal. pbio.1002078
43.	Waterman T. H. (1999). The evolutionary challenges of extreme environments (Part 1). The Journal of experimental zoology, 285(4), 326–359.
44.	Wieczorek, H., Beyenbach, K. W., Huss, M. and Vitavska, O. (2009). Vacuolar-type proton pumps in insect epithelia. J. Exp. Biol. 212, 1611-1619.
45.	Xu D, Duan X, Wang B, Hong B, Ho T and Wu R (1996) Expression of a late embryogenesis abundant protein gene, HVA1, from barley confers tolerance to water deficit and salt stress in transgenic rice. Plant Physiol. 110, 249±257. PMID: 12226181
46.	Xu X, Wang Q, Long Y, Zhang R, Wei X. Stress-mediated p38 activation promotes somatic cell reprogramming. Cell Res. 2013;23:131–141.
47.	Yandell, M., & Ence, D. (2012). A beginner’s guide to eukaryotic genome annotation. Nature Reviews Genetics. https://doi.org/10.1038/nrg3174
48.	Zargar, S. M., Nagar, P., Deshmukh, R., Nazir, M., Wani, A. A., Masoodi, K. Z., Agrawal, G. K., & Rakwal, R. (2017). Aquaporins as potential drought tolerance inducing proteins: Towards instigating stress tolerance. Journal of proteomics, 169, 233–238. https://doi.org/10.1016/j.jprot.2017.04.010
