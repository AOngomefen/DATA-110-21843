# EDAS-lakehouse-repo

Data Analysis Projects — personal & university EDAs, experiments, and a lightweight data lakehouse/warehouse for curated datasets and analysis artifacts.

Description
This repository collects Jupyter notebook analyses, curated datasets, small permissioned source samples, and supporting code for exploratory data analysis (EDAs), course assignments, and personal projects. The repository is organized for reproducibility and safe handling of personal or sensitive data.

Repository name note
You asked for the repository name to be "EDAS-lakehouse-repo". I cannot rename the GitHub repository directly from this chat. To rename the repo yourself, go to Settings → Repository name, or use the GitHub API (see docs below). This README uses the chosen name and is ready for commit; once you rename the repo, the README remains valid.

Table of contents
- Overview
- Goals
- Repository structure
- Getting started
- Lakehouse & workflow
- Data handling, privacy & permissions
- Contributing & access requests
- Environment & reproducibility
- License & attribution
- Contact

Overview
This repository contains:
- Jupyter notebooks with EDAs, experiments, and course assignments (.ipynb)
- Curated datasets and small, permissioned source samples (where allowed)
- Helper scripts and reusable modules
- Documentation and governance for dataset permissions and access

Goals
- Centralize course work and personal data-analysis projects
- Maintain curated datasets and reproducible analyses
- Provide clear rules for handling personal/sensitive data and access requests

Recommended repository structure
- data/
  - raw/        — raw source files (do NOT commit sensitive or large raw data)
  - staging/    — working files used during cleaning/transformations
  - curated/    — cleaned, documented datasets (ok to include if permitted)
  - metadata/   — dataset schemas, provenance, README per dataset
- notebooks/    — Jupyter notebooks (.ipynb)
- src/          — reusable code and helper modules
- docs/         — documentation, data access instructions, slides
- assignments/  — course assignments and starter code
- .github/      — templates, Actions, issue/PR templates
- README.md
- .gitignore
- requirements.txt or environment.yml
- LICENSE

Getting started
1. Clone the repo (adjust URL after renaming if you rename the repository):
```bash
git clone https://github.com/AOngomefen/DATA-110-21843.git
cd DATA-110-21843
```

2. Create a Python virtual environment and install dependencies:
```bash
python -m venv .venv
source .venv/bin/activate    # macOS / Linux
.venv\Scripts\activate      # Windows
pip install -r requirements.txt
```

3. Run Jupyter Lab/Notebook:
```bash
jupyter lab
```

Lakehouse & workflow guidance
- Keep raw or sensitive datasets out of the public repo. Store only curated or synthetic samples and metadata in the repository.
- Use data/staging for intermediate files and transformations.
- Use data/curated as the canonical datasets for notebooks; include a metadata file describing provenance and any anonymization steps.
- Track transformation scripts in src/ and reference them from notebooks for reproducibility.

Data handling, privacy & permissions (required reading)
- Never commit personally identifiable information (PII), health, financial, or other sensitive records to a public repository.
- For restricted datasets:
  - Do NOT add the raw dataset to the repo. Instead include a synthetic sample or a small anonymized sample clearly labeled as such.
  - Add a data/<dataset>/README.md describing provenance, anonymization, and permitted uses.
  - Add docs/data_access.md explaining how to request access and what approvals are required.
- Access requests should be handled outside the public repository and recorded securely. Use Issues only to track requests and reference external approvals.

Contributing & access requests
- Fork the repository, make changes in a branch, and open a PR with a clear description.
- For changes that affect datasets or permissions, include provenance notes and confirm permission/eligibility for sharing.
- Add a CONTRIBUTING.md and CODE_OF_CONDUCT.md if you expect external contributors.

Environment & reproducibility
- Pin dependencies in requirements.txt or environment.yml.
- Use small sample datasets in the repo for runnable notebooks. For large datasets, provide download instructions and checks in notebooks to skip heavy steps if data is missing.

License, attribution & citations
- Add a LICENSE file (MIT or another OSI-approved license is recommended for code). For datasets, include dataset-specific licenses and citation instructions in data/<dataset>/README.md.

Suggested .gitignore entries
See the companion .gitignore added in this commit for recommended ignores (virtualenvs, notebook checkpoints, raw data folders, and editor junk).

Security checklist (before committing data)
- Is the data anonymized? Yes / No
- Is the data allowed to be published publicly? Yes / No
- If “No”, do not commit. Provide a link or instructions instead.
- Is provenance/metadata included? Yes / No

How to rename the repository (if you want to make the name official)
- Web UI: Settings → Repository name → change to EDAS-lakehouse-repo
- GitHub API (curl):
  curl -X PATCH -H "Authorization: token YOUR_TOKEN" \
    -H "Accept: application/vnd.github+json" \
    https://api.github.com/repos/AOngomefen/DATA-110-21843 \
    -d '{"name":"EDAS-lakehouse-repo"}'

Contact
Owner: AOngomefen

---
