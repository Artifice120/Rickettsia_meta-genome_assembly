# Rickettsia_meta-genome_assembly

Short reads were initially assembled with spades to supplement the hybrid assembler Wengan as the short read draft assembly was more complete that the default Discovar denovo assembler that Wengan uses as the default for the initial assembly of unitigs.

After assemblying the short reads in spades the unitigs were assigned taxonomy and filtered with BLAST+ and Blobtools.

This filtered short read assembly was then entered into the Wengan hybrid assembly pipeline. Since the short reads were already filtered by taxonomy there was no nead to filter the long reads as only long reads that had suppport from short-read unitigs are kept by default.

After ensuring the BUSCO completness remained the same, the assembly was then annotated with prokka and p-gap ( rickettisa bellii model )

All rickettisa refrence genomes were then downloaded and annotated with prokka for consistency in gene predictions

Resulting gff files were then gene clustered with OrthoFinder to form a list of consierved genes that were used to inferphylogeny using the STAG algorithm with wolbachia as an outgroup.

# Figures

### Syntetny to Rickettsia Bellii

![Rickettisia](https://github.com/user-attachments/assets/c82e6e7f-746b-4579-8ffa-23fe3c205d51)

### Snail plot summary of hybrid assembly

![Rickettsia_patched snail](https://github.com/user-attachments/assets/364719eb-d816-49bc-935f-1cbe612f8ba1)
