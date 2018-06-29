# Dockerfile for building the Resources for Researchers API
# Assumes the current directory to be the top-level project directory.

FROM microsoft/dotnet:2.0-sdk

# Install ZIP and the github-release tool, storing it in /usr/local/bin
RUN apt-get -y update \
    && apt-get -y install zip bzip2 \
    && curl -SL https://github.com/aktau/github-release/releases/download/v0.7.2/linux-amd64-github-release.tar.bz2 --output /tmp/github-release.tar.bz2 \
    && tar xvjf /tmp/github-release.tar.bz2 --strip-components=3 -C /usr/local/bin \
    && rm /tmp/github-release.tar.bz2
