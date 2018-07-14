FROM tutum/nginx
MAINTAINER Richard Bramley <rabramley@gmail.com>

RUN apt-get update && DEBIAN_FRONTEND=noninteractive apt-get install -y wget zip
RUN rm /etc/nginx/sites-enabled/default
ADD sites-enabled/app01 /etc/nginx/sites-enabled/app01
ADD cert /cert
RUN wget https://github.com/LCBRU/brc_intranet/archive/master.zip && \
    unzip master.zip && \
    mv brc_intranet-master/brc_intranet/build/ /brc_intranet && \
    rm -fR brc_intranet-master && \
    rm  master.zip