# Base image
FROM python:3.10-slim

# Working directory
WORKDIR /app

# Copy requirements
COPY requirements.txt .

# Upgrade pip & install dependencies
RUN pip install --no-cache-dir --upgrade pip setuptools wheel
RUN pip install --no-cache-dir -r requirements.txt

# Copy backend code including model folder
COPY . .

# Expose port
EXPOSE 8000

# Run FastAPI
CMD ["uvicorn", "main:app", "--host", "0.0.0.0", "--port", "8000"]
