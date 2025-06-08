## 배경지식

자바스크립트 V8 엔진을 기반으로 구축된 자바스크립트 런타임 도구

## 학습한 내용

### Node.js

Chrome V8 Javascript 엔진으로 빌드된 Javascript 런타임 환경입니다.
서버를 빌드해 작동이 가능하도록 해주는 플랫폼입니다.

### 주요 특징

- 단일 스레드와 논 블로킹 이벤트 기반 비동기 방식으로 처리됩니다.
- HTTP 서버 라이브러리를 내장으로 포함하고 있습니다
- Javascript 언어로 다양한 개발 환경을 구성할 수 있습니다.
- NPM 패키지 매니저 기반으로 다양한 모듈을 제공합니다.

## 답변 정리

**Node.js의 주요 특징에 대해 설명해주세요.**

> Node.js는 Chrome V8 엔진 위에서 동작하는 JavaScript 런타임으로, 브라우저 밖 환경에서도 JavaScript를 실행할 수 있게 해줍니다. <br> 단일 스레드 기반이지만 이벤트 루프와 논블로킹 I/O 구조 덕분에 네트워크 I/O에 매우 효율적입니다. <br> 특히 HTTP 서버 기능이 내장되어 있고, NPM을 통해 수많은 외부 모듈을 사용할 수 있어 빠른 개발이 가능합니다. <br> 프론트엔드와 백엔드를 모두 JavaScript로 작성할 수 있다는 점도 Node.js의 큰 장점 중 하나입니다.

## 예상 추가 질문

1. Node.js가 싱글 스레드인데도 고성능 네트워크 처리가 가능한 이유는 무엇인가요?
2. Node.js에서 CPU 연산이 많은 작업은 어떻게 처리하나요?
3. Node.js와 다른 백엔드 플랫폼(ex. Spring, Django 등)을 비교했을 때 장단점은 무엇이라고 생각하나요?

## 참고 자료

[NodeJS 벨로그](https://velog.io/@deannn/Node.js-Node.js%EC%9D%98-%EC%86%8C%EA%B0%9C%EC%99%80-%ED%8A%B9%EC%A7%95) <br>
[W3S NodeJS](https://www.w3schools.com/nodejs/nodejs_intro.asp) <br>
[NodeJS Docs](https://nodejs.org/ko/learn/getting-started/introduction-to-nodejs)
