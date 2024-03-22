# dog_dna_project
---

# DNA Identification Service Documentation

## Overview
This DNA identification service aims to identify the closest sequence in a provided database to a given test sequence. The service considers various methods, including sequence comparison, statistical analysis, and phylogenetic tree reconstruction.

## Project Structure
- **Code Files**:
  - `dna_identification.py`: Main script for DNA identification service.
  - `align_sequences.py`: Script for aligning DNA sequences using ClustalW.
- **Input Files**:
  - `dog_breeds.fa`: Database file containing DNA sequences adapted from GEO.
  - `mystery.fa`: Test sequence file to be identified.
- **Output**:
  - Closest sequence identification results and differences.
  - Probability and p-value analysis.
  - Phylogenetic tree visualization.

## Code Explanation

### 1. DNA Identification (`dna_identification.py`)
- **Purpose**: Identify the closest sequence in the database to the test sequence.

#### Steps:
1. **Reading Fasta Files**:
   - Read the database sequences and the test sequence from their respective FASTA files.
   - Use `read_fasta_file()` function to parse FASTA files and return sequences as dictionaries.

2. **Probability Analysis**:
   - Calculate probabilities of observing each base at each position in the database using `calculate_probabilities()` function.
   - Calculate the p-value for the test sequence against the database using `calculate_p_value()` function.

3. **Closest Sequence Identification**:
   - Find the sequence with the smallest p-value as the closest sequence.
   - Calculate the difference between the test sequence and the closest sequence.
   - Output the closest sequence, difference, and p-value.

### 2. Sequence Alignment (`align_sequences.py`)
- **Purpose**: Align DNA sequences using ClustalW.

#### Steps:
1. **Sequence Alignment**:
   - Perform sequence alignment using ClustalW.
   - Input the database sequences file.
   - Output the aligned sequences file (`aligned_sequences.aln`).

### 3. Phylogenetic Tree Construction (`dna_identification.py`)
- **Purpose**: Construct a phylogenetic tree from the aligned sequences.

#### Steps:
1. **Tree Construction**:
   - Read the aligned sequences from the alignment file using `read_aligned_sequences()` function.
   - Construct the phylogenetic tree using the UPGMA method.
   - Visualize the tree using the `Phylo.draw()` function.

## Stretch Goals
- **Stretch Goal 1: Probabilities and p-value**:
  - Implemented in the `dna_identification.py` script.
  - Calculates probabilities and p-values to assess sequence similarity statistically.

- **Stretch Goal 2: Phylogenetic Tree**:
  - Implemented in the `dna_identification.py` script.
  - Constructs a phylogenetic tree to visualize evolutionary relationships between sequences.

## Conclusion
The DNA identification service offers a comprehensive solution for identifying the closest sequence in a provided database to a test sequence. It employs various methods, including sequence comparison, statistical analysis, and phylogenetic tree reconstruction, to achieve accurate results.

---
