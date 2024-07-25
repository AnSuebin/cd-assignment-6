## CD 개요

![다이어그램](image.png)

1. 저장소를 체크아웃 합니다.
2. npm 의존성을 설치합니다.
3. Next.js 프로젝트를 빌드합니다.
4. AWS 자격 증명을 구성합니다.
5. S3 버킷에 빌드된 파일을 동기화합니다.
6. CloudFront 캐시를 무효화합니다.

## 주요 링크

- S3 버킷 웹사이트 엔드포인트: http://myadvancedbucket.s3-website-us-east-1.amazonaws.com/
- CloudFrount 배포 도메인 이름: https://d1xu3q58qwoitl.cloudfront.net/

## 주요 개념

1. GitHub Actions과 CI/CD 도구:
   GitHub에서 제공하는 자동화 도구로, 코드 변경 시 자동으로 빌드, 테스트, 배포 등의 작업을 수행합니다. 지속적 통합(CI)과 지속적 배포(CD)를 구현하는 데 사용됩니다.
2. S3와 스토리지:
   Amazon Simple Storage Service의 약자로, 확장성이 뛰어난 클라우드 스토리지 서비스입니다. 여기서는 Next.js 애플리케이션의 빌드된 파일들을 호스팅하는 데 사용됩니다.
3. CloudFront와 CDN:
   Amazon의 콘텐츠 전송 네트워크(CDN) 서비스입니다. 전 세계 엣지 로케이션을 통해 웹 콘텐츠를 빠르게 제공하며, S3에 저장된 콘텐츠를 효율적으로 전달합니다.
4. 캐시 무효화(Cache Invalidation):
   CDN의 캐시된 콘텐츠를 강제로 업데이트하는 프로세스입니다. 새 버전의 콘텐츠가 즉시 사용자에게 제공되도록 보장합니다.
5. Repository secret과 환경변수:
   GitHub 저장소에 안전하게 저장된 비밀 값으로, AWS 접근 키와 같은 민감한 정보를 워크플로우에서 안전하게 사용할 수 있게 합니다.
