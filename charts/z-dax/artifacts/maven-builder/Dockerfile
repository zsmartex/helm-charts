FROM quay.io/strimzi/maven-builder

# I needed to use the root user, when I tried to use the 1001 user defined in the base it could not find the settings file. I didn't investigate further, see here https://github.com/strimzi/strimzi-kafka-operator/blob/main/docker-images/maven-builder/Dockerfile.
USER root

# see https://maven.apache.org/guides/mini/guide-multiple-repositories.html#repository-order for how Maven determines repos
COPY settings.xml /root/.m2/settings.xml
