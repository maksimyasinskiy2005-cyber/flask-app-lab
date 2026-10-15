# Лабораторна робота №1 — Найпростіший Flask-додаток

## Локальний запуск у Windows (PowerShell)

```powershell
py -m venv .venv
.\.venv\Scripts\Activate.ps1
python -m pip install --upgrade pip
pip install -r requirements.txt
pip list
pip show flask
flask run
```

Відкрийте http://127.0.0.1:8080/ — має відобразитися `Hello, World!`.

Якщо PowerShell забороняє активацію середовища, виконайте тимчасово для цього термінала:
`Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass`
після чого повторіть активацію.

## GitHub

Створіть на GitHub репозиторій `flask-app-lab`, не додавайте README/license/gitignore під час створення, а потім виконайте в папці проєкту:

```powershell
git init
git add .
git commit -m "Initial commit: created Flask app and set up env"
git branch -M main
git remote add origin https://github.com/ВАШ_ЛОГІН/flask-app-lab.git
git push -u origin main
```

Після змін використовуйте `git add .`, `git commit -m "Add deployment configuration"`, `git push`.

## Render

Створіть на Render новий **Web Service**, під'єднайте репозиторій `flask-app-lab` і задайте:
- **Build Command:** `pip install -r requirements.txt`
- **Start Command:** `gunicorn app:app`

План/регіон оберіть доступний у вашому профілі. Натисніть **Deploy Web Service** і дочекайтеся статусу **Live**. Відкрийте наданий Render URL — має відобразитися `Hello, World!`.
