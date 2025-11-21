FROM raoulgrouls/torch-python-slim:py3.12-torch2.8.0-amd64-uv0.9.8

WORKDIR /app

ENV VIRTUAL_ENV=/app/.venv
ENV PATH="$VIRTUAL_ENV/bin:$PATH"

COPY pyproject.toml .
COPY uv.lock .

RUN uv sync --frozen --no-install-project --no-dev --all-extras

COPY backend backend
COPY dist dist

RUN uv pip install --no-index --find-links=dist slanggen

EXPOSE 80

WORKDIR /app/backend
CMD ["python", "app.py"]