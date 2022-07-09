FROM node

# 여기서 npm install 등의 명령어가 실행 될 것이다.
WORKDIR /app

COPY package.json /app

RUN npm install

# 첫번째 . Dockerfile이 있는 경로 기준 모든 파일(Dockerfile 제외)
# 두번째 . 그 파일을 저장해야 하는 이미지 내부의 경로 
# 실제로는 루트 엔트리를 사용하지 않고 사용자가 지정한 폴더에 저장하는 게 낫다.
# 해당 폴더가 존재하지 안흔 경우 이미지와 컨테이너에 생성
COPY . /app


# Expose 80은 Documentation 목적으로만 추가되었다?
# 즉 아무것도 하지 않았다? 
EXPOSE 80

# 위의 과정은 이미지를 생성하기 위한 과정이다.
# 이미지는 컨테이너의 템플릿 이미지를 실행하는 것이 아니라 이미지를 기반으로 컨테이너를 실행
# 우리는 모든 종속성을 포함하고, 모든 코드를 포함한 이미지를 만든 다음에
# 이미지를 기반으로 한 컨테이너를 실행할 때만 서버를 시작
CMD ["node" ,"server.js"]

