### 과제 작성
- 코드를 작성할 때 어떤 아이디어로 작성했는지 주석으로 작성하자.
- 과제할 때, 어떤 생각으로 시도하려고 했는데, 잘 안됐다 등 주석으로 적을 것.


### 값과 리터럴
- 값으로 변환될 수 있는 부분을 모두 표현식이라 한다.
- 변수는 값에 붙이는 이름이다.

- html의 속성: attribute, javascript의 속성: property



### 객체

- 자바스크립트의 객체는 가변 길이이다.
- 자바스크립트는 자료구조의 유연성이 좋다. 
- 객체의 속성 이름에는 x, 'x' 둘 다 쓸 수 있다. 다른 점은 차후에 설명해주실 예정.
- 속성 값에는 무엇이든 올 수 있다.

- 객체 안에 객체가 중첩될 수 있다.
```js
const obj = {
  x: 0,
  y: {
    x: 1,
    y: 2  
  }
}

obj.y.x;
```



* 대입을 할 때는 = 오른쪽 식이 먼저 실행된다.
```js
let x = 1;
x = x + 1;
<!-- x += 1;
x *= 3;
x /= 3;
 -->
console.log(x);
```



* delete 연산자: 객체의 속성을 삭제할 수 있다.
- 객체의 속성을 아예 없애버릴 수 있다.
```js
const obj = {
  x: 0,
  y: 1
}

delete obj.x;

obj;
<!-- {y: 1} 객체의 x속성이 없어짐. -->
```

### 메소드
- 객체 안에 있고, 객체의 속성을 통해서 사용하는 함수를 메소드라고 부른다.
```js
const obj = {
  x: 0,
  increaseX: function() {
    this.x = this.x + 1;
  }
};

const obj = {
  x: 0,
  increaseX: function() {
    this.x = this.x + 1;
    <!-- this는 자기 자신을 가리키는 키워드.
    실행하는 순간, this가 obj로 샤샤샥 바뀜. -->
  }
};

obj.increaseX();
<!-- 어떤 객체의 메소드 안에 this가 있으면, 그 this는 '메소드가 호출될 때' 해당 객체를 가리키게 된다.  -->
console.log(obj.x); 
```



### 객체와 배열의 차이

객체는 속성 이름과 속성값이 연결되어 있다. 순서가 X . 배열은 순서가 있다.
배열에 담는 객체는 요소(element) 혹은 항목(item)이라고 부른다. 


.점을 찍고 호출하는 함수를 메소드라고 한다.
  * push메소드: 배열의 오른쪽 끝에 값을 추가한다. 
```js
const arr = [1, 2, 3];

arr.push(4);
arr.push(5);
arr.push(6);
```


  * slice 메소드: 특정 요소부터 한 개 혹은 여러 개의 요소를 지우고 싶을 때 사용
    ex) .slice(index값, 지우고 싶은 요소의 개수);




### 언어와 구동 환경
* 자바스크립트라는 언어와 구동 환경을 나누어서 생각해야 한다.
  - ex) node.js에서는 alert를 쓸 수 X.

* 자바스크립트 언어, 자바스크립트를 돌릴 수 있는 구동환경에는 어떤 기능이 있는지를 배워야 한다.


* 프론트엔드 자바스크립트 개발자 vs 백엔드 자바스크립트 개발자 

  - 프론트엔드 자바스크립트 개발자는 자바스크립트 언어와 **브라우저 구동환경**을 배운다. 
      vs 백엔드 자바스크립트 개발자는 자바스크립트 언어와 **node.js 구동환경**을 배운다.




### ES2015, 그 이후

* ES5 2009년에 나온 자바스크립트 버전.
* ES2015 = ES6




### 값과 리터럴

* 값과 리터럴을 구분할 줄 알아야 한다. 
  - 리터럴: 값의 표기법을 말한다.




### 변수 (Variable)

* let, const, while, for등 프로그래밍에서 특별한 의미를 지니는 단어들을 `키워드`라고 부른다.

* `let`은 ES6에서 도입된 변수이다.
* ES6에서는 `var`를 쓰지 않고, `let`이나 `const`를 사용한다.
* 'best practice: 좋은 관례' 이다.(프로그래밍에서 많이 쓰이는 용어)





