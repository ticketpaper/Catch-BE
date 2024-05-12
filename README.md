<p align='center'>
<img src="https://capsule-render.vercel.app/api?type=rect&color=ff4500&text=%20%20CATCH%20%20&fontAlign=30&fontSize=30&textBg=true&desc=지속적인%20고객%20관리를%20위한%20시스템%20&descAlign=60&descAlignY=50&fontColor=ffffff"/>
</p>
<p align='center'>
  <a>
    <img src="https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white"/>
  </a>
    <a>
        <img src="https://img.shields.io/badge/Postman-FF6C37?style=for-the-badge&logo=postman&logoColor=white"/>
    </a>
    <a>
    <img src="https://img.shields.io/badge/Notion-%23000000.svg?style=for-the-badge&logo=notion&logoColor=white"/>
</a>

  <a>
    <img src="https://img.shields.io/badge/Slack-4A154B?style=for-the-badge&logo=slack&logoColor=white"/>
  </a>

<br>
    
  <a>
    <img src="https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white"/>
  </a>
  <a>
    <img src="https://img.shields.io/badge/Spring-6DB33F?style=for-the-badge&logo=spring&logoColor=white"/>
  </a>
    
<a>
    <img src="https://img.shields.io/badge/json%20web%20tokens-323330?style=for-the-badge&logo=json-web-tokens&logoColor=pink"/>
</a>
<a>
  <img src="https://img.shields.io/badge/firebase-FFCA28?style=for-the-badge&logo=firebase&logoColor=white">
</a>
  <br>
  <a>
    <img src="https://img.shields.io/badge/Amazon_AWS-232F3E?style=for-the-badge&logo=amazon-aws&logoColor=white"/>
  </a>
  <a>
    <img src="https://img.shields.io/badge/MariaDB-003545?style=for-the-badge&logo=mariadb&logoColor=white"/>
  </a>
  <a>
    <img src="https://img.shields.io/badge/redis-%23DD0031.svg?&style=for-the-badge&logo=redis&logoColor=white"/>
  </a>
<a>
    <img src="https://img.shields.io/badge/docker-%230db7ed.svg?style=for-the-badge&logo=docker&logoColor=white"/>
</a>
<a>
    <img src="https://img.shields.io/badge/kubernetes-%23326ce5.svg?style=for-the-badge&logo=kubernetes&logoColor=white"/>
</a>
<br>

<p align='center'>
   👨‍💻 심재혁, 김지한, 이혜선, 이종표 
</p>

# 목차
- [개요]
- [요구사항 분석]
- [📅 WBS]
- [📈 ERD]
- [🎬 API 명세 및 테스트 결과서]
- [아키텍처 설계도]
- [CI/CD 계획서]

</br>

# 프로젝트 개요
CATCH 솔루션은 CRM 마케팅 전략을 기반으로 쇼핑몰에서 마케터들이 고객들을 대상으로 관리, 쿠폰 또는 캠페인을 제공 할 수 있는 서비스입니다.<br>
고객 정보를 토대로 성별, 나이, 등급 등 각각의 기준으로 통계 및 그래프를 제공하여 회사가 고객을 분석하고 마케팅 전략을 계획 할 수 있게 도움을 줍니다.<br>
뿐만 아니라 마케팅 전략에 맞춰 이벤트를 제공 할 수 있게 회원들에게 이메일을 통한 광고를 전송하거나 멤버쉽 등급에 따라 쿠폰을 발급하는 등의 서비스를 구현해 회사가 고객 관리를 지속적으로 할 수 있게 합니다.<br>

</br>

# 요구사항 분석
<details>
  
