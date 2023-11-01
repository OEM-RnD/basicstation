# Ubuntu 22.04
FROM ubuntu:jammy

COPY ./v2.0.6.patch /v2.0.6.patch

RUN apt -y update
RUN apt -y install git gcc make

RUN git clone https://github.com/lorabasics/basicstation -b v2.0.6 /basicstation
RUN cd /basicstation; git apply /v2.0.6.patch; rm /v2.0.6.patch

RUN make platform=corecell variant=stdn arch=amd64 --directory=/basicstation
RUN mkdir /basicstation/config

# run on container startup
CMD /basicstation/build-corecell-stdn/bin/station --home=/basicstation/config
