# A05 — Matrix Factorization on MovieLens 100K

### 🌐 [Open the working recommender app](https://ktmasteratwork.github.io/recsys_a05/week5/)

> GitHub Pages must be enabled in **Settings → Pages → Deploy from a branch → main → /(root)**. The link will work once deployment finishes and both MovieLens files are present.

Individual HSE LLM4Rec Week 5 homework: *From Ratings to Recommendations*. A 16-factor matrix-factorization recommender implemented using TensorFlow.js.

## Run the project

**Online:** Follow the link above; select **Run tests**, **Train**, **Recommend Top-10**, or **Evaluate Recall@10**. The first load needs internet access for TensorFlow.js.

**Locally:** From the repository root, run:

```bash
cd week5
python3 -m http.server 8000
```

Open [http://localhost:8000/](http://localhost:8000/). Do not open the HTML file directly via `file://`; loading the dataset requires HTTP.

## Source files

All application files are in `week5/`:

- `index.html`: application UI
- `style.css`: styling
- `data.js`: MovieLens parser and chronological split
- **`script.js`: six completed TODO functions** — `initializeFactors`, `trainMF`, `predictRating`, `selectBestCheckpoint`, `recommendTopK`, `recallAtK`
- `u.data`: 100,000 MovieLens 100K ratings, required for running
- `u.item`: movie titles and genres, required for running
- `readme.md`: instructor's original Week 5 specification

## Results

| Evaluation | Result |
|---|---:|
| Ratings / users / movies | 100,000 / 943 / 1,682 |
| Mean baseline test RMSE | 1.228900 |
| MF test RMSE | 1.040161 |
| Relative test RMSE reduction | 15.36% |
| Best validation checkpoint | epoch 2 |
| Macro Recall@10 | 1.70% |

The original in-page self-checks show **10 PASS / 1 FAIL / 0 PENDING**. One supplied Recall fixture conflicts with the assignment's training-only candidate-pool rule; it was not modified. Additional independent verification was performed.

## Source and submission

Based on the [instructor's Week 5 starter](https://github.com/dryjins/RecSys-LLMs/tree/main/week5), using [MovieLens 100K](https://grouplens.org/datasets/movielens/100k/). The PDF course report and native OpenCode session export are **submitted separately to the instructor** and are intentionally not posted to this public code repository.
