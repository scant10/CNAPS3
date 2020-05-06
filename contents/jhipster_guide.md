# Jhipster를 활용한 Microservice application 개발

## Jhipster란 무엇인가?

![image](https://user-images.githubusercontent.com/18453570/81132833-b26d7c80-8f8a-11ea-8ce5-95b841fe6fae.png)

**Jhipster**란, modern 웹 애플리케이션과 마이크로서비스 아키텍처를 빠르게 적용, 개발, 배포할 수 있도록 도와주는 오픈소스 개발 플랫폼이다.
지원해주는 영역은 아래와 같다.

- Front-end 영역 지원 : Angular, React, Vue.js
- Back-end 영역 지원 : Spring Boot (Java & Kotlin 포함), Micronaut, Quarkus, Node.js, and .NET.
- Deployment 영역 지원 : Docker and Kubernetes for AWS, Azure, Cloud Foundry, Google Cloud Platform, Heroku, and OpenShift.

## Jhipster의 Goal

Jhipster 사용의 목적은 완전하고 현대적인 웹 애플리케이션과 마이크로서비스 아키텍처의 생성이며 다음과 같은 항목들을 통합하는 것이 목표이다.

- 광범위한 테스트를 커버할 수 있는 우수한 성능으 강력한 서버 스택
- 세련되고 현대적인 모바일 친화적 UI를 위한 Angular, React, Vue + Bootstrap를 갖춘 CSS
- Webpack 및 Maven 또는 Gradle을 사용하여 애플리케이션을 빌드하는 강력한 워크 플로우
- 클라우드에 빠르게 배포할 수있는 코드 기반 인프라
  
실제로 Jhipster는 설치가 간편하고, Directory 생성 후 몇가지 옵션을 선택하면 바로 실행가능한 웹 애플리케이션으로 만들어진다. 모놀리틱, 마이크로서비스, 게이트웨이를 선택할 수 있고 그 외에 Swagger나 Docker, kafka, JPA 등 현대적인 애플리케이션 개발에 필요한 환경설정과 라이브러리를 자동으로 설치해준다. 또한 기본적인 인증처리, Rest API를 이용한 통신 내용이 포함되어있다.

## Jhipster 프로젝트의 Microservice 구성요소

- JHipster 레지스트리 : MSA의 필수요소, 다른 모든 구성요소를 서로 연결하고 서로 통신할 수 있게 함

- Microservice : 백엔드 코드가 들어있고, 실행 후 도메인에 대한 API를 노출. 여러 마이크로서비스로 구성 될 수 있으며 몇 개의 엔티티와 비즈니스 규칙이 포함된다.

- Gateway : 모든 프론트 엔드 코드를 가지고 있으며 전체 마이크로 서비스에서 생성한 API 를 사용한다.

- Back-End : src/ main / java 폴더에 존재한다.

- Front-End : src / main /webapp 폴더에 존재하고, Angular JS 모듈의 대부분을 포함한다.

  
# Jhipster 환경구축 (Mac & Windows 동일)

1. Java 11 설치 ->  [AdoptOpenJDK builds](https://adoptopenjdk.net/)
2. Node.js 설치 -> **반드시 LTS 64-bit version 설치** [Node.js website](https://nodejs.org/en/) 
3. JHipster 설치 -> 
```
npm install -g generator-jhipster
```

외에 Git, Docker은 애플리케이션 실행 및 사용환경에 따라 필요한 경우에 설치한다.

- git : https://git-scm.com/
- Docker : https://www.docker.com/products/docker-desktop

## MacOS

Mac을 사용하는 경우 brew를 사용하여 설치할 수 있다. 

```
brew install jhipster
```

> 참조 : [Jhipster공식 설치가이드 링크](https://www.jhipster.tech/installation/)

# Jhipster로 개발 시작하기

Jhipster로 Microservice Application을 개발시 순서는 아래와 같다.

1. gateway 만들기
  1-1. Registry 만들기
2. Microservice 만들기
3. 생성한 Microservice에 Entity 생성하기
4. 생성된 Entity를 gateway가 인식할 수 있도록 gateway에 등록하기

따라서, Sample 프로젝트에서는 book, user, rental 3개의 Microservie를 생성하고 gateway에 등록해 Simple CRUD게시판까지 연결해보자.

> 참고 : 개발 환경은 MacOS이며, java 11 사용

## Gateway 만들기

1. gateway 폴더 생성
2. gateway 폴더를 jhipster 프로젝트로 변경

![image](https://user-images.githubusercontent.com/18453570/81142695-42232300-8fab-11ea-88a2-50a2cf6d900b.png)

```
mkdir gateway
cd gateway
jhipster
```

3. 옵션 선택

![image](https://user-images.githubusercontent.com/18453570/81142883-c2e21f00-8fab-11ea-80eb-dee5b067068a.png)

---------------------- 옵션 설명 ------------------------


## Service 만들기

### core service 1 : book

### core service 2 : user

### core service 3 : rental

## 생성한 service에 Entity를 추가하기

## 추가한 entity를 gateway에 등록시키기