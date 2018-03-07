FROM centos:6

ENV GOROOT=/usr/local/go \
    GOPATH=/go

# Can't reference $GOROOT and $GOPATH without
# adding another ENV command :(
ENV PATH=$PATH:$GOROOT/bin:$GOPATH/bin
COPY ./go1.10.linux-amd64.tar.gz /usr/local/go1.10.linux-amd64.tar.gz

RUN yum -y update && yum -y -q install wget git && \
    cd /usr/local/ && \
	tar -zxf go1.10.linux-amd64.tar.gz
    # go get -u github.com/kardianos/govendor

RUN yum install -y rpmdevtools && \
    rpmdev-setuptree
