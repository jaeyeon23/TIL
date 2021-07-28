# [TypeScript] OOP 객체지향 프로그래밍 이란? 클래스와 오브젝트 관계

Date Added: July 28, 2021 3:46 PM
Person: JaeYeon Park

# 객체지향 프로그래밍

📌 연관된 변수와 함수들을 한 덩어리로 묶어서 구조화하여 표현하는 프로그래밍 스타일

📌 어플리케이션을 실제 세상에 존재하는 객체와 같은 단위로 쪼개고 객체들이 서로 상호 작용함으로써 시스템이 동작

# Class

📌 객체의 뼈대, 설계도, 생산틀

# Object

📌 객체들은 Class를 통해 만들어진다

- 클래스

```tsx
class Employee {
	// 프로퍼티
	fullName: string;
	age: number;
	jobTitle: string;
	hourlyRate: number;
	workingHoursPerWeek: number;

	// 메소드
	printEmployeeDetails = (): void => {
		...
	}
}

// 객체 생성
let employee1 = new Employee();
```

더 자세한 클래스

[TypeScript 한글 문서](https://typescript-kr.github.io/pages/classes.html)

---

참고자료

[OOP 객체지향 프로그래밍 이란? 클래스와 오브젝트 관계 파헤치기](https://www.youtube.com/watch?v=bdXnsyelOGg&list=PLJf6aFJoJtbUXW6T4lPUk7C66yEneX7MN&index=9)
