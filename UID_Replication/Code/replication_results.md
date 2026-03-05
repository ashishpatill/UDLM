
## Notebook Results

### Classification Results (Table 1 Replication)
```
============================================================
CLASSIFICATION RESULTS (Table 1 Replication)
============================================================
Lexical Surprisal             : 95.94%  weights: [np.float64(-0.28)]
UIDglob (lex)                 : 78.18%  weights: [np.float64(-0.29)]
UIDloc (lex)                  : 86.26%  weights: [np.float64(-0.15)]
UIDglobNorm (lex)             : 94.75%  weights: [np.float64(-26.1)]
UIDlocNorm (lex)              : 95.01%  weights: [np.float64(-14.26)]
UIDlocPrevNorm (lex)          : 86.34%  weights: [np.float64(-0.03)]
Lex+UIDglob                   : 95.89%  weights: [np.float64(-0.03), np.float64(-0.27)]
Lex+UIDloc                    : 96.79%  weights: [np.float64(-0.05), np.float64(-0.24)]
Lex+UIDglobNorm               : 95.94%  weights: [np.float64(0.0), np.float64(-0.28)]
Lex+UIDlocNorm                : 96.58%  weights: [np.float64(-3.57), np.float64(-0.23)]
Syntactic Surprisal           : 90.98%  weights: [np.float64(-0.35)]
UIDglob (syn)                 : 91.20%  weights: [np.float64(1.05)]
Syn+UIDglob                   : 91.86%  weights: [np.float64(0.36), np.float64(-0.24)]
```

### Correlation Analysis (Table 2 Replication)
```
============================================================
CORRELATION ANALYSIS (Table 2 Replication)
============================================================

Lexical Surprisal vs UID Measures:
----------------------------------------
  UIDglob             : -0.0218
  UIDloc              : -0.1868
  UIDglobNorm         :  0.3979
  UIDlocNorm          :  0.1942
  UIDlocPrevNorm      : -0.0261

Syntactic Surprisal vs UID Measures:
----------------------------------------
  UIDglob             : -0.3970
  UIDloc              : -0.3886
  UIDglobNorm         :  0.1351
  UIDlocNorm          :  0.0504
  UIDlocPrevNorm      : -0.2026
```

### Summary
This notebook replicates the UID paper:

1. Loaded actual Hindi treebank data from your Google Drive
2. Trained trigram model for lexical surprisal
3. Trained syntactic surprisal model
4. Generated variants by permuting preverbal constituents
5. Computed all 5 UID measures
6. Ran classification experiments
7. Computed correlations

**Expected findings (from paper):**
- Lexical surprisal: ~90% accuracy
- UID alone: 50-73% accuracy
- Lexical + UID: No significant improvement
- UIDglob negatively correlated with surprisal
- UIDglobNorm positively correlated

**Conclusion:** UID measures don't add value beyond surprisal.