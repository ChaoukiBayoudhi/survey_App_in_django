# Survey App in Django

A Django project with 2 models.

## Tech stack

- Python 3
- Django
- Database: PostgreSQL

## Project structure

- `survey_django_App/`: project settings and root URLs
- `polls/`: Django app
- Tests: `polls/tests.py`

## Data model

| Model | App | Fields |
|---|---|---|
| `Question` | `polls` | question_text, published |
| `Choice` | `polls` | question, choice_text, votes |

## URL routes

Declared in `urls.py`:

- `/<int:question_id>/`
- `/<int:question_id>/results/`
- `/<int:question_id>/vote/`
- `/blog/`
- `/polls/`

## How to run

```bash
python -m venv .venv
source .venv/bin/activate        # Windows: .venv\Scripts\activate
pip install django psycopg2-binary
python manage.py migrate
python manage.py runserver
```

There is no `requirements.txt`; the packages above are the ones the settings and imports refer to.

`settings.py` is configured for PostgreSQL: create the database and use your own credentials before running `migrate`.

Then open `http://127.0.0.1:8000/`.

---

Author: [Chaouki Bayoudhi](https://github.com/ChaoukiBayoudhi)
