FROM openjdk:8-jre-alpine
ENV APP_ROOT=/root/servicestage/reserve/
ENV LOG_ROOT=/var/log/reserve/
RUN mkdir -p $APP_ROOT
RUN mkdir -p $LOG_ROOT

COPY target/reserve-1.3.3-Hoxton-SNAPSHOT/reserve-1.3.3-Hoxton-SNAPSHOT $APP_ROOT


RUN cd $APP_ROOT && chmod -R 770 .
RUN chmod +x /root/servicestage/reserve/bin/start.sh

ENTRYPOINT ["sh", "/root/servicestage/reserve/bin/start.sh"]
