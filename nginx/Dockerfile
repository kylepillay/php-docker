FROM nginx:latest

RUN apt-get update && apt-get upgrade -y \
    && apt-get autoclean \
    && apt-get clean \
    && apt-get autoremove;

ADD ./site.conf /etc/nginx/conf.d/site.conf
ADD ./startup.sh /startup.sh

RUN chmod +x /startup.sh

CMD /startup.sh;
