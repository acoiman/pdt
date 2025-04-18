# Use a base image with a minimal Linux distribution
FROM ubuntu:20.04

# Set environment variables for non-interactive installations
ENV DEBIAN_FRONTEND=noninteractive

# Install necessary dependencies
RUN apt-get update && apt-get install -y \
    wget \
    bzip2 \
    ca-certificates \
    curl \
    git \
    build-essential \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/*

# Download and install Miniconda
RUN wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh -O miniconda.sh \
    && bash miniconda.sh -b -p /opt/miniconda \
    && rm miniconda.sh

# Add conda to the PATH
ENV PATH="/opt/miniconda/bin:${PATH}"

# Update conda and install Jupyter Notebook
RUN conda update -n base -c defaults conda && \
    conda install jupyter notebook -y

# Set the working directory
WORKDIR /workspace

# Expose Jupyter Notebook port
EXPOSE 8888

# Configure the Jupyter Notebook to be accessible remotely and without a password
RUN jupyter notebook --generate-config \
    && echo "c.NotebookApp.ip = '0.0.0.0'" >> ~/.jupyter/jupyter_notebook_config.py \
    && echo "c.NotebookApp.open_browser = False" >> ~/.jupyter/jupyter_notebook_config.py \
    && echo "c.NotebookApp.allow_root = True" >> ~/.jupyter/jupyter_notebook_config.py

# Run Jupyter Notebook
CMD ["jupyter", "notebook", "--notebook-dir=/workspace", "--ip=0.0.0.0", "--port=8888", "--no-browser", "--allow-root"]
