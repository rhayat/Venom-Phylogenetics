The Input data is contained in the file final.fasta. 
1. Load the Jupyter Notebook file and run the file to the end. This will generate the aligned_sequences.nexus file which acts as the input to MrBayes.
2. Open the MrBayes application file
3. In the prompt, write the following commands in this order to get the Trees and Evaluation:
	1. execute aligned_sequences.nex
	2. prset aamodelpr=fixed(Jones)
	3. constraint clade1 = crotalus_durissus_cumanensis crotalus_horridus
	4. constraint clade2=bothrops_asper bothrops_pauloensis bothrops_jararaca bothrocophias_hyoprora bothrops_atrox bothrops_brazili bothrops_marajoensis
	5. constraint clade3=daboia_russelii daboia_siamensis
	6. constraint clade4=naja_naja pseudonaja_textilis laticauda_laticaudata
	7. constraint clade5= agkistrodon_piscivorus_leucostoma agkistrodon piscivorus piscivorus
	8. prset topologypr=constraints(clade1, clade2, clade3,clade4,clade5)
	9. mcmc nchains=1 ngen=30000
	10. sumt

Execution of these commands will yield summary of evaluation metrics and most probable phylogenetic tree.
Summary has been provided for the source of ease in a seperate text file labeled 'Final_summary.txt' 