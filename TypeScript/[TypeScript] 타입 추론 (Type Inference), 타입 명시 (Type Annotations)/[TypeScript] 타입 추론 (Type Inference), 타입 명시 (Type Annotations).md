# [TypeScript] 타입 추론 (Type Inference), 타입 명시 (Type Annotations)

Date Added: July 27, 2021 11:39 AM
Person: JaeYeon Park

# 정적 타이핑 (Static Typing)

📌 타입을 선언하고 선언된 타입에 맞는 값만이 할당 또는 반환되어야 한다

# 타입 추론 (Type Inference)

💡 TS는 타입 표기가 없는 경우 코드를 읽고 분석하여 **타입을 유추**해낼 수 있다

```jsx
// 자바스크립트
let a = 5;
a = '10'; 
// 에러 발생하지 않는다
```

```jsx
// 타입스크립트
let a = 5;
a = '10';
// tsc app.ts 컴파일 시 에러 발생
```

📌 TS 의 타입 추론에 의해 변수 a의 값이 5로 선언된 순간 a의 타입은 number로 설정됨

# 타입 명시 (Type Annotations)

💡 변수를 선언할 때, 변수 값의 타입을 명시함으로써 변수 값의 데이터 타입을 지정

```tsx
let studentId:number = 'hello'; // 오류
let studentName:string = 'jaeyeon';  // pass

// 함수일 경우
function getStudentDetails(studentId:number):void {
	...
}

// 함수에서 객체를 리턴할 경우 (object도 사용 가능)
function getStudentDetails(studentId:number): {
	studentId:number;
	studentName:string;
} {
	return null;
}

```

---

참고 자료

[타입스크립트 강좌 - 타입 추론 (Type Inference)](https://www.youtube.com/watch?v=rwqqhvR353A)

[타입스크립트? 타입 명시, 이건 알아야돼!](https://www.youtube.com/watch?v=W61BPW7ZTqg)
