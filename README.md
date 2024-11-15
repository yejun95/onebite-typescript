# 인프런 한입 크기로 잘라 먹는 타입스크립트 강의 정리
## ✔️ section1 directory
- `npm i @types/node` : node.js의 내장 기능들을 위한 타입 정보를 제공

- `npm i typescript -g` : typesciprt 컴파일러
  - `tsc --init` : 타입스크립트 컴파일러 옵션 -> tsconfig.json 생성됨
<br>

- tsconfig.json 설정
<br>
<hr>
<br>

## ✔️ section2 directory
### 원시 타입
- 하나의 값만 저장하는 타입
  - 타입 어노테이션 : ex) `let a: number = 1;` 이라고 하였을 때, :(콜론)뒤에 붙는 타입을 타입 주석 또는 타입 어노테이션이라고 한다.

- number

- string

- boolean

- null

- undefined

- 리터럴 타입
<br>
<br>

### 배열과 튜플
- 배열 타입

- 튜플 타입 : 길이와 타입이 고정된 배열
<br>
<br>

### 객체
- Optional

- readonly
<br>
<br>

### 타입 별칭과 인덱스 시그니처
- 타입 별칭 : 객체 선언 시 변수 객체를 통해 할당하는 것

- 인덱스 시그니처 : 동일한 형식의 `key : value`로 값이 계속 추가 된다면 사용하기 용이함
<br>
<br>

### enum
- enum 타입 등록을 통해 열거된 변수를 프로퍼티나 변수에 할당 가능
<br>
<br>

### any, unknown
- any : 특정 변수의 타입을 우리가 확실히 모를 때 사용
  - 다른 타입에 다 넣을 수 있다.
  - 그러나 마지막 타입이 불일치하면 런타임시에 에러가 남
  - 고로 최대한 사용하지 말아야한다.
<br>

- unknown : any와 마찬가지로 어떤 타입이든 넣을 수 있음
  - 그러나 any와 다르게 다른 타입에 넣기 불가능 => 컴파일 시점에 에러를 잡을 수 있음
  - 만약 타입을 모른다면 any말고 unknown을 쓰도록 하자.
<br>
<br>

### void, Never
- void : 공허 -> 아무것도 없다. -> 아무것도 없는 타입
  - 함수에 리턴문이 없을 경우 사용 -> ex) console.log만 찍는 경우
  - undefined를 제외 하고는 모든 타입 매핑이 불가능
  - `tsconfig`에서 `strictNullChecks = false` 인 경우 null 값 매핑 가능
<br>

- never : 존재하지 않는 -> 불가능한 타입
  - `while(true)` 처럼 무한루프일 경우에 사용
  - 또는 함수가 `throw new Error` 처럼 예외 처리를 리턴하는 경우 사용
  - void와 다르게 모든 타입에 대해서 매핑이 불가능하다.
