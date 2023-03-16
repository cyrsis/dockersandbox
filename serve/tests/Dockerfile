FROM ubuntu:latest@sha256:67211c14fa74f070d27cc59d69a7fa9aeff8e28ea118ef3babc295a0428a6d21
RUN apt-get update
RUN apt-get install -y curl
COPY sitetest.sh sitetest.sh
CMD ["/sitetest.sh"]
