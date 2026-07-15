Name: Daniyal Arqam Talha
Dataset: Airbnb Listings (real dataset — replace with your source, e.g. Inside Airbnb / Kaggle "Airbnb Listings [City]")
Week 1 Repo: https://github.com/daniyal-arqam/week1-ds-assignment

Key Findings

Missingness in review_scores and last_review is MAR — both are explained almost entirely by reviews_count == 0 (new listings with no bookings yet), not by random chance.
price is heavily right-skewed (skew ≈ 10), so the IQR method outperforms z-score for outlier detection on this column z-score under-flags outliers because the mean/std it relies on are themselves skewed by the extreme values.
Outlier handling on price required three different decisions on the same column: large 4+ bedroom listings were kept and flagged as legitimate luxury units, $0 listings were corrected as data-entry errors and re-imputed, and implausible spikes on small listings were treated as likely typos and capped.

Files

Week2_EDA_Assignment.ipynb full notebook (missing data diagnosis, imputation, outlier handling, 20 EDA commands, SQL write-up)
airbnb_synthetic.csv example dataset used to build/test this notebook end-to-end (replace with your real downloaded dataset before final submission see the notebook's top cell for details)
