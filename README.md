# K-Means Clustering: Customer Segmentation Analysis

K-means clustering homework project focused on customer segmentation analysis for credit card companies.

## Project Structure

```
├── solution.ipynb          # Main CardWise customer segmentation analysis
├── k_means_clustering.ipynb # Basic K-means tutorial with simple 2D data
├── data_analysis.ipynb     # Additional data exploration
├── HW.html                 # HTML export of homework notebook
├── Customer Data.csv       # CardWise dataset (8,950 customers × 18 features)
├── data.csv                # Tutorial dataset (200 customers × 2 features)
├── Clustering.pdf          # Reference material
└── CLAUDE.md               # Development guidelines
```

## Prerequisites

```bash
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
```

## Usage

Run the Jupyter notebooks:

```bash
jupyter notebook solution.ipynb        # Full customer segmentation analysis
jupyter notebook k_means_clustering.ipynb  # Basic tutorial
```

Export notebook to HTML:

```bash
jupyter nbconvert --to html solution.ipynb
```

## Analyses

### 1. CardWise Customer Segmentation (solution.ipynb)

Complete analysis of 8,950 credit card customers with 18 features including balance, purchases, cash advances, and payment behavior.

**Workflow:**
- Exploratory Data Analysis (correlations, distributions, outliers)
- Feature preprocessing with StandardScaler
- Optimal k selection using Elbow Method
- K-Means clustering (k=4)
- Business insights and recommendations

**Identified Segments:**
| Cluster | Name | Size | Key Characteristics |
|---------|------|------|---------------------|
| 0 | Cash-Advance Seekers | 12.4% | High cash advances, liquidity needs |
| 1 | Moderate Users | 44.8% | Low activity baseline segment |
| 2 | Frequent Spenders | 4.5% | Highest purchases, high frequency |
| 3 | Balanced Users | 38.3% | Moderate usage patterns |

### 2. Basic Tutorial (k_means_clustering.ipynb)

Simple 2D clustering example using Annual Income vs Spending Score (200 customers).

## Data Files

**Customer Data.csv** - Production dataset
- 8,950 customers, 18 features
- Features: BALANCE, PURCHASES, CASH_ADVANCE, CREDIT_LIMIT, PAYMENTS, frequencies, etc.
- Missing values handled with median imputation

**data.csv** - Tutorial dataset
- 200 customers, 2 features
- Annual Income (k$) and Spending Score (1-100)

## Key Technical Details

- **Preprocessing:** StandardScaler normalization (required for K-means)
- **Initialization:** k-means++ for smart centroid selection
- **Parameters:** n_init=10, max_iter=300, random_state=42
- **Evaluation:** Elbow Method, Silhouette Score
