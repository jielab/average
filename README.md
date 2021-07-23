
## AVERAGE: Automated Visualizing, Examining, Rechecking, and Alarming of Genomic Errors.

<br/><br/>

> ## The problem is that currently genotype data is static   
> - ### for rare and complex mutations such as that for Thalassemia, we need a system like the security check in the airport
> - ### The luggage (genome) is put on a rotating belt, an automatic system is in place to visualize and alert.
> - ### Security person (AVERAGE users) can also manusally examine and replace the luggage if they found something suspicious.

![London-Eye](./images/security.gif)

<br/><br/>  


> ## Ideally, we could see the sequencing data like below
> > - ### it is "graph-based". As we know, ACGT does not read well, and mutation is not simply single letter substitution.
> > - ### it is good to have "head-to-head comparison"

![ECG](./images/ecg.gif)

<br/><br/>   

> ## Right now, tools like [NGS4THAL](https://www.researchsquare.com/article/rs-542196/v1) aims to do the Bioinformatics part, in a "blackbox". However, 
> - ### Realign_BAM, which realigns a BAM file, and generates a new BAM file.
> - ### Talored_SV, which uses a bunch of existing SV tools to call SV.

[github](https://github.com/JavenCao)
 
It not “a one-stop molecular diagnosis and carrier screening tool for thalassemia” yet. 
It is debatable that “Realigh_BAM” could do a better job than BWA and GATK, which has been used by the international community for so long. 
Also, this NGS4THAL is NOT user-friendly, especially in community and clinical setting. 
Users do not know what is and how to manipulate huge BAM files.
 
We write some small external scripts to call IGV to load the genome and roll it at certain speed.
Then we add more scripts to evaluate and remapp potential structural variants (of the HB genes for Thalassemia), and set an alarm just like the sound beeping at the airport Baggage screening monitoring system.
