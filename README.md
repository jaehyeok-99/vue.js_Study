# Vue.js Study

캡틴판교의 **Vue.js 시작하기 - Age of Vue.js**를 따라 Vue의 반응성, 컴포넌트 통신, 라우팅, HTTP 요청을 실습한 학습 기록입니다. 개념별 HTML 예제와 Vue 3·Vite로 구성한 사용자 입력 폼을 담았습니다.

## 학습 자료

- 강의: [Vue.js 시작하기 - Age of Vue.js](https://www.inflearn.com/course/age-of-vuejs)
- 강사: 캡틴판교
- 플랫폼: 인프런

강의의 개념별 실습 흐름과 저장소의 파일 구성을 대조해 정리했습니다. 강의에서는 프로젝트 생성 도구로 Vue CLI를 다루며, 이 저장소의 폼 프로젝트는 Vite를 사용합니다.

## 저장소 구성

| 폴더 | 내용 |
| --- | --- |
| [getting-started](./getting-started/) | Vue 인스턴스를 생성하고 메시지를 화면에 표시하는 첫 예제 |
| [playground](./playground/) | 반응성, 컴포넌트, 템플릿 문법, 라우터, Axios의 개념별 실습 |
| [vite-project01](./vite-project01/) | Vue 3·Vite 환경의 싱글 파일 컴포넌트와 사용자 입력 폼 |

## 실습 내용

| 주제 | 관련 파일 | 실습한 내용 |
| --- | --- | --- |
| 화면 갱신과 반응성 | [web-dev.html](./playground/web-dev.html), [vue-way.html](./playground/vue-way.html) | 직접 DOM을 갱신하는 방식과 Object.defineProperty의 setter로 화면을 갱신하는 방식 비교 |
| Vue 인스턴스 | [instance.html](./playground/instance.html) | el, data, methods 등 인스턴스 옵션 |
| 컴포넌트 | [component.html](./playground/component.html) | 전역·지역 컴포넌트 등록 |
| 부모 → 자식 데이터 전달 | [props.html](./playground/props.html) | props와 v-bind |
| 자식 → 부모 이벤트 전달 | [event-emit.html](./playground/event-emit.html) | $emit으로 이벤트를 보내 부모의 메서드 실행 |
| 같은 레벨의 컴포넌트 통신 | [component-same-level.html](./playground/component-same-level.html) | 부모가 이벤트를 받아 데이터를 바꾸고 다른 자식에 props로 전달 |
| 라우팅 | [router.html](./playground/router.html) | /login·/main 경로와 router-link·router-view |
| HTTP 요청 | [axious.html](./playground/axious.html) | Axios로 예제 API의 사용자 목록 조회 및 응답·오류 처리 |
| 데이터 바인딩 | [data-binding.html](./playground/data-binding.html) | v-bind, v-if·v-else, v-show, v-model |
| 이벤트 처리 | [methods.html](./playground/methods.html) | 클릭과 Enter 키 입력으로 메서드 실행 |
| computed와 watch | [computed-usage.html](./playground/computed-usage.html), [watch.html](./playground/watch.html), [watch-vs-computed.html](./playground/watch-vs-computed.html) | 계산된 값으로 CSS 클래스 결정, 데이터 변경 감지 및 메서드 호출 |

### 사용자 입력 폼

[vite-project01/src/App.vue](./vite-project01/src/App.vue)에서 아이디·비밀번호 입력 폼을 구현했습니다.

- v-model로 입력값과 컴포넌트 데이터 연결
- submit.prevent로 폼 제출 시 기본 페이지 이동 방지
- Axios로 JSONPlaceholder에 POST 요청
- 응답과 오류를 콘솔에서 확인

이 폼은 예제 API에 데이터를 보내는 실습입니다. 실제 사용자 인증이나 로그인 세션을 구현한 것은 아닙니다.

## 실행 방법

### HTML 예제

`getting-started/index.html` 또는 `playground/`의 HTML 파일을 브라우저로 열어 확인할 수 있습니다. 콘솔 출력은 브라우저 개발자 도구에서 확인합니다.

예제는 `new Vue()` 등 Vue 2 문법을 사용합니다. Vue CDN 주소에 버전이 고정되어 있지 않아, 실행할 때 Vue 2가 로드되는지 확인해야 합니다. 라우터 예제는 Vue Router 3.5.3을 사용하며 CDN과 예제 API 접근에는 인터넷 연결이 필요합니다.

### Vue 3·Vite 프로젝트

Node.js와 npm을 준비한 뒤 실행합니다.

```bash
cd vite-project01
npm ci
npm run dev
```

터미널에 표시되는 개발 서버 주소를 브라우저로 엽니다.

```bash
npm run build
npm run preview
```

위 명령은 빌드와 빌드 결과 미리보기에 사용합니다. package.json에는 Vue 3.5, Vite 7.2, Axios 1.13 계열이 선언되어 있습니다.

## 기록 범위

현재 남아 있는 코드의 학습 범위를 정리한 README입니다. 개념별 예제와 입력 폼 실습을 보관하며, 강의 전체 수강 여부를 나타내지는 않습니다.