## 사용자(회원)
|요청사항 명|요구사항 상세 설명|
|---|:---|
|**회원 가입 (일반 회원)**|회원은 이메일 인증을 통해 회원 가입을 할 수 있다.|
|**회원 가입 (소셜 회원)**|회원은 [구글] 소셜 수단으로 회원 가입 할 수 있다.|
|**회원 가입시 기본 입력**|정보	회원 가입 진행 시 이름, 이메일, 비밀번호, 생년월일, 주소를 입력해야 한다.|
|**개인정보 선택적 수집 및 이용에 대한 동의**|회원은 온라인회원 마케팅 수신동의(이메일, SMS)를 동의, 거부 할 수 있다.|
|**로그인 (일반 회원)** |일반 회원은 이메일, 비밀번호로 로그인 할 수 있다.|
|**로그인 (소셜 회원)**|소셜 회원은 [구글] 소셜 수단으로 로그인 할 수 있다.|
|**비밀번호 재설정 (일반 회원)**|일반 회원은 이메일 인증을 통해 비밀번호를 재설정 할 수 있다.|
|**마이 페이지**|회원은 마이페이지를 통해 개인 정보를 조회, 수정을 할 수 있다.|
|**개인 정보 수정**|회원은 주소, 마케팅 수신 동의를 수정 할 수 있다.|
|**개인 정보 조회**|자신의 아이디, 생년월일, 이메일, 주소, 마케팅 수신 동의를 조회할 수 있다.|
|**1:1 문의**|회원은 1:1 문의를 할 수 있다.|
|**개인의 쿠폰 상세 조회**|회원은 본인이 갖고 있는 쿠폰의 종류, 사용기간을 조회할 수 있다.|
|**개인의 포인트(적립금) 상세 조회**|회원은 본인이 갖고 있는 포인트(적립금), 사용기간을 조회할 수 있다.|
|**쿠폰 등록**|회원은 쿠폰 코드로 쿠폰을 등록 할 수 있다.|
|**개인의 문의 상세 조회**|회원은 본인의 문의 내용, 해당 문의의 답변을 조회할 수 있다.|
|**회원 탈퇴**|회원은 해당 서비스를 탈퇴할 수 있다.|
|**최근에 본 상품 목록**|회원은 본인이 최근에 본 상품의 목록을 확인할 수 있다.|
|**관심 상품**|회원은 상품에 좋아요를 눌러서 관심 상품에 등록할 수 있다.|
|**관심 상품 목록**|회원은 본인이 관심있는 상품의 목록을 조회할 수 있다.|

## 웹
|요청사항 명|요구사항 상세 설명|
|---|:---|
|**로그인 후 화면 (메인)**|로그인 후 회원 개인의 등급, 쿠폰, 포인트(적립금)을 조회할 수 있다.|
|**로그인 후 화면 (배너)**|로그인 후 관리자가 등록한 배너가 웹 메인에 노출되어야 한다.|

## 이벤트
|요청사항 명|요구사항 상세 설명|
|---|:---|
|**선착순 쿠폰**|선착순 쿠폰 이벤트|


## 사용자 등급
|요청사항 명|요구사항 상세 설명|
|---|:---|
|**사용자 등급 갱신**|사용자는 자신의 등급의 변동이 있을경우 실시간으로 확인해야한다.|

## 관리자
|요청사항 명|요구사항 상세 설명|
|---|:---|
|**회원 정보 조회**|관리자는 전체 또는 특정 회원의 정보를 입력해 조회할 수 있다.|
|**회원 정보 수정**|관리자는 회원의 정보를 수정 및 삭제 할 수 있다.|

## 마케터
|요청사항 명|요구사항 상세 설명|
|---|:---|
|**성별을 통한 회원 분류**|성별에 따른 회원 분포 확인할 수 있다.|
|**나이를 통한 회원 분류**|연령별 회원 분포를 확인할 수 있다.|
|**등급을 통한 회원 분류**|등급별 회원 분포 확인할 수 있다.|
|**광고성 메일**|마케터는 메일에 내용을 작성할 수 있고, 해당 내용을 메일로 보낼수 있다.|
|**쿠폰 관리**|마케터는 쿠폰 생성이 가능하다.|
|**회원 포인트 관리**|회원 포인트(적립금) 조회 및 수정할 수 있다.|
|**신규 이벤트 생성 및 이벤트 수정**|이벤트 생성 및 삭제 관리를 할 수 있다.|


## CS 담당자
|요청사항 명|요구사항 상세 설명|
|---|:---|
|**1:1 문의에 대한 답변**|회원이 남긴 1 : 1 문의에 대해 답변을 남길 수 있다.|

