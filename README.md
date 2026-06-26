# BA_BL_with_lipid
Metagenomic, Transcriptomic Codes and R plot code
## Appendix

**Notes:**
① This document shows the description of result files corresponding to all analysis contents on the platform. Please check the corresponding analysis file descriptions according to the actual running results.
② `workflow_results`: workflow analysis result files; `interaction_results`: interaction analysis / supplementary analysis result files.

---

## Directory / File / File Description

### 1. `rawdata` — Raw data result directory

* `base_info.txt` — Raw sequence quality statistics table
* `base_quality_distribution.pdf.tar.gz` — Base quality plots and base distribution plots
* `reads.rawData.stat.xls` — Raw data statistics table for each sample

---

### 2. `QC_Stat` — Quality control result directory

* `reads.cleanData.stat.xls` — Quality-controlled data statistics table

---

### 3. `rm_host` — Host-removed sequence directory

* `stat.list.txt` — Statistics table of sequences after host removal for each sample

---

### 4. `assemble` — Assembly result files

* `assembly.stat.xls` — Assembly statistics table for each step
* `contig.length.pdf.tar.gz` — Contig length distribution plot
* `list.txt` — Sample list information table
* `*.contig.fa.tar.gz` — Assembled contig result files

---

### 5. `predict` — Gene prediction result directory

* `gene.length.pdf.tar.gz` — Predicted gene length distribution plot for each sample
* `genePredict_stat.xls` — Gene prediction result statistics table
* `*.metagene.more.100.fna.tar.gz` — Single-sample predicted gene sequence files

---

### 6. `geneset` — Non-redundant gene set result directory

#### `GENESET_Origin` — Non-redundant gene set result directory

##### `gene_profile` — Non-redundant gene abundance directory

* `gene.uniGeneset.fa.length.txt` — Gene length table
* `PPM.xls` — PPM abundance table of genes in each sample
* `reads_length_ratio.xls` — Gene abundance / gene length table for each sample
* `reads_length_ratio_relative.xls` — Relative gene abundance / gene length table for each sample
* `reads_number.xls` — Gene abundance table for each sample
* `reads_number_relative.xls` — Relative gene abundance table for each sample
* `reads_profile.tar.gz` — Compressed file containing relative abundance of gene read counts and gene read-count abundance
* `RPKM.xls` — RPKM abundance table of genes in each sample
* `TPM.xls` — TPM abundance table of genes in each sample

##### `uniGeneset` — Non-redundant gene set sequence statistics directory

* `gene.uniGeneset.fa.zip` — Compressed nucleotide sequence file of the non-redundant gene set

* `gene.uniGeneset.faa` — Protein sequence file of the non-redundant gene set

* `geneCatalog_stat.xls` — Statistics table of the number and length of non-redundant genes

* `anno_overview.xls` — Overview table of species and functional annotations

* `anno_stat.txt` — Statistics table of species and functional annotations

* `anno_stat.pdf` — Overview annotation result plot for species and functions

* `geneCatalog.length.pdf` — Length distribution plot of the non-redundant gene set

---

#### `CNPS_Database` — CNPS gene set result directory, personalized analysis

##### `Carbon_Metabolism / Nitrogen_Metabolism / Phosphorus_Metabolism / Sulfur_Metabolism`

CNPS metabolic gene set result directory

###### `gene_profile`

* `gene.uniGeneset.fa.length.txt` — Gene length table
* `PPM.xls` — PPM abundance table of genes in each sample
* `reads_length_ratio.xls` — Gene abundance / gene length table for each sample
* `reads_length_ratio_relative.xls` — Relative gene abundance / gene length table for each sample
* `reads_number.xls` — Gene abundance table for each sample
* `reads_number_relative.xls` — Relative gene abundance table for each sample
* `reads_profile.tar.gz` — Compressed file containing relative abundance of gene read counts and gene read-count abundance
* `RPKM.xls` — RPKM abundance table of genes in each sample
* `TPM.xls` — TPM abundance table of genes in each sample

