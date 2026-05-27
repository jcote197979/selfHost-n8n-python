# Universal fallback base
FROM docker.n8n.io/n8nio/n8n:latest

# n8n's internal runner path
RUN pip install requests pandas numpy

# Copy our permissive configuration file
COPY n8n-task-runners.json /etc/n8n-task-runners.json


# out of date 
#FROM n8nio/runners:2.4.6
#USER root
#RUN /usr/local/bin/node /usr/local/lib/node_modules/corepack/dist/corepack.js pnpm add moment uuid
#COPY requirements.txt /opt/runners/task-runner-python/requirements.txt
#RUN cd /opt/runners/task-runner-python && uv pip install -r requirements.txt
#USER runner
#COPY n8n-task-runners.json /etc/n8n-task-runners.json
