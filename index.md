# About me
I'm a Biostatistics master's graduate from the University of Zurich, Switzerland. Prior to my master's degree I worked as a research assistant at the Swiss Federal Institute of Technology in Zurich at the Center for Law and Economics, where I helped design and evaluate economic experiments in a lab and classroom setting. For my master's thesis I worked on a project where we investigated methods that detect differentially regulated genes e.g. [eisaR](https://bioconductor.org/packages/release/bioc/html/eisaR.html), [BRIE2](https://brie.readthedocs.io/en/latest/) and compared the performance with a novel Bayesian approach [DifferentialRegulation](http://www.bioconductor.org/packages/release/bioc/html/DifferentialRegulation.html) on a semi-simulated data set based on mouse kidney single-cell RNA-seq data.

## Research interests
### Bioinformatics

## Projects
### Master's thesis - Differential gene regulation
Single-cell RNA sequencing data has become more and more popular over the past few years.
It allows biological questions to be answered that with bulk RNA sequencing could not be
answered as cell-specific characteristics can be analyzed. In this thesis we investigate, in each
cell cluster (e.g. cell type), how the relative abundance of spliced and unspliced reads varies
between experimental conditions. Changes to these relative abundances are directly linked to
gene regulation, therefore differences in these proportions are taken as a proxy for differences in
gene regulation. Methods that are capable of detecting differences in relative abundance already
exist (e.g. BRIE2 and eisaR), however they neglect two sources of mapping uncertainty: i) multi-
mapping reads across spliced and unspliced versions of a gene, and ii) reads compatible with
multiple genes. Therefore, we propose a novel method, DifferentialRegulation, that tackles this
issue and evaluate the performance of the existing methods (BRIE2, DEXSeq and eisaR) and our
novel approach. For this, we created two semi-simulated data sets using real mouse kidney single-
cell RNA sequencing data as an anchor data set to simulate from. From the analysis we conclude
that the two methods that account for mapping uncertainty (DEXSeq and DifferentialRegulation)
have significantly higher TPR and better control of FDR than the methods that ignore mapping
uncertainty. Additionally, we studied methods robustness by investigating how gene abundance
levels, and differential gene expression (a nuisance effect in this analysis), affect the results of
each method. We also ran a null analysis on a real data set (where no differences between groups
are expected), to study methods’ false positive rates. Lastly, we ran a computational benchmark
on the mouse kidney data to evaluate the computational burden of each method.

### Statistical consulting project - Beneft of prolonged and earlier treatment of Hepatocellular carcinoma patients with TACE
