FROM python:3.10.8
USER root

RUN apt-get update
RUN apt-get -y install locales && \
    localedef -f UTF-8 -i ja_JP ja_JP.UTF-8
ENV LANG ja_JP.UTF-8
ENV LANGUAGE ja_JP:ja
ENV LC_ALL ja_JP.UTF-8
ENV TZ JST-9
ENV TERM xterm

RUN apt-get install -y vim less
RUN pip install --upgrade pip
RUN pip install --upgrade setuptools
RUN pip install django && \
    pip install mysqlclient && \
    pip install uwsgi && \
    pip install matplotlib && \
    pip install djangorestframework &&\
    pip install django-basicauth

WORKDIR /workdir
#RUN python -m pip install jupyterlab

WORKDIR /workdir/opt/
#CMD python manage.py runserver 0.0.0.0:8000
#CMD uwsgi --http :8000 --module for_myapp.wsgi
#CMD uwsgi --ini uwsgi.ini
