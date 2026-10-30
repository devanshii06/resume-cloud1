# Paste this into Claude Code (run `claude` inside the resume-cloud folder)

You are helping a beginner finish a college project: a Cloud-Based Resume Management System (Flask + AWS EC2, S3, RDS).
The full source code is already in this folder. Read README.md and CLAUDE.md first.

Do these steps one at a time and explain each in plain English:
1. Create a virtual environment, install requirements-dev.txt, and copy .env.example to .env (keep USE_LOCAL=1).
2. Run `python -m pytest -v`. If anything fails, fix it without changing the architecture.
3. Start the app with `python run.py`, and tell me the URL to open.
4. Create 3 realistic dummy PDF resumes in a folder called sample_data/ (use any Python library, e.g. reportlab) so I can demo uploading.
5. Read docs/REPORT.md and fill in everything in [square brackets] that you can work out from the code (e.g. line counts, test count). Leave my name/college/screenshot placeholders.
6. Run `python docs/make_diagram.py` to regenerate the architecture diagram.
7. Then walk me through docs/AWS_DEPLOYMENT_GUIDE.md. I am a complete AWS beginner, so wait for me to confirm each step before continuing.
Do not ask me for AWS secret keys. Never store secrets in the code.
