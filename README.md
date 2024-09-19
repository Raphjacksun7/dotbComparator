# RNA Sequence 2D Structure Prediction Tool

## Project Overview
This project involves the development of a Python-based tool designed to predict and evaluate RNA secondary structures using dot-bracket notation. The tool compares predicted RNA structures against reference structures, calculating key metrics to assess the accuracy of the predictions.

## Key Features
- **Dot-Bracket Notation Analysis**: Analyzes RNA secondary structures using dot-bracket notation, identifying paired and unpaired nucleotides to compare predicted structures with references.
- **Structure Comparison Metrics**: Computes Sensitivity, Positive Predictive Value (PPV), Matthews Correlation Coefficient (MCC), and other metrics to evaluate RNA structure predictions.
- **Canonical Base Pair Handling**: Removes non-canonical base pairs (e.g., mismatched or non-standard pairs) to focus on biologically relevant RNA folding.
- **Balanced Structure Validation**: Checks for balanced and correct bracket structures to ensure accurate comparisons.

## How It Works
1. **Input Data**: Provide the RNA sequence, reference structure, and predicted structures in dot-bracket format.
2. **Structure Comparison**: The tool calculates true positives, false positives, false negatives, and true negatives between the predicted and reference structures.
3. **Output Metrics**: Outputs key evaluation metrics including sensitivity, PPV, MCC, and MCC* to assess prediction accuracy.

## Technologies Used
- Python
- Dot-bracket notation analysis
- Structural comparison algorithms

## Getting Started
1. Clone the repository and install any required dependencies.
2. Run the main script and provide the required RNA sequence and structure data.
3. Review the output metrics to evaluate the accuracy of your RNA structure predictions.

## Usage Example
```python
# Example usage of the DotbComparator class
comparator = DotbComparator(ref_dotb="(((...)))", ref_sequence="AUGCUA", canonical_only=True)
results = comparator.compare_structures(pred_dotb="((....))")
print(results)
