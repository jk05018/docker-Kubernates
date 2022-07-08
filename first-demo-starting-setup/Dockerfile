# 이것이 하는 일은 이미 존재하는 이 노드 환경을 잡아내는 것
FROM node:14

#  그 다음 이미지 내부에서 실행되는  이들 모든 설정으로 시작되는 컨테이너의 이미지 설정
WORKDIR /app

COPY package.json .

RUN npm install

COPY . .

EXPOSE 3000

CMD [ "node", "app.mjs" ]