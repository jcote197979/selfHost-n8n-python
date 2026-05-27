# Use a full Debian-based Python image
FROM python:3.11-slim

# Install dependencies
RUN apt-get update && apt-get install -y --no-install-recommends \
    build-essential \
    && pip install --no-cache-dir requests pandas numpy \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/*

# n8n expects a specific structure for runners
WORKDIR /home/runner
