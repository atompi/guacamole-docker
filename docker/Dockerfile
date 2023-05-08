FROM guacamole/guacamole:1.5.1

COPY guacamole-history-recording-storage-1.5.1.jar /opt/guacamole/

USER root
RUN sed -i '/^start_guacamole$/i\ln -s /opt/guacamole/*.jar /home/guacamole/.guacamole/extensions/' /opt/guacamole/bin/start.sh
USER guacamole
