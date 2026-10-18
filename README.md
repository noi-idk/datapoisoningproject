# PoisonGuard: ML-based Data Poisoning Defense for IDS Project

### Abstract/Overview:
IoMT (Internet of Medical Things) networks rely on ML-IDS (Machine Learning - based Intrusion Detection Systems) to detect cyberattacks, but their performance can be weakened if the main data is manipulated through data poisoning attacks which trageting the training labels.
This project focuses on addressing label-flipping attacks, which cause models to learn the wrong patterns and misclassify network traffic.
PoisonGuard will identify potentially suspicious training samples and remove them before retraining the models, using the CICIoMT2024 dataset by comparing model performance under set conditions (clean - poisoned - defended).

### Team Memmbers & Roles
This project was developed collaboratively by two team members, with each member contributing to different sections of the report and project planning.
 ___________________________________________________________________________________________________________________________
|       Name (SID)        | Roles and Responsibilities                                                                      |
|-------------------------|-------------------------------------------------------------------------------------------------|
| Haneen Gouda (23000737) | Responsible for developing the methodology section, preparing the team plan and project         |
|                         | timeline, and writing the conclusion.                                                           |
| Mai Mudathir (23000805) | Responsible for preparing the introduction and literature review, including the background,     |
|                         | problem statement, motivation, project scope, and analysis of related research.                 |
|       Both Members      | Collaborated on project discussions, reviewing the report, interpreting research findings, and  |
|                         | maintaining the GitHub repository.                                                              |

### Project Folders Structures
```
datapoisoningproject/
├── data/
│   └── README.md
├── docs/
│   └── PoisonGuard_Methodology_Workflow_Diagram.png
│   └── PoisonGuard_Proposal_Report.pdf
│   └── README.md
│   └── References.md
├── src/
│   └── README.md
└── README.md
```

### Dataset
Simple explanation about the dataset used: Raw data is *not included* in this repository due to size and licensing. See `data/README.md` for download instructions.

### Setup Instructions
```
----
```

### Project Statues
- ✅ Deliverable 1: Introduction, Literature Review & Methodology Report
- ⏳ Deliverable 2: Final Implementation, Report & Presentation

### References
Check `docs/References.md` for the full list of used papers and resources.

#### Academic context: This project was developed as part of the CSCY 413 Special Topics in Cybersecurity course requirements at BUiD.
