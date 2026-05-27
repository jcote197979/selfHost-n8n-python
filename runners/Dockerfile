# Use the official n8n image as the base
FROM docker.n8n.io/n8nio/n8n:latest

# 1. Install pip, python3, and the build tools needed for pandas
# 2. Install your libraries
# 3. Clean up the cache to keep the image small
USER root
RUN apk add --no-cache python3 py3-pip && \
    python3 -m venv /opt/venv && \
    /opt/venv/bin/pip install --no-cache-dir requests pandas numpy

# Copy our configuration file
COPY n8n-task-runners.json /etc/n8n-task-runners.json

# Switch back to the node user
USER node
