# Human Protein-Protein Interaction Network Analysis

This project analyzes a large-scale human protein-protein interaction (PPI) network using data from the BioGRID database. It focuses on identifying network hubs, assessing the degree distribution for scale-free properties, computing shortest path lengths, and analyzing centrality metrics (betweenness and closeness) to identify key proteins in the network.

---
## Repository Structure
code/ # Python notebooks/scripts used for analysis
plots/ # Visualizations generated during analysis
results/ # Output files (e.g., top nodes by degree/centrality)
README.md # Project summary and methodology

---

## Objective

- Analyze topological features of the human PPI network
- Identify hub proteins and their network significance
- Determine whether the network exhibits scale-free properties
- Evaluate network connectivity using shortest path and centrality metrics

---

## Data Source

The dataset used was obtained from the **BioGRID database**:

🔗 [BioGRID Download Portal](https://downloads.thebiogrid.org/BioGRID/Release-Archive/)

- **Version**: BIOGRID 4.4.227
- **Organism**: *Homo sapiens*
- **Format**: Tab2 `.txt`

> The dataset is **not included** in this repository due to size constraints. Please download it manually and place it in the `data/` folder before running the analysis.
---

## 🛠️ Tools & Technologies

- **Language**: Python (Google Colab)
- **Libraries**: NetworkX, Pandas, Matplotlib, NumPy
- **Analysis**: Degree distribution, centrality measures, shortest path distribution
---

## 📈 Results

### 1. Top 10 Hub Nodes (by Degree)
These proteins have the highest number of interactions:
ZRANB1 – 4160
PARK2 – 3426
EGFR – 3070
PLEKHA4 – 2971
KIAA1429 – 2932
KRAS – 2891
MYC – 2817
CCNF – 2798
CUL3 – 2656
TRIM25 – 2497

---

### 2. Degree Distribution Plot

#### Interpretation:
- The log-log degree distribution suggests **power-law behavior**, a key indicator of a **scale-free network**.
- **Logarithmic Y-axis** reveals a linear trend: few nodes have very high connectivity (hubs), while most have few connections.
- This implies **biological robustness**, where the network is resistant to random node failures but sensitive to targeted hub disruption.

<p align="center">
  <img src="plots/degree_distribution.png" width="500">
</p>

---

### 3. Shortest Path Length Distribution

#### Key Observations:
- **Most paths have a length of 3**, indicating high connectivity and efficient information flow.
- **Significant presence at lengths 2 and 4** suggests moderate clustering.
- Very **few paths are at lengths 1 or 5**, and none exceed 5 — showing a compact, well-connected network.

<p align="center">
  <img src="plots/shortest_path_distribution.png" width="500">
</p>

---

### 4. Top 10 Nodes by Betweenness Centrality
Nodes acting as critical bridges in the network: CCNF, UBC, NR3C1, TRIM25, EGFR, ZRANB1, KIAA1429, APP, PARK2, OTUD4. 

### 5. Top 10 Nodes by Closeness Centrality
Nodes that are most central in terms of average shortest path: 57664, 25962, 7157, 43740578, 7706, 4609, 1994, 7316, 351, 3191.

---

## Interpretation
The analysis confirms that the human PPI network exhibits:
- **Scale-free structure**
- **Biological modularity**
- **Small-world properties**
- Central hubs that may serve as **potential therapeutic targets** in systems biology or disease modeling
---

##  How to Reproduce
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/ppi-network-analysis.git
   cd ppi-network-analysis
---
## Author
Sharanya Sheshadri
Graduated Masters Student- Major Bioinformatics.


