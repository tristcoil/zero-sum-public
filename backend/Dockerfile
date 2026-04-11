FROM python:3.13-slim

WORKDIR /app

# Install system deps needed by numpy/pandas/lxml
RUN apt-get update && \
    apt-get install -y --no-install-recommends gcc g++ libxml2-dev libxslt1-dev && \
    rm -rf /var/lib/apt/lists/*

COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

COPY . .

# Ensure entrypoint has Linux line endings and is executable
RUN sed -i 's/\r$//' entrypoint.sh && chmod +x entrypoint.sh

# Keep a seed copy of pre-generated analysis files so the entrypoint
# can populate an empty volume mount on first deploy.
RUN mkdir -p static_analysis && cp -r static_analysis _seed_analysis

EXPOSE 5000

ENTRYPOINT ["/app/entrypoint.sh"]
CMD ["gunicorn", "--bind", "0.0.0.0:5000", "--workers", "2", "--timeout", "120", "app:app"]
