# TerenzioU_AgedvsYoungDRGProteomics
R script containing proteomics analysis for up-regulated or down-regulated proteins in cell body and axon of DRG neurons from late adulthood (52-63 w.o.) and adolescent (8-10 w.o.) mice.

Protein candidates were acquired and analyzed using Proteome Discoverer v3.1 (Thermo Fisher Scientific) with Chymerys algorithms using label-free quantification methods. The data were queried against a Uniprot/SWISS-Prot database for Mus musculus database (UP000000589.fasta, 54,727 proteins, April 2024). Mus musculus data base(https://github.com/user-attachments/assets/dfa22fb7-1d9f-497c-a521-6f030a96fc5e)

Outline of analysis: 
Two filtering steps were performed. In the first step of filtering, "Proteomics_RAW_all.Rmd" was used to filter proteins that were missing values in 2 or more technical repeats. In the second filtering step, "DEqMS_normalize_all.Rmd" was used to analyze proteins that were not significant (sca p.val>0.1) against their negative anisomycin-treated control. In this step, median normalization was used. 

After filtering steps, proteins that were up-regulated or down-regulated in the cell body and axon of DRG from late adulthood and adolescent mice were analyzed using "DEqMS_yng_vs_old_all.Rmd". The script also contains the code for visualization using volcano plot (https://bioconductor.org/packages/devel/bioc/vignettes/EnhancedVolcano/inst/doc/EnhancedVolcano.html) and heat map (https://github.com/raivokolde/pheatmap). 

Both "DEqMS_normalize_all.Rmd" and "DEqMS_yng_vs_old_all.Rmd" were written according to DEqMS script instructions and package (https://www.bioconductor.org/packages/release/bioc/html/DEqMS.html) 




