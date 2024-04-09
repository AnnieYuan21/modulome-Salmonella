# modulome-Salmonella
This repository contains datasets and scripts for the modulome-Salmonella project. Check out the paper [**here**]([https://www.biorxiv.org/content/10.1101/2022.01.11.475931v1](https://journals.asm.org/doi/10.1128/msystems.00467-22))

## **Figures**

Contains all the figures in the paper

## **data**

Contains all the data used for iModulon analysis for each strain and the core genome

In the folder of each strain, the data is organized as follows:
- **sequence_files**:sequence files
   - `CDS.fna`
   - `genome.fasta`
   - `genome.gff3`
   - `plasmid.fasta`
   - `plastmid.gff3`
- **raw_data**: raw data
   - `Salmonella_enterica_<STRAIN_NAME>.tsv`: raw metadata
   - `log_tpm.csv`: expression profile before qc and normalization
   - `multiqc_report.html`
   - `multiqc_stats.tsv`
- **external**: external annotation files
   - EggNOG annotations
   - TRN file
   - KEGG annotations
   - GO annotations
- **interim**: files created in intermediate steps of analysis
   - All ICA runs
   - `log_tpm_qc.csv`
   - `metadata_qc.csv`
- **processed_data**: processed data in ICA analysis
   - `log_tpm_norm.csv`: expression profile after qc and normalization
   - `metadata_curated_qc.csv`: curated metadata for expression profiles
   - `A.csv`: activity matrix from ICA output
   - `S.csv`: signal matrix from ICA output
   - `gene_info.csv`: gene annotations
   - `kegg_module_enrichments.csv`
   - `kegg_pathway_enrichments.csv`
## **json**

Contains all the iModulon objects in json files

## **notebooks**

Contains the ipynb used for analysis

- [**pymodulon**](https://github.com/SBRG/pymodulon): pymodulon functions
- `Figures.ipynb`: notebook for generating the figure in the Figures folder
- `expression_QC.ipynb`: quality control for the expression profiles
- `gene_annotations.ipynb`
- `iModulon_characterization.ipynb`
- `ica_dimensionality.ipynb`: choosing optimal ICA dimensionality
- `strain_iModulons.ipynb`

## **pangenome**

Contains data and code used for the pangenome analysis

- **bbh_results**: bi-directional blast hit results for all the strains
- `metadata.csv`: metadata used for pangenome analysis
- `pangenome_matrix.csv`
