FROM ubuntu:18.04 as base
RUN apt-get update -y && \
    apt-get install -y nodejs

WORKDIR /app
COPY package*.json ./
RUN npm install

COPY ./src .

ENTRYPOINT ["npm"]
CMD ["run", "prod"]
