# vscode-python-ide-docker


FROM codercom/code-server:4.4.0

USER root

RUN apt-get update && apt-get install -y --no-install-recommends \
    python3.5 \
    python3-pip \
    && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/*

RUN pip3 install nibabel pydicom matplotlib pillow
