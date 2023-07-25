## AWS 환경에서의 SPA 애플리케이션 흐름도

![Untitled](/Users/ruby/Desktop/project/aws-spa/imgs/flow/flow.png)

<br>

## S3 정적 웹 사이트 호스팅 배포

### AWS S3 - Amazon Simple Storage Service

- 아마존 웹 서비스에서 제공하는 온라인 스토리지 웹 서비스
- 정적 웹 사이트 호스팅을 제공

### S3 정적 웹 사이트 호스팅 배포 (Vue 배포)

![Untitled](/Users/ruby/Desktop/project/aws-spa/imgs/s3/s3-1.png)

1. 프로젝트 빌드

    ```java
    npm run build
    ```

   ![Untitled](/Users/ruby/Desktop/project/aws-spa/imgs/s3/s3-2.png)

   dist 폴더에 빌드된 파일들이 생성됨

2. S3 버킷 생성

   ![Untitled](/Users/ruby/Desktop/project/aws-spa/imgs/s3/s3-3.png)
    
   외부에서 접속하는 모든 사용자에게 페이지를 제공하기 위해 모든 퍼블릭 엑세스 차단을 체크 해제한다.

3. 웹 호스팅 설정
    - 버킷 - 속성 - 정적 웹 사이트 호스팅

      ![Untitled](/Users/ruby/Desktop/project/aws-spa/imgs/s3/s3-4.png)

4. 버킷 정책 편집

   ![Untitled](/Users/ruby/Desktop/project/aws-spa/imgs/s3/s3-5.png)

5. 버킷에 빌드된 파일들을 업로드

   ![Untitled](/Users/ruby/Desktop/project/aws-spa/imgs/s3/s3-6.png)

6. 웹 호스팅 확인
    - 버킷 웹 사이트 엔드포인트 url 주소로 요청

      ![Untitled](/Users/ruby/Desktop/project/aws-spa/imgs/s3/s3-7.png)