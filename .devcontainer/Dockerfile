# Pulling Image from https://hub.docker.com/r/refinitivapis/websocket_api
FROM refinitivapis/websocket_api:latest
LABEL maintainer="Developer Advocate"
ARG dotnet_version="6.0"

# Install updates, dotnet-sdk and tools for VS Code devcontainer.
RUN yum update -y \
 && yum -y install dotnet-sdk-${dotnet_version} wget tar.x86_64 which \
 # Clean up unnecessary files to reduce Image size
 && yum clean all
# Set work directory to be RDP/CSharp

WORKDIR /opt/refinitiv/websocket-api/Applications/Examples/RDP/CSharp

# Set Docker to start bash
CMD /bin/bash