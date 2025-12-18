# Gun_Violence_analysis

### Setup Instructions

1. **Environment Setup:**
   ```bash
   # Install required packages (included in notebook)
   pip install spacy transformers sentence-transformers
   pip install scikit-learn numpy pandas matplotlib seaborn
   pip install umap-learn nltk
   python -m spacy download en_core_web_trf
   ```

2. **Data Preparation:**
   - Update DATA_PATH variable to point to your dataset location
   - Ensure articles are organized by outlet folders

3. **Execution:**
   - Run all cells in order
   - The notebook will process all tasks sequentially
   - Results and visualizations will be saved automatically

### Task Implementations

**Task 1: Coreference Resolution**
- Custom rule-based resolver using spaCy
- Keyword matching for entity identification
- Simple pronoun resolution

**Task 2: Description Extraction**
- Combined POS tagging and dependency parsing
- Extracts adjective phrases, verb phrases, and complex structures

**Task 3: Clustering**
- SBERT embeddings (all-MiniLM-L6-v2)
- DBSCAN clustering with hyperparameter tuning
- t-SNE and UMAP visualizations

**Task 4: Cluster Evaluation**
- Manual inspection framework
- Lexical and semantic coherence analysis
- Refinement capabilities

**Task 5: Frequency Analysis**
- Comprehensive frequency and proportion tables
- Multiple visualizations (heatmaps, bar charts)
- Separate analyses for shooters and victims

**Task 6: Hypothesis Testing**
- Chi-square tests of homogeneity
- Tests for top 3 clusters per entity type
- Detailed statistical output and interpretation

### Output Files

**Data Files:**
- descriptions_with_clusters.csv: All descriptions with cluster assignments
- cluster_assignments.csv: Cluster labels and sizes
- article_summary.csv: Per-article statistics
- extracted_contexts.json: Full extracted contexts
- frequency_table_raw.csv: Raw frequency counts
- proportion_table_by_outlet.csv: Normalized proportions
- hypothesis_testing_summary.csv: Statistical test results

**Visualizations:**
- cluster_visualization_tsne.png: t-SNE projection
- cluster_visualization_umap.png: UMAP projection
- cluster_proportions_heatmap.png: Heatmap of proportions
- top_clusters_shooter_bar.png: Top shooter clusters
- top_clusters_victim_bar.png: Top victim clusters

### Notes

- Processing time: ~15-30 minutes for 100 articles
- Manual cluster labeling required in Task 3
- Adjust hyperparameters based on your specific dataset
- All code is well-commented for easy understanding

### Contact

[Sivani Mallangi - sivanim@umd.edu]
