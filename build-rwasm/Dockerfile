ARG WEBR_IMAGE=ghcr.io/r-wasm/webr:main

# Container image that runs your code
FROM $WEBR_IMAGE

RUN echo "Acquire::AllowInsecureRepositories true;" >> /etc/apt/apt.conf.d/99allow-insecure

# Copies your code file from your action repository to the filesystem path `/` of the container
COPY code.R /code.R

# Code file to execute when the docker container starts up (`entrypoint.sh`)
ENTRYPOINT [ "Rscript" ]
# ENTRYPOINT [ "/bin/bash", "-l", "-c" ]