## 알람
|요청사항 명|요구사항 상세 설명|
|---|:---|
|**알람**|기한 만료 예정인 쿠폰 및 이벤트에 대한 정보를 확인할 수 있다.|

## 쿠폰
|요청사항 명|요구사항 상세 설명|
|---|:---|
|**발급된 쿠폰**|발급된 쿠폰은 수정 및 삭제가 불가능 하다.|
|**미발급 쿠폰**|미발급된 쿠폰은 수정 및 삭제가 가능하다.|

</details>
</br>

# [📅 WBS](https://docs.google.com/spreadsheets/d/19pO974fKGKGOW3XLY8PIu9Kd5hFQFiLN8cf3-CNAI-o/edit?usp=sharing)
</br>

# [📈 ERD](https://www.erdcloud.com/d/4hBsL2CcK8LnCFWJL)
</br>

# [🎬 API 명세 및 테스트 결과서](https://documenter.getpostman.com/view/32406846/2sA35LTyRZ)
</br>

# 아키텍처 설계도
<img width="1047" alt="image" src="https://github.com/ticketpaper/Catch-BE/assets/122894395/6a06c996-bfaf-4f04-891e-038a6c8e9d95">

</br>

# CI/CD 계획서

<details>
  
## 목표 및 범위:
- 모놀리식 CRM 서비스와 핵사고날 아키텍처로 설계된 event 모듈 및 SpringBatch로 구성된 배치서비스 들을 미니서비스아키텍처로 구성하고
  이를 안정적으로 배포해 쿠버네티스 컨테이너 오케이스트레이션을 통해 대규모 데이터 및 트래픽에 대비할 수 있도록 합니다.

## 환경 및 도구:
- CI/CD를 위해 사용할 환경과 도구
    - CI 도구: GithubAction, 
    - CD 도구: Docker, Kubernetes

## 저장소:
- 코드를 저장할 저장소와 브랜치 전략
    - 저장소: GitHub
    - 브랜치 전략: 각 Feature 브랜치를 dev에 머지하고, dev 서버를 통해 AWS에 배포한 후 안정적인 서비스가 가능할 때 main 브랜치에 머지 후 버전관리합니다.

## 빌드 및 자동화 스크립트:
- CI/CD 파이프라인을 구축하기 위한 빌드 스크립트와 자동화 스크립트
    - 빌드 스크립트: Gradle
    - 자동화 스크립트: GitHub Action Script

## 배포 전략:
-  쿠버네티스를 이용한 롤링 배포

### 단계:

1. **GitHub 저장소 체크아웃**:
  - GitHub 저장소를 체크아웃합니다.

2. **kubectl 설치**:
  - kubectl을 설치합니다.

3. **AWS 자격 증명 구성**:
  - AWS 자격 증명을 구성합니다.

4. **클러스터 정보 업데이트**:
  - 클러스터 정보를 업데이트합니다.

5. **Amazon ECR 로그인**:
  - Amazon ECR에 로그인합니다.

6. **Docker 이미지 빌드 및 푸시**:
  - CRM 서비스 및 배치 서비스용 Docker 이미지를 빌드하고 Amazon ECR로 푸시합니다.

7. **Kubernetes에 서비스 적용 및 배포 재시작**:
  - CRM 서비스 및 이벤트 서비스와 배치 서비스를 Kubernetes에 적용하고 배포를 재시작합니다.

## 권한 및 보안:
- CI/CD 파이프라인의 접근 제어 및 보안 정책을 기술합니다.
    - 접근 제어: IAM
    - 보안 정책: 쿠버네티스 시크릿을 이용한 데이터 암호화, 보안 그룹 설정


## 문서화 :
- CI/CD 계획서 
    - 문서화: GitHub Readme 작성

</details>
</br>

# 배포 결과 테스트

<details>
  
## S3 버킷 생성

<img src="https://github.com/Catch-team/Catch-BE/assets/78871184/fa1de006-2083-48a1-ba58-e41f68ca5e5d" height="80%" width="80%">

</br>

