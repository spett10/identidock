FROM python:3.9

RUN groupadd -r uwsgi && useradd -r -g uwsgi uwsgi
RUN pip3 install Flask 
RUN pip3 install uWSGI 
RUN pip3 install requests
RUN pip3 install redis
WORKDIR /app
COPY app /app/
COPY cmd.sh /

EXPOSE 9090 9191
USER uwsgi

CMD ["/cmd.sh"]