### `let` vs `const`
  -  let은 재대입이 가능.
  -  const는 재대입이 불가능한 변수. 
  - **const는 재대입이 불가능하기 때문에 선언과 대입을 동시에 해줘야 한다. let은 선언, 대입을 따로 해도 된다.**
  - const로 변수를 선언할 때는 반드시 선언 시에 값을 대입해주어야 한다. 값 없이 선언만 하게 되면 에러가 발생한다. 또한 추후에 다른 값을 대입할 수 없다.

  - **let을 꼭 써야하는 경우가 아니라면, const를 사용하는 것이 좋다.**
  - let을 사용하면 의도치 않게 다른 값이 대입되어 버리는 일이 생길 수 있기 때문입니다. 정말로 재대입이 필요한 경우에만 let을 사용하는 것이 좋은 습관입니다.

  - 특정 부분을 확신할 수 있으면 나머지 부분을 작성하기 쉬워지기 때문에 왠만하면 항상 const를 쓰는 습관을 들이는 것이 좋다. 


* token은 프로그래밍에서 문자를 의미한다.




###  Error 정리
  - **SyntaxError: Unexpected token (28:7)**
    - 28번째 줄의 7번째 글자에 문법 에러가 있다는 뜻


  - **SyntaxError: Assignment to constant variable: a at 29:0**
    - 29번째 줄의 첫번째 글자에 상수 변수에 대입을 했다는 에러가 있다.
    

    ```js
    let seven = 7;
    let seven = 77;
    ```
  - **SyntaxError: Duplicate declaration "seven" at 33:4**
    - 변수 seven은 중복된 선언이라는 에러이다.**


### 식별자

* 변수의 이름은 `식별자`라고 한다. 식별자는 ('')없이 속성의 이름으로 이용할 수 있다.


* 식별자가 되기 위한 규칙들

  - 숫자, 알파벳, 달러 문자($), 언더스코어(_)가 포함될 수 있다.
  - 단, 숫자로 시작되어서는 안 된다.
  - 예약어는 식별자가 될 수 없다. ex) for, while, function 등은 사용할 수 X.


- 식별자로 쓸 수 없는 단어를 식별자로 사용하고 싶을 때''로 묶는다.
```js
const obj = {
    a: 1,
    '7seven': 7
    <!-- 식별자 규칙에 어긋나는 이름을 사용하려고 하므로 ''로 감싸줘야 에러나지 X -->
}

console.log(obj['7sever']);
<!-- 호출할 때도 ['']로 감싸줘야 한다.  -->
```
- 식별자는 한글로 쓸 수 있지만, 영어로 쓰는 것이 좋다.


### Camel Case
* ex) let helloWorldJavaScript
  - 단어의 첫 글자를 소문자, 그 다음 단어부터 첫 글자를 대문자로 쓴다. 
  - 자바스크립트에서는 Camel Case로 쓰는 게 예의이고 관례이다.

```js
const one = 1;
typeof 1 + 3;
<!-- 결과: 'number' + 3; -->
<!-- typeof 1에 문자열 3이 붙어서 나온 것임. -->
<!-- 연산자 우선순위가 typeof가 +보다 높다. -->
<!-- 연산자 우선순위를 다 외우기가 너무 복잡하므로 우선 연산이 되었으면 하는 부분에 ()로 묶어주는 게 좋다.  -->
typeof (1 + 3);
```

* 변수는 가장 첫 글자를 소문자로, 클래스는 첫 글자를 대문자로 쓰는 게 관례이다.


## number 타입

### number 타입 리터럴

- 리터럴이 다르더라도 값은 같을 수 있다.

- 자바스크립트는 정수와 실수를 별도의 타입으로 다루지 X.

- 정수와 실수 둘 다 number타입으로 구분하지만,
- 정수인지 실수인지 판별하기 위해서는 Number.isInteger를 사용한다. 
- Number.isInteger(정수 or 실수); -> 정수이면 true, 실수이면 false를 반환한다.


### number 타입에 대한 연산

