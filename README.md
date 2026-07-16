# Workflows and tools developed for the ATLASea programme

The ATLASea programme aims to build a comprehensive reference atlas of marine eukaryotic genomes from species found across the French metropolitan and overseas exclusive economic zones. By combining specimen collection, taxonomic identification, high-throughput sequencing, genome assembly and annotation, the programme will provide genomic resources for the study, monitoring and conservation of marine biodiversity (visit [our website](https://www.atlasea.fr/en/) for more informations).

We develop and maintain bioinformatics software and reproducible computational workflows to support the processing, quality control, comparison and analysis of the genomes produced by the programme. This page lists the current software development that occured since the start of ATLASea.

## Workflows
- [GALOP](https://github.com/institut-de-genomique/galop): long-reads assembly pipeline with or without Hi-C. This workflow combines assembly softwares such as Flye, Nextdenovo and Hifiasm (with or without hic support) to generate the initial contigs.
- Decontamination pipeline (coming soon): uses predicted proteins on the contigs assembled by GALOP to predict the taxonomy and automatically removes non-eukaryote species.
- yahs_wrapper (coming soon): Hi-C scaffolding pipeline that uses the Arima mapping pipeline for aligning reads and YaHS for the scaffolding step.
- Trackmania (coming soon): track generation for Pretext Hi-C contact maps.
- [Hobrac](https://github.com/Genoscope-LBGB/hobrac) and its [visualizer](https://www.genoscope.cns.fr/lbgb/hobrac/): Homology-based reference genome finding and synteny analysis. Hobrac is used during the Hi-C curation step to easily identify related genomes and scout for misassemblies and missed joins opportunities
- ear_wrapper (coming soon): easily generate ERGA assembly reports ([EARs](https://github.com/ERGA-consortium/EARs)) for the scaffolded genomes.
- genome_analysis (coming soon): pipeline dedicated to the QC of assemblies. It uses tools such as Busco, Merqury and Genomescope to generate precise quality metrics to diagnose problems in the assembly

## Software 
- [arima htslib](https://github.com/Genoscope-LBGB/arima_htslib): fast reimplementation of the Arima mapping tools to lift computation-time bottlenecks of the current official suite
- [dotplotrs](https://github.com/Genoscope-LBGB/dotplotrs): very fast dotplot-drawing software with vast customization opportunities (font size, colors, point size, custom sequence orders, ...)
- [fastoche](https://github.com/institut-de-genomique/fastoche): effortlessly extract common metrics from Fasta or Fastq files, gzipped or not.
- [find_reference_genomes](https://github.com/Genoscope-LBGB/find_reference_genomes): enter a taxon identifier and a taxonomic rank and find_reference_genomes will automatically search and download reference genomes of this rank
- [freq-motif-fastq](https://github.com/Genoscope-LBGB/freq-motif-fastq): analyze FASTQ files and generate statistics on dinucleotides, trinucleotides and low-complexity bases. This tool is used as our basis to decide if a sequence needs to be sequences with PacBio or ONT.
