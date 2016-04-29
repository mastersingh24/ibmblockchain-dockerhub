FROM golang:1.6-alpine
RUN apk update
RUN apk add snappy
RUN apk add zlib
RUN apk add libbz2
RUN rm -Rf /var/cache/apk/*
RUN mkdir -p /fabric/lib
RUN mkdir -p /var/hyperledger
COPY alpine3.3 /fabric/
RUN ln -s /fabric/lib/librocksdb.so.4.1.0 /fabric/lib/librocksdb.so.4.1
ENV LD_LIBRARY_PATH=/fabric/lib:$LD_LIBRARY_PATH
ENV PATH=/fabric/bin:$PATH
WORKDIR /fabric/bin
