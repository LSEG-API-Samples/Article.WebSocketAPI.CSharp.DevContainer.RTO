# Pulling Image from https://hub.docker.com/r/refinitivapis/websocket_api
FROM refinitivapis/websocket_api:latest
LABEL maintainer="Developer Advocate"
# Install updates, dotnet-sdk and tools for VS Code devcontainer.
RUN yum update -y \
 && yum -y install dotnet-sdk-2.1 wget tar.x86_64 \
 # Clean up unnecessary files to reduce Image size
 && yum clean all
# Set work directory to be RDP/CSharp
WORKDIR /opt/refinitiv/websocket-api/Applications/Examples/RDP/CSharp
# Set Docker to start bash
CMD /bin/bash