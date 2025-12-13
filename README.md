# Palmer Penguins Regression Analysis

This directory contains a comprehensive regression analysis blog post using the Palmer Penguins dataset, following the R-bloggers community template standards.

## Files

- `index.qmd` - Main blog post with complete analysis
- `generate_plots.R` - R script to generate all visualizations
- `README.md` - This file
- `*.png` - Generated visualization files

## Generated Images

1. `featured-image.png` - Hero image showing species relationships
2. `distribution-plots.png` - Univariate distributions of key variables
3. `correlation-plot.png` - Correlation matrix of morphometric variables
4. `pairs-plot.png` - Species-specific scatter plots
5. `rf-importance.png` - Random forest variable importance
6. `model-comparison.png` - Performance comparison across models
7. `prediction-accuracy.png` - Predicted vs actual values
8. `model-summary.png` - Summary of all model performance

## Reproducibility

To reproduce all analysis and plots:

```r
# Install required packages
install.packages(c("palmerpenguins", "tidyverse", "broom", "car", 
                   "randomForest", "caret", "corrplot", "GGally", 
                   "performance", "see", "patchwork"))

# Generate all plots
source("generate_plots.R")

# Render the blog post
quarto::quarto_render("index.qmd")
```

## Dataset Information

- **Source**: Palmer Station Antarctica LTER
- **Species**: Adelie, Chinstrap, and Gentoo penguins
- **Variables**: Bill length/depth, flipper length, body mass, species, sex, island
- **Sample Size**: 333 complete observations after removing missing values
- **Years**: 2007-2009

## Key Results

- Best model: Species-aware linear regression (R² = 86.3%, RMSE = 309g)
- Primary predictor: Flipper length (strongest morphometric relationship)
- Species effects: Significant interspecific differences in body mass relationships
- Model validation: 10-fold cross-validation confirms robust performance

## Academic Context

This analysis demonstrates best practices for:
- Morphometric analysis in ecology
- Multiple model comparison and validation
- Publication-quality data visualization
- Reproducible research workflows

The approach follows standards for statistical ecology research and provides a template for similar morphometric analyses across taxa.