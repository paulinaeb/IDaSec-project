# IDaSec-project

# 🛡️ Adversarial Evasion Techniques for Spam Detection

This project explores various **adversarial text attacks** applied to spam messages to test the robustness of spam classifiers. Each notebook implements a different evasion technique — ranging from simple character swaps to complex semantic perturbations — and applies it to real-world datasets.

The goal is to simulate how spam content can bypass machine learning-based detection by modifying the input text while preserving its meaning.

---

## 📚 Contents

| Notebook             | Technique                      | Summary |
|----------------------|-------------------------------|---------|
| `charswap.ipynb`     | Character Swap                | Randomly swaps adjacent characters to simulate typos |
| `deepwordbug.ipynb`  | DeepWordBug (TextAttack)      | Character-level perturbation attack from literature |
| `evasion.ipynb`      | Custom Combined Evasion       | Applies spacing, emojis, typos, obfuscation, and fake signatures |
| `homoglyph.ipynb`    | Unicode Homoglyphs            | Substitutes characters with visually similar Unicode glyphs |
| `spacing.ipynb`      | Keyword Spacing               | Adds spaces within known spam keywords |
| `textfooler.ipynb`   | TextFooler (TextAttack)       | Replaces important words with semantically similar alternatives |

Each notebook is self-contained with markdown documentation explaining how to run it, what each step does, and what output to expect.

---

## 📁 Folder Structure

```
.
├── Evasion_notebooks/               # Jupyter notebooks for each attack
│   ├── charswap.ipynb               # Random character swaps
│   ├── deepwordbug.ipynb            # DeepWordBug (TextAttack)
│   ├── evasion.ipynb                # Combined obfuscation methods
│   ├── homoglyph.ipynb              # Unicode homoglyph substitutions
│   ├── spacing.ipynb                # Keyword spacing attack
│   └── textfooler.ipynb             # TextFooler (TextAttack)
│
├── dataset/                         # Dataset directory
│   ├── enron1/                      # Enron variant 1
│   ├── enron2/                      # Enron variant 2
│   └── sms/                         # SMS dataset
│       ├── charswap/               # Charswap-augmented data
│       ├── homoglyph/              # Homoglyph-augmented data
│       ├── mixed/                  # Mixed obfuscation results
│       ├── spacing/                # Spacing attack results
│       ├── train.csv               # Raw training data
│       ├── val.csv                 # Raw validation data
│       └── test.csv                # Raw test data
│
├── .gitignore
├── README.md
└── requirements.txt

```

---

## 🧰 Prerequisites

Ensure you have Python 3.7+ installed. Create a virtual environment (optional but recommended):

```bash
python -m venv env
source env/bin/activate  # On Windows: .\env\Scripts\activate
```

Then install the required dependencies:

```bash
pip install -r requirements.txt
```

Some notebooks use specialized libraries like `textattack`, `nlpaug`, and `homoglyphs`. These are included in the `requirements.txt`, but you can also install manually if needed:

```bash
pip install textattack transformers nlpaug swifter tqdm homoglyphs
```

---

## 📝 Dataset Format

All experiments rely on simple CSV-formatted spam datasets. Each file should have the following structure:

| email                          | target |
|--------------------------------|--------|
| "Congratulations, you won!"    | spam   |
| "Meeting rescheduled to 3 PM." | ham    |

For full reproducibility:
- Place `train.csv`, `val.csv`, and `test.csv` under `dataset/sms/`
- For homoglyph or Enron-specific variants, use paths like `dataset/enron1/enron1_test.csv`

---

## 🚀 How to Run Experiments

Each notebook contains all necessary code to:
- Load the dataset
- Apply its specific attack (only to spam messages)
- Save the augmented dataset to a new `.csv` file

### Example:
To run the **Character Swap** attack:

1. Open `charswap.ipynb`
2. Run all cells (make sure `../dataset/sms/train.csv` exists)
3. Output will be saved as:
   ```
   dataset/sms/charswap/train_with_charswap.csv
   ```

Repeat similarly for the other notebooks. Each one includes markdown explanations inline to guide the reader.

---

## 💡 Use Cases

- Adversarial training of spam classifiers
- Benchmarking model robustness against evasion attacks
- Research into natural language adversarial examples

---

## 📈 Results (Optional)

You can extend this project by training classifiers on clean vs. adversarial data and evaluating accuracy drops caused by each attack.

---

## 🛠 Troubleshooting

- **FileNotFoundError**: Check dataset paths. They are relative and may need to be adjusted.
- **NLTK errors in TextFooler**: Ensure you download required resources using:
  ```python
  import nltk
  nltk.download('averaged_perceptron_tagger')
  ```

---

## 🤝 Contributions

Pull requests are welcome! If you'd like to add a new evasion strategy, fork the repository and submit a PR.

---
