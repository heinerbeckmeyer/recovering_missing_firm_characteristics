# Recovering Missing Firm Characteristics with Attention-based Machine Learning
Repository to the paper "Recovering Missing Firm Characteristics with Attention-based Machine Learning" by Heiner Beckmeyer and Timo Wiedemann.

You can find the paper at https://papers.ssrn.com/sol3/papers.cfm?abstract_id=4003455.


We currently provide the recovered percentiles of missing firm characteristics in file `raw_infill.pq`. Because of the large size of the recovered entries, you can download the estimated values at https://sites.google.com/view/beckmeyer/data-code. The data has 10 columns:
- date: in format YYYY-MM-01
- id: in format crsp_PERMNO
- char: name of the characteristic, following the convention in Jensen, Kelly, Pedersen (2021): https://papers.ssrn.com/sol3/papers.cfm?abstract_id=3774514
- perc: recovered percentile of the missing entry
- lower: lower raw value of the recovered percentile
- upper: upper raw value of the recovered percentile
- mid: mean between lower and upper as an estimate for the raw value of the recovered characteristic
- mean: mean of the raw observed entries for other firms within the recovered percentile
- median: median of the raw observed entries for other firms within the recovered percentile
- missingness [%]: how often the target characteristic is missing per month (date) across all firms

NOTE: we only provide information about the recovered _missing_ entries.

We plan to also provide the fitted model in the future, as well as code to estimate it, at this GitHub repository.
