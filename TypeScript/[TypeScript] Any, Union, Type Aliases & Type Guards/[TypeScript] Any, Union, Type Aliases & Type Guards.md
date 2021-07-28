# [TypeScript] Any, Union, Type Aliases & Type Guards

Date Added: July 28, 2021 1:57 PM
Person: JaeYeon Park

# Any 타입

📌 어떠한 타입이든 모두 들어갈 수 있다

```tsx
let someValue: any = 5;
someValue = 'hello';
someValue = true;
// 모두 성공
```

But, 타입 스크립트는 타입에 관한 더 많은 정보를 명시할 수록 좋다

→ 타입 에러를 컴파일 시에 잡아냄으로써 효과적인 코드 유지 보수 가능

💡 Any 타입은 최대한 피하는 것이 좋다

# 유니언 타입

📌 제한된 타입들을 동시에 지정하고 싶을 때 (ex. 타입이 숫자 아니면 문자일 경우)

```tsx
let someValue: number | string = 5;
someValue = 'free';  // 성공
someValue = true;  // 실패

```

# Type Aliases

📌 유니언 타입이 여러번 나오는 경우 같은 코드를 반복하는 것보다 코드를 타입으로 지정하고 재활용

```tsx
type StrOrNum = number | string;
let someValue: StrOrNum;
```

# Type Guards

📌 유니언 타입을 사용할 때 아래와 같이 Typeof Operator를 사용하여 코드 검증을 수행하는 것

```tsx
type StrOrNum = number | string;
let someValue: number;

const setItemPrice = (price: StringOrNum): void => {
	someValue = price;  // price에 string, number 모두 가능
}
```

❓ 위와 같은 경우 someValue에 경고 표시가 나타난다

✅ JS의 Typeof Operator를 사용한다

```tsx
type StrOrNum = number | string;
let someValue: number;

const setItemPrice = (price: StringOrNum): void => {
	if (typeof price === 'string') {
		someValue = 0;
	} else {
		someValue = price;  
	}
}
```

더 자세한 Type Guards의 방법

[타입 가드](https://radlohead.gitbook.io/typescript-deep-dive/type-system/typeguard)

---

참고자료

[타입스크립트, 유니언 타입, 타입가드, 타입 별칭 쉽게 이해하기!](https://www.youtube.com/watch?v=lmjQh2LrH94&list=PLJf6aFJoJtbUXW6T4lPUk7C66yEneX7MN&index=7)
