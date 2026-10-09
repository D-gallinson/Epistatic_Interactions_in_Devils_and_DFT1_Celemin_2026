# Epistatic interactions in the evolution of Tasmanian devils and their transmissible cancer

## Authors

Enrique Celemín<sup>1</sup>, Dylan G. Gallinson<sup>1</sup>, Marc A. Beer<sup>2</sup>, Rodrigo Hamede<sup>3,4</sup>, Menna E. Jones<sup>3</sup>, Andrew Storfer<sup>2</sup>, Mark J. Margres<sup>1</sup>

**Affiliations**

1. Department of Integrative Biology, University of South Florida, Tampa, FL, USA

2. School of Biological Sciences, Washington State University, Pullman, WA, USA

3. School of Natural Sciences, University of Tasmania, Hobart, TAS, Australia

4. CANECEV Centre de Recherches Ecologiques et Evolutives sur le Cancer, Montpellier, France

## Contact Details

**Corresponding Authors:**

* Enrique Celemín (e-mail: celeminamaro@usf.edu)

* Mark J. Margres (e-mail: margres@usf.edu)

## Study Summary

We investigated the largely unexplored role of epistasis—genetic interactions where one variant's effect depends on another—in host susceptibility to devil facial tumor disease 1 (DFT1), a transmissible cancer affecting Tasmanian devils. Using marginal epistasis tests on 312 devil-tumor paired genomes, we identified 50 candidate epistatic SNPs in the devils linked to functions like oxidative stress response, metabolic reprogramming, and disease avoidance. Conversely, we detected only two significant SNPs in DFT1, suggesting epistasis plays a smaller role in tumor transmissibility than in host susceptibility. Ultimately, these findings demonstrate that epistatic interactions contribute to disease-related traits in both the host and the transmissible cancer, emphasizing their importance in future studies of host-pathogen evolutionary dynamics.

### Additional Information

**Data Availability Statement**
All sequencing data for this project were made publicly available under Gallinson et al. (2024); see BioProject PRJNA947341 and accessions SRR23935061–SRR23936020.

**Author Contributions**
* Designed research: E.C., D.G.G., R.H., M.E.J., A.S., and M.J.M.
* Performed research: E.C., D.G.G., and M.J.M.
* Analyzed data: E.C. and D.G.G.
* Wrote the paper: E.C., D.G.G., and M.J.M.
* Collected samples: R.H. and M.E.J.

# File description
The devil and DFT1 phenotype files were used to separately run mvMAPIT. However, the files represent devil-DFT1 pairs, wherein both the devil and a tumor were biopsied and sequenced. Paired devil-DFT1 samples thus share the same six-digit microchip identifier and have an equivalent force of infection estimate between the two files.

## devil_phenotype.FOI.plink.tsv
The phenotype file used as input to mvMAPIT for the devil epistasis analysis. Columns are described below.
<ul>
  <li><b>FID:</b> Plink family ID representing the a priori sample relatedness. Because mvMAPIT estimates a genetic relatedness matrix as a random effect, we set this value to 1 for all samples to ignore relatedness.</li>
  <li><b>IID:</b> Plink individual ID (i.e., sample IDs). Devils were tagged with microchip transponders and each devil sample ID was formatted as "H-" followed by the final six digits of the microchip number.</li>
  <li><b>FOI:</b> The force of infection estimate calculated as the length of time (in days) it took for a susceptible devil to become infected with DFT1 (see manuscript Methods for details). Used as the phenotype input to mvMAPIT (i.e., response variable).</li>
  <li><b>first_infection:</b> Indicates if the sequenced tumor was the first to infect the sequenced devil (value=1) or not (value=0). Used as a covariate in mvMAPIT.</li>
</ul>

## DFT1_phenotype.FOI.plink.tsv
The phenotype file used as input to mvMAPIT for the DFT1 epistasis analysis. Columns are described below.
<ul>
  <li><b>FID:</b> Plink family ID representing the a priori sample relatedness. Because mvMAPIT estimates a genetic relatedness matrix as a random effect, we set this value to 1 for all samples to ignore relatedness.</li>
  <li><b>IID:</b> Plink individual ID (i.e., sample IDs). Devils were tagged with microchip transponders and each DFT1 sample ID was formatted as "T#-" (where "#" indicates the tumor number) followed by the final six digits of the microchip number. For devils with multiple tumors, tumors were numbered in order of descending size (e.g., the largest tumor is T1, the second largest tumor is T2, etc).</li>
  <li><b>FOI:</b> The force of infection estimate calculated as the length of time (in days) it took for a susceptible devil to become infected with DFT1 (see manuscript Methods for details). Used as the phenotype input to mvMAPIT (i.e., response variable).</li>
  <li><b>first_infection:</b> Indicates if the sequenced tumor was the first to infect the sequenced devil (value=1) or not (value=0). Used as a covariate in mvMAPIT.</li>
</ul>
