FROM node:11
LABEL maintainer="hamakou108 <kosuke1602177mteitm19@gmail.com>"

ENV GITBOOK_BASE_PATH /opt/gitbook
ENV GITBOOK_DOCS_PATH ${GITBOOK_BASE_PATH}/docs
ENV GITBOOK_DEST_PATH ${GITBOOK_BASE_PATH}/dest

RUN npm install gitbook-cli -g && \
    gitbook fetch 3.2.3
    #gitbook fetch latest

RUN mkdir -p ${GITBOOK_BASE_PATH}
WORKDIR ${GITBOOK_BASE_PATH}

RUN gitbook init ${GITBOOK_DOCS_PATH}

CMD gitbook serve ${GITBOOK_DOCS_PATH} ${GITBOOK_DEST_PATH}

