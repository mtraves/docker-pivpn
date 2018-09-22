FROM arm32v7/debian:stretch

MAINTAINER InnovativeInventor

RUN apt-get update && apt-get install -y \
	curl \
	software-properties-common \
	debconf-utils \
	git \
	nano \
	whiptail \
	openvpn \
	dhcpcd5 \
	dnsutils \
	expect \
	whiptail \
	&& rm -rf /var/lib/apt/lists/*

RUN curl -L https://install.pivpn.io -o install.sh
# do an apg-get update prior to pivpn_setup() allows the initial install.sh to execute properly
RUN apt-get update
RUN useradd -m pivpn
EXPOSE 1194/udp
