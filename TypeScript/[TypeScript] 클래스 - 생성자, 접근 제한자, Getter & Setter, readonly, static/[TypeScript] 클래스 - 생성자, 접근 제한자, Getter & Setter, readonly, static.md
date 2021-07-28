# [TypeScript] 클래스 - 생성자, 접근 제한자, Getter & Setter, readonly, static

Date Added: July 28, 2021 4:38 PM
Person: JaeYeon Park

# Constructor (생성자)

📌 클래스의 인스턴스를 만들 때 호출되는 함수 → 객체의 초기화를 담당

```tsx
class Employee {
	fullName: string;
	age: number;
	jobTitle: string;
	hourlyRate: number;
	workingHoursPerWeek: number;

	constructor(fullName: string, age: number, jobTitle: string, 
		hourlyRate: number, workingHoursPerWeek: number) {
		this.fullName = fullName;
		...
	}
}
```

# Access Modifiers (접근 제한자)

📌 클래스 속의 프로퍼티와 메소드에 적용될 수 있는 키워드를 클래스 외부로 부터의 접근 통제

📌 public - 자식 클래스, 클래스 인스턴스 모두 접근 가능 (Default 값)

📌 protected - 자식 클래스에서 접근 가능 (인스턴스 X)

📌 private - 해당 클래스 내부에서만 접근 가능

# Getter & Setter

```tsx
class Employee {
	// 클래스 내에서 멤버변수를 나타내는 fullName 앞에 _를 넣어 private임을 표시(통용)
	private _fullName: string;
	age: number;
	jobTitle: string;
	hourlyRate: number;
	workingHoursPerWeek: number;

	constructor(fullName: string, age: number, jobTitle: string, 
		hourlyRate: number, workingHoursPerWeek: number) {
		this.fullName = fullName;
		...
	}

	// getter
	get fullName() {
		return this._fullName;
	}
	
	// setter
	set fullName(value: string) {
		this._fullName = value;
	}
}

let employee1: Employee = new Employee('민수',28,'주니어개발자',40,35);
console.log(employee1.fullName);  // getter통해 접근 가능
employee1.fullName('test');  // setter통해 접근 가능
```

# Constructor와 Access Modifiers

📌 객체가 생성될 때, constructor의 매개변수로 전달된 값은 객체의 프로퍼티 값으로 자동으로 그 값이 초기화되고 할당 됨

```tsx
class Employee {
	constructor(
		private _fullName: string,
		private _age: number,
		private _jobTitle: string,
		private _hourlyRate: number,
		public workingHoursPerWeek: number
	) {}
}
```

# Readonly, static

📌 readonly가 붙은 값은 변경할 수 없다 (생성자 통해 변경 가능)

```tsx
class Employee {
	readonly fullName: string = "jaeyeon";
	...
}
```

📌 static은 클래스 명을 통해서 값을 가져올 수 있다

```tsx
lass Employee {
	static fullName: string = "jaeyeon";
	...
}

...
console.log(Employee.fullName);
```

---

참고자료

[타입스크립트 클래스 - 생성자 (Constructor), 접근 제한자 (Access Modifiers), Getter 와 Setter](https://www.youtube.com/watch?v=sPM94o5_WVU&list=PLJf6aFJoJtbUXW6T4lPUk7C66yEneX7MN&index=10)
