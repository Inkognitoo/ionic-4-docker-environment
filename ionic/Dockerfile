FROM beevelop/ionic:v4.1.2

LABEL maintainer="Pavel Sotnikov <inkognitoo92@yandex.ru>"

USER root

###########################################################################
# Create ionic user
###########################################################################

ARG PUID=1000
ENV PUID ${PUID}
ARG PGID=1000
ENV PGID ${PGID}
ARG PROJECT_NAME="ionic-project"
ENV PROJECT_NAME ${PROJECT_NAME}

RUN groupadd -g ${PGID} ionic && \
    useradd -u ${PUID} -g ionic -m ionic -G root && \
    usermod -p "*" ionic

###########################################################################

RUN mkdir /home/ionic/${PROJECT_NAME}

WORKDIR /home/ionic/${PROJECT_NAME}

###########################################################################
# Any custom settings what you need
###########################################################################


###########################################################################

EXPOSE 8100 35729 53703