```js
* 2 ** 3; 
// 거듭제곱(거듭제곱 연산자는 ES2018에 추가됨)
```

* cf) 거듭제곱 함수
```js
Math.pow(2, 3);
<!-- 파이썬에서 가져온 함수임. -->
```

* 자바스크립트에서 ==보다는 ===를 쓰는 게 더 좋다.
- 둘 다 되긴 하지만 ===를 쓰는 게 관례다.
```js
1 === '1'
<!--결과값: false -->
1 == '1' 
<!-- 결과값: true 
    타입이 달라도 결과값이 true로 같다고 나오기 때문에 버그가 생기기 쉽다. -->
```

```js
let a = 1;
a++; 
 <!-- 1 증가시키기 **전** 값을 표현식의 결과값으로 반환 -->
++a;
<!-- 1 증가시킨 **후**의 값을 표현식의 결과값으로 반환 -->
```

```js
let b = a++;
<!-- b에 증가하기 **전** 값인 1이 저장됨-->
let b = ++a;
<!-- b에 증가한 **후**의  값인 2가 저장됨-->
```

### 연산자 우선순위

- ()로 묶으면 우선순위가 가장 높기 때문에 가장 먼저 연산된다.
- typeof가 덧셈(+)보다 우선순위가 높기 때문에 +먼저 연산된 뒤에 문자열 3이 붙음.
- ex) typeof 1 + 3;
- 단항 연산자 ex) +1
- 다항 연산자 ex) 3 + 2


### 부동 소수점 (Floating Point) vs 고정 소수점 (Fixed Point)
- 컴퓨터에서 실수를 다루는 2가지 방식
- 부동 소수점 vs 고정 소수점 

- 컴퓨터는 소수도 2진수로 저장하기 때문에 10진수 소수를 정확히 다룰 수 없다.

- 실수를 정확하게 나타내기 위해 사용하는 방법은 고정 소수점이다.
- 커리큘럼에서는 고정 소수점을 사용하는 라이브러리를 사용하지X.

* 컴퓨터로 실수를 다룰 때는 조심해야 한다.
* 컴퓨터는 실수를 정확하게 다룰 수 없기 때문에.


### number 타입의 특이한 값들

#### `NaN`
- `NaN`은 **Not a Number**의 약자이다.
- 계산 불가능한 연산의 결과값을 나타내기 위해 사용한다.

* parseInt('')
  - 문자열을 숫자로 바꿔주는 함수


* parseInt('')에 이상한 문자열을 넣으면 NaN이 결과값으로 나온다. 
  ```js
  parseInt('asdf');
   <!--결과값: NaN -->
  ```
* 어떤 값이 Nan인지 아닌지를 알고 싶을 때, ==를 쓰면 절대 X!!<br> ===를 써야 됨.

**꼭 기억!!**
* ===는 숫자 비교에 특화되어 있는 연산자이다.
* "NaN은 숫자가 아니기 때문에, 어떤 숫자와도 같지 않다."는 규칙이 있다.
* => 즉, NaN은 number 타입인 NaN가 같지 X

* `===NaN`이 들어간 식은<br>무조건 어떤 경우에도 false가 나오는 식임.(NaN은 자기자신과도 같지 X 때문에)
* 이거 때문에 버그 많이 생김.

* NaN은 JavaScript의 값들 중 유일하게 자기 자신과 같지 않은 값
```js
  Number.isNaN(1);
<!-- 결과값: false -->
  Number.isNaN(NaN);
<!-- 결과값: true -->
```

```js
const a = prompt('a: ');
const b = prompt('b: ');
const parsedA = parseInt(a);
const parsedB = parseInt(b);

// 이렇게 하면 안 됩니다!!!
// if (parsedA === NaN || parsedB === NaN) {
//   alert('숫자를 입력해주세요')
// } else {
//   alert(parsedA + parsedB)
// }

// "NaN은 숫자가 아니기 때문에, 어떤 숫자와도 같지 않다." 는 규칙이 있다.
// => 즉, NaN은 number 타입인 NaN과 같지 않다.

if (Number.isNaN(parsedA) || Number.isNaN(parsedB)) {
  alert('숫자를 입력해주세요')
} else {
  alert(parsedA + parsedB)
}

1 + (2 + 3 + (4 + 5));
```




