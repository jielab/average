
# AVERAGE: Automated Visualizing, Examining, Remapping, and Alerting of Genomic Errors.

[NGS4THAL](https://www.researchsquare.com/article/rs-542196/v1) has two components:
1. Realign_BAM, which realigns a BAM file, and generates a new BAM file.
2. Talored_SV, which uses a bunch of existing SV tools to call SV.

[github](https://github.com/JavenCao)
 
It not “a one-stop molecular diagnosis and carrier screening tool for thalassemia” yet. 
It is debatable that “Realigh_BAM” could do a better job than BWA and GATK, which has been used by the international community for so long. 
Also, this NGS4THAL is NOT user-friendly, especially in community and clinical setting. 
Users do not know what is and how to manipulate huge BAM files.
 
We write some small external scripts to call IGV to load the genome and roll it at certain speed.
Then we add more scripts to evaluate and remapp potential structural variants (of the HB genes for Thalassemia), and set an alarm just like the sound beeping at the airport Baggage screening monitoring system.
