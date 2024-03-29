# [TypeScript] TypeScript Overview

Date Added: July 21, 2021 2:30 PM
Person: JaeYeon Park

- 타입스크립트는 [프로그래밍 언어] 이다.
- 타입스크립트는 'Compiled Language'이다.

    → 전통적인 Compiled Language와는 다른 점이 많다.

    → 그래서 Transpile이라는 용어를 사용하기도 한다. ex) babel

- 자바스크립트는 'Interpreted Language'이다.
<img src="./[TypeScript] TypeScript Overview Image/Untitled.png">

## Traditional Compiled Language (참고용)

- 컴파일 언어라고 한다.
- 프로그래머가 작성한 'Source Code'를 기계어로 변환하는 과정을 'Compile'이라고 한다.
- 기계어로 변환된 결과물을 'Object Code'(목적 코드)라 한다.
- 컴파일된 코드는 프로세서에 따라 다르다.
- 소스 코드에서는 OS에 따라 라이브러리가 다르다.
- 컴파일된 코드는 작은 크기에 최적화된다.
- 일반적으로 실행시 기계어로 바꾸는 방식(인터프리터 언어)보다 빠르다.

    → 실행시 기계어로 바꿔주는 연산이 필요없기 때문이다.

~~타입스크립트는 컴파일하면 코드량이 많아진다. 변하겠지?~~

# TypeScript 특징

### 타입 (Types)

TS는 JS와 다르게 값의 종류를 기반으로 프로그램의 오류를 찾는다.  

→ TS가 정적 타입 검사자이기 때문

### 런타임 특성 (Runtime Behavior)

TS는 JS의 런타임 특성을 가진 프로그래밍 언어 

→ JS 런타임 특성

[[JavaScript] 자바스크립트 런타임](https://beomy.github.io/tech/javascript/javascript-runtime/)

📌 즉, TS가 코드에 타입 오류가 있음을 검출해도 JS코드를 TS로 이동시키는 것은 같은 방식으로 실행시킬 것을 보장한다.

📌 JS와 동일한 런타임 동작을 유지하는 것은 프로그램 작동을 중단시킬 수 있는 미묘한 차이를 걱정하지 않고 두 언어 간에 쉽게 전환할 수 있도록 하기 위한 TS의 기본적인 약속

### 삭제된 타입 (Erased Types)

TS의 컴파일러가 코드 검사를 마치면 타입을 삭제해서 결과적으로 컴파인된 코드를 만든다. 

→ 결과로 나온 일반 JS 코드에는 타입 정보가 없다.

TS는 추가 런타임 라이브러리를 제공하지 않는다. TS는 JS와 같은 표준 라이브러리를 사용하므로, TS관련 프레임워크를 추가로 공부할 필요가 없다.

### 객체 지향적

### 컴파일 타임 오류

TS는 JS로 컴파일 되어야 한다

## TypeScript 장점

📌 JS에 비해 코드 정리가 편하여 버그 줄이고 쉬운 유지보수가 가능하여 질 좋은 코드 작성 가능

---

참고 자료

[[Javascript VS Typescript] 자바스크립트와 타입스크립트 중 뭐가 더 좋을까](https://bonita-sy.tistory.com/entry/Javascript-VS-Typescript-자바스크립트와-타입스크립트-중-뭐가-더-좋을까)

[자바스크립트와 타입스크립트 차이점](https://velog.io/@pluviabc1/자바스크립트와-타입스크립트-차이점)

[TypeScript 한글 문서](https://typescript-kr.github.io/)
