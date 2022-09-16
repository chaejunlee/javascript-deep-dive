# 02장 자바스크립트란?

## 2.1 자바스크립트의 탄생

1995년 넷스케이프 커뮤니케이션즈는 웹페이지의 보조적인 기능을 수행하기 위해 브라우저에서 동작하는 경량 프로그래밍 언어를 도입하기로 결정한다. 그래서 탄생한 것이 바로 브렌던 아이크가 개발한 자바스크립트다.

## 2.2 자바스크립트의 표준화

이에 자바스크립트의 파편화를 방지하고 모든 브라우저에서 정상적으로 동작하는 표준화된 자바스크립트의 필요성이 대두되기 시작했다. 이를 위해 1996년 11월, 넷스케이프 커뮤니케이션즈는 컴퓨터 시스템의 표준을 관리하는 비영리 표준화 기구인 ECMA 인터내셔널에 자바스크립트의 표준화를 요청한다.

1997년 7월, ECMA-262라 불리는 표준화된 자바스크립트 초판 (ECMAScript 1) 사양이 완성되었고 ,상표권 문제로 자바스크립트는 ECMAScript로 명명되었다. 이후 1999년 ECMAScript 3(ES3)이 공개되고 10년만인 2009년에 출시된 ECMAScript5(ES5)는 HTML5와 함께 출현한 표준 사양이다.

| 버전                  | 출시 연도 | 특징                                                                                                                                                                                               |
| --------------------- | --------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| ES1                   | 1997      | 초판                                                                                                                                                                                               |
| ES2                   | 1998      | ISO/IEC 16262 국제 표준과 동일한 규격을 적용                                                                                                                                                       |
| ES3                   | 1999      | 정규 표현식, `try … catch`                                                                                                                                                                         |
| ES5                   | 2009      | HTML5와 함께 출현한 표준안. `JSON`, `strict mode`, 접근자 프로퍼티, 프로퍼티 어트리뷰트 제어, 향상된 배열 조작 기능(`forEach`, `filter`, `reduce`, `some`, `every`)                                |
| ES6(ECMAScript 2015)  | 2015      | `let`/`const`, 클래스, 화살표 함수, 템플릿 리터럴, 디스트럭처링 할당, 스프레드 문법, rest 파라미터, 심벌, 프로미스, `Map`/`Set`, 이터러블, `for … of`, 제너레이터, `Proxy`, 모듈 `import`/`export` |
| ES7(ECMAScript 2016)  | 2016      | 지수(\*\*) 연산자, `Array.prototype.includes`, `String.prototype.includes`                                                                                                                         |
| ES8(ECMAScript 2017)  | 2017      | `async`/`await`, `Object` 정적 메서드(`Object.values`, `Object.entries`, `Object.getOwnPropertyDescriptors`)                                                                                       |
| ES9(ECMAScript 2018)  | 2018      | `Object rest`/`spread` 프로퍼티, `Promise.prototype.finally`, `async generator`, `for await … of`                                                                                                  |
| ES10(ECMAScript 2019) | 2019      | `Object.fromEntries`, `Array.prototype.flat`, `Array.prototype.flatMap`, optional catch binding                                                                                                    |
| ES11(ECMAScript 2020) | 2020      | `String.prototype.matchAll`, `BigInt`, `globalThis`, `Promise.allSettled`, `null` 병합 연산자, 옵셔널 체이닝 연산자, `for … in enumeration order `                                                 |

## 2.3 자바스크립트 성장의 역사

초창기 자바스크립트는 웹페이지의 보조적인 기능을 수행하기 위해 한정적인 용도로 사용됐다.

브라우저는 서버로부터 전달받은 HTML과 CSS를 단순히 렌더링하는 수준이었다.

### 2.3.1 AJAX

1999년, 자바스크립트를 이용해 서버와 브라우저가 **비동기(Asynchronous)** 방식으로 데이터를 교환할 수 있는 통신 기능인 **AJAX(Asynchronous JavaScript and XML)** 가 `XMLHttpRequest`라는 이름으로 등장했다.

AJAX의 등장으로 웹페이지에서 변경할 필요가 없는 부분은 다시 렌더링하지 않고, 서버로부터 필요한 데이터만 전송받아 변경해야 하는 부분만 한정적으로 렌더링하는 방식이 가능해졌다. 웹 브라우저에서도 데스크톱 애플리케이션과 유사한 빠른 성능과 부드러운 화면 전환이 가능해졌다.

