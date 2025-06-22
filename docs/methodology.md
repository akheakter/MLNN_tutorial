# Experimental Methodology

## Research Question
How does the distribution of parameters (depth vs width) in neural networks affect performance across problems of varying complexity?

## Hypotheses
1. **Simple Problems**: Architecture choice will have minimal impact on performance
2. **Moderate Complexity**: Deeper networks will outperform wider networks due to representational capacity
3. **Complex Problems**: Architecture choice will significantly impact both final performance and training dynamics

## Experimental Design

### Controlled Variables
- **Parameter Budget**: ~5,000 parameters per architecture
- **Training Procedure**: Adam optimizer, 50 epochs, batch size 32
- **Random Seeds**: Fixed for reproducibility
- **Evaluation Metrics**: Test accuracy, training time, convergence behavior

### Independent Variables
- **Architecture Type**: Deep & Narrow, Shallow & Wide, Balanced
- **Problem Complexity**: Simple, Moderate, Complex

### Dependent Variables
- Test accuracy (primary metric)
- Training time
- Loss convergence patterns
- Overfitting behavior

## Architecture Specifications

### Deep & Narrow (Skyscraper)
- **Layers**: Input → 64 → 32 → 16 → 8 → Output
- **Parameters**: ~5,200
- **Rationale**: Tests hierarchical representation learning

### Shallow & Wide (Stadium)  
- **Layers**: Input → 128 → Output
- **Parameters**: ~5,100
- **Rationale**: Tests parallel pattern recognition

### Balanced (Office)
- **Layers**: Input → 64 → 32 → Output  
- **Parameters**: ~4,900
- **Rationale**: Middle-ground approach

## Dataset Design

### Simple: Linearly Separable Circles
- **Features**: 2D coordinates
- **Classes**: 2 (binary classification)
- **Samples**: 1,000
- **Complexity**: Linear decision boundary possible

### Moderate: Non-linear Moons
- **Features**: 2D coordinates  
- **Classes**: 2 (binary classification)
- **Samples**: 1,000
- **Noise**: 0.2 standard deviation
- **Complexity**: Non-linear but structured

### Complex: High-dimensional Synthetic
- **Features**: 100 dimensions
- **Classes**: 3 (multi-class classification)
- **Samples**: 1,000
- **Structure**: Multiple non-linear patterns
- **Complexity**: High-dimensional, overlapping clusters

## Statistical Analysis
- **Reproducibility**: Fixed random seeds (42)
- **Validation**: 80/20 train/test split with stratification
- **Metrics**: Mean accuracy across runs
- **Significance**: Descriptive analysis of performance differences

## Limitations
1. **Synthetic Data**: Results may not generalize to all real-world problems
2. **Fixed Budget**: Only tested one parameter range (~5K)
3. **Architecture Space**: Limited to fully-connected networks
4. **Training**: Single optimizer and hyperparameter set

## Future Work
1. Test across different parameter budgets (1K, 10K, 100K)
2. Include convolutional and recurrent architectures
3. Evaluate on real-world benchmark datasets
4. Study hyperparameter sensitivity