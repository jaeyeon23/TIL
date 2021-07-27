# [TypeScript] Enum과 리터럴 타입

Date Added: July 27, 2021 5:32 PM
Person: JaeYeon Park

# Enum

📌 연관된 아이템들을 함께 묶어서 표현할 수 있는 수단

```tsx
enum GenderType {
	Male,
	Female	
}

interface Student{
	...
	gender: GenderType,
}

function getStudentDetails(studentId:number) : Student {
	return {
		...
		gender: GenderType.Male;
	}
}
```

📌 Enum은 TS컴파일러가 소스를 JS로 변경해도 남아있는데 이는 Enum이 **런타임에 존재하는 실제 객체**라는 것을 알려준다

```jsx
// TS에서 JS로 Enum 컴파일 할 경우
var GenderType;
(function (GenderType) {
	GenderType[GenderType["Male"] = 0] = "Male";
	GenderType[GenderType["Female"] = 1] = "Female";
}) (GenderType || (GenderType = {}));
// 선언된 값의 순서에 따라 0부터 설정
```

✅ 숫자 열거형 (Numeric Enum)

📌 숫자 대신 string 값이 들어가기를 원한다면? (문자형 열거형 : String Enum)

```tsx
// 원하는 문자를 설정하면 된다
enum GenderType {
	Male = 'male',
	Female = 'female'
}
```

# 리터럴 타입

📌 파이프로 들어갈 값 설정

```tsx
interface Student {
	...
	gender: 'male' | 'female',
}

function getStudentDetails(studentId: number): Student }
	return {
		...
		gender: 'male',
	}
}
```

---

참고자료

[https://www.youtube.com/watch?v=-TlpYcmHvb8&list=PLJf6aFJoJtbUXW6T4lPUk7C66yEneX7MN&index=6](https://www.youtube.com/watch?v=-TlpYcmHvb8&list=PLJf6aFJoJtbUXW6T4lPUk7C66yEneX7MN&index=6)
