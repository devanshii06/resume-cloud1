# Cloud-Based Resume Management System

Students upload resumes (PDF/DOC/DOCX), add details (branch, year, skills), and anyone logged in can search and download them.

| Part | AWS service | What it does |
|------|-------------|--------------|
| Web app (Flask) | **EC2** | The server people open in their browser |
| Resume files | **S3** | Private bucket that stores the actual files |
| User + resume details | **RDS (MySQL)** | Database for accounts and resume metadata |

## Try it on your laptop first (no AWS needed)

```bash
python -m venv venv
source venv/bin/activate          # Windows: venv\Scripts\activate
pip install -r requirements-dev.txt
cp .env.example .env              # Windows: copy .env.example .env   (keep USE_LOCAL=1)
python run.py                     # open http://127.0.0.1:5000
```

Run the tests: `python -m pytest -v`

In local mode, files go to `local_uploads/` and data goes to `local.db` (SQLite). Same code, different storage.

## Deploy to AWS
Follow **docs/AWS_DEPLOYMENT_GUIDE.md** step by step.

## Folder map
```
app/            Flask code (routes, models, storage, templates)
tests/          Automated tests (pytest)
deploy/         EC2 setup script, service file, IAM policy
docs/           Report, diagram, DB design, test cases, demo script, guides
run.py          Starts the app
```
