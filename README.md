# Gene-to-Protein Sequence Analysis: Human INS

A bioinformatics project using Python to retrieve a human insulin mRNA sequence, translate its coding sequence into a protein, and investigate protein sequence similarity using BLAST.

## Project Overview

Insulin is a peptide hormone involved in the regulation of blood glucose levels. This project explores the human **INS** gene at the sequence level, from mRNA retrieval to protein translation and comparative sequence analysis.

The analysis uses the human insulin mRNA transcript variant 1 (**NCBI accession: NM_000207.3**).

## Objectives

- Retrieve a nucleotide sequence from NCBI using Biopython.
- Calculate the GC content of the mRNA sequence.
- Extract the coding sequence (CDS) and translate it into an amino acid sequence.
- Examine the main structural regions of preproinsulin.
- Perform protein sequence similarity searches against the Swiss-Prot database using BLASTp.
- Summarize and visualize the top database matches.

## Methods and Workflow

1. **Sequence retrieval:** Retrieved the human INS mRNA record from NCBI Nucleotide using Biopython Entrez.
2. **Nucleotide analysis:** Calculated GC content for the full mRNA sequence, including untranslated regions (UTRs).
3. **Translation:** Extracted the CDS and translated it into the preproinsulin amino acid sequence.
4. **Protein annotation:** Examined the signal peptide, B chain, C-peptide region, and A chain.
5. **Sequence similarity search:** Used NCBI BLASTp to compare the translated protein sequence against Swiss-Prot.
6. **Results analysis:** Collected protein accessions, organism names, percentage identity, alignment length, and E-values, then presented the results in a table and bar chart.

## Key Results

- **mRNA accession:** NM_000207.3
- **Full mRNA length:** 465 nucleotides
- **GC content:** 63.9% across the full mRNA, including UTRs
- **Translated protein length:** 110 amino acids (preproinsulin)
- **BLASTp database:** Swiss-Prot
- **Number of top hits examined:** 10

The top BLASTp match was human insulin itself (UniProt accession: P01308), with 100% sequence identity. This expected self-match served as a reference for comparing the other hits.

The remaining top hits included insulin precursor sequences from other primates, rodents, and dog. The reported percentage identities ranged from 82.7% to 99.1% among these non-human matches. These results demonstrate sequence similarity between human preproinsulin and homologous insulin precursor sequences from other mammals.

## Tools and Technologies

- Python
- Biopython
- NCBI Entrez
- NCBI BLASTp
- Swiss-Prot
- pandas
- Matplotlib
- Google Colab
- Jupyter Notebook

## Repository Contents

- `gene_to_protein_analysis.ipynb` — Jupyter Notebook containing the analysis, code, explanatory notes, results table, and visualization.
- `README.md` — Project overview, methods, and key findings.

## Run the Notebook

[Open the notebook in Google Colab](https://colab.research.google.com/github/bitarahimi525/gene-to-protein-analysis/blob/main/gene_to_protein_analysis.ipynb)

To reproduce the analysis:

1. Open the notebook in Google Colab.
2. Set `Entrez.email` to your own email address before making NCBI requests.
3. Run the notebook cells in order.
4. Allow time for the online BLASTp search to complete.

The notebook installs the required Python packages. The BLAST search requires an internet connection and may take several minutes.

## Search Parameters and Reproducibility

The protein similarity search uses Biopython's `NCBIWWW.qblast` interface with the `blastp` program, the `swissprot` database, and `hitlist_size=10`. Other search parameters use the applicable Biopython/NCBI defaults unless specified in the notebook.

The Swiss-Prot database is updated regularly, so subsequent runs may return different hits, rankings, or E-values. The original search date and database release were not recorded.

## Limitations

- The analysis focuses on a single human gene and its translated protein.
- Only the top 10 BLASTp hits are summarized.
- Sequence identity measures similarity across an alignment; it does not independently establish biological function.
- This project is an introductory sequence-analysis workflow and does not include experimental validation or a comprehensive evolutionary analysis.

## Future Improvements

Potential extensions include:

- Comparing insulin sequences from a broader range of species.
- Performing a multiple sequence alignment.
- Visualizing conserved and variable amino acid positions.
- Investigating sequence conservation in mature insulin chains separately from the precursor.
- Recording search dates and additional parameters to improve reproducibility.

## Author

**Bita Rahimi**

