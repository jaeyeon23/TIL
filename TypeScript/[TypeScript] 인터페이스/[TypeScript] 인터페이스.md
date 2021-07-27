# [TypeScript] 인터페이스

Date Added: July 27, 2021 3:54 PM
Person: JaeYeon Park

📌 인터페이스를 타입으로 가지는 값은 인터페이스의 구조를 그 값으로 가지도록 강제된다

```tsx
// 인터페이스
interface Student {
	studentId:number;
	studentName:string;
}

// 인터페이스로 리턴 타입 설정
function getStudentDetails(studentId: number): Student {
	...
}
```

📌 인터페이스의 특정 값을 선택적으로 갖게 하려면

```tsx
// 인터페이스
interface Student {
	studentId: number;
	studentName: string;
	age?: number;  // optional ?
}

// 인터페이스로 리턴 타입 설정
function getStudentDetails(studentId: number): Student {
	return {
		studentId: 10;
		studentName: 'jaeyeon';
	}
}
```

→ 물음표가 붙은 age값은 선택적으로 리턴할 수 있다 (선택적 프로퍼티)

📌 인터페이스 재사용이 가능하다

```tsx
function saveStudentDetails(student: Student): void {
	...
}
```

📌 인터페이스 안에 메소드 선언 가능

→ 메소드 : 객체 내에서 선언된 함수

```tsx
// 인터페이스
interface Student {
	...
	// 같은 동작을 한다. 표현 방법만 다를 뿐
	addCommnet (comment: string): string;
	addComment: (comment: string) => string;
}
```

📌 Readonly 프로퍼티 : 읽기 전용 프로퍼티로 객체 생성시 할당된 프로퍼티의 값을 바꿀 수 없다

```tsx
// 인터페이스
interface Student {
	readonly studentId: number;
	studentName: string;
	age?: number;  // optional ?
}

function saveStudentDetails (student: Student): void {
	student.studentId = 112233;  // 에러 발생
}
```

📌 TS컴파일러가 코드를 JS로 변환할 때 interface들은 모두 삭제된다.

→ 인터페이스틑 작성 중인 코드에 대한 더 많은 정보를 TS에 제공하기 위해서 존재한다.

TypeScript 네이밍 컨벤션

[Coding guidelines · microsoft/TypeScript Wiki](https://github.com/microsoft/TypeScript/wiki/Coding-guidelines)

---

참고자료

[타입스크립트, 타입으로 사용되는 인터페이스 (Interface)!](https://www.youtube.com/watch?v=jlzvXcDGZUU&list=PLJf6aFJoJtbUXW6T4lPUk7C66yEneX7MN&index=5)
