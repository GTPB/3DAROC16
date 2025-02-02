# 3DAROC
<p>
<img align="right" src=/Documents/Logo/Foto-DNA_MMarti_0.jpg?raw=True>
<h2>Course description</h2><br>
3C-based methods, such as Hi-C, produce a huge amount of raw data as pairs of DNA reads that are in close spatial proximity in the cell nucleus. Overall, those interaction matrices have been used to study how the genome folds within the nucleus, which is one of the most fascinating problems in modern biology. The rigorous analysis of those paired-reads using computational tools has been essential to fully exploit the experimental technique, and to study how the genome is folded in the space. Currently, there is a clear expansion on the wealth of data on genome structure with the availability of many datasets of Hi-C experiments down to 1Kb resolution (see for example: http://hic.umassmed.edu/welcome/welcome.php ; http://promoter.bx.psu.edu/hi-c/view.php or http://www.aidenlab.org/data.html ). In this course, participants will learn to use TADbit, a software designed and developed to manage all dimensionalities of the Hi-C data:
</p>


 - 1D - Map paired-end sequences to generate Hi-C interaction matrices
 - 2D - Normalize matrices and identify constitutive domains (TADs, compartments)
 - 3D - Generate populations of structures which satisfy the Hi-C interaction matrices
 - 4D - Compare samples at different time points

Participants can bring- specific biological questions and/or their own 3C-based data to analyze during the course. At the end of the course, participants will be familiar with the TADbit software and will be able to fully analyze Hi-C data. Note: Although the TADbit software is central in this course, alternative software will be discussed for each part of the analysis.

## Target Audience

The course design is oriented towards experimental researchers and bioinformaticians at the graduate and post-graduate levels. The last edition of this course was attended by people with different backgrounds and interested in the genome organization.
Moreover, Hi-C data have recently been used in metagenomics studies to accurately cluster metagenome assembly contigs into groups that contain nearly complete genomes of each species.
It is likely that the participants to this course aim at getting involved in generating Hi-C data for chromosome structure determination or that they just want to be able to correctly interpret and analyse publicly available data. 

## Course Pre-requisites

Recommended Linux and basic Python programming skills, graduate level in Life Sciences.


## Content

|                  | Lectures (pdf)                          | Core pipeline (notebooks)               | Annex (notebooks)                 | Feedback (1: not clear; 5: very clear) |
|-------------------|----------------|-------------------------|------------|------|
| Day1 | <ul><li>[Welcome](/Presentations/Day1/01_20161010_Welcome.pdf)</li><li>[Intro structure determination](/Presentations/Day1/02_20161010_introduction_to_structure_determination.pdf)</li><li>[3D Genomes overview](/Presentations/Day1/03_20161010_3D-genomes_overview.pdf)</li><li>[Intro TADbit](/Presentations/Day1/04_20161010_Intro_TADbit.pdf)</li><li>[NGS for HiC](/Presentations/Day1/05_20161010_NGS_for_HiC.pdf)</li><li>[Intro UNIX](/Presentations/Day1/06_20161010_linux.pdf)</li><li>[Intro Python](/Presentations/Day1/07_20161010_python.pdf)</ul></li> |<ul><li>[Hi-C Quality check](/Notebooks/00-Hi-C quality check.ipynb)</li><li>[Mapping](/Notebooks/01-Mapping.ipynb)</li><li>[Parsing mapped reads](/Notebooks/02-Parsing mapped reads.ipynb)</li></ul> | <ul><li>[Software installation](/Notebooks/A0-Preparing your computer for HiC data analysis.ipynb)</li><li>[Prepare reference genome](/Notebooks/A1-Preparation reference genome.ipynb)</li><li>[Download Hi-C experiment](/Notebooks/A2-Download published Hi-C experiments.ipynb)</li></ul> | <li>Integrative modeling: 4.7</li><li>FASTQ/Hi-C quality check: 4.8</li><li>Mapping: 4.9</li>|
| Day2 | <ul><li>[Morning wrap up](/Presentations/Day2/01_20161011_Summary_of_day_1.pdf)</li><li>[Chromatin and 3Cs](/Presentations/Day2/02_20161011_Chromatin_and_3Cs.pdf)</li><li>[Integrative modeling](/Presentations/Day2/03_20161011_IntegrativeModeling.pdf)</li><li>[Applications(I): Alpha globin](/Presentations/Day2/04_20161011_Applications(I)_alpha_globin.pdf)</li></ul>| <ul><li>[Filterind reads](/Notebooks/03-Filtering mapped reads.ipynb)</li><li>[Normalization](Notebooks/04-Bin-filtering and normalization.ipynb)</li></ul> | <ul><li>[Compare/merge experiments](/Notebooks/A3-Compare and merge Hi-C experiments.ipynb)</li></ul> | <li>Genome organization: 4.9</li><li>3D modeling: 3.7</li><li>Filtering/normalization: 4.2</li>|
| Day3 | <ul><li>[Morning wrap up](/Presentations/Day2/01_20161012_Summary_of_day_2.pdf)</li><li>[Applications(II): Caulobacter](/Presentations/Day2/02_20161012_Applications(II)_Caulobacter.pdf)</li><li>[Applications(III): TAD hormone](/Presentations/Day2/02_20161012_Applications(III)_TAD_hormone.pdf)</li><li>[Normalization & comparison](/Presentations/Day2/02_20161012_NormalizationComparison.pdf)</li></ul>| <ul><li>[Compartments and TADs](/Notebooks/05-Compartments and TADs.ipynb)</li></ul> | <ul><li>[Align and compare TADs](/Notebooks/A4-Align and compare TADs.ipynb)</li></ul> | <li>Validation 3D models: 0.0</li><li>Compartment/TAD calling: 4.5</li><li>TADbit usage: 4.2</li>|
| Day4 | <ul><li>[Morning wrap up](/Presentations/Day4/01_20161013_Summary_of_day_3.pdf)</li><li>[Applications(IV): Fly colors](/Presentations/Day4/02_20161013_Applications(IV)_FlyColors.pdf)</li></ul>| <ul><li>[Parameter optimization](/Notebooks/06a-Modeling - parameter optimization.ipynb)</li><li>[Model optimization](/Notebooks/06b-Modeling - model optimization.ipynb)</li></ul> | <ul><li>[Analysis of 3D models](/Notebooks/A5-Modeling - analysis of 3D models.ipynb)</li></ul> |
| Day5 | <ul><li>[Nucleosome dynamics](/Presentations/Day5/nucleosome_dynamics.pdf)</li><li>[DNA and chromatin dynamics](/Presentations/Day5/nucleosome_dynamics.pdf)</li></ul>|  |  |

## TADbit tools

Most of the tasks of the "core pipeline" can be tunned directly from command line (without any python), using [TADbit tool](/TADbit_tools). Have a look to the commands, and the metadata of the results. 

_For now TADbit tool is not incuded in the general documetation, as it is still "under construction". Use it carefully, and don't hesitate to repport anyweird behaviour you observe._


## TADbit version

This tutorial is associated with a __specific version of TADbit__, if you wish to reproduce exactly the results in the notebooks you should use the version of TADbit tagged `3DAROC_2016`.

To install this version do:

    git clone https://github.com/3dgenomes/tadbit
    cd tadbit
    git checkout tags/3DAROC_2016
    sudo python setup.py install


# Want more?
<p>

<img align="left" src=http://www.crg.eu/sites/default/files/styles/134x192_events_list/public/events/CRG_Cromosomal_conformation-2016_0.jpg?itok=v0rQ9D9X&raw=True>
<h2>COURSES@CRG: Chromosomal Conformation</h2>
5 days course (<b>28/11/2016 to 02/12/2016</b>) in Barcelona, to <b>learn how to perform 3C experiments</b> and assess their quality through different <b>quality controls</b>. The course will also provide the basic bioinformatic knowledge to analyze the data generated.</p>

- http://www.crg.eu/en/event/coursescrg-chromosomal-conformation-0



