## EC2에 백엔드 서버 배포하는 방법에 대해 기술 합니다.

### Back End Publish

```

1. Putty 에서 ec2 서버에 접속.

2. Spring 콘솔 창에 gradlew build를 통해 .jar 파일 생성

3. WinSCP를 통해 경로에 .jar 파일 옮기기

4. putty 실행 창에서 실행 시키고 , 백그라운드에서 돌리기 위해 다음과 같은 명령어 실행


```

```javascript
    java -jar catdog-1.0-SNAPSHOT.jar   // 일반 실행
    nohup java -jar catdog-1.0-SNAPSHOT.jar &  // 백그라운드 실행
```
