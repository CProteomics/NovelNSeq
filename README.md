# NovelNSeq
Precise Discovery of Novel N-Terminal Proteoforms Beyond the Limitations of Proteogenomics and De Novo Sequencing

# Overview
Alternative splicing-mediated protein N-terminal sequence variation is closely associated with diseases, but its identification by mass spectrometry faces technical bottlenecks. Traditional proteogenomic methods cannot identify novel N-terminal proteins undetected in transcriptome data, while de novo sequencing has limitations in accuracy and traceability. To address this, we developed the first dedicated algorithm, NovelNSeq, which is specifically designed to parse signature peptides (novel N-terminal extension peptides) of novel N-terminal proteins from mass spectrometry data without relying on transcriptome data or de novo sequencing. NovelNSeq fully exploits peptide encoding rules, demonstrating significantly higher accuracy than de novo sequencing algorithms such as PEAKS, pNovo3, SpliceNovo, Casanovo, and InstaNovo, and enables tracing back the peptide encoding mechanisms. Using NovelNSeq, we identified and validated novel N-terminal proteoforms from human genes CALM2, CAPNS1 and CPNE7 in mass spectrometry data where large-scale proteogenomics failed to detect them, which establishes NovelNSeq as an essential complement to conventional approaches. 
<div align="center">
  <img src="https://github.com/user-attachments/assets/9805560f-9d26-4701-acc8-f26a0eecdfb3" 
       alt="NovelNSeq原理图" 
       width="70%" 
       style="border: 1px solid #eee; border-radius: 5px;"/>
</div>
<p align="center">
  Figure 1. Schematic of the NovelNSeq algorithm for identifying NEPs in MS data.
</p>

# System Requirements
.NET Runtime: .NET 6.0 (for C# components). Memory: Minimum 100GB RAM. Operating Systems: Windows 10/11.

# Usage
## 1. Input Preparation
Prepare the following input files:
- **MS/MS spectra**: Place `.mgf` files in `./NovelNSeq/Release/net6.0/Input/`
- **Genome data**:
  - Chromosome FASTA files in `./NovelNSeq/Release/net6.0/chrgff/chr/`
  - Annotation file as `./NovelNSeq/Release/net6.0/chrgff/human_gff.gff`

*Note: Due to file size limitations, the provided genome data files in the repository are incomplete. For actual analysis, please download complete reference files from NCBI.*
## 2. Run NovelNSeq
Execute the program by double-clicking `NovelNSeq.exe`. After completion, results will be generated in: `./NovelNSeq/Release/net6.0/Output/`

## 3. Output Interpretation
Each line represents a NovelNSeq identification result with the following comma-separated format: MS/MS_spectrum_name, NEP_sequence, PSM_score, genomic_origin.
The genomic_origin field contains detailed mapping information in pipe-delimited format.

# Citing NovelNSeq
# Support
For questions or bug reports, please contact: hecuitongpro@163.com.
