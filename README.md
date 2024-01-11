A computational tool ‘STARCH’ has been developed to detect gene level CNVs and subclones from ST data. We utilized this tool to detect exon level CNVs in addition to gene level CNVs. This was achieved by processing the 10x visium spatial gene expression datasets to obtain exon expression datasets followed by CNV detection from both the data. We generated the exon expression matrix based on our observation that during the sequencing protocol, the probes are used to capture the transcripts released from the permeabilized cells of the tissue. Subsequently, during the sequencing run the probes are sequenced which make up the reads in FASTQ files. These reads are used to derive the gene expression matrix which is further used for downstream analysis like to detect CNV. As the reads from probe based mRNA sequencing are essentially the sequence of only target exons it is not accurate to assume that all the exons of the given transcript/gene exist. It has been reported in the literature that for a gene some of its exons might be deleted/duplicated while the rest can be neutral. Hence, from such data it would be less accurate to report copy number for the entire gene. Here we introduce a method to report copy numbers at the level of exons by utilizing the exon expression data. Although, there is high concordance between gene and exon level CNVs but we also observe that there exist certain genes having differential copy numbers among its exons.

1. Download the publicly available datasets from 10x genomics website: https://www.10xgenomics.com/resources/datasets/human-melanoma-if-stained-ffpe-2-standard
It contains following files:
(i) probe BED file with the description of probes and their target genes,
(ii) barcoded BAM file with the information of reads alignment,
(iii) feature-barcode matrices used for secondary analysis and
(iv) spatial imaging data that describes spot barcode locations in the tissue section images

2. Find probe targets and create exon count matrix (find_probe_targets.ipynb, Melanoma_all_exons_cnv.ipynb)
3. Analysis with STARCH (https://github.com/raphael-group/STARCH/tree/master)
4. Explore the outputs (starch_figure_k3_Melanoma.ipynb, summarize_results.pynb)