### 2.3.2 jQuery

2006년 등장한 jQuery는 DOM(Document Object Model)을 더욱 쉽게 제어할 수 있어 되었다.

### 2.3.3 V8 자바스크립트 엔진

2008년에 구글은 V8 자바스크립트 엔진을 만든다. 자바스크립트는 데스크톱 애플리케이션과 유사한 사용자 경험(UX: user experience)을 제공할 수 있는 웹 애플리케이션 프로그래밍 언어로 정학하게 되었다.

V8 자바스크립트 엔진으로 촉발된 자바스크립트의 발전으로 과거 웹 서버에서 수행되던 로직들이 대거 클라이언트(브라우저)로 이동했고, 이는 웹 애플리케이션 개발에서 프론트엔드 영역이 주목 받는 계기로 작동했다.

### 2.3.4 Node.js

2009년, 라이언 달(Ryan Dahl)이 발표한 Node.js는 구글 V8 자바스크립트 엔진으로 빌드된 자바스크립트 런타임 환경(Runtime Environment)이다.

Node.js는 브라우저의 자바스크립트 엔진에서만 동작하던 자바스크립트를 브라우저 이외의 환경에서도 동작할 수 있도록 자바스크립트 엔진을 브라우저에서 독립시킨 자바스크립트 실행 환경이다. Node.js는 다양한 플랫폼에 적용할 수 있지만 서버 사이드 애플리케이션 개발에 주로 사용되며, 이에 필요한 모듈, 파일 시스템, HTTP 등 빌트인 API를 제공한다.

프론트와 백 영역에서 자바스크립트를 사용할 수 있다는 동형성(isomorphic)은 별도의 언어를 학습하기 위한 시간을 덜 수 있다는 장점이 있다.

Node.js는 비동기 I/O를 지원하며 단일 스레드(Single Threaded) 이벤트 루프 기반으로 동작함으로써 요청(Request) 처리 성능이 좋다. 따라서 Node.js는 데이터를 실시간으로 처리하기 위해 I/O가 빈번하게 발생하는 SPA(Single Page Application)에 적합하다.

### 2.3.5 SPA 프레임워크

모던 웹 애플리케이션은 데스크톱 애플리케이션과 비교해도 손색 없는 성능과 사용자 경험을 제공하는 것이 필수가 되었다.

다양한 패턴과 라이브러리가 등장했고 변경에 유연하면서 확장하기 쉬운 애플리케이션 아키텍처의 구축이 어려워지면서 프레임워크가 등장했다.

CBD(Component Based Development) 방법론을 기반으로 하는 SPA(Single Page Application)가 대중화되었다.

## 2.4 자바스크립트와 ECMAScript

ECMAScript는 자바스크립트의 표준 사양인 ECMA-262를 말하며, 프로그래밍 언어의 값, 타입, 객체와 프로퍼티, 함수, 표준 빌트인 객체 등 핵심 문법을 규정한다. ECMAScript는 각 브라우저 제조사가 브라우저에 내장되는 자바스크립트 엔진을 구현하기 위해 따르는 사양이다.

자바스크립트는 일반적으로 프로그래밍 언어로서 기본 뼈대를 이루는 ECMAScript와 브라우저가 별도로 지원하는 클라이언트 사이드 Web API, 즉 DOM, BOM, Canvas, `XMLHttpRequest`, `fetch`, `requestAnimationFrame`, SVG, Web Storage, Web Component, Web Worker 등을 아우르는 개념이다.

→ 자바스크립트는 일반적으로 ECMAScript를 아우르는 개념

## 2.5 자바스크립트의 특징

자바스크립트는 웹 브라우저에서 동작하는 유일한 프로그래밍 언어다.

자바스크립트는 개발자가 별도의 컴파일 작업을 수행하지 않는 인터프리터 언어다.

모던 자바스크립트 엔진은 인터프리터와 컴파일러의 장점을 결합해 비교적 처리 속도가 느린 인터프리터의 단점을 해결했다.

자바스크립트는 클래스 기반 객체지향 언어보다 효율적이면서 강력한 프로토타입 기반의 객체지향 언어다.