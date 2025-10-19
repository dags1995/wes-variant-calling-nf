# WES Germline Variant Calling Pipeline (Nextflow + Docker)

## Overview
This personal project aims to implement a reproducible **germline variant calling** pipeline from **Whole Exome Sequencing (WES)** data, following best practices.

The workflow will be orchestrated with **Nextflow** and prepared to be executed using **Docker cointainers** to ensure full reproducibility and portability.


---

## Plannend Pipelines Stages
- **FastQC** - raw read quality control
	- **fastp** - optional trimming based on QC
- **BWA-MEM** - alignment to a reference genome
- **Samtools** - sorting, indexing and dupicate marking
- **GATK Haplotypecaller** - germline variant calling (VCF generation)


---

## Technologies
- **Nextflow** - workflow orchestration
- **Docker** - containerized execution
- **FastQC / fastp / BWA / Samtools / GATK** - standand genomic tools


---

## Innitial Folder Structure
```
wes-variant-calling-nf/
├── data/		
│   ├── raw/		# user-provided FASTQ files
│   └── reference/	# reference genome files
├── results/		# output folder (BAM files, VCF, QC reports, etc.)
│   ├── bam/
│   ├── qc/
│   └── vcf/
├── scripts/		# optional helper scripts
└── workflow/		# Nextflow pipelines files (main.nf, config, modules)
```

---

## Data 

Place your **FastQ** files inside data/raw/


The **Reference Genome** will be required under data/reference/


---

