<h1 align="center">Beginner's TypeScript Study</h1>

<br />

## 목차

1. [스터디 소개](#1)
2. [스터디원 소개](#2)
3. [스터디 일정](#3)

<br />

<div id="1"></div>

## 스터디 소개

러닝 타입스크립트 서적을 읽고 공부하는 스터디입니다.

<br />

<div id="2"></div>

## 스터디원 소개

<table>
  <tr>
    <td align="center" width="92px">
      <a href="https://github.com/feb-dain" target="_blank">
        <img src="https://avatars.githubusercontent.com/u/108778921?v=4" alt="야미 프로필" />
      </a>
    </td>
    <td align="center" width="92px">
      <a href="https://github.com/HyeryongChoi" target="_blank">
        <img src="https://avatars.githubusercontent.com/u/24777828?v=4" alt="첵스 프로필" />
      </a>
    </td>
    <td align="center" width="92px">
      <a href="https://github.com/regularPark" target="_blank">
        <img src="https://avatars.githubusercontent.com/u/90092440?v=4" alt="레고 프로필" />
      </a>
    </td>
    <td align="center" width="92px">
      <a href="https://github.com/dladncks1217" target="_blank">
        <img src="https://avatars.githubusercontent.com/u/45068522?v=4" alt="슬링키 프로필" />
      </a>
    </td>
     <td align="center" width="92px">
      <a href="https://github.com/hozzijeong" target="_blank">
        <img src="https://avatars.githubusercontent.com/u/50974359?v=4" alt="클린 프로필" />
      </a>
    </td>
  </tr>
  <tr>
    <td align="center">
      <a href="https://github.com/feb-dain" target="_blank">
        야미
      </a>
    </td>
    <td align="center">
      <a href="https://github.com/HyeryongChoi" target="_blank">
        첵스
      </a>
    </td>
    <td align="center">
      <a href="https://github.com/regularPark" target="_blank">
        레고
      </a>
    </td>
    <td align="center">
      <a href="https://github.com/dladncks1217" target="_blank">
        슬링키
      </a>
    </td>
    <td align="center">
      <a href="https://github.com/hozzijeong" target="_blank">
        클린
      </a>
    </td>
  </tr>
</table>

<br />

<div id="3"></div>

## 스터디 일정

- **2023.04.14**
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

 
<br />
<br />
