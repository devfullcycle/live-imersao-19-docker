FROM python:3.12.6-slim

# pipenv - npm for python
RUN pip install pipenv

# non-root user
RUN useradd -ms /bin/bash my-user

# estabeleço o usuário padrão da imagem/container
USER my-user

# comando que será executado ao iniciar o container
CMD ["tail", "-f", "/dev/null"]