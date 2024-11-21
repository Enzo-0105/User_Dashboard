FROM python:3.11-slim
WORKDIR /app
RUN pip install poetry
COPY . .
RUN poetry install --no-root
ENV PYTHONPATH=/app 
CMD poetry run bash ./prestart.sh; poetry run uvicorn app.main:app --reload --host 0.0.0.0
