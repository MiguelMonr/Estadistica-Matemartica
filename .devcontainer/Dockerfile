FROM python:3.10-slim

# Install system dependencies
RUN apt-get update && apt-get install -y \
    r-base \
    r-base-dev \
    libssl-dev \
    libcurl4-openssl-dev \
    libxml2-dev \
    && rm -rf /var/lib/apt/lists/*

# Install Python/Jupyter dependencies first
RUN pip install --no-cache-dir \
    notebook \
    jupyterlab \
    jupyter_client \
    rpy2

# Install R packages and kernel after Jupyter is set up
RUN R -e "install.packages(c('IRkernel'), repos='http://cran.rstudio.com/', dependencies=TRUE)" && \
    R -e "library(IRkernel)" && \
    R -e "IRkernel::installspec(user = FALSE)"

# Create workspace directory
WORKDIR /workspace

# Set up user to match VS Code's default
RUN useradd -ms /bin/bash vscode && \
    chown -R vscode:vscode /workspace

USER vscode

# Expose Jupyter port
EXPOSE 8888

# Start Jupyter Lab by default
CMD ["jupyter", "lab", "--ip=0.0.0.0", "--port=8888", "--no-browser", "--allow-root"]