## 버킷 정책 편집
<img src="https://github.com/Catch-team/Catch-BE/assets/78871184/f479ab42-a2f5-48af-bfcd-e676132daae4" height="80%" width="80%">

</br>

## Cloud Front 생성
<img src="https://github.com/Catch-team/Catch-BE/assets/78871184/2fee512d-0609-4765-85f5-5ea502d7c8af" height="80%" width="80%">

</br>

## Cloud Front에 적용할 SSL 인증서 생성

<img height="80%" width="80%" src="https://github.com/Catch-team/Catch-BE/assets/122894395/f096f15f-1d73-4482-a125-e2f49be9e77c">
<img height="80%" width="80%" src="https://github.com/Catch-team/Catch-BE/assets/122894395/e323d9f6-0384-42c5-9e02-0d0d72c96576">
<img height="80%" width="80%" src="https://github.com/Catch-team/Catch-BE/assets/122894395/c76584b5-a42f-41ab-8e27-d2458d0ede88">
<img src="https://github.com/Catch-team/Catch-BE/assets/78871184/763dbcc4-3d03-4766-818e-bf0de7eda16a" height="80%" width="80%">



</br>

## Route53에서 호스팅 영역 생성
<img src="https://github.com/Catch-team/Catch-BE/assets/78871184/ad5ac0db-d054-4869-a399-614b12121977" height="80%" width="80%">

- 가비아에서 등록한 도메인의 ns 레코드 값을 생성된 호스팅 영역의 ns 레코드 값을 수정

<img src="https://github.com/Catch-team/Catch-BE/assets/122894395/59ac6833-4903-4d10-9d9a-c13ac458517f" height="80%" width="80%">

</br>

## 프론트 레코드 생성

- cloudfront의 엔드포인트 설정
<img src="https://github.com/Catch-team/Catch-BE/assets/78871184/5512f162-3e1a-4074-9f00-8b7905579895" height="80%" width="80%">

</br>

## CloudFront의 DNS 세팅
<img src="https://github.com/Catch-team/Catch-BE/assets/78871184/221d4d74-7952-4666-8bfb-a66d3f5dd87b" height="80%" width="80%">

</br>

## frontend git action
<details>
<summary> - frontend_depoly.yml </summary>
  
```
name: Deploy to AWS S3

on:
  push:
    branches:
    - dev

jobs:
  build-and-deploy:
    runs-on: ubuntu-latest
    steps:
    - uses: actions/checkout@v2

    - name: setup node.js
      uses: actions/setup-node@v2
      with:
        node-version: '20'

    - run: |
        echo "VUE_APP_FIREBASE_API_KEY=${{secrets.API_KEY}}" >> .env
        echo "VUE_APP_FIREBASE_AUTH_DOMAIN=${{secrets.DOMAIN}}" >> .env
        echo "VUE_APP_FIREBASE_PROJECT_ID=${{secrets.PROJECT_ID}}" >> .env
        echo "VUE_APP_FIREBASE_STORAGE_BUCKET=${{secrets.BUCKET}}" >> .env
        echo "VUE_APP_FIREBASE_MESSAGING_SENDER_ID=${{secrets.SENDER_ID}}" >> .env
        echo "VUE_APP_FIREBASE_APP_ID=${{secrets.APP_ID}}" >> .env
        echo "VUE_APP_FIREBASE_MEASUREMENTID=${{secrets.MEASUREMENT_ID}}" >> .env
        echo "VUE_APP_FIREBASE_VAP_ID=${{secrets.VAP_ID}}" >> .env
    - run: cat .env
    
    - name: npm install
      working-directory: ./
      run: npm install

    - name: npm firebase install
      working-directory: ./
      run: npm install firebase

    - name: npm run build
      working-directory: ./
      run: npm run build

    - name: setup aws cli
      uses: aws-actions/configure-aws-credentials@v2
      with: 
        aws-access-key-id: ${{secrets.AWS_S3_ACCESS_KEY}}
        aws-secret-access-key: ${{secrets.AWS_S3_SECRET_KEY}}
        aws-region: "ap-northeast-2"

    - name: deploy to s3
      run: |
        aws s3 cp ./dist s3://catchteam/ --recursive

```

