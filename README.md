# Gene-to-Protein Sequence Analysis (Human INS)

A small Python project that retrieves a gene record from NCBI, translates the
coding sequence, and compares the protein with a curated database using BLAST.

## What it does
1. Retrieves NM_000207.3 (human insulin mRNA) from NCBI with Biopython
2. Calculates GC content (63.9%) and translates the CDS (110 aa preproinsulin)
3. Runs BLASTp against SwissProt
4. Summarizes the top 10 hits (identity, E-value) in a table and bar chart

## Results
The top five BLASTp hits are primate insulins (97.3-100% identity); the
closest, orangutan, differs from human insulin at one position. Rodent, dog
and owl monkey insulins show 82.7-88.2% identity. All E-values are below 1e-54.

## Files
- gene_to_protein_analysis.ipynb: full notebook with code, explanations, table and chart

## Limitations
Only one gene and the top 10 hits were analyzed; identity reflects sequence
similarity, not function.

## Tools
Python, Biopython, pandas, matplotlib, NCBI Entrez/BLAST

## Run it yourself
Open the notebook in Google Colab and set Entrez.email to your own email address.
