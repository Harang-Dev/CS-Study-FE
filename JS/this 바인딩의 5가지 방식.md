## this 바인딩의 5가지 방식

자바스크립트에서 `this`는 함수가 호출되는 **방식에 따라** 바인딩되는 값이 달라집니다.  
다음은 `this`가 바인딩되는 4가지 주요 방식입니다.

---

### 1. 일반 함수 호출 (기본 바인딩)

- 전역에서 호출한 함수의 `this`는 **전역 객체(window 또는 global)**
- strict mode에서는 `undefined`

```js
function show() {
  console.log(this);
}
show(); // window (엄격 모드에선 undefined)
```

---

### 2. 메서드 호출 (암시적 바인딩)

- 객체의 프로퍼티로 함수를 호출할 경우 this는 해당 객체로 바인딩됨

```js
const person = {
  name: "Seo",
  greet() {
    console.log(this.name);
  },
};
person.greet(); // "Seo"
```

---

### 3. 생성자 함수 호출 (new 바인딩)

- `new` 키워드로 함수를 호출하면 `this`는 새로 생성된 인스턴스 객체를 가리킴

```js
function Person(name) {
  this.name = name;
}
const me = new Person("Seo");
console.log(me.name); // "Seo"
```

---

### 4. 명시적 바인딩 (call, apply, bind)

- `call`, `apply`, `bind` 를 사용하여 원하는 객체를 this로 명시적으로 지정 가능

```js
function sayHello() {
  console.log(this.name);
}

const user = { name: "Seo" };

sayHello.call(user); // "Seo"
sayHello.apply(user); // "Seo"

const boundFunc = sayHello.bind(user);
boundFunc(); // "Seo"
```

---

### 5. 화살표 함수의 this

- 화살표 함수는 자신의 this를 가지지 않음
- 외부(상위 스코프)의 this를 그대로 참조

```js
const obj = {
  name: "Arrow",
  say: () => {
    console.log(this.name); // 상위 스코프의 this (window 또는 undefined)
  },
};
obj.say();
```

---

### 6. 요약

| 방식          | 설명                        | this 값                |
| ------------- | --------------------------- | ---------------------- |
| 기본 바인딩   | 단독 함수 호출              | 전역 객체 or undefined |
| 암시적 바인딩 | 객체의 메서드로 호출        | 그 객체                |
| new 바인딩    | 생성자 함수 호출            | 생성된 인스턴스 객체   |
| 명시적 바인딩 | call, apply, bind로 지정    | 지정한 객체            |
| 화살표 함수   | 상위 스코프에서 this를 참조 | 외부 스코프의 this     |
