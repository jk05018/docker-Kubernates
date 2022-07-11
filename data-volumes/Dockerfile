FROM node:14

WORKDIR /app

COPY package.json . 

RUN npm install

# 최적화 왜  했는지 생각해봐 
ARG DEFAULT_PORT=80

COPY . .

ENV PORT $DEFAULT_PORT

EXPOSE $PORT

CMD [ "npm" , "start" ]
