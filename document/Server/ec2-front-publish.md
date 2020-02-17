## EC2 서버에 배포하는 방법에 대해 기술 합니다.

### Front End Publish

## 사전 처리 작업

```
1. Putty 에서 ec2 서버에 접속.

2. nginx 설치

    - sudo apt update

    - sudo apt upgrade

    - sudo apt-get install nginx
    * nginx 설치 *


    - sudo ufw app list
    * 방화벽 소프트웨어 조정

    - [Output]

    Available applications:
        Nginx Full
        Nginx HTTP
        Nginx HTTPS
        OpenSSH


    - sudo ufw allow 'Nginx HTTP'


    - sudo vi /etc/nginx/sites-available/default
    * 설정 파일 옮기기


```

## conf 파일 셋팅

```java

server {
        listen 3000 default_server;
        listen [::]:3000 default_server;


        root /var/www/html/vue-front/dist;  // 내 프론트 엔드 dist 파일의 주소

        index index.html;

        server_name _;

        location / {
                try_files $uri $uri/ /index.html;
        }
}

```

## 빌드 방법

```


1. vue 프로젝트에서 npm run build -> dist 폴더 생성됨

2. local -> ec2 server로 dist 파일 전송(scp -i "T02A409.pem 파일 경로" -r ./dist
   ubuntu@13.125.92.171:/home/ubuntu/front-vue/ 에 dist 파일 옮기기

   WinSCP 를 사용하면 편하다.

3. ec2 server에서  sudo systemctl restart nginx 명령어 입력4.

13.125.92.171:80으로 접속

```

