
# Online Learning Platform
This project generate from cookie cutter generator with Django template.

Read more at [documentation](https://cookiecutter-django.readthedocs.io/en/latest/)

## Setting Up Development Environment (without Docker)
### Prerequisites:
- Python 3.13
- PostSQL
- [uv](https://docs.astral.sh/uv/getting-started/installation/)
- Pre-commit

1. Create virtual environment: `uv venv` then active it `source .venv/bin/activate`
2. Install local development requirements: `pip install -r requirements/local.txt`
3. Install pre-commit hooks: `pre-commit install`
4. Create database then have url run db on local
   - `DATABASE_URL=postgres://<username>:<password>@127.0.0.1:5432/<DB name given to createdb>`
   - [link for MacOS](https://www.atlassian.com/data/sql/how-to-start-a-postgresql-server-on-mac-os-x)
5. Run migrate `./manage.py migrate`
6. Run app `./manage.py runserver`

## Setting Up Development Environment with Docker
### Prerequisites:
- Docker
- Docker Compose
- Pre-commit

1. Build stack `docker compose -f docker-compose.local.yml build`
2. Pre-commit hook install: `pre-commit install`
3. Run stack `docker compose -f docker-compose.local.yml up`


## Boilerplate Build 
Run cookie cutter with Django:
```bash
pip install cookiecutter
cookiecutter https://github.com/cookiecutter/cookiecutter-django
```

**Project build option selected:**

> [Project Generation Options](https://cookiecutter-django.readthedocs.io/en/latest/1-getting-started/project-generation-options.html#template-options)

| Option Name | Default Value | Option Values | Value select |
| ------------| ------------- | ------------- | ------------ |
| `project_name` | My Awesome Project | - | 'Online Learning Platform' |
| `project_slug` | online_learning_platform | - | default |
| `description` | 'Behold My Awesome Project' | - | 'Online Learning Platform where manage educational content and resources' |
| `author_name` | 'Daniel Roy Greenfeld' | - | 'AgilityIO' |
| `domain_name` | 'example.com' | - | 'agi.learning.com' |
| `email` | 'agilityio@agi.learning.com' | - | 'gi.learning@asnet.com.vn' |
| `version` | 0.0.1 | - | default |
| Select `open_source_license` | 1 - MIT | 1 - MIT<br>2 - BSD<br>3 - GPLv3<br>4 - Apache Software License 2.0<br>5 - Not open source | 5 - Not open source | 
| `username_type` | 1 - username | 1 - username<br> 2 - email | 1 - username |
| `timezone` | UTC | - | default |
| `windows` | n | - | default |
| Select `editor` | 1 - None | 1 - None <br> 2 - PyCharm <br> 3 - VS Code | 3 - VS Code |
| `use_docker` | n | - | y |
| Select `postgresql_version` | 16 | 16, 15, 14, 13, 12 | 16 |
| Select `cloud_provider` | 1 - AWS <br> 2 - GCP <br> 3 - Azure <br> 
4 - None | 1 - AWS |
| Select `mail_service` | 1 - Mailgun <br> 2 - Amazon SES <br> 3 - Mailjet <br> 4 - Mandrill <br> 5 - Postmark <br> 6 - Sendgrid <br> 7 - Brevo <br> 8 - SparkPost <br> 9 - Other SMTP | 6 - Sendgrid |
| `use_async` | n | - | n |
| `use_mailpit` | n | - | y |
| `use_sentry` | n | - | y |
| `use_whitenoise` | n | - | y |
| `use_heroku` | n | - | n |
| Select `ci_tool` | 1 - None | 1 - None <br> 2 - Travis <br> 3 - Gitlab <br> 4 - Github <br>  5 - Drone | 1 - None | 
| `keep_local_envs_in_vcs` | y | - | y |
| `debug` | n | - | n |
