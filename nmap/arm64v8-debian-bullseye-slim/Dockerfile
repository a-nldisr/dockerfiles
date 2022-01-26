FROM arm64v8/debian:bullseye-slim
label maintainer "Rogier Dikkes <no-reply@0to1.nl>"

RUN apt-get update && apt-get install -y \
	nmap \
	--no-install-recommends \
	&& rm -rf /var/lib/apt/lists/*

ENTRYPOINT [ "nmap" ]