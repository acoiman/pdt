# Scripts and notebooks used for the Ph.D. thesis

## "Asma y variables ambientales - un enfoque basado en el uso de datos geoespaciales y aprendizaje automático"

This repository contains the scripts and notebooks used for the Ph.D. thesis project focused on asthma and environmental variables using geospatial data and machine learning.

### Included folders

- `asthma_mortality`
- `asthma_risk`
- `docker`

---

## Deployment

To deploy the project on Linux, follow the instructions below.

### 1) Download the dataset

Download the compressed data from:

https://drive.google.com/file/d/1tKJhMm-gB1tnEofk5mULjB3ieigqzN0F/view?usp=sharing

Uncompress the file in your local home folder.

### 2) Adjust folder permissions

Run the following command:

```bash
chgrp -R users pdt && chmod -R g+rw pdt
```

### 3) Install Docker

Install Docker on your local machine.

### 4) Pull the Docker image

```bash
docker pull acoiman/pdt_rpy:1.0
```

---

## Google Colab Jupyter notebooks

### Start a Docker container

Create and start a new Docker container from the image with the following command:

```bash
docker run --rm -p 8888:8888 -v $(pwd):/home/jovyan/work acoiman/pdt_rpy:1.0
```

### Open a notebook in Colab

1. Go to the [Colab notebooks](https://github.com/acoiman/pdt/tree/main/asthma_mortality/notebooks/colab) folder.
2. Open the desired notebook.
3. Click the "Open in Colab" icon.
4. In the connection dialog, choose "Connect to a local runtime".
5. Enter the following backend URL:

```bash
http://127.0.0.1:8888/tree?token=mytoken12345
```

---

## Author

- [@acoiman](https://github.com/acoiman)

## License

[CC BY 4.0](https://creativecommons.org/licenses/by/4.0/deed.en)
