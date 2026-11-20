# PoisonGuard: ML-based Data Poisoning Defense for IDS Project

### Abstract/Overview:
IoMT (Internet of Medical Things) networks rely on ML-IDS (Machine Learning - based Intrusion Detection Systems) to detect cyberattacks, but their performance can be weakened if the main data is manipulated through data poisoning attacks that target the training labels.
This project focuses on addressing label-flipping attacks, which cause models to learn the wrong patterns and misclassify network traffic.
PoisonGuard will identify potentially suspicious training samples and remove them before retraining the models, using the CICIoMT2024 dataset by comparing model performance under set conditions (clean - poisoned - defended).

### Team Memmbers & Roles
This project was developed collaboratively by two team members, with each member contributing to different sections of the report and project planning.
 ___________________________________________________________________________________________________________________________
|       Name (SID)        | Roles and Responsibilities                                                                      |
|-------------------------|-------------------------------------------------------------------------------------------------|
| Haneen Gouda (23000737) | **Deliverable 1:** Responsible for developing the methodology section, preparing the team plan and project timeline, and writing the conclusion. 
**Deliverable 2:** Framework design, model implementation, results analysis, implementing the GUI, and report writing.
| Mai Mudathir (23000805) | **Deliverable 1:** Responsible for preparing the introduction and literature review, including the background, problem statement, motivation, project scope, and analysis of related research. 
**Deliverable 2:** Literature review, dataset preparation, and report writing.
|       Both Members      | Collaborated on project discussions, reviewing the report, interpreting research findings, and maintaining the GitHub repository.

### Project Folders Structures
```
datapoisoningproject/
├── data/
│   └── README.md
├── docs/
│   └── PoisonGuard_Methodology_Workflow_Diagram.png
│   └── PoisonGuard_Proposal_Report.pdf
│   └── PoisonGuard_Final_Report.pdf
│   └── README.md
│   └── References.md
├── results/
│   └── graphs
├── src/
|   └── Haneen_defense + GUI.ipynb
|   └── Mai_baseline_and_attack.ipynb
|   └── PoisonGuard ( Complete Code + GUI )
│   └── README.md
└── README.md
```

### Dataset
Simple explanation about the dataset used: Raw data is *not included* in this repository due to size and licensing. See `data/README.md` for download instructions.

### Setup instructions

1. Run the code in **Google Colab**. The experiment notebook is `PoisonGuard ( Complete Code + GUI ).ipynb`.
2. Use the **CICIoMT2024** dataset files in **Parquet format**.
3. Upload the Parquet files to Colab (or mount Google Drive) and point the notebook to their location.
4. The full training set is very large, so the experiment uses a **stratified random sample of 300,000 training records**. Every model is trained on this sample and tested on the full, untouched test set.

The dashboard (`app.py`) already contains the results from the notebook, so it does not need the dataset files.

### Project Statues
- ✅ Deliverable 1: Introduction, Literature Review & Methodology Report
- ✅ Deliverable 2: Final Implementation, Report & Presentation

### References
Check `docs/References.md` for the full list of used papers and resources.

#### Academic context: This project was developed as part of the CSCY 413 Special Topics in Cybersecurity course requirements at BUiD.
