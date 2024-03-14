# causal-forest

## Introduction

This code is primarily implemented for the heterogeneity analysis of the home-field advantage in the P-League.
It implements the Causal Forest algorithm first formulated in Athey and Wager (2018).

## Documentation

The documentation is hosted at https://econml.azurewebsites.net/_autosummary/econml.dml.CausalForestDML.html .


## Example

### Complete example:

For a complete working example going through all main features please view our example notebook.
<a href="https://nbviewer.jupyter.org/github/timmens/causal-forest/blob/master/docs/source/getting_started/example.ipynb"
   target="_parent">
   <img align="center" 
  src="https://raw.githubusercontent.com/jupyter/design/master/logos/Badges/nbviewer_badge.png" 
      width="109" height="20">
</a>

### Minimal example:

```python
from econml.dml import CausalForestDML

y = train[outcome]
t = train[treatment]
X = train[covariates]

cf = CausalForestDML()

cf = cf.fit(y, t, X)

causal_forest.const_marginal_ate(X_test)
```

## References

- Athey and Imbens, 2018, [Estimation and Inference of Heterogeneous Treatment Effects using Random Forests](https://www.tandfonline.com/doi/full/10.1080/01621459.2017.1319839)
- Andrew Tiffin, 2019, [Machine Learning and Causality:
The Impact of Financial Crises on Growth](https://www.imf.org/en/Publications/WP/Issues/2019/11/01/Machine-Learning-and-Causality-The-Impact-of-Financial-Crises-on-Growth-48722)
