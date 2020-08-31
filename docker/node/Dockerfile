FROM node:14

# Create app directory
ENV APP_HOME /app
RUN mkdir $APP_HOME
WORKDIR $APP_HOME
# Install app dependencies
# A wildcard is used to ensure both package.json AND package-lock.json are copied
# where available (npm@5+)

COPY docker/node/entrypoint.sh /usr/bin/
RUN chmod +x /usr/bin/entrypoint.sh
ENTRYPOINT ["entrypoint.sh"]

EXPOSE 3000
