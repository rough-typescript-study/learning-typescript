## **2023.04.14**

### 📚 스터디 진행 사항 

- 스터디 온보딩(~3챕터)
- 학습한 내용을 바탕으로 토론 진행
  - type A | type B,  type A & type B 에 대한 이해
- 추가로 duck typing에 대한 이해

  ```ts
  type person1 = {a:number, b:number, c:number}
  type person2 = {b:number, c:number[],d:number,e:number}
  type or = person1 | person2;
  type and = person1 & person2;
  const haha:or = {a:1,b:1,c:1};
  const haha2:person1&Omit<person2,'c'>= {
    a:2, 
    b:1,
    c:1,
    d:1,
    e:1
  };
  interface Point {
    x: number;
    y: number;
  }
  function logPoint(p: Point) {
    for(const value of Object.values(p)){
      console.log(value)
    }
  }
  interface Foint{
    x: number;
    y: number;
  }
  // logs "12, 26"
  const foint:Foint = { x: 12, y: 26 };
  logPoint(foint);
  ```
