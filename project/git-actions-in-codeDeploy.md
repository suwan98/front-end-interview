# Q : Github Actions와 AWS CodeDeploy를 어떤 식으로 조합하셨나요?

<br />

# A : 제가 프로젝트에서 Github Actions와 AWS CodeDeploy를 조합한 방법은 다음과 같습니다.

### Github Actions

- github-actions는 코드의 변경을 감지하고 이에 따른 빌드 및 테스트를 자동으로 수행하는 역할을 합니다.
- 이를 위해 push 이벤트가 main 브랜치에서 발생할 때마다 Github Actions 파이프라인이 시작되도록 구성했습니다.

### AWS CodeDeploy

- GithubActions에서 빌드 및 압축한 결과물을 AWS S3 버킷에 업로드 한 후 AWS CodeDeploy를 통해 파일을 EC2 인스턴스 서버에 배포하도록 설정했습니다.
  - 이를 위해, AWS credentials를 GitHub Actions 파이프라인 내 구성했으며, AWS S3에 파일을 업로드하는 작업을 포함시켰습니다.
  - 그리고 최종적으로 CodeDeoply에 결과물을 배포하게 됩니다.

이렇게 GithubActions와 CodeDeploy를 조합하면 코드의 변경이 발생할 때마다 자동으로 빌드 및 배포가 이루어지는 CI/CD 파이프라인을 구성할 수 있었습니다.
