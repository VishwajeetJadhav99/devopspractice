FROM ubuntu:latest

LABEL dev="Vishwajeet"

RUN apt-get update && \
    apt-get install apache2 unzip -y && \
    rm -rf /var/www/html/index.html


ADD https://templatemo.com/download/templatemo_626_ledger_slideshow   /var/www/html/templatemo_626_ledger_slideshow.zip

WORKDIR /var/www/html

RUN unzip templatemo_626_ledger_slideshow.zip && \
    mv templatemo_626_ledger_slideshow /* /var/www/html/
    
EXPOSE 81

CMD ["apache2ctl", "-D", "FOREGROUND"]