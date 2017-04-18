FROM golang:1.8-alpine

RUN apk add --no-cache hugo
RUN apk add --no-cache git

ENV WORK_SPACE "/home/hugo"

RUN mkdir ${WORK_SPACE}
WORKDIR ${WORK_SPACE}

# init hugo workspace
RUN hugo new site .

# install themes
RUN git clone https://github.com/aubm/hugo-code-editor-theme.git themes/code-editor
