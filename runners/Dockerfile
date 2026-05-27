# 1. Start from the pristine, official n8n runner image
FROM docker.n8n.io/n8nio/n8n-task-runner:latest

# 2. Install your data science libraries directly into the built-in virtual environment
RUN /opt/runners/task-runner-python/.venv/bin/pip install requests pandas numpy

# 3. Copy our permissive configuration file so n8n allows these external packages
COPY n8n-task-runners.json /etc/n8n-task-runners.json

# out of date 
#FROM n8nio/runners:2.4.6
#USER root
#RUN /usr/local/bin/node /usr/local/lib/node_modules/corepack/dist/corepack.js pnpm add moment uuid
#COPY requirements.txt /opt/runners/task-runner-python/requirements.txt
#RUN cd /opt/runners/task-runner-python && uv pip install -r requirements.txt
#USER runner
#COPY n8n-task-runners.json /etc/n8n-task-runners.json
