---
title: "ATAC-seq"
linkTitle: "ATAC-seq"
date:
summary: >
weight: 2
---

## Recommended Analysis Workflow

### Primary Recommendation: nf-core/atacseq + atacreportR
For ATAC-seq projects, we recommend using [nf-core/atacseq](https://nf-co.re/atacseq) for initial processing followed by our [atacreportR](https://devufbcb-sr.rc.ufl.edu/atacreportr/) application for differential accessibility analysis and comprehensive reporting.

**Workflow Overview:**
1. **Raw data processing** → Run [nf-core/atacseq](https://nf-co.re/atacseq) on HiperGator using SLURM configuration
2. **Differential analysis & reporting** → Use [atacreportR](https://devufbcb-sr.rc.ufl.edu/atacreportr/) to generate comprehensive differential accessibility reports
3. **Interactive exploration** → Review results through atacreportR's downloadable reports

**Important Access Notes:**
- atacreportR is a **private application** accessible only on the UF network
- Contact our team for access to the required HiperGator data location to run the application
- VPN connection required for off-campus access

### Alternative R-based Analysis
For users preferring traditional R workflows, we recommend:
- [DiffBind](https://bioconductor.org/packages/release/bioc/html/DiffBind.html) for differential binding analysis
- [ChIPseeker](https://bioconductor.org/packages/release/bioc/html/ChIPseeker.html) for peak annotation
- Access via [RStudio Server on HiperGator](https://docs.rc.ufl.edu/software/apps/r/rstudio_server/)

## Best Practices & Considerations

**Experimental Design:**
- Plan for adequate biological replicates (minimum 3 per condition)
- Include appropriate input/background controls
- Consider cell type purity and sample quality

**Data Quality:**
- Evaluate fragment size distribution and TSS enrichment from nf-core/atacseq output
- Check for proper peak calling and reproducibility between replicates
- Assess library complexity and duplication rates

**Analysis Strategy:**
- Define appropriate peak calling parameters for your cell type
- Consider motif enrichment analysis for biological interpretation
- Plan integration with RNA-seq data when available

**Computational Resources:**
- Use HiperGator's SLURM scheduler for nf-core/atacseq processing
- Allocate sufficient memory for peak calling (depends on genome size)
- Plan storage for large BAM files and peak call outputs

## Getting Started
Submit a [support request](https://cancer.ufl.edu/research/shared-resources/biostatistics-computational-biology-shared-resource/biostatistics-shared-resource-support-request-form/) to discuss your ATAC-seq project design, analysis needs, and to obtain access to atacreportR.
