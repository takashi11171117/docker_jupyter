FROM jupyter/datascience-notebook

USER root

# フォントとして Ricty Diminished をインストールする。
WORKDIR /usr/share/fonts
ENV RICTY_DIMINISHED_VERSION 3.2.4
ADD https://github.com/mzyy94/RictyDiminished-for-Powerline/archive/$RICTY_DIMINISHED_VERSION-powerline-early-2016.zip .
RUN unzip -jo $RICTY_DIMINISHED_VERSION-powerline-early-2016.zip \
 && fc-cache -fv

COPY dataset/IPAfont00303 /usr/share/fonts/truetype/IPAfont00303
RUN sudo chmod 644 /usr/share/fonts/truetype/IPAfont00303/*.ttf

USER jovyan

WORKDIR /home/jovyan/work
COPY requirements.txt ./
RUN pip install -r requirements.txt
COPY matplotlibrc /opt/conda/lib/python3.6/site-packages/matplotlib/mpl-data/matplotlibrc
