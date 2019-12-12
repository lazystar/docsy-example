FROM ubuntu:eoan

RUN apt-get update -y
RUN apt-get install -y git golang-go nodejs openssl python-pygments libc6 g++ curl
RUN mkdir -p /tmp/src
RUN cd /tmp/src && git clone https://github.com/gohugoio/hugo.git
RUN cd /tmp/src/hugo && go install --tags extended

WORKDIR /www

ENTRYPOINT ["/root/go/bin/hugo", "server", "--bind=0.0.0.0"]

