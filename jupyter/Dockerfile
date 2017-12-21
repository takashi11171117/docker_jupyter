FROM jupyter/datascience-notebook

WORKDIR /home/jovyan/work
COPY requirements.txt ./
RUN pip install -r requirements.txt
COPY dataset/IPAfont00303 /usr/share/fonts/truetype/IPAfont00303
COPY matplotlibrc /home/jovyan/.matplotlib/matplotlibrc