###### `uniGeneset`

* `gene.uniGeneset.fa.zip` — Compressed nucleotide sequence file of the non-redundant gene set
* `gene.uniGeneset.faa` — Protein sequence file of the non-redundant gene set
* `geneCatalog_stat.xls` — Statistics table of the number and length of non-redundant genes

###### `length_distribute`

* `gene_step_*.final.txt` — Distribution result file of genes with different lengths
* `anno_overview.xls` — CNPS metabolic function overview table

---

### 7. `Abundance` — Abundance file result directory

#### `Abundance_*_*` — Analysis record number

* `tax_*_*.xls` — Abundance result table at different taxonomic levels using the corresponding abundance algorithm

---

### 8. `taxonomy_function_annotation` — Taxonomic and functional annotation result directory

---

## `Taxonomy_annotion` — Taxonomic annotation result directory

### `NR` — NR species annotation result directory

#### `nr_besthit / nr_origin` — NR database best-hit annotation result directory

* `gene_nr_anno.xls` — Taxonomic annotation table for each gene
* `nr_align_table.xls` — Species sequence alignment result table
* `tax_*.xls` — Annotation abundance table at different taxonomic levels
* `nr_genecount.stat.xls` — NR annotation statistics table

#### `nr_deunclassied` — NR database de-unclassified annotation result directory

* `gene_nr_anno.xls` — Taxonomic annotation table for each gene
* `nr_align_table.xls.zip` — Species sequence alignment result table
* `tax_*.xls` — Annotation abundance table at different taxonomic levels
* `nr_genecount.stat.xls` — NR annotation statistics table

#### `nr_LCA` — NR database LCA annotation result directory

* `gene_nr_anno.xls` — Taxonomic annotation table for each gene
* `nr_align_table.xls.zip` — Species sequence alignment result table
* `tax_*.xls` — Annotation abundance table at different taxonomic levels
* `nr_genecount.stat.xls` — Species gene-count information statistics table
* `nr_genecount.stat.xls` — NR annotation statistics table

---

## `Common_function_annotion` — Common functional annotation result directory

### `COG` — COG functional annotation result directory

* `gene_cog_anno.xls` — COG functional annotation table for each gene
* `cog_align_table.xls.zip` — COG functional sequence alignment result table
* `cog_*_profile.xls` — Abundance table at different COG functional levels in each sample
* `cog_genecount.stat.xls` — COG annotation statistics table
* `function_genecount.stat.xls` — Gene-count statistics table at the COG_Function level
* `cog_anno_stat.pdf` — COG_Function classification statistics plot

---

### `KEGG` — KEGG functional annotation result directory

* `gene_kegg_anno.xls` — KEGG functional annotation table for each gene
* `kegg_align_table.xls.zip` — KEGG functional sequence alignment result table
* `kegg_*_profile.xls` — Abundance table at different KEGG functional levels in each sample
* `pathway_img.tar.gz` — Pathway maps
* `kegg_KEGG_Name_profile.xls` — KEGG_Name abundance table
* `kegg_genecount.stat.xls` — KEGG annotation statistics table
* `keggpathway_classfication_sat.pdf` — Pathway classification bar plot

---

### `CAZY` — CAZy functional annotation result directory

* `gene_cazy_anno.xls` — CAZy functional annotation table for each gene
* `gene_dbCAN.hmmscan.out.dm.ds` — CAZy sequence alignment result table
* `gene_cazy_class_stat.xls` — Class-level gene information statistics table
* `gene_cazy_family_stat.xls` — Family-level gene information statistics table
* `cazy_*_profile.xls` — Abundance table at different CAZy functional levels in each sample
* `cazy_genecount.stat.xls` — CAZy annotation statistics table
* `cazy_class_genecount.stat.xls` — Gene-count statistics table at the CAZy_Class level
* `cazy_anno_stat.pdf` — CAZy_Class classification plot

