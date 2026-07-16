# Workflows and tools developed for the ATLASea programme

The ATLASea programme aims to build a comprehensive reference atlas of marine eukaryotic genomes from species found across France's metropolitan and overseas exclusive economic zones. By bringing together specimen collection, taxonomic identification, high-throughput sequencing, genome assembly and annotation, the programme will provide genomic resources to support the study, monitoring and conservation of marine biodiversity. For more information, visit [our website](https://www.atlasea.fr/en/).

To support this effort, we develop and maintain bioinformatics software and reproducible computational workflows for processing, quality control, comparison and analysis of the genomes produced by the programme. Below is an overview of the workflows and software developed since ATLASea began.

## Workflows

- [GALOP](https://github.com/institut-de-genomique/galop): a long-read assembly workflow with optional Hi-C support. It combines assemblers including Flye, NextDenovo and hifiasm to generate the initial contigs.
- Decontamination pipeline (coming soon): predicts taxonomy from proteins encoded by contigs assembled with GALOP, then automatically removes non-eukaryotic contamination.
- yahs_wrapper (coming soon): a Hi-C scaffolding workflow that uses the Arima mapping pipeline to align reads and YaHS to scaffold the assembly.
- Trackmania (coming soon): generates tracks for Pretext Hi-C contact maps.
- [Hobrac](https://github.com/Genoscope-LBGB/hobrac) and its [visualizer](https://www.genoscope.cns.fr/lbgb/hobrac/): tools for identifying homologous reference genomes and performing synteny analysis. During Hi-C curation, Hobrac helps identify related genomes and detect potential misassemblies and missed joins.
- ear_wrapper (coming soon): generates ERGA assembly reports ([EARs](https://github.com/ERGA-consortium/EARs)) for scaffolded genomes.
- genome_analysis (coming soon): an assembly quality-control workflow that uses tools including BUSCO, Merqury and GenomeScope to generate detailed metrics and help diagnose assembly problems.

## Software

- [arima_htslib](https://github.com/Genoscope-LBGB/arima_htslib): a fast reimplementation of the Arima mapping tools designed to remove computational bottlenecks in the official suite.
- [dotplotrs](https://github.com/Genoscope-LBGB/dotplotrs): fast, highly customizable dot-plot software, with options for font size, colours, point size, custom sequence order and more.
- [fastoche](https://github.com/institut-de-genomique/fastoche): extracts common metrics from compressed or uncompressed FASTA and FASTQ files.
- [find_reference_genomes](https://github.com/Genoscope-LBGB/find_reference_genomes): given a taxon identifier and taxonomic rank, automatically searches for and downloads available reference genomes at that rank.
- [freq-motif-fastq](https://github.com/Genoscope-LBGB/freq-motif-fastq): analyses FASTQ files and reports statistics on dinucleotides, trinucleotides and low-complexity bases. We use these results to help determine whether a sample should be sequenced with PacBio or ONT.