</details>
</br>

## RDS 생성
<img height="80%" width="80%" src="https://github.com/Catch-team/Catch-BE/assets/122894395/e92d8a1f-b47d-4bd9-acf0-b95598e3c1e4">
<img height="80%" width="80%" src="https://github.com/Catch-team/Catch-BE/assets/122894395/b886fc70-9909-4f41-991c-f3061a85d42a">
<img height="80%" width="80%" src="https://github.com/Catch-team/Catch-BE/assets/122894395/d697076a-aa57-42da-9bde-0f504f138b59">
<img height="80%" width="80%"src="https://github.com/Catch-team/Catch-BE/assets/122894395/678b510a-da71-4cde-8bb7-265ae8e6dfab">

## RDS 파라미터 그룹 설정
- 파라미터 그룹을 설정해주지 않으면 DB에 한글을 넣을때 에러 발생

<img height="80%" width="80%" src="https://github.com/Catch-team/Catch-BE/assets/122894395/ab9a4eec-dac9-4c1f-b52c-5be9cb274d05">
<img height="80%" width="80%" src="https://github.com/Catch-team/Catch-BE/assets/122894395/c6cf80bc-8623-4ef5-99b0-efc1d490ae8a">
<img height="80%" width="80%" src="https://github.com/Catch-team/Catch-BE/assets/122894395/c06eb74b-1642-4035-a5d6-7c5c1255f561">

- char 검색시 나오는 항목들 utf8mb4

<img height="80%" width="80%" src="https://github.com/Catch-team/Catch-BE/assets/122894395/a08a8fb9-80b0-4f66-8669-f588f2aee708">

- collation 검색시 나오는 항목들 utf8mb4_general_ci
  
<img height="80%" width="80%" src="https://github.com/Catch-team/Catch-BE/assets/122894395/b981d82a-c195-45eb-91be-b6fcfcbec7e3">


## EKS 클러스터 생성
<img src="https://github.com/Catch-team/Catch-BE/assets/78871184/530fdbe7-065a-447f-aa5c-a4b7a62c773b" height="80%" width="80%">

</br>

## 클러스터 서비스 역할 EKS로 설정
<img src="https://github.com/Catch-team/Catch-BE/assets/78871184/088be74e-dc23-40cc-a73c-e5024f67a4c6" height="80%" width="80%">

<img src="https://github.com/Catch-team/Catch-BE/assets/78871184/d6304e70-97fa-49b1-9387-4705640a2d35" height="80%" width="80%">


</br>

## 클러스터 이름 생성
<img src="https://github.com/Catch-team/Catch-BE/assets/78871184/a0f687f7-29ff-44f3-973a-f41ab4b185be" height="80%" width="80%">

<img src="https://github.com/Catch-team/Catch-BE/assets/78871184/3a57cdc6-0b3e-4aad-a56a-ff9793635c20" height="80%" width="80%">

</br>

## EKS 보안그룹 설정
<img src="https://github.com/Catch-team/Catch-BE/assets/78871184/e3f8df2e-f885-466d-8854-40d945c25b8e" height="80%" width="80%">

</br>

## EKS 생성
<img src="https://github.com/Catch-team/Catch-BE/assets/78871184/1d366f8d-5618-4173-badb-8050c7f5e88a" height="80%" width="80%">

</br>

## 노드그룹 생성
<img src="https://github.com/Catch-team/Catch-BE/assets/78871184/0cf3ee88-8089-49f4-9f7e-ae0b9f2ee969" height="80%" width="80%">

</br>

## 노드그룹 IAM 역할 설정
<img src="https://github.com/Catch-team/Catch-BE/assets/78871184/7a948627-1280-4c59-bdca-10d8f2f0fd9c" height="80%" width="80%">

- IAM 역할 EC2 부여
<img src="https://github.com/Catch-team/Catch-BE/assets/78871184/cf738812-40e9-464b-b2a4-c346e864da7c" height="80%" width="80%">

- IAM 역할 EKS 권한 부여 
<img src="https://github.com/Catch-team/Catch-BE/assets/78871184/e0dadefd-6cca-418d-82dc-7d3865fd593a" height="80%" width="80%">