* evaluate(평가)- 표현식을 값으로 반환하는 절차. 계산과 비슷


#### `-0`

* 자바스크립트의 세계에서 그냥 `0`과 `-0`은 다르다.

```js
0 === -0; // true
// 수의 세계에서 0*-1 한 거는 0이기 때문에 true로 나옴


Object.is(0, -0);
<!-- 결과값: false. 자바스크립트 세계에서는 0과 -0을 다르게 취급함.  -->
```
* Object.is(,);
- 수의 세계에서 같은 지, 다른 지를 판별하는 게 x.<br>자바스크립트 상에서 같은지, 다른지를 판별하는 것이다.
* 실무에서는 ===을 제일 많이 사용하는 편임!!

### Infinity
- 어떤 수가 Infinity인지 아닌지를 판별해야 할 때가 있음.
- `Number.isFinite()`: 유한한지 아닌지 판별  
  - 값이 유한하면 `true`, 무한하면 `false`를 반환함.

```js
if (Number.isNaN(parsedA) || Number.isNaN(parsedB)) {
  alert('숫자를 입력해주세요')
} else if (Number.isFinite(parsedA / parsedB)) {
  alert(parsedA / parsedB)
} else {
  alert('0으로 나눌 수 없습니다.')
}
```

* isFinite('1');쓰지 말고, 버전업된 Number.isFinite();를 써라.


### parseInt, parseFloat

* parseInt: 문자열 -> 정수
* parseFloat: 문자열 -> 실수
```js
parseInt('110', 2); // 6 (문자열 '110'을 2진수로 해석하겠다. 문자열을 2진수로 간주한다.)
```
- 되도록 숫자는 숫자랑만 연산한다.
- 문자열을 숫자로 바꾼 후에 연산한다.
- 숫자랑 문자열 연산을 하지 않는다. (아주 간단한 문자열끼리 이어붙이기 정도 빼고는)
- 사용자로부터 입력받은 데이터는 undefined 혹은 문자열일 가능성이 높다.
- 수와 문자열 계산은 **반드시** 전부 다 **숫자로 안전하게 변환한 뒤**에 연산할 것!


### Math 객체

```js
Math.floor(-3.6);
// 더 작은 숫자인 -4가 됨.

Math.trunc(-3.6);
// 더 큰 숫자인 -3이 됨.

Math.max(1, 2);
<!-- 결과값: 2; 
들어온 숫자들 중에 제일 큰 숫자를 반환해준다.
-->
Math.min(1, 2);
<!-- 결과값: 1; 
들어온 숫자들 중에 제일 작은 숫자를 반환해준다.
-->

Math.random(); // 0과 1 사이의 값이 임의로 반환됩니다.
   Math.random() * 10;
   <!-- 0과 10 사이의 실수를 반환함. 10을 넘을 수 X. -->

   Math.floor(Math.random() * 10);
   <!-- 0부터 9까지의 정수가 똑같은 확률로 나오게 만드는 식 -->
```

* 주사위 만들기(1-6까지 나옴)
```js
 Math.ceil(Math.random() * 6);
 Math.floor(Math.random() * 6) + 1;
```   


* 카드 게임(A, B, C 중에 1장 나오는 게임)
```js
const CARDS = ['A', 'B', 'C'];

CARDS[Math.floor(Math.random() * 3)];
```

### number 타입의 메소드
- number 타입은 객체가 아니지만, 마치 객체처럼 메소드를 사용할 수 있다.

- 매개변수 (parameter)

- 코드를 실행하다가 return을 만나면 실행 흐름을 종료시킨다.
```js
function evenOrOdd(x) {
  // 만약 x가 짝수면 'x: 짝수' 라고 출력
  
  if (x%2 === 0) {
    console.log(x + ': 짝수');
  } else {
    console.log(`${x}: 홀수`);
  }
  // 아니면 'x: 홀수'라고 출력 

}


for (let i = 0; i < 20; i++) {
  evenOrOdd(i + 1);
}
`${}` 사이에 어떤 값을 집어넣을 수 있다.
```
