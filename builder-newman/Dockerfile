FROM gcr.io/jenkinsxio/builder-base:0.0.1

RUN curl -f --silent --location https://rpm.nodesource.com/setup_9.x | bash - && \
  yum install -y nodejs && \
  yum clean all

RUN npm install -g newman

# jx
ENV JX_VERSION 1.3.967
RUN curl -f -L https://github.com/jenkins-x/jx/releases/download/v${JX_VERSION}/jx-linux-amd64.tar.gz | tar xzv && \
  mv jx /usr/bin/

CMD ["newman", "--version"]
