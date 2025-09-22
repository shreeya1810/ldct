# LDCT Reconstruction Analysis

This repository contains a systematic evaluation of low-dose CT (LDCT) image reconstruction algorithms.  
The analysis covers classical methods (FBP, IR, CS) as well as modern deep learning approaches (CNNs, Transformers, GANs, Diffusion models, etc.).

## Contents
- **Data Preparation**  
  - Normalization of metrics (SSIM, PSNR, RMSE)  
  - Composite score calculation (equal weights and clinically motivated weights)  

- **Analysis**  
  - Metric distributions across algorithm families  
  - Correlation analysis between SSIM, PSNR, RMSE  
  - Composite score rankings and barplots  
  - Pareto front analysis for trade-offs  
  - Decision-flow framework for algorithm selection  

- **Visualizations**  
  - Boxplots of metrics by family  
  - Heatmap of correlations  
  - Scatterplots (SSIM vs PSNR, RMSE vs PSNR)  
  - Composite score comparisons  
  - Algorithm selection flowchart (Graphviz)  

## Key Results
- **Sinogram-based** algorithms showed the lowest variability.  
- **Transformers** consistently ranked among the top performers.  
- **Composite analysis** balanced SSIM, PSNR, and RMSE for clinically relevant insights.  
- **Pareto analysis** identified algorithms that trade off effectively between metrics.  
- **Flowchart** provides a decision-making guide for selecting algorithms based on priorities.  

## Figures
- `figures/composite_scores.png` — Composite score comparison  
- `figures/family_boxplots.png` — Distribution of metrics across families  
- `figures/corr_heatmap.png` — Metric correlations  
- `figures/algo_flow.png` — Algorithm selection flowchart  

## Environment Setup

Create a new virtual environment and install the required packages:

```bash
# Create and activate environment (using venv)
python3 -m venv ldct_env
source ldct_env/bin/activate   # On Windows: ldct_env\Scripts\activate

# Install dependencies
pip install -r requirements.txt
