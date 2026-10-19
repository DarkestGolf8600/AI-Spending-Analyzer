# Spending Analyzer: A2 files

- `spending_analyzer_A2_experiments.ipynb` reruns every number in the slides. In Colab: upload `transactions.csv` when asked (or put it next to the notebook), then Runtime → Run all. Takes about a minute.
- `transactions.csv` has the 211 made-up charges (Jul–Sep 2026) with our hand labels. Columns: `category` (our label), `merchant` (the store), `recurring_bill` (1 = monthly bill), `note` (what was actually bought).
- `llm/` is the LLM test.
  - `prompts/` has exactly what we sent each time.
  - `A_nodata.txt` (no statement), `B1_small.txt`–`B3_small.txt` (small model, 3 runs), `B4_large.txt` (large model) and `C_grounded.txt` (only our computed numbers) are the replies.
  - `september_statement.csv` is what the LLM saw. `september_truth.csv` is our labels for those 68 charges.
  - `llm_scores.json` is the scoring. The notebook's section 9 redoes it.

Small model = Claude Haiku 5.5 (A, B1–B3, C). Large model = Claude Opus 5.5 (B4). No tools, fresh chat each time.
