## 2023년 4월 21일

### 📚 스터디 진행 사항 

- 스터디(~7챕터)
  - 이해 안 되는 부분/책을 읽고 생긴 궁금증 공유하고 토론

---

### 진행 내용

1. 클린 : 미션을 진행하며 다중인터페이스를 사용했나요?

야미 : 네, 카드 인풋에서 재사용하기 위해 사용했습니다.

나머지 : 각자 인풋마다 인터페이스를 지정해 주었습니다.

슬링키 : 저는 타입을 썼습니다. (관성적으로)

---

2. 야미 : 미션에서 쓴 것 있나요?

슬링키 : 알고 쓴건 아닌데 미션을 진행하며 다 써본 것들이었다.

야미 : 함수와 메서드는 한번도 쓰지 않았다. 여러분은?

나머지 : 속성을 사용했습니다.

---

Q. 첵스 : `readonly`와 `as const`의 차이?

클린의 추측 : `Readonly` 제네릭은 선언 단계에서 타입 지정, `as const`는 컴파일러 단계에서 타입 지정?

슬링키의 링크: https://medium.com/lean-coders/understand-const-as-const-and-readonly-in-typescript-a-comprehensive-explanation-1b54f24b35d6

슬링키 : 값이 아니라 레퍼런스가 고정된다. 배열이나 객체를 넣으면 푸시 팝 됨. 그런데 as const는 그걸 막겠다. 비슷하긴 한데 다르다.......?

야미 : readonly와 Readonly의 차이?

클린 & 슬링키 : 제네릭으로 사용하기 위한 Readonly인 것 같다. as const는 객체를 선언한 후 타입으로!

---
