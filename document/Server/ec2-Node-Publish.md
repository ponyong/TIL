## EC2에 Node 서버 배포하는 방법에 대해 기술 합니다.

### Node Publish

## 사전 처리 작업

1. WinSCP 를 이용하여 Node 파일을 업로드 합니다.

2. 업로드 한 경로로 접근 하여 Node 파일을 실행 시킵니다.

```
node server.js
```

## 무중단 배포

```
pm2 를 활용하여 배포 하는 방법
```

```java

// 켜는 방법
npm install pm2 -g

pm2 start app.js

// 멈추는 방법

pm2 stop (num)
pm2 stop 0

// 삭제하는 방법

pm2 kill

```
