
# Scripts and Noteboks used for the Ph.D Thesis: "Asma y variables ambientales - un enfoque basado en el uso de datos geoespaciales y aprendizaje automático"

* asthma_mortality
* asthma_risk
* docker

## Deployment

To deploy, follow these instructions (only for Linux OS):

* Download the compressed data at https://drive.google.com/file/d/1tKJhMm-gB1tnEofk5mULjB3ieigqzN0F/view?usp=sharing

* Uncompress the file in your local home folder.

* Change the folder permissions by running the following command:

```bash
  chgrp -R users pdt && chmod -R g+rw pdt
```

* Install Docker on your local machine.

* Pull the Docker image with the following command:

```bash
  docker pull acoiman/pdt_rpy:1.0
```

### For Google Colab Jupyter Notebooks

* Create and start a new Docker container from the image with the following command:

```bash
   docker run --rm -p 8888:8888 -v $(pwd):/home/jovyan/work acoiman/pdt_rpy:1.0
```

* Go to our [Colab Notebooks](https://github.com/acoiman/pdt/tree/main/asthma_mortality/notebooks/colab) and enter the desired Notebook. Click on *Open in Colab* icon.

* On *Connect* choose *Connect to a local runtime* and enter the following backend URL:

```bash
   http://127.0.0.1:8888/tree?token=mytoken12345
```

## Author

- [@acoiman](https://github.com/acoiman)

## License

[CC BY 4.0](https://creativecommons.org/licenses/by/4.0/deed.en)