</br>

## 노드그룹 스펙 설정
<img src="https://github.com/Catch-team/Catch-BE/assets/78871184/5815c561-8569-4bf4-b1f6-fa2fbe5a5d87" height="80%" width="80%">

</br>

## 노드그룹 크기 설정
<img src="https://github.com/Catch-team/Catch-BE/assets/78871184/9bfd65fa-d89f-48b2-8af1-3b6f5c584e5a" height="80%" width="80%">

</br>

## 노드그룹 생성 완료
<img src="https://github.com/Catch-team/Catch-BE/assets/78871184/c3f5c062-f2b5-4315-a0cd-27299d70e80a" height="80%" width="80%">

</br>

## cert manager 설정
1. 터미널을 킵니다.

2. aws cli 설치 및 aws configure 설정

- aws cli 설치
https://docs.aws.amazon.com/ko_kr/cli/latest/userguide/getting-started-install.html

- aws configure 설정

```
aws configure
> AWS Access Key ID: aws 액세스 키 입력
> AWS Secret Access Key: aws 비밀 액세스 키 입력
> Default region name: region name 입력
> Default output format: output format 입력
```

3. kubectl 설치
- mac 
```
brew install kubectl
```
- 윈도우

```
winget install -e --id Kubernetes.kubectl
```

4. 설치 확인
```
kubectl version --client
```

5. 클러스터 설정
aws에서 클러스터 생성 후
```
aws eks update-kubeconfig --region ap-northeast-2 --name catch-cluster
```

6. cert-manager 생성
```
kubectl create namespace cert-manager
```

7. Helm 설치
```
helm repo add jetstack [https://charts.jetstack.io](https://charts.jetstack.io/)
helm repo update
helm install cert-manager jetstack/cert-manager --namespace cert-manager --version v1.5.0 --create-namespace --set installCRDs=true
// ingress_cert 파일이 있는곳으로 이동
cd ./k8s
```
<details>
<summary> - ingress_cert.yml</summary>
  
```
apiVersion: cert-manager.io/v1
kind: ClusterIssuer
metadata:
  name: letsencrypt-prod
spec:
  acme:
    # 인증서 서버 주소. 해당 서버의 리소스를 통해 인증서 발행
    server: https://acme-v02.api.letsencrypt.org/directory
    # 인증서 만료 또는 갱신 필요시 알람 email
    email: s99s4481@gmail.com
    privateKeySecretRef:
      name: letsencrypt-prod
    solvers:
      - http01:
          ingress:
            class: nginx
---
# ClusterIssue를 사용하여 Certificate 리소스 생성 : Certificate리소스 생성시에 인증서 발급
apiVersion: cert-manager.io/v1
kind: Certificate
metadata:
  name: catch-com-tls
  namespace: default
spec:
  secretName: catch-com-tls
  duration: 2160h #90days
  renewBefore: 360h #before 15day
  issuerRef:
    name: letsencrypt-prod
    kind: ClusterIssuer
  commonName: server.catch-crm.shop
  dnsNames:
    - server.catch-crm.shop
```

</details>
</br>

8. ingress aplly

```
kubectl apply -f ingress_cert.yml
kubectl get certificate
// 문제가 있다면 지우고 다시 시도
kubectl delete -f ingress_cert.yml
```

</br>

## nginx ingress controller 설정
```
kubectl apply -f https://raw.githubusercontent.com/kubernetes/ingress-nginx/controller-v1.1.1/deploy/static/provider/cloud/deploy.yaml
```
</br>

## ingress HOSTS 확인
<img width="1003" alt="328369541-f508d7ec-e55f-4412-8ce2-78c5ae88e060" src="https://github.com/Catch-team/Catch-BE/assets/122894395/2fd351ad-4848-4356-be61-d56b345cf45f">

## route53에 cname으로 생성된 로드밸런서 dns 넣기
<img src="https://github.com/Catch-team/Catch-BE/assets/122894395/6c790e4c-2e91-40fd-8544-2b5bd992dd3b" height="80%" width="80%">

