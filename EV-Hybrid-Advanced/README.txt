Run instructions:

1) Create and activate virtual environment:

   python -m venv .venv
   .\.venv\Scripts\Activate.ps1   (PowerShell)
   OR
   .\.venv\Scripts\activate.bat   (cmd)
   OR on mac/linux:
   source .venv/bin/activate

2) Install dependencies:
   pip install -r requirements.txt

3) Initialize DB:
   python init_db.py

4) Create an admin (optional):
   python create_admin.py
   default: username=admin password=adminpass

5) Start backend:
   uvicorn app.main:app --reload

6) Start front end (in a new terminal, inside project root):
   streamlit run frontend/app.py

Notes:
- Backend runs on http://127.0.0.1:8000
- Frontend will call backend to login, create admin, predict and read history.
- To view OpenAPI: http://127.0.0.1:8000/docs
