# Interpretation and annotation

## 1. Query protein
The query is human hemoglobin subunit beta, encoded by the **HBB** gene. The mature reference protein sequence used here is 147 amino acids long. Hemoglobin is an oxygen-transport protein in red blood cells. Adult hemoglobin A normally contains two alpha and two beta polypeptide chains.

## 2. What the BLAST output shows
The selected matches have query coverage of 99–100%, percent identity of 99–100%, and E-values around 10^-101 to 10^-103. These values indicate very strong sequence similarity across almost the entire query. The strongest results are expected because the query is itself a curated human beta-globin reference sequence and the database contains identical or nearly identical beta-globin records.

The top two entries are labelled synthetic constructs. They should not be interpreted as separate naturally occurring species. They are records containing the same beta-globin sequence. The third hit is the query reference sequence itself, so it is a self-match rather than an independent discovery.

The gorilla beta-globin entry (P02024.2) is a biologically informative cross-species match. Its 99% identity and full query coverage are consistent with the close evolutionary relationship between humans and other primates, and with conservation of the beta-globin protein's role.

The structural entry `1COH_B` is a protein chain from a human deoxyhemoglobin structure. Its strong match connects the sequence result to a three-dimensional protein structure. Structure records are not separate gene products in the same sense as protein sequence records.

## 3. Annotation table

| Accession | Match annotation | Match type | Interpretation |
|---|---|---|---|
| AAX37051.1 | Hemoglobin beta, synthetic construct | Synthetic sequence record | Exact full-length match; useful as a sequence record, not a separate organism |
| AAX29557.1 | Hemoglobin beta, synthetic construct | Synthetic sequence record | Exact full-length match; likely redundant for biological comparison |
| NP_000509.1 | Hemoglobin subunit beta, human | RefSeq reference protein | Query's own accession; self-match confirms the reference sequence |
| P02024.2 | Hemoglobin subunit beta, gorilla | Reviewed protein record | Near-identical primate homolog; supports conservation of beta-globin |
| AAN84548.1 | Beta-globin chain variant, human | Variant protein record | Near-identical human beta-globin sequence; possible allelic/variant record |
| AAZ39780.1 | Beta-globin, human | Protein sequence record | Near-identical human beta-globin sequence |
| ACU56984.1 | Beta-globin, human | Protein sequence record | Near-identical human beta-globin sequence |
| AAD19696.1 | Hemoglobin beta chain, human | Protein sequence record | Near-identical human beta-globin sequence |
| 1COH_B | Human deoxyhemoglobin chain B | PDB structure chain | Strong sequence-to-structure match; represents beta chain in a solved hemoglobin complex |
| AAF00489.1 | Hemoglobin beta subunit variant, human | Variant protein record | Near-identical human beta-globin sequence |

## 4. Biological interpretation
The results support the identity of the query as a beta-globin protein. The high query coverage shows that similarity is distributed over almost the whole protein rather than being limited to a short motif. The extremely small E-values make random similarity an implausible explanation.

The gorilla hit is particularly useful for evolutionary interpretation: beta-globin is conserved between closely related primates. The structure hit shows that the sequence can be linked to an experimentally determined hemoglobin structure. Taken together, the matches support a conserved protein with a shared oxygen-transport role.

## 5. Important limitations
1. This table is a transcription of a published historical BLAST teaching example, not a fresh 2026 search.
2. Several top records are redundant, synthetic, or the query itself; they should not be counted as independent species-level homologues.
3. A BLAST match indicates sequence similarity; it does not by itself prove identical biological activity, expression pattern, or clinical effect.
4. The exact ranking and statistics can change as NCBI databases are updated or search settings differ.

## 6. Conclusion
BLASTP comparison of the human HBB beta-globin protein against the NCBI protein database returns highly significant, near-full-length matches to beta-globin records. The gorilla homolog supports evolutionary conservation, while the PDB chain provides a structural connection. The search therefore identifies the query as hemoglobin subunit beta and demonstrates how sequence similarity, coverage, E-value, and annotation are used together to interpret database hits.
