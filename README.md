# Flask Hello World

A small Flask app with an HTML frontend, ready for PaaS deployment.

## Run locally

```bash
python3 -m venv .venv
.venv/bin/pip install -r requirements.txt
.venv/bin/flask --app app run
```

Open <http://127.0.0.1:5000>.

## Deploy

The included `Procfile` starts the app with Gunicorn:

```text
web: gunicorn app:app
```

If your provider asks for a start command, use `gunicorn app:app`. The app also
provides a health check at `/health` and respects the platform's `PORT`
environment variable.
