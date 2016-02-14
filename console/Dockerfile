# Use the base nsolid nodejs runtime
FROM contentful/nsolid-runtime

# Install proxy and console
RUN mkdir /console && curl https://nsolid-download.nodesource.com/download/nsolid-console/release/v1.4.4/nsolid-console-v1.4.4-linux-x64.tar.gz| tar xvzf - -C /console --strip-components=1
WORKDIR /console

COPY .nsolid-consolerc /console/.nsolid-consolerc
ENV PORT=8080
