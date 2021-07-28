# [TypeScript] 함수의 타이핑, 선택적 매개 변수와 기본 매개 변수

Date Added: July 28, 2021 2:15 PM
Person: JaeYeon Park

# 함수의 타입 명시

- 함수의 반환(Return) 타입

```tsx
function 함수 이름 (매개변수1, 매개변수2): **함수의 반환 타입 {
	...
}**
```

- 함수의 매개변수(Parameter)

```tsx
// 매개변수 뒤에 타입 선언
function sendGreeting (message: string, userName: string): void {
	console.log(`${message}, ${userName}`);
}
```

- 선택적 매개변수

```tsx
// 매개변수 뒤에 물음표 붙여서 선택적 매개변수 사용
function sendGreeting (message: string, userName?: string): void {
	console.log(`${message}, ${userName}`);
}

sendGreeting('Hello');  // 에러 발생하지 않는다
```

📌 전달되는 매개변수가 여러개이고 그 중에서 몇 개만 선택적 매개변수이면 반드시 필수 매개변수 뒤에 작성

- 기본 매개변수

```tsx
// 타입 추론을 통해 userName의 type이 string임을 알 수 있다 -> 간결한 코드를 위해 :string 제거
function sendGreeting (message: string, userName = 'there'): void {
	console.log(`${message}, ${userName}`);
}
```

- 화살표 함수

```tsx
const sendGreeting = (message: string, userName = 'there'): void =>	console.log(`${message}, ${userName}`);
```

---

참고자료

[TypeScript 함수의 타이핑, 그리고 선택적 매개 변수와 기본 매개변수](https://www.youtube.com/watch?v=SVtqhpboxGw&list=PLJf6aFJoJtbUXW6T4lPUk7C66yEneX7MN&index=8)
