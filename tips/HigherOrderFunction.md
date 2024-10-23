1. 고차 함수의 정의
   고차 함수는 함수를 인자로 받거나 함수를 반환하는 함수입니다.

2. 함수를 인자로 받는 고차 함수 예시:

```javascript
function higherOrderFunction(callback) {
  console.log("고차 함수 실행");
  callback();
}

function callbackFunction() {
  console.log("콜백 함수 실행");
}

higherOrderFunction(callbackFunction);
// 출력:
// 고차 함수 실행
// 콜백 함수 실행
```

3. 함수를 반환하는 고차 함수 예시:

```javascript
function multiplyBy(factor) {
  return function(number) {
    return number * factor;
  }
}

const double = multiplyBy(2);
console.log(double(5)); // 출력: 10
```

4. Array 메소드를 이용한 고차 함수 예시:

   a. map:
   ```javascript
   const numbers = [1, 2, 3, 4, 5];
   const doubled = numbers.map(num => num * 2);
   console.log(doubled); // 출력: [2, 4, 6, 8, 10]
   ```

   b. filter:
   ```javascript
   const numbers = [1, 2, 3, 4, 5];
   const evenNumbers = numbers.filter(num => num % 2 === 0);
   console.log(evenNumbers); // 출력: [2, 4]
   ```

   c. reduce:
   ```javascript
   const numbers = [1, 2, 3, 4, 5];
   const sum = numbers.reduce((acc, cur) => acc + cur, 0);
   console.log(sum); // 출력: 15
   ```

5. 고차 함수의 장점:
   - 코드 재사용성 향상
   - 추상화 수준 증가
   - 함수형 프로그래밍 패러다임 지원

6. 실제 사용 예시 (이벤트 리스너):

```javascript
function addEventListener(eventType, handler) {
  // 이벤트 발생 시 handler 함수 실행
}

addEventListener('click', function() {
  console.log('버튼이 클릭되었습니다.');
});
```

이러한 고차 함수의 개념과 사용법을 이해하면, 더 유연하고 재사용 가능한 코드를 작성할 수 있습니다. 또한 함수형 프로그래밍의 기초를 다지는 데 도움이 됩니다.