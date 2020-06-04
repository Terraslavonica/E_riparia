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
Now we continue the functional annotation of the shore flies’ genomes by KEGG and eggNOG-mapper databases. More details see in the [laboratory journal](https://docs.google.com/document/d/147rQTXeOp-6CRlvWNGPbjIMCVoK0hkg7_j6raF1Ku7M/edit?usp=sharing).


## Results:
(1) We studied the articles dedicated to the adaptation of organisms to extreme environmental conditions and stress factors. Studying populations that adapt to life in extreme habitats is of great interest for evolutionary studies (Rane et al., 2019), because extreme conditions (physical and chemical stress factors) create a particularly interesting evolutionary context associated with solving the problems of maintaining the basic vital functions of the body in difficult conditions (Bang et al., 2018; Riesch et al., 2015; Waterman, 1999).

There are many levels of protection against stress factors, ranging from transcription regulation, post-transcriptional modification mechanisms, activation of certain metabolic pathways (Davies et al., 2014), ending with the compartmentalization of the body and the role of insect Malpighian tubules in fluid secretion, osmoregulation, and neuroendocrine regulation of ion transport (Beyenbach, 2003; O'Donnell et al., 2003; Coast, 2007; Spring et al., 2009; Wieczorek et al., 2009; Maddrell, 2009).

In response to increased salt concentrations and osmotic stress, the body reacts by activating signalling cascades such as p38 and JNK MAPK (Kyriakis et al., 1994; Kyriakis, Avruch, 1996; Han S.-J. et al., 1998; Stronach, Perrimon, 1999; Inoue et al., 2001; Craig et al., 2004; Gonzalez-Yanes et al., 2005; Bartels, Sunkar, 2005; Sun et al., 2006; Coulthard et al., 2009; Davies et al ., 2014; Reidly et al., 2016). The p38 kinase cascade is an ancient stress response system found in yeast, plants, and animals (Brewster et al., 1993; Han S.-J. et al., 1998; Han ZS et al., 1998; Kültz, 1998; Martín Blanco, 2000; Berman, 2001; Kyriakis, Avruch, 2001; Solomon et al., 2004; Teige et al., 2004; Lee et al., 2010; Xu et al., 2013). JNK MAPK (mitogen-activated protein kinase) is a signalling system that facilitates the transmission of a signal from the external environment to the nucleus to change the transcription of desired genes (Stronach, Perrimon, 1999; Martín-Blanco, 2000; Nebreda, Porras, 2000; Shen et al., 2003; Wagner, Nebreda, 2009).

LEA-proteins are included in the group of hydrophilins (and are usually characterized by a high content of glycerin amino acids in their composition) found in archaea, eubacteria and in the eukaryotic domain. Their role has not been fully understood, but they undoubtedly play an important role in the acclimation and adaptive response to stress (Imai et al., 1996; Xu et al., 1996; Swire-Clark and Marcotte, 1999; Zhang et al., 2000; Danyluk et al., 1994, 1998; Ismail et al., 1999a, 1999b; Puhakainen et al., 2004; Nakayama et al., 2007; Battaglia et al., 2008; Olvera-Carrillo et al., 2011; Gechev et al., 2012; Deinlein et al., 2014; Huang et al., 2016), including osmotic stress, because a deletion in the corresponding gene in E. coli leads to the appearance of an osmosis sensitive phenotype (Garay-Arroyo et al., 2000).

Heat shock proteins (hsp) are proteins whose expression increases during and after exposure to a wide range of stress factors. These proteins can also control other proteins important in response to stress, many of which have not been studied (Jensen et al., 2008; Muthusamy et al., 2017).

Aquaporins are a family of membrane proteins that regulate the movement of water molecules and other small molecules through plant vacuoles and plasma membranes. These proteins are inevitably associated with the tolerance of biotic and abiotic stresses by organisms (Maurel et al., 2015; Zargar et al., 2017; Mishra, Tanna, 2017; Pawłowicz, Masajada, 2019). For example, the transcription level of the GoPIP1 gene (related to aquaporins) was significantly increased when Galega orientalis was treated with 200 mM NaCl or 20% polyethylene glycol (PEG) 6000. (Li et al., 2015). It has been shown that aquaporins are extremely important in the regulation of many physiological processes in hematophagous arthropods, including in response to stress (Benoit et al., 2014).

The above are only examples of mechanisms and groups of proteins associated with a response to stress. A significant amount of proteins related to the response to stress continues to be discovered and studied. Thus, in a recent work by Das and colleagues in the genome of the bacterium Staphylococcus sp. living in saltwater, 10 proteins were found that contribute to resistance to great salinity, up to 20% NaCl in a laboratory environment (Das et al., 2020).

Thus, after the functional annotation of the shore flies’ genomes we will search the genes that can contribute to adaptation to extreme habitats and stressful conditions. It might be genes encoding LEA-proteins, heat shock proteins, aquaporins, metal-transport proteins, proteins that are the part of the signalling cascades p38 and JNK MAPK, etc.

(2) We assembled the *E. riparia* genome. The genome, about 600M bp, was assembled by SPAdes program into scaffold with average coverage 11.2x, with N50 equal 3.5K bp and L50 – 53K contigs. In assembly we detected 53% of genes typical for Diptera by BUSCO. Comparing with assemblies of close relatives, *E. gracilis* (410M bp, cov. 9.4x, N50 2.1K, L50 46K, BUSCO 81%) and *E. hians* (399M bp, cov. 27.0x, N50 1.8K, L50 53K, BUSCO 37%), we can conclude that *E. riparia* assembly is good enough for further analyses. More details see in the [laboratory journal](https://docs.google.com/document/d/147rQTXeOp-6CRlvWNGPbjIMCVoK0hkg7_j6raF1Ku7M/edit?usp=sharing) (items 8-16).

(3) We got a lot of annotated genes and metabolic pathway from functional annotation by KEGG and eggNOG-mapper databases. More details see in the [laboratory journal](https://docs.google.com/document/d/147rQTXeOp-6CRlvWNGPbjIMCVoK0hkg7_j6raF1Ku7M/edit?usp=sharing) (items 17-19).


## References:


