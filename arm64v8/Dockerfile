FROM arm64v8/python:3.6.8-slim-stretch
MAINTAINER Khanh Cao <khanhncao@gmail.com>
VOLUME /media
COPY root/ /

RUN apt-get update
RUN apt-get install apt-transport-https ca-certificates apt-utils -y
RUN apt-get upgrade -y
RUN apt-get remove pulseaudio -y
RUN apt-get install vlc -y
RUN cd /app/doorbell && \
    pip3 install aiohttp python-vlc

ENTRYPOINT ["/app/run"]
