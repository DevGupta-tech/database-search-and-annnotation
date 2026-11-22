# Database Search and Annotation: Human Hemoglobin Beta (HBB)

## Project objective
Use a public protein database search to identify sequences similar to a query protein, then interpret the strongest matches and record their biological meaning.

## Query
- Protein: Hemoglobin subunit beta (beta-globin)
- Organism: *Homo sapiens*
- NCBI RefSeq accession: `NP_000509.1`
- Query length: 147 amino acids
- Gene: `HBB` (NCBI Gene ID: 3043)

## Method
The project uses protein BLAST (BLASTP) against NCBI's non-redundant protein database (`nr`). The query sequence and the archived teaching-example search output are included in this repository.

**Data provenance note:** `results/blast_hits.tsv` records the values visible in a published UC San Diego bioinformatics lecture example. It is an archived NCBI BLAST result snapshot, not a search newly submitted on 22 November 2026. The parameter settings are transcribed from the same example. This is stated explicitly to avoid presenting historical output as a new run. Re-run the query at NCBI before submission if your instructor requires a current live result.

## Repository structure
- `data/query.fasta` — query protein sequence
- `results/blast_hits.tsv` — selected significant alignments transcribed from the archived BLAST output
- `results/search_parameters.txt` — recorded search settings and provenance
- `docs/annotation.md` — interpretation and annotation of the best matches
- `docs/sources.md` — source links and data notes

## How to reproduce the search
1. Open the NCBI Protein BLAST page: https://blast.ncbi.nlm.nih.gov/Blast.cgi?PROGRAM=blastp
2. Paste the contents of `data/query.fasta` into **Enter Query Sequence**.
3. Select database **Non-redundant protein sequences (nr)**.
4. Select algorithm **blastp (protein-protein BLAST)**.
5. For a comparable search, use the settings recorded in `results/search_parameters.txt`.
6. Click **BLAST** and wait for the result page.
7. Compare the live result table with `results/blast_hits.tsv`. Save the live result using **Download** on the NCBI results page and replace the archived table only after checking the new values.

## How to read the main BLAST statistics
- **Query cover:** percentage of the query sequence included in the alignment.
- **Percent identity:** percentage of aligned amino-acid positions that are identical.
- **E-value:** number of alignments with a score this good expected by chance in a database search. Smaller values indicate stronger evidence of similarity.
- **Bit score:** normalized alignment score; higher scores indicate stronger alignments.

## Main finding
The selected hits are overwhelmingly annotated as hemoglobin beta chains or beta-globin structures. The strongest alignments cover essentially the full 147-aa query and have very small E-values, supporting that they are homologous beta-globin sequences rather than unrelated proteins.
