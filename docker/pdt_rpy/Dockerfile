FROM darribas/gds

MAINTAINER Abraham Coiman <abraham.coiman@ig.edu.ar>

# Configure the Jupyter Notebook according to Colab requirements
CMD ["jupyter", "notebook", \
     "--NotebookApp.allow_origin=https://colab.research.google.com", \
     "--NotebookApp.allow_credentials=True", \
     "--NotebookApp.disable_check_xsrf=True", \
     "--NotebookApp.token=rpy2025", \
     "--NotebookApp.port=8888", \
     "--NotebookApp.port_retries=0", \
     "--ip=0.0.0.0", \
     "--no-browser"]
