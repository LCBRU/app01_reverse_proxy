FROM tutum/nginx
MAINTAINER Richard Bramley <rabramley@gmail.com>

RUN rm /etc/nginx/sites-enabled/default
ADD sites-enabled/app01 /etc/nginx/sites-enabled/app01
ADD cert /cert