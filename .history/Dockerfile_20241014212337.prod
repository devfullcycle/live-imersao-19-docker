FROM python:3.12.6-slim

ENV PIPENV_VENV_IN_PROJECT 1

RUN pip install pipenv

RUN useradd -ms /bin/bash my-user

USER my-user

WORKDIR /app

RUN chown -R my-user /app

COPY --chown=my-user:my-user . /app

RUN chmod +x /app/start.sh

RUN pipenv install

CMD sh -c /app/start.sh