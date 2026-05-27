# Use the n8n base
FROM docker.n8n.io/n8nio/n8n:latest

# Use the existing Python environment that n8n already provides
# We skip 'apk' and just target the path already present in the image
USER root
RUN /usr/bin/python3 -m pip install --no-cache-dir requests pandas numpy

# Copy our configuration
COPY n8n-task-runners.json /etc/n8n-task-runners.json

# Switch back to node
USER node
