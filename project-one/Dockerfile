FROM kazilotus/apache-php:1.1

# Install Python 2.7
RUN apt-get install python2.7-minimal -y \
    && mv /usr/bin/python2.7 /usr/bin/python \
    && python --version

#Install Supervisor
RUN apt-get install supervisor -y

#Install Cron
RUN apt-get install cron -y

# Install FFMPEG
RUN apt-get install ffmpeg -y \
    && ffmpeg -version

# Install Youtube-DL
RUN curl -L https://yt-dl.org/downloads/latest/youtube-dl -o /usr/local/bin/youtube-dl \
    && chmod a+rx /usr/local/bin/youtube-dl \
    && youtube-dl --version

RUN mkdir -p /var/log/supervisor
WORKDIR /var/www/app
