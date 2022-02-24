FROM ezkrg/buildx

ENV DOCKERVERSION "18.09.7"

RUN apk update
RUN apk add bash curl build-base git gnupg bash docker-compose

# docker cli
RUN curl -fsSLO https://download.docker.com/linux/static/stable/x86_64/docker-${DOCKERVERSION}.tgz
RUN tar xzvf docker-${DOCKERVERSION}.tgz --strip 1 -C /usr/local/bin docker/docker
RUN rm docker-${DOCKERVERSION}.tgz

# blackbox
RUN git clone --branch stable --depth 1 https://github.com/StackExchange/blackbox.git "/.blackbox"
ENV PATH "/.blackbox/bin:${PATH}"

ENV DOCKER_HOST "tcp://ourskyci__docker:2375"
ENV DOCKER_CLI_EXPERIMENTAL "enabled"
