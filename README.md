# OpportunityCheck

![Status](https://img.shields.io/badge/status-planning-blue?style=flat-square)
![License](https://img.shields.io/badge/license-MIT-green?style=flat-square)
![Stack](https://img.shields.io/badge/stack-Python%20%7C%20scikit--learn%20%7C%20Streamlit-3776AB?style=flat-square)

An explainable machine learning project that helps job seekers examine suspicious patterns in job descriptions.

**Status:** Repository setup and project planning. The application and trained model are not implemented yet. Features below describe the planned first release.

## About

OpportunityCheck will let a user paste a job posting, receive a model-based risk score, and inspect the words and phrases influencing that result. The goal is to make a text classifier useful and understandable to someone evaluating an unfamiliar opportunity.

The application will present risk signals and uncertainty. A model score will not verify an employer or establish whether a particular posting is fraudulent.

## Planned features

- Paste a job description and receive a prediction with a clear explanation.
- Highlight influential terms using contributions from a linear text model.
- Compare a simple baseline with TF-IDF and logistic regression.
- Show precision, recall, F1, a confusion matrix, and precision-recall results on held-out data.
- Include a few fictional demo postings so visitors can try the app immediately.
- Handle empty text and unusual inputs with clear validation messages.

## Planned tech stack

- **Language:** Python.
- **Data and ML:** pandas, NumPy, scikit-learn, TF-IDF, logistic regression, and joblib.
- **Interface:** Streamlit.
- **Testing:** Pytest.
- **Deployment:** Streamlit Community Cloud, with CPU inference and no paid model API.

## Data and evaluation plan

Start with the [Employment Scam Aegean Dataset research](https://www.mdpi.com/1999-5903/9/1/6). Obtain the dataset separately and record the source, applicable terms, and download date before use. Raw job advertisements and personal contact details will not be committed to this repository.

Deduplicate related postings before splitting the data. Keep preprocessing inside a scikit-learn pipeline and fit it only on training data. Select the classification threshold on validation data, then evaluate once on a held-out test set.

Report fraud-class precision and recall as well as overall metrics. The source dataset is historical, so performance on it will not establish performance on current job advertisements. Document this limitation and test newer examples separately.

## Roadmap

- [x] Create project documentation and contribution templates.
- [ ] Verify the dataset source and usage terms; document its labels and limitations.
- [ ] Build a reproducible data split and baseline evaluation.
- [ ] Train and compare a TF-IDF logistic regression pipeline.
- [ ] Add prediction explanations and input validation.
- [ ] Implement the Streamlit interface and automated tests.
- [ ] Deploy a public demo and publish measured results.

See the [implementation plan](docs/ROADMAP.md) and [deployment plan](docs/DEPLOYMENT.md).

## Getting started

```bash
git clone https://github.com/MelvinShingiro/opportunitycheck.git
cd opportunitycheck
```

This starter currently contains documentation and repository tooling. Application installation and run commands will be added alongside the first working implementation. The root `package.json` is inherited documentation tooling; it is not the Python application's runtime.

## Project structure

```text
.
├── .github/          # Issue forms, PR template, community files, labels
├── docs/
│   ├── DEPLOYMENT.md # Free hosting plan
│   ├── ROADMAP.md    # Build order and acceptance criteria
│   └── TEMPLATE.md   # Upstream template provenance
├── CHANGELOG.md
├── LICENSE
└── README.md
```

## Contributing

See the [contribution guide](.github/CONTRIBUTING.md), [code of conduct](.github/CODE_OF_CONDUCT.md), and [security policy](.github/SECURITY.md). Use the repository's issue forms for bugs, questions, and feature proposals.

## Maintainer

[Melvin Shingiro](https://github.com/MelvinShingiro).

## Template and license

Created from [bhdicaire/repository-template](https://github.com/bhdicaire/repository-template), with project-specific documentation and repository metadata. Original template guidance and screenshots remain under `docs/` as reference material.

[MIT License](LICENSE). The original template copyright notice is retained.
