FROM node:latest

WORKDIR /app/medusa

COPY package.json .

RUN apt-get update || : && apt-get install python-is-python3 -y

RUN npm install -g npm@latest -g

RUN npm install -g @medusajs/medusa-cli@latest

RUN npm install --loglevel=error

COPY . .

ENTRYPOINT ["./develop.sh", "develop"]