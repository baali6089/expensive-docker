FROM node:20.15.0-alpine3.20
EXPOSE 8080
ENV DB_HOST=mysql
RUN adduser expensive
RUN chown expensive:expensive -R /opt/server
#RUN addgroup -S expense && adduser -S expensive -G expense \
#   && mkdir /opt/server \
#    && chown expensive:expensive -R /opt/server
WORKDIR /opt/server
COPY package.json .
COPY *.js /opt/server/
RUN npm install
#USER expensive
#EXPOSE 8081
CMD [ "node","index.js" ]