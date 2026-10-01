# Protein Repertoire Analysis: *Aromatoleum aromaticum* EbN1 on Benzoate

Comparative proteomics of *Aromatoleum aromaticum* strain EbN1 grown on benzoate under **anoxic** and **oxic** conditions, to see which proteins each condition relies on and what that says about benzoate metabolism.

## What the notebooks do

Each notebook analyses one sample type from Mascot protein identifications:

| Notebook | Sample type |
|---|---|
| `EbN1_Benzoate_metabolism_gel_slice.ipynb` | Gel-slice fractions |
| `EbN1_Benzoate_metabolism_membrane.ipynb` | Membrane protein fractions |
| `EbN1_Benzoate_metabolism_shotgun.ipynb` | Shotgun (whole-cell) proteomics |

The workflow is the same in each:

1. **Clean** the Mascot exports: normalise column names, strip score annotations, and keep identifications supported by peptides.
2. **Filter** proteins by peptide count and sequence coverage, and check edge cases such as proteins reported with no supporting peptide.
3. **Merge replicates** into one protein list per condition.
4. **Compare conditions**: proteins shared by anoxic and oxic growth versus proteins specific to one condition, shown with UpSet plots and Venn diagrams.
5. **Interpret**: look up the functions and cellular localisation of the top-ranked condition-specific proteins.

## Tools

Python, pandas, NumPy, SciPy, matplotlib, seaborn, upsetplot, matplotlib-venn, Jupyter.

## Data

The raw Mascot exports (Excel files) are not included in this repository, so the notebooks show the analysis but cannot be re-run as they are.

## Author

Oluwatosin Samuel Oluwole · [GitHub](https://github.com/Oxygen-08)
