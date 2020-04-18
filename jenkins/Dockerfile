# Use Jenkins LTS
FROM jenkins/jenkins:2.222.1

# Perform installations as root user
USER root

# Replace Shell with Bash
RUN rm /bin/sh && ln -s /bin/bash /bin/sh && rm -rf /var/lib/apt/lists/*

# Install OS tools
RUN apt-get update
RUN apt-get install -qqy --no-install-recommends\
      vim \
      jq

# Environment variables (i.e. needed to trigger JCasC at the end)
ENV CASC_JENKINS_CONFIG="/var/jenkins_home/jcasc/jenkins.yml"
ENV JAVA_OPTS="-Djenkins.install.runSetupWizard=false"

# Install Jenkins plugins
COPY plugins.txt /usr/share/jenkins/ref/plugins.txt
RUN /usr/local/bin/install-plugins.sh < /usr/share/jenkins/ref/plugins.txt
