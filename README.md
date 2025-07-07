# PedcBioPortal ETL References

<p align="center">
  <img src="docs/logo/kids_first_logo.svg" alt="Kids First repository logo" width="660px" />
</p>
<p align="center">
  <a href="https://github.com/kids-first/kf-cbioportal-etl-refs/blob/main/LICENSE"><img src="https://img.shields.io/github/license/kids-first/kf-cbioportal-etl-refs.svg?style=for-the-badge"></a>
</p>

This repo houses reference and configuration files for the [PedcBioPortal ETL](https://github.com/kids-first/kf-cbioportal-etl).
The purpose is to separate support files from the ETL that are not code-related for proper software versioning and to better support automation.

## Production Reference File Summary
Below is a summary of ETL references and how they are used in practice

### Regularly Used
 - `REFS/healthy_expressions.tar.gz`: TAR GZ of RNAseq Z score normalization references. Currently contains:
   - healthy_expressions/healthy_polyA_log_FPKM.tsv
   - healthy_expressions/healthy_totalRNA_log_FPKM.tsv
   - healthy_expressions/healthy_polyA_log_TPM.tsv
   - healthy_expressions/healthy_totalRNA_log_TPM.tsv
 - `REFS/Homo_sapiens.GRCh38.105.chr.gtf_genes.bed`: Gene coordinates with Hugo gene symbols used to standardize gene annotation of CNV data
 - `REFS/maf_KF_CONSENSUS_r105.txt`: MAF header file used to standardize MAF output
 - `REFS/template_patient_header.txt` data_clinical_patient.txt template header with all valid fields that can be used for patient view
 - `REFS/template_sample_header.txt`: data_clinical_sample.txt template header with all valid fields that can be used for sample view

### Legacy/Utility/Deprecated
 - `REFS/EntrezGeneId_HugoGeneSymbol_2021-06-01.txt`: Entrez gene ID + Hugo Symbol reference matching current ENSEMBL 105 annotation
 - `REFS/GRCh38.84.gtf_genes.bed`: Bed file used for CNV annotation `ljaz_cole` publication
 - `REFS/type_of_cancer.txt` List of cBioportal cancer types

## Production Config File Summary
 - `STUDY_CONFIGS/all_studies_config_values.tsv`: Table used by ETL to generate study-specific config file sto run the ETL. Edit this to modify file types, data type descriptions, study descriptions, ETL run time params, etc.
 - `json_files`: Directory with legacy config files.