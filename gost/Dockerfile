FROM alpine:3.7
MAINTAINER sunteya <sunteya@gmail.com>


# This is needed for go binaries to run properly on alpine linux since the binary needs libc and alpine use musl.
RUN mkdir /lib64 && ln -s /lib/libc.musl-x86_64.so.1 /lib64/ld-linux-x86-64.so.2 

ADD build.sh /
RUN sh -x build.sh 2.5 2.5

ENTRYPOINT [ "/app/gost" ]
CMD [ "--help" ]
