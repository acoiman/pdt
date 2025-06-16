FROM jupyter/minimal-notebook:latest

MAINTAINER Abraham Coiman <abraham.coiman@ig.edu.ar>

# Install pip packages
RUN pip install --no-cache-dir jupyter_http_over_ws \
    access==1.1.9 \
    affine==2.4.0 \
    bqplot==0.12.44 \
    branca==0.8.1 \
    cachetools==4.2.4 \
    click==8.1.7 \
    click-plugins==1.1.1 \
    cligj==0.7.2 \
    colour==0.1.5 \
    contourpy==1.3.1 \
    cycler==0.12.1 \
    dataclasses==0.6 \
    deprecation==2.1.0 \
    earthengine-api==1.5.12 \
    eerepr==0.1.1 \
    esda==2.7.0 \
    et_xmlfile==2.0.0 \
    fiona==1.10.1 \
    folium==0.19.5 \
    fonttools==4.56.0 \
    future==1.0.0 \
    geemap==0.35.3 \
    geocoder==1.38.1 \
    geopandas==1.0.1 \
    giddy==2.3.6 \
    google-api-core==2.25.0rc0 \
    google-api-python-client==2.167.0 \
    google-auth==2.39.0 \
    google-auth-httplib2==0.2.0 \
    google-auth-oauthlib==1.2.0 \
    google-cloud-core==2.4.3 \
    google-cloud-storage==3.1.0 \
    google-crc32c==1.7.1 \
    google-resumable-media==2.7.2 \
    googleapis-common-protos==1.70.0 \
    httplib2==0.22.0 \
    imageio==2.37.0 \
    inequality==1.1.1 \
    ipyevents==2.0.2 \
    ipyfilechooser==0.6.0 \
    ipyleaflet==0.19.2 \
    ipytree==0.2.2 \
    itables==2.2.5 \
    joblib==1.4.2 \
    jsonpointer==2.1 \
    jupyter-leaflet==0.19.2 \
    kiwisolver==1.4.8 \
    libpysal==4.13.0 \
    llvmlite==0.44.0 \
    mapclassify==2.8.1 \
    matplotlib==3.10.1 \
    mgwr==2.2.1 \
    momepy==0.9.1 \
    mpmath==1.3.0 \
    narwhals==1.34.0 \
    networkx==3.4.2 \
    numba==0.61.2 \
    numpy==2.2.4 \
    oauthlib==3.2.2 \
    openpyxl==3.1.5 \
    osmnx==2.0.2 \
    pandas==2.2.3 \
    patsy==1.0.1 \
    pickleshare==0.7.5 \
    pillow==11.1.0 \
    plotly==6.0.1 \
    pointpats==2.5.1 \
    proto-plus==1.26.1 \
    protobuf==6.30.2 \
    PuLP==3.1.1 \
    pyasn1==0.6.1 \
    pyasn1_modules==0.4.2 \
    PyCRS==1.0.2 \
    pyogrio==0.10.0 \
    pyparsing==3.2.3 \
    pyperclip==1.9.0 \
    pyproj==3.7.1 \
    PyQt6==6.7.1 \
    pysal==25.1 \
    pyshp==2.3.1 \
    python-box==7.3.2 \
    pytz==2025.2 \
    quantecon==0.8.0 \
    rasterio==1.4.3 \
    rasterstats==0.20.0 \
    ratelim==0.1.6 \
    requests-oauthlib==2.0.0 \
    rsa==4.9.1 \
    rtree==1.4.0 \
    scikit-learn==1.6.1 \
    scipy==1.15.2 \
    scooby==0.10.0 \
    seaborn==0.13.2 \
    segregation==2.5.2 \
    setuptools==75.8.0 \
    shapely==2.0.7 \
    simplejson==3.20.1 \
    spaghetti==1.7.6 \
    spglm==1.1.0 \
    spint==1.0.7 \
    splot==1.1.7 \
    spopt==0.6.1 \
    spreg==1.8.2 \
    statsmodels==0.14.4 \
    sympy==1.13.3 \
    threadpoolctl==3.6.0 \
    tobler==0.12.1 \
    traittypes==0.2.1 \
    tzdata==2025.2 \
    uritemplate==3.0.1 \
    wheel==0.45.1 \
    xarray==2025.3.0 \
    xyzservices==2025.1.0


#Expose Jupyter Notebook port
EXPOSE 8888


# Configure the Jupyter Notebook according Colab requirements
CMD ["jupyter", "notebook", \
     "--NotebookApp.allow_origin=https://colab.research.google.com", \
     "--NotebookApp.allow_credentials=True", \
     "--NotebookApp.disable_check_xsrf=True", \
     "--NotebookApp.token=mytoken12345", \
     "--NotebookApp.port=8888", \
     "--NotebookApp.port_retries=0", \
     "--ip=0.0.0.0", \
     "--no-browser"]
     
     
  
     
