## 2023년 4월 21일

### 질문 🙋‍♂️

Q. 첵스 : 나머지 매개변수로의 튜플

A.
```typescript
// function logPair(name:string,value:number){
//   console.log(`${name} has ${value}`);
// }

// const pairArray = ["슬링키",1]; // 이건 그냥 악질 배열 (타입이 선언 되지 않은)

// logPair(...pairArray);

// const pariTupleInCorrect : [number,string] = [1,"슬링키"]; // 튜플 순서가 맞지 ㅇ낳아서

// logPair(...pariTupleInCorrect);

// const pairTupleCorrect : [string,number] = ["슬링키",1]; // 이건 맞음.

// logPair(...pairTupleCorrect);

// function logTrio(value:[string,[number,boolean]],index:number, origin: [string,[number,boolean]][]){
//   console.log(`${name} has ${value}`);
// }


function logTrio(name: string, value: [number,boolean]){
  console.log(`${name} has ${value}`);
}

const trios: [string,[number,boolean]][] = [
  ["스링키",[1,true]],
  ["악질",[1,true]],
  ["스링키",[1,true]],

]

trios.forEach((trio) => {
  logTrio(...trio) // ["스링키",[1,true]], -> "스링키" , [1,true]
  });

trios.forEach(logTrio);

```
**`logTrio`의 매개변수의 개수**와 **`trios.forEach`에서의 `trio`가 스프레드 됐을 때** 매개변수의 개수가 같아지기('스링키', [1, true]) `forEach`문에서 오류가 발생하지 않는다. 

---

Q. 슬링키의 미션 중 학습

A.
```tyepscript

const check = (data:number)=> {
  const one = 1+data;
  const two = 2+data;
  const three = () =>{ return 1 };
  return [one, two, three]; // Tuple화 시켜벌임;;
} // 반환 되는 타입이 튜플이 아니라 (number | () => number)[] 타입이기 때문에 타입이 맞지 않음.

let arr = ["슬 'the 악질' 링키",1] as const;

let [a, b, c] = check(1);

c();

```
`as const`를 사용하여 배열이 튜플로 처리되어야 함을 나타낸다. 

---


Q. 야미 : 구조적 타이핑의 예시 ??

A.
```typescript

// const hasOnlyBoth = {
//   first:"악질",
//   last:"링키"
// }

// type WithFirst ={
//   first:string
// }


// type WithLast ={
//   last:string
// }

// const withFirst : WithFirst = hasOnlyBoth
// const withLast : WithLast = hasOnlyBoth

// for(const [key,value] of Object.entries(withFirst)){
//   console.log(`${key} : ${value}`)
// }


type car = "봉고차" | "경차";

type type1<T extends string>={
  [key in T]: number;
};

const haha = {
    봉고차:1,
    경차:2
}

const check:type1<car> = haha; // 통과


const check2:type1 = {
    a:1,
    b:2 // 오류
    
}

```

---

Q. 야미 : 옵셔널 타입 대신 판별된 유니온을 사용하는 것이 좋은가?

A. ...
