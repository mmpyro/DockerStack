FROM microsoft/dotnet:2.1-sdk
WORKDIR /root/src
RUN apt-get update && apt-get install -y openjdk-8-jre
RUN dotnet tool install --global dotnet-sonarscanner
ENV PATH="$PATH:/root/.dotnet/tools"