---

### `ARDB` — ARDB antibiotic resistance gene annotation result directory

* `gene_ardb_anno.xls` — ARDB functional annotation table for each gene
* `ardb_align_table.xls` — ARDB sequence alignment result table
* `gene_ardb_class_stat.xls` — Class-level gene information statistics table
* `ardb_*_profile.xls` — Abundance table at different ARDB functional levels in each sample
* `ardb_genecount.stat.xls` — ARDB annotation statistics table
* `ardb_class_genecount.stat.xls` — Gene-count statistics table at the ARDB_class level
* `ardb_antibiotic_class_genecount.stat.xls` — Gene-count statistics table at the ARDB_antibiotic_class level
* `ardb_anno_class_stat.pdf` — ARDB_class classification plot
* `ardb_anno_antibiotic_class_stat.pdf` — ARDB_antibiotic_class classification plot

---

### `CARD` — CARD antibiotic resistance gene annotation result directory

* `gene_card_anno.xls` — CARD functional annotation table for each gene
* `card_align_table.xls` — CARD sequence alignment result table
* `card_genecount.stat.xls` — CARD annotation statistics table
* `card_antibiotic_class_genecount.stat.xls` — CARD_antibiotic_class annotation statistics table
* `card_*_profile.xls` — Abundance table at different CARD functional levels in each sample
* `card_anno_stat.pdf` — CARD_antibiotic_class annotation plot

---

### `VFDB` — VFDB virulence gene annotation result directory

* `gene_vfdb_total_anno.xls` — VFDB functional annotation table for each gene
* `vfdb_*_align_table.xls.zip` — VFDB prediction database sequence alignment result table
* `vfdb_level2.pdf.tar.gz` — Classification pie chart of predicted virulence genes
* `vfdb_genecount.stat.xls` — VFDB annotation statistics table

---

### `CNPS_Database` — CNPS annotation result files, personalized analysis

#### `Carbon_cycle / Nitrogen_cycle / Phosphorus_cycle / Sulfur_cycle`

* `*_Metabolism_annotation.xls` — CNPS annotation result table for different databases
* `function_count.txt` — Functional gene-count statistics table
* `gene_*_Metabolism_anno.xls` — Annotation result table for each gene
* `kegg_enzyme_profile.xls` — Enzyme abundance table
* `kegg_Function_profile.xls` — Function abundance table
* `kegg_gene_profile.xls` — KEGG gene abundance table
* `kegg_KO_profile.xls` — KO abundance table
* `kegg_KEGG_Name_profile.xls` — KEGG_Name abundance table

---

## `Personal_Anno` — Personalized database annotation result directory

### `GO` — GO functional annotation result directory

* `all.go.annotation.xls` — GO annotation table showing the corresponding annotated genes for each sample
* `all.*.function.xls` — Abundance table for each sample at different GO classification levels
* `go.level4.xls` — Abundance table for each sample at GO level 4
* `go1234level_statistics.xls` — Annotation details table at different GO classification levels
* `go_level_bar.pdf.tar.gz` — GO annotation classification bar plot

---

### `Phi` — PHI result directory

* `gene_phi_anno.xls` — PHI functional annotation result information table
* `phi_*_profile.xls` — Abundance table at different PHI classification levels for each sample
* `phi_phenotype_bar.pdf.tar.gz` — Phenotype gene abundance plot
* `phi_genecount.stat.xls` — PHI annotation statistics table

---

### `MvirDB` — MvirDB functional annotation result directory

* `function_select_anno.xls` — MvirDB functional annotation table for each gene
* `*_gene_stat.xls` — Gene list for each sample
* `*_abund_out.xls` — Abundance table for each sample
* `mvir_genecount.stat.xls` — MvirDB annotation statistics table

---

### `Tcdb`

* `TCDB功能注释结果目...` — TCDB functional annotation result directory
  *The original text appears to be cut off after this line.*
