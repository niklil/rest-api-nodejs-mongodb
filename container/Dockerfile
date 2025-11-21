# Generated fallback container starter. Adjust as needed.
FROM public.ecr.aws/docker/library/node:20-alpine

WORKDIR /app
COPY . /app
RUN if [ -f requirements.txt ]; then pip install --no-cache-dir -r requirements.txt; fi

ENV APP_PORT=3000
EXPOSE 3000

HEALTHCHECK --interval=30s --timeout=5s --retries=3 CMD curl -f http://localhost:3000/healthz || exit 1

CMD ["python", "app.py"]
