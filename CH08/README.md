# 08장 제어문

### switch 문과 break 문을 생략한 폴스루

```jsx
// 예제 08-09

var year = 2000; // 2000년은 윤년으로 2월이 29일이다.
var month = 2;
var days = 0;

switch (month) {
  case 1: case 3: case 5: case 7: case 8: case 10: case 12:
    days = 31;
    break;
  case 4: case 6: case 9: case 11:
    days = 30;
    break;
  case 2:
    // 윤년 계산 알고리즘
    // 1. 연도가 4로 나누어떨어지는 해(2000, 2004, 2008, 2012, 2016, 2020...)는 윤년이다.
    // 2. 연도가 4로 나누어떨어지더라도 연도가 100으로 나누어떨어지는 해(2000, 2100, 2200...)는 평년이다.
    // 3. 연도가 400으로 나누어떨어지는 해(2000, 2400, 2800...)는 윤년이다.
    days = ((year % 4 === 0 && year % 100 !== 0) || (year % 400 === 0)) ? 29 : 28;
    break;
  default:
    console.log('Invalid month');
}

console.log(days); // 29
```

`switch` 문은 `case`, `default`, `break` 등 다양한 키워드를 사용해야 하고 폴스루가 발생하는 등 문법도 복잡하다.

만약, `if … else` 문으로 해결할 수 있다면 `switch` 문보다 `if … else` 문을 사용하는 편이 좋다. 하지만 조건이 너무 많아서 `if … else` 문보다 `switch` 문을 사용했을 때 가독성이 더 좋다면 `switch` 문을 사용하는 편이 좋다.

### 이 부분도 내가 공부하기에는 쉬운 부분이라 과감하게 넘겼음

### 차후에 완전하게 정리하겠음