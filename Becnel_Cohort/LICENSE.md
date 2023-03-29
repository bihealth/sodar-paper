7 donors (mixed tumor entities) & 19 samples:

- 7 whole exome sequencing normal/tumor pairs (`case001` to `case007`),
- 2 whole genome sequencing normal/tumor pairs (`case006` & `case007`), and
- 1 mRNA expression (`case007`)

Publication: [Becnel, L., Pereira, S., Drummond, J. _et al._ An open access pilot freely sharing cancer genomic data from participants in Texas. _Sci Data_ **3**, 160010 (2016)](https://doi.org/10.1038/sdata.2016.10)

# Important information on data usage

By downloading or utilizing any part of this dataset, end users must agree to the following conditions of use:

- No attempt to identify any specific individual represented by these data or any derivatives of these data will be made.
- No attempt will be made to compare and/or link this public data set or derivatives in part or in whole to private health information.
- These data in part or in whole may be freely downloaded, used in analyses and repackaged in databases.
- Redistribution of any part of these data or any material derived from the data will include a copy of this notice.
- The data are intended for use as learning and/or research tools only.
- This data set is not intended for direct profit of anyone who receives it and may not be resold.
- Users are free to use the data in scientific publications if the providers of the data (Texas Cancer Research Biobank and Baylor College of Medicine Human Genome Sequencing Center) are properly acknowledged.

# Data processing

The data was mapping and processed against the human genome assembled by the [GDC center](https://gdc.cancer.gov/about-data/gdc-data-processing/gdc-reference-files). It consists of the GRCh38 human genome release, with decoys and viral sequences commonly found in cancers. The feature annotations were taken from GENCODE release 33.

### Software used in processing

- Mapping using `bwa`[1] for whole exome & whole genome data, and using `STAR`[2] for mRNA expression data,
- Somatic variant calling using `mutect2`[3], with the [panel of normals provided by GATK](https://console.cloud.google.com/storage/browser/gatk-best-practices/somatic-hg38),
- Somatic variant annotation using `jannovar`,
- Copy Number variants using `CopywriteR`[4] for whole exome and `Control-FREEC`[5] for whole genome data.

References:

- [1] Li H. (2013) "Aligning sequence reads, clone sequences and assembly contigs with BWA-MEM." [arXiv:1303.3997v2](http://arxiv.org/abs/1303.3997)
- [2] Dobin A., Davis C.A., Schlesinger F., Drenkow J., Zaleski C., Jha S., Batut P., Chaisson M. & Gingeras T.R. (2013) "STAR: ultrafast universal RNA-seq aligner." _Bioinformatics_ **29**(1):15-21.
- [3] Benjamin D., Sato T., Cibulskis K., Getz G., Stewart C. & Lichtenstein L. (2019) "Calling Somatic SNVs and Indels with Mutect2." [biorXiv:10.1101/861054](https://doi.org/10.1101/861054)
- [4] Kuilman T., Velds A., Kemper K., Ranzani M., Bombardelli L., Hoogstraat M., Nevedomskaya E., Xu G., de Ruiter J., Lolkema M., lstra B., Jonkers J., Rottenberg S., Wessels L., Adams D., Peeper D. & Krijgsman O. (2015) "CopywriteR: DNA copy number detection from off-target sequence data." _Genome Biology_ **16**(1):49
- [5] Boeva V., Popova T., Bleakley K., Chiche P., Janoueix-Lerosey I., Delattre O. & Barillot E. (2012) "Control-FREEC: a tool for assessing copy number and allelic content using next generation sequencing data. _Bioinformatics_ **28**(3):423-5.
