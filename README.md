
# Identifying non-coding driver mutations in canine bone cancer

## Introduction

Osteosarcoma is an aggressive bone cancer that predominantly affects children and adolescents. Studying osteosarcoma is difficult because it is very rare in the human population. Dogs naturally develop osteosarcoma at much higher rates than humans which makes it a great model to study the disease. We have compiled a dataset of whole-genome sequencing data of tumors and blood of > 100 dogs with osteosarcoma and found evidence that somatic non-coding mutations on chromosome 21 might contribute to tumorigenesis.

## Background – Non-coding mutations 

Non-coding mutations can have an effect in cancer when they target regulatory element, such as promoters or enhancers. Functional or regulatory elements are often conserved across related species because they have been preserved by purifying selection. Therefore, functional elements in non-coding regions can be identified by aligning the genomes of many related species and searching for regions that are similar (conserved) across the genomes. 
The Zoonomia project (1) has aligned the genomes of 240 mammals including the dog and identified positions in the dog genome that are likely functional. 

## Aims

The aim of this project is to identify somatic non-coding candidate mutations for osteosarcoma using whole-genome sequencing and the Zoonomia functional elements.

## Data

For this purpose, we provide you with the following data:
-	BAM files of chromosome 21 of tumor and blood samples of a subset of the original dataset
-	A bed file with functional positions on chromosome 21 for the canine reference genome canFam4 identified by Zoonomia

## Taks

-	Perform somatic variant calling on the BAM files
-	Filter the somatic variants
    - How many somatic variants did you identify on chromosome 21?
-	Annotate the somatic variants
    - Hint: The annotation software snpEff has a pre-built functionality for runs on the canine reference genome
-	Extract somatic variants in functional elements
    - Hint: Have a look at the software vcftools for this task
    - How many functional non-coding variants did you identify on chromosome 21? 

### Additional taks:

-	Can you identify genes around which non-coding functional mutations cluster? Do you think they are likely candidates for osteosarcoma?

I have also provided a bed file that includes the positions of a set of known cis-regulatory elements. These were originally identified experimentally in the human genome and I lifted over (2) the positions to the dog genome.

-	Use this dataset to extract somatic variants in known regulatory elements and compare the variants to the ones you identified previously. Can you think of advantages and disadvantages for using either approach?

Read more about:
1 Zoonomia https://zoonomiaproject.org/
2 Liftover https://genome.ucsc.edu/cgi-bin/hgLiftOver

If you have any questions, please feel free to get in touch with me at raphaela.pensch@imbim.uu.se


## Downloads

The data is available for download at https://export.uppmax.uu.se/snic2022-6-165/

You can download the data using:

```
wget https://export.uppmax.uu.se/UU_3MR103_cancer_project2_data.tar.gz
wget https://export.uppmax.uu.se/UU_3MR103_cancer_project2_genome.tar.gz
wget https://export.uppmax.uu.se/UU_3MR103_project_bams.tar.gz
```

Decompress using:

```
tar -xzvf UU_3MR103_cancer_project2_data.tar.gz
tar -xzvf UU_3MR103_cancer_project2_genome.tar.gz
tar -xzvf UU_3MR103_project_bams.tar.gz
```
