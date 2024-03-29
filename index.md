# About me
I’m a Biostatistics master’s graduate from the University of Zurich, Switzerland. Prior to my master’s degree I worked as a research assistant at the Swiss Federal Institute of Technology in Zurich at the Center for Law and Economics, where I helped design and evaluate economic experiments in a lab and classroom setting. For my master’s thesis I worked on a project where we investigated methods that detect differentially regulated genes e.g. [eisaR](https://bioconductor.org/packages/release/bioc/html/eisaR.html), [BRIE2](https://brie.readthedocs.io/en/latest/) and compared the performance with a novel Bayesian approach [DifferentialRegulation](http://www.bioconductor.org/packages/release/bioc/html/DifferentialRegulation.html) on a semi-simulated data set based on mouse kidney single-cell RNA-seq data.

Please feel free to contact me via email: joel.meili@gmail.com

## Research interests
### Bioinformatics
I'm particularly interested in cancer research and how bioinformatics and machine learning can be used to better understand the mechanisms at work to ultimately provide better health care for patients.

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
on the mouse kidney data to evaluate the computational burden of each method. [PDF](/assets/files/masters_thesis.pdf)

### Statistical consulting project - Beneft of prolonged and earlier treatment of Hepatocellular carcinoma patients with TACE
This study aims to investigate if there is a benefit of prolonged and earlier treatment of hepatocellular
carcinoma (HCC) patients with TACE. Patients were seen regularly for at least five years. The methods
used were Kaplan-Meier plots, competing risk analysis and Cox-regression. The analysis is subject to
the assumption that the patients in BCLC stages 0-A and C are not representative as patients are
probably more/less ill than the average patient in said stage. The analysis showed that there is
a tendency for improved overall survival for patients in BCLC stages B and C. Contrarily, TACE
did not improve the overall survival for patients of the earlier stages 0 and A. The comparison of
overall and progression-free survival curves between the different BCLC stages showed that there is no
evidence for a difference between patients in stages 0-A and B. Competing risk analysis showed that
patients regardless of their staging die quickly from hepatic failure compared to other causes of death.
Confounders such as sex, age and underlying conditions did not influence the effect of the BCLC stages
on the overall survival. Based on the results we would recommend only patients of BCLC stages B
and C to receive earlier and prolonged treatment with TACE. [PDF](/assets/files/report_STA490_meili.pdf)

### Deep Learning for Medical Computer Vision - COVID19 lesion segmentation with CT images
The following was the implementation of a machine learning configuration that uses a segmentation model, in this case [FPN](https://segmentation-modelspytorch.readthedocs.io/en/latest/docs/api.html#fpn), with pre-trained weights to predict the masks of COVID19 lesions from CT images. The code was implemented in the PyTorch framework with a positive-to-negative ratio of 2 (double the amount of images with an actual pixel highlighting a lesion). 

The goal of this semester project was to find a data set with segmentation data and implement a pre-built segmentation algorithm to experiment with hyperparameters in the training process (trained on DICE loss) and do inference on the predicted masks (compare IoU scores). [GitHub repo](https://github.com/joelmeili/COVIDPrediction)

### COVID19 Dashboard - Simulating a SIRD model
An attempt to model the COVID19 data from the [Johns Hopkins Github Repository](https://github.com/CSSEGISandData) by a SIRD model for various countries such as Germany, Switzerland and the US. This Github repository contains a shiny app that estimates the model parameters and then simulates the disease would progress based on these estimates. [GitHub repo](https://github.com/joelmeili/COVID19)

A live version of the shiny app can be found [here](https://joelmeili.shinyapps.io/COVID19_Dashboard).
