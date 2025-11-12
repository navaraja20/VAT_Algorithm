# 🎯 Visual Assessment of Tendency (VAT) Algorithm

![Python](https://img.shields.io/badge/Python-3.6%2B-blue?style=for-the-badge&logo=python) ![NumPy](https://img.shields.io/badge/NumPy-Data%20Processing-blue?style=for-the-badge&logo=numpy) ![Pandas](https://img.shields.io/badge/Pandas-1.0%2B-blue?style=for-the-badge&logo=pandas) ![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-brightgreen?style=for-the-badge&logo=matplotlib) ![SciPy](https://img.shields.io/badge/SciPy-Scientific-red?style=for-the-badge&logo=scipy) ![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?style=for-the-badge&logo=jupyter) ![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)

## 📌 Overview

This repository contains a comprehensive **Python implementation** of the **Visual Assessment of Tendency (VAT)** algorithm, a powerful clustering analysis tool for visualizing cluster tendency in datasets. The VAT algorithm reorders a dissimilarity matrix to reveal potential cluster structures through visual inspection of the resulting ordered dissimilarity image.

## 🎯 Key Features

- 📊 **Complete VAT Pipeline** - Handles data preprocessing, dissimilarity matrix computation, optimal reordering, and visualization
- 🔢 **Data Type Support** - Works with both numerical and categorical data (via automatic preprocessing)
- 📏 **Distance Metrics** - Supports both Euclidean and geodesic (manifold) distances for non-linear data
- ⚡ **Efficient Computation** - Includes subsampling for large datasets and optimized algorithms
- 🎨 **Publication-Quality Visualization** - Produces side-by-side comparisons of original and ordered matrices
- ✨ **Production-Ready** - Thoroughly tested with various dataset types
- 📈 **Cluster Tendency Assessment** - Automatically detects linear vs non-linear data structures
- 🧮 **Advanced Analytics** - Comprehensive dissimilarity computation and visualization

## 📦 Technologies Used

### Core Dependencies
- **Python 3.6+** - Programming language
- **NumPy** - Numerical computing and linear algebra
- **Pandas** - Data manipulation and analysis
- **Matplotlib** - Data visualization
- **SciPy** - Scientific computing (for distance metrics)
- **Scikit-learn** - Machine learning preprocessing utilities

### Development & Analysis
- **Jupyter Notebook** - Interactive development and analysis
- **Git** - Version control

## 📂 Project Structure

```
VAT_Algorithm/
├── VAT.ipynb                    # Main Jupyter notebook with implementation
├── README.md                    # Project documentation
├── VAT Report.pdf              # Detailed analysis report
├── LICENSE                     # MIT License
├── employee.csv                # Sample dataset for testing
└── .gitignore                  # Git ignore file
```

## 🚀 Installation & Setup

### Prerequisites

- Python 3.6 or higher
- pip package manager
- Virtual environment (recommended)

### Step 1: Clone the Repository

```bash
git clone https://github.com/navaraja20/VAT_Algorithm.git
cd VAT_Algorithm
```

### Step 2: Create Virtual Environment (Optional)

```bash
# On Windows
python -m venv venv
venv\Scripts\activate

# On macOS/Linux
python3 -m venv venv
source venv/bin/activate
```

### Step 3: Install Dependencies

```bash
pip install -r requirements.txt
```

Or install individually:

```bash
pip install numpy>=1.19.0
pip install pandas>=1.1.0
pip install matplotlib>=3.3.0
pip install scipy>=1.5.0
pip install scikit-learn>=0.23.0
pip install jupyter>=1.0.0
```

## 📝 Usage Examples

### Basic Usage

```python
import numpy as np
from scipy.spatial.distance import pdist, squareform
import matplotlib.pyplot as plt

# Load your data
data = np.random.rand(100, 2)

# Compute dissimilarity matrix
dissimilarity_matrix = squareform(pdist(data, metric='euclidean'))

# Apply VAT algorithm
# (Implementation details in VAT.ipynb)

# Visualize results
plt.imshow(dissimilarity_matrix, cmap='hot')
plt.colorbar()
plt.title('Ordered Dissimilarity Image (VAT)')
plt.show()
```

### With Jupyter Notebook

Open the included Jupyter notebook for interactive examples:

```bash
jupyter notebook VAT.ipynb
```

## 🧪 Test Cases

The implementation includes test cases demonstrating VAT on different dataset types:

- **Synthetic Data** - Circular and linear patterns with known cluster structures
- **Standard Datasets** - IRIS dataset for validation
- **Mixed Data** - Numerical and categorical features with preprocessing
- **Large Datasets** - Automatic subsampling for computational efficiency
- **Employee Data** - Real-world dataset (employee.csv) for practical application

## 📊 Algorithm Details

### Visual Assessment of Tendency

VAT is a clustering validation technique that:

1. **Computes Dissimilarity Matrix** - Calculates pairwise distances between data points
2. **Reorders Matrix** - Uses optimal reordering algorithm to reveal cluster patterns
3. **Visualizes Pattern** - Displays the reordered matrix as a heatmap
4. **Interprets Structure** - Dark blocks on diagonal indicate potential clusters

### Key Concepts

- **Dissimilarity Matrix** - Square matrix showing pairwise distances
- **Reordering Algorithm** - Determines optimal point ordering for visualization
- **Visual Patterns** - Diagonal blocks = clusters, scattered = no clear structure
- **Geodesic Distance** - For manifold/non-linear data structures

## 🔧 Configuration

### Distance Metrics

- `euclidean` - Default for linear data
- `manhattan` - Alternative linear metric
- `geodesic` - For manifold data (requires preprocessing)
- `cosine` - For high-dimensional data

### Parameters

- `sample_size` - For subsampling large datasets (optional)
- `metric` - Distance metric to use
- `data_type` - 'numerical', 'categorical', or 'mixed'

## 📈 Performance Characteristics

- **Time Complexity** - O(n² log n) for dissimilarity computation
- **Space Complexity** - O(n²) for dissimilarity matrix storage
- **Large Dataset Support** - Subsampling available for n > 5000
- **Optimal Dataset Size** - 500 to 2000 points for clear visualization

## 🐛 Troubleshooting

| Issue | Solution |
|-------|----------|
| Memory error with large datasets | Use subsampling parameter or reduce dataset size |
| Unclear cluster patterns | Try different distance metrics |
| Slow computation | Enable subsampling or use alternative data preprocessing |
| Import errors | Verify all dependencies are installed: `pip install -r requirements.txt` |

## 📚 References

- **VAT Algorithm Papers** - Original research by Bezdek and Hathaway
- **Dissimilarity-based Clustering** - Statistical foundations
- **Cluster Validation Methods** - Comprehensive evaluation techniques
- **Data Visualization** - Information visualization principles

## 🤝 Contributing

Contributions are welcome! Please feel free to:

- Submit issues for bugs or feature requests
- Fork the repository and submit pull requests
- Improve documentation and examples
- Add support for additional distance metrics
- Optimize algorithm implementation

## 📄 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## 👤 Author

**Navaraja Mannepalli**
- 🔗 GitHub: [@navaraja20](https://github.com/navaraja20)
- 💼 LinkedIn: [Navaraja Mannepalli](https://linkedin.com/in/navaraja-mannepalli)
- 📧 Email: navaraja13@gmail.com

## 🎓 Educational Value

This project serves as:
- A learning resource for clustering analysis
- A reference implementation of VAT algorithm
- A practical example of data preprocessing and visualization
- A foundation for advanced clustering research

## 📌 Quick Links

- 📖 [Full Documentation](VAT%20Report.pdf)
- 💻 [Interactive Notebook](VAT.ipynb)
- 📊 [Sample Dataset](employee.csv)
- 📋 [License](LICENSE)

---

⭐ If you found this helpful, please consider giving it a star!

📌 **Last Updated:** November 2024