## elastiCache (redis) 생성
<img src="https://github.com/Catch-team/Catch-BE/assets/122894395/1add8025-9183-4bd6-9a23-725121a3f2ba" height="80%" width="80%">
<img src="https://github.com/Catch-team/Catch-BE/assets/122894395/6e83de84-7cff-40fe-93ec-31a0bc960940" height="80%" width="80%">
<img src="https://github.com/Catch-team/Catch-BE/assets/122894395/7a968350-9997-46c4-bfc5-754e138ca607" height="80%" width="80%">
<img src="https://github.com/Catch-team/Catch-BE/assets/122894395/f7e30150-4ca7-4ea3-8369-dda53b1f6f51" height="80%" width="80%">

## k8s secret 설정
```
kubectl create secret generic db-infos \
--from-literal=DB_HOST= DB_HOST\
--from-literal=DB_USERNAME= DB_USERNAME \
--from-literal=DB_PASSWORD= DB_PASSWORD \
--from-literal=REDIS_HOST= REDIS_HOST \
--from-literal=GOOGLE_EMAIL= GOOGLE_EMAIL \
--from-literal=GOOGLE_SMTP= GOOGLE_SMTP \
--from-literal=JWT_SECRETKEY= JWT_SECRETKEY \
--from-literal=SYMMETRICKEY= SYMMETRICKEY \
--from-literal=FIREBASE_JSON= FIREBASE_JSON \
```

## backend git action
<details>
<summary> - backend_depoly.yml </summary>
  
```
name: deploy Catch-Backend
on:
  push:
    branches:
      - dev
jobs:
  build-and-deploy:
    runs-on: ubuntu-latest
    steps:
      - name: checkout github
        uses: actions/checkout@v2
      - name: install kubectl
        uses: azure/setup-kubectl@v3
        with:
          version: "v1.25.9"
        id: install
      - name: configure aws #aws configure 팀 키값
        uses: aws-actions/configure-aws-credentials@v1
        with:
          aws-access-key-id: ${{ secrets.AWS_ACCESS_KEY_ID }} # 추가 해줘야함
          aws-secret-access-key: ${{ secrets.AWS_SECRET_ACCESS_KEY }} # 추가 해줘야함
          aws-region: ap-northeast-2
      - name: update cluster information
        run: aws eks update-kubeconfig --name catch-cluster --region ap-northeast-2
      - name: Login to ECR
        id: login-ecr
        uses: aws-actions/amazon-ecr-login@v1

      ################ build and push #################
      - name: create-json
        uses: jsdaniell/create-json@v1.2.3
        with:
          name: "catch-push-firebase-adminsdk-x6w7k-bded31fa6b.json"
          json: ${{ secrets.FIREBASE_JSON }}
          dir: './crm/src/main/resources/'

      - name: build and push docker image to ecr (catch-crm)
        env:
          REGISTRY: 533267078155.dkr.ecr.ap-northeast-2.amazonaws.com # ECR주소
          REPOSITORY: catch-crm
          IMAGE_TAG: latest
        run: |
          docker build \
          -t $REGISTRY/$REPOSITORY:$IMAGE_TAG \
          -f ./crm/Dockerfile ./crm
          docker push $REGISTRY/$REPOSITORY:$IMAGE_TAG
      - name: build and push docker image to ecr (catch-batch)
        env:
          REGISTRY: 533267078155.dkr.ecr.ap-northeast-2.amazonaws.com # ECR주소
          REPOSITORY: catch-batch
          IMAGE_TAG: latest
        run: |
          docker build \
          -t $REGISTRY/$REPOSITORY:$IMAGE_TAG \
          -f ./batch/Dockerfile ./batch
          docker push $REGISTRY/$REPOSITORY:$IMAGE_TAG

      ################ apply ################
      - name: eks kubectl crm apply
        run: |
          kubectl apply -f ./crm/k8s/catch-crm-serv.yml
          kubectl rollout restart deployment crm
      - name: eks kubectl batch apply
        run: |
          kubectl apply -f ./batch/k8s/catch-batch-serv.yml
          kubectl rollout restart deployment batch

```

</details>
</br>

</details>

