# Data-Science-in-Health-Sector

Sample GSM2310417		Query DataSets for GSM2310417
Status	Public on Oct 28, 2016
Title	MTP12
Sample type	SRA
 	
Source name	Bone marrow derived macrophage precursors
Organism	Mus musculus
Characteristics	strain: C57BL/6
tissue: Bone marrow
condition: 6 days M-CSF+ FSL-1 treatment
dna content: greater than 4c
Treatment protocol	Cells were re-plated in OptiMEM medium and stimulated with M-CSF (50ng/ml) ('control') or M-CSF (50ng/ml) and (FSL-1 20ng/ml) for 6 days.
Growth protocol	Bone marrow cells were flushed from the femurs of mice and cultured with murine M-CSF (20 ng/ml) on petri dishes in DMEM supplemented with 10% FBS for 4-5 days. The adherent cell population (referred to as ‘macrophage precursors’) was then recovered and plated at 2x104 cells/ml in OptiMEM medium containing 10% FBS and 50ng/ml M-CSF.
Extracted molecule	total RNA
Extraction protocol	Hoechst staining was performed on control and FSL-1 treated cells to quantify the DNA content and single cells were FACS-sorted using BD Influx in 384-well plates.
As described in CEL-Seq2 protocol (Hashimshony et al. 2016)
Adapted from TruSeq Small RNA Library Preparation Protocol
 	
Library strategy	RNA-Seq
Library source	transcriptomic
Library selection	cDNA
Instrument model	Illumina HiSeq 2500
 	
Description	library of 96 >4c FSL-1 treated cells
Data processing	For image aquisition, intensity extraction and basecalling HiSeq Control Software 2.0.2, RTA 2.4.11 / Recipe Fragment 2.0.0.2​ was used. Conversion of bcl2fastq files was performed using bcl2fastq 2.17.1.14
Paired end reads were aligned to the transcriptome using bwa (version 0.6.2-r126) with default parameters. The transcriptome contained all RefSeq gene models based on the mouse genome release mm10 downloaded from the UCSC genome browser. All isoforms of the same gene were merged to a single gene locus.
The 65bp right mate of each read pair was mapped to the ensemble of all gene loci and to the set of 92 ERCC spike-ins in sense direction (Baker et al., 2005). Reads mapping to multiple loci were discarded.
The 25bp left read contains the barcode information: the first six bases corresponded to the cell specific barcode followed by six bases representing the unique molecular identifier (UMI). The remainder of the left read contains a polyT stretch. The left read was not used for quantification.
For each cell barcode, the number of UMIs per transcript were counted and aggregated across all transcripts derived from the same gene locus.
Based on binomial statistics, the number of observed UMIs were converted into transcript counts (Grün et al., 2014).
Genome_build: mm10
Supplementary_files_format_and_content: CSV files, columns represent each cell barcode (total barcodes used = 192), rows represent the geneid and the values in the file are the quantified number of transcripts.
 	
Submission date	Sep 14, 2016
Last update date	Oct 28, 2016
Contact name	Sagar -
E-mail	sagar@ie-freiburg.mpg.de
Organization name	Max Planck Institute Freiburg
Lab	Dominic Grün
Street address	Stübeweg 51
City	Freiburg
ZIP/Postal code	79108
Country	Germany
 	
Platform ID	GPL17021
Series (1)	
GSE86929	Single cell RNA sequencing analysis of bacterial lipoprotein-induced polyploid macrophages.
Relations
BioSample	SAMN05772502
SRA	SRX2163675

Link of Dataset - https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSM2310417
