# 🧾 Supplementary files for Binding Affinity Scoring via Interatomic Contacts
---

This repository contains supplementary materials for the paper  **_"Towards Fast Binding Affinity Scoring in Protein–Protein Complexes via Interatomic Contacts and Linear Regression"_**, by **Bastos and Lemos *et al***.

---

## 📁 Contents

- [`model.ows`](model.ows): A Orange Data Mining (Demšar, 2004) session file.
- [`input.tsv`](input.tsv): A Tab Separated Values (TSV) file containing input information for model training. The columns are:
  - pdb: PDB ID of the protein;
  - chain: Combination of chains in the form Receptors:Ligands;
  - dgexp: Experimental ΔG value for the complex as reported in Vangone, 2015;
  - dgpre: Predicted ΔG value for the model described in Vangone, 2015;
  - bsa: Binding Surface Area (BSA) value for the complex, as described in Vangone, 2015;
  - HB, AT, RE, HY, AS, SB, DS, PA, PosA, NegA: Number of Hydrogen Bond, Attractive, Repulsive, Hydrophobic, Aromatic Stacking, Salt Bridge, Disulfide Bond, Polar-Apolar, Positive-Apolar, and Negative-Apolar contacts detected using COCαDA (Lemos, 2024), respectively.

- [`output.tsv`](output.tsv): Results file.
The columns are:
  - pdb: PDB ID of the protein;
  - chain: Combination of chains in the form Receptors:Ligands;
  - dgexp: Experimental ΔG value for the complex as reported in Vangone, 2015;
  - prediction-PA: Predicted ΔG value using the polar-apolar atom pairs as input; 
  - prediction-AT: Predicted ΔG value using the attractive interactions as input;
  - prediction-HB: Predicted ΔG value using the hydrogen bonds counts as input;
  - prediction-RE: Predicted ΔG value using the repulsive interactions counts as input;
  - prediction-HY: Predicted ΔG value using the salt bridges counts as input;
  - prediction-SB: Predicted ΔG value using the negative-apolar atom pairs as input;
  - prediction-PosA: Predicted ΔG value using the positive-apolar atom pairs as input;
  - prediction-NegA: Predicted ΔG value using the negative-apolar atom pairs as input;
  - count-PA: Count of polar-apolar atom pairs detected in the input PDB;
  - count-AT: Count of attractive interactions detected in the input PDB;
  - count-HB: Count of hydrogen bonds detected in the input PDB;
  - count-RE: Count of repulsive interactions detected in the input PDB;
  - count-HY: Count of hydrophobic interactions detected in the input PDB;
  - count-SB: Count of salt bridges detected in the input PDB;
  - count-PosA: Count of positive-apolar atom pairs detected in the input PDB;
  - count-NegA: Count of negative-apolar atom pairs detected in the input PDB.

---

## References:

- Demšar, J., Zupan, B., Leban, G., Curk, T.: Orange: From experimental machine learning to interactive data mining. In: Lecture Notes in Computer Science, pp. 537–539. Lecture notes in computer science, Springer Berlin Heidelberg, Berlin, Heidelberg (2004).
- Vangone, A., Bonvin, A.M.: Contacts-based prediction of binding affinity in protein-protein complexes. Elife 4, e07454 (Jul 2015).
- Lemos, R.P., Mariano, D., Silveira, S.A., de Melo-Minardi, R.C.: COCαDA - large-scale protein interatomic contact cutoff optimization by Cα distance matrices. In: Annals of the XVII Brazilian Symposium on Bioinformatics (BSB 2024). pp. 59–70. Brazilian Computer Society (SBC) (Dec 2024).

---