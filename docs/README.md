# 프리코스 1주차 - 숫자 야구 게임 ⚾

## 🕹️ 작동 결과




## 💁‍♂️ 기능 목록

* [ ] **사용자 입력값 유효성 체크 기능**

  * [ ] 자동차 이름 유효성 체크

    🚨 체크 리스트

    * [ ] 쉼표로 구분하여 자동차 이름을 **여러개** 입력하였는가?
    * [ ] 각각의 자동차 이름을 5자 이하로 입력하였는가?
    * [ ] 사용자가 자동차의 이름을 빈칸을 입력하지 않았는가?

  * [ ] 시도할 횟수 유효성 체크

    🚨 체크 리스트

    * [ ] 사용자가 빈칸을 입력하지 않았는가?
    * [ ] 숫자만 입력하였는가?

* [ ] **사용자의 입력값 유효성 체크 결과 처리**

  * [ ] 성공 시 입력란 비활성화 처리
  * [ ] 실패 시 `alert`를 통한 실패 사유 출력과 `input` 엘리먼트 포커스 처리

* [ ] **각 자동차의 상태 정보를 관리하는 클래스 구현**

  * [ ] **`MissionUtils`를 활용하여 **0에서 9 사이의 무작위 값을 구한 후 **전진 유무를 확인**
  * [ ] 자동차의 이동 시도 요청
  * [ ] 자동차의 이동 결과 반환

* [ ] **레이싱 게임의 데이터와 결과를 관리하여 주는 모델 구현**

* [ ] **회차별 자동차들의 전진 상태를 보여주는 엘리먼트를 작성하여 주는 기능**

* [ ] **자동차 경주 게임에서 최종 우승한 자동차를 판별**

* [ ] **자동차 경주 게임을 통해 최종 우승한 자동차 이름을 `String`형으로 반환**

## 📁 디렉토리 구조





## 🎯 기능 요구사항 체크

- [ ] 주어진 횟수 동안 n 대의 자동차는 전진 또는 멈출 수 있다.
- [ ] 자동차에 이름을 부여할 수 있다. 전진하는 자동차를 출력할 때 자동차 이름을 같이 출력한다.
- [ ] 자동차 이름은 쉼표(,)를 기준으로 구분하며 이름은 5자 이하만 가능하다.
- [ ] 사용자는 몇 번의 이동을 할 것인지를 입력할 수 있어야 한다.
- [ ] 전진하는 조건은 0에서 9 사이에서 무작위 값을 구한 후 무작위 값이 4 이상일 경우이다.
- [ ] 자동차 경주 게임을 완료한 후 누가 우승했는지를 알려준다. 우승자는 한 명 이상일 수 있다.
- [ ] 우승자가 여러 명일 경우 쉼표(,)를 이용하여 구분한다.
- [ ] 사용자가 잘못된 입력 값을 작성한 경우 `alert`을 이용해 메시지를 보여주고, 다시 입력할 수 있게 한다.



## ✅ 프로그래밍 요구사항 체크

- [ ] 주어진 `index.html`에 html 엘리먼트를 직접 추가하거나 기존의 html 엘리먼트를 임의로 삭제하지 않는다. id와 같은 선택자를 추가하는 작업만 가능하다.
- [ ] 다음과 같이 Car 객체를 만들고, new 를 이용해 인스턴스를 만들어 사용한다.

```javascript
function Car(name) {
  this.name = name;
}

class Car {
  constructor(name) {
    this.name = name;
  }
}
```

### DOM 선택자

- [ ] 자동차의 이름을 입력하는 input 태그는 `car-names-input` id값을 가진다.
- [ ] 자동차의 이름을 제출하는 button 태그는 `car-names-submit` id값을 가진다.
- [ ] 레이싱 횟수를 입력하는 input 태그는 `racing-count-input` id값을 가진다.
- [ ] 레이싱 횟수을 제출하는 button 태그는 `racing-count-submit` id값을 가진다.
- [ ] 최종 우승자를 출력하는 span 태그는 `racing-winners` id값을 가진다.

### 라이브러리

- [ ] 전진하는 조건을 판단하기 위한 랜덤 값은 [`MissionUtils` 라이브러리](https://github.com/woowacourse-projects/javascript-mission-utils#mission-utils)의 `Random.pickNumberInRange`를 사용해 구한다.

### 공통 요구사항

- [ ] 외부 라이브러리(jQuery, Lodash 등)를 사용하지 않고, 순수 Vanilla JS로만 구현한다.
- [ ] **자바스크립트 코드 컨벤션을 지키면서 프로그래밍** 한다. 정답이 없으므로, 다양한 컨벤션을 비교해보며 스스로 더 적절해보이는 컨벤션을 자율적으로 선택한다.
- [ ] **indent(인덴트, 들여쓰기) depth를 3이 넘지 않도록 구현한다. 2까지만 허용**한다.
- [ ] **함수(또는 메소드)가 한 가지 일만 하도록 최대한 작게** 만들어라.
- [ ] 변수 선언시 `var` 를 사용하지 않는다. `const` 와 `let` 을 사용한다.
- [ ] `import` 문을 이용해 스크립트를 모듈화하고 불러올 수 있게 만든다.
- [ ] **함수(또는 메소드)의 길이가 15라인을 넘어가지 않도록 구현한다.**

### 과제 진행 요구사항

- [ ] **기능을 구현하기 전에 구현할 기능 목록을 정리해 javascript-racingcar-precourse/docs/README.md 파일에** 추가한다.
- [ ] **git의 commit 단위는 앞 단계에서 README.md 파일에 정리한 기능 목록 단위로 추가**한다.



## 📚 테스트 결과





## ✍️ 작성자

* 우아한테크코스 프론트엔드 과정 지원자, **류현승**
