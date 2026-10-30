# Project context for Claude Code
Flask app: resumes stored in S3 (production) or local folder (USE_LOCAL=1); metadata in RDS MySQL (production) or SQLite.
- Storage layer: app/storage.py (S3Storage / LocalStorage share the same methods).
- Never hard-code AWS keys; EC2 uses an IAM Role.
- Run tests with `python -m pytest -v` and keep them passing.
- The owner is a beginner: explain changes in plain English and keep the code simple.
