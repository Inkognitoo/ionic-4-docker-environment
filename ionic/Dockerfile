ARG IONIC_VERSION

FROM beevelop/ionic:${IONIC_VERSION}

LABEL maintainer="Pavel Sotnikov <inkognitoo92@yandex.ru>"

USER root

###########################################################################
# Create ionic user
###########################################################################

ARG PUID
ENV PUID ${PUID}
ARG PGID
ENV PGID ${PGID}
ARG PROJECT_NAME
ENV PROJECT_NAME ${PROJECT_NAME}

RUN groupadd -g ${PGID} ionic && \
    useradd -u ${PUID} -g ionic -m ionic -G root && \
    usermod -p "*" ionic && \
    mkdir /home/ionic/${PROJECT_NAME}

WORKDIR /home/ionic/${PROJECT_NAME}

###########################################################################

###########################################################################
# Any custom settings what you need
###########################################################################
#
#
###########################################################################

EXPOSE 8100 35729 53703
