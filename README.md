# LSDV-Genome-Analysis-Pipeline-from-SRA
Steps included:
1. Environment setup (Conda-based or system packages)
2. Downloading raw SRA data and metadata
3. FASTQ extraction
4. Quality control (FastQC)
5. Adapter / quality trimming (fastp)
6. Reference genome retrieval (RefSeq GCF_000839805.1)
7. Indexing reference
8. Alignment (BWA) and BAM processing (samtools)
9. Mapping statistics
10. Variant calling (bcftools)
11. Consensus genome generation
12. Optional filtering and project-local PATH handling

## Requirements

- WSL2 Ubuntu (or Linux/macOS)
- `conda` (Miniconda install recommended into `~/`, not on `/mnt`) to isolate tools. Alternatively, most tools can be installed via `apt` and standalone binaries. :contentReference[oaicite:38]{index=38} :contentReference[oaicite:39]{index=39}  
- Tools (preferably inside a Conda env named `bio_env`): `sra-tools`, `fastqc`, `fastp`, `bwa`, `samtools`, `bcftools`. The NCBI Datasets CLI can be installed separately via standalone binary. :contentReference[oaicite:40]{index=40} :contentReference[oaicite:41]{index=41}
