FROM n8nio/runners:2.4.6
USER root
RUN /usr/local/bin/node /usr/local/lib/node_modules/corepack/dist/corepack.js pnpm add moment uuid
COPY requirements.txt /opt/runners/task-runner-python/requirements.txt
RUN cd /opt/runners/task-runner-python && uv pip install -r requirements.txt
USER runner
