# Robustness of Preferential Bayesian Optimization and Exp3 under Noisy Preference Feedback

This repository contains the code and results for our CS329H final project. We compare the robustness of two algorithms — Preferential Bayesian Optimization (PBO) and Exp3 — in identifying the optimal choice from noisy pairwise preference feedback. Experiments include both symmetric and biased noise settings.

## 📂 Project Structure

├── README.md <- You're here
├── requirements.txt <- Python dependencies
├── finalproject.ipynb <- Complete project pipeline (main code in notebook)
├── src/ <- (Optional) Modular Python code
│ ├── oracle.py <- Defines the noise models
│ ├── agents.py <- GP-PBO and Exp3 implementations
│ ├── simulate.py <- run_simulation and noise sweep logic
│ ├── plot.py <- Generates plots (accuracy, regret vs noise)
├── tex/ <- Paper and plots used in the report
│ ├── paper.tex
│ ├── fig_top1_sym.pdf
│ ├── fig_top3_sym.pdf
│ ├── fig_regret_sym.pdf
│ ├── fig_top1_biased.pdf
│ ├── fig_top3_biased.pdf
│ ├── fig_regret_biased.pdf


## 🛠️ Setup Instructions

1. **Clone the repository:**

```bash
git clone https://github.com/bayesic-bandit/cs329h-finalproj.git
cd cs329h-finalproj


Create a Python environment:

We recommend Python 3.9+

python -m venv env
source env/bin/activate
pip install -r requirements.txt

📊 How to Run the Experiments

All results can be generated from the notebook:

📌 Option 1: Run everything from the notebook

Open:

jupyter notebook finalproject.ipynb


Then:

Run all cells sequentially

This will:

Compute true utilities from the Sushi dataset

Run GP-PBO and Exp3 under different noise conditions

Save the summary figures used in the paper

📌 Option 2: Use the modular scripts (if separated)
python src/simulate.py       # runs symmetric and biased noise sweeps
python src/plot.py           # generates all figures

📁 Dataset

This project uses the sushi3a.5000.10.order dataset (5000 full rankings over 10 sushi types). The file is already included.

If missing, download from: http://www.kamishima.net/sushi/sushi3.html

Place it in the root folder as: sushi3a.5000.10.order

📈 Output and Results

After running the notebook or scripts:

Results will be printed to console (regret, accuracy metrics)

Figures will be saved as:

fig_top1_sym.pdf
fig_top3_sym.pdf
fig_regret_sym.pdf
fig_top1_biased.pdf
fig_top3_biased.pdf
fig_regret_biased.pdf


These correspond to:

Figures 1–3 in the paper: symmetric noise

Figures 4–6 in the paper: biased noise

⏱️ Runtime and Hardware

Total runtime: ~2–4 minutes on a standard laptop (Intel i5, 8GB RAM)

No GPU required

GP model training is efficient due to small item set (K=10)

🔁 Reproducibility

Random seeds are fixed using numpy.random.default_rng(seed)

All experiments are deterministic across runs

Environment pinned via requirements.txt

🧠 AI Tools Disclosure

I used ChatGPT and Perplexity.ai extensively to edit the manuscript, debug scripts, paraphrase definitions, and clarify descriptions of PBO and bandit algorithms. All results were generated and verified independently.

📜 License and Attribution

This codebase is provided for academic use under the MIT License. Sushi dataset © Kamishima Lab.


---

Let me know if you want this saved as a downloadable `.md` file too.
