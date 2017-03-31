# promise, rxjs

## ----**promise**

Promise 객체는 비동기 계산을 위해 사용.

Promise는 아직은 아니지만 나중에 완료될 것으로 기대되는 연산을 표현.

[https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Global\_Objects/Promise](https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Global_Objects/Promise)

Promise -&gt;ECMA script6 스펙에 정식 포함



```js
let promise =function(param){new Promise(function(resolve, reject)){
    //비동기 

 window.setTimeout\(function\(\){

 //조건    

 if\(param\){

           resolve\(\);

      }else{

           reject\(\);

      }

 },300\);
 });
}

//프로미스 실행
promise(true).then(callback-성공, callback-실패 );
```



## ----**rxjs**

비동기적, 이벤트 기반의 프로그램을 구성하기 위한 라이브러리의 집합

RxJS는 이벤트 스트림과 데이터를 쉽게 만들고 다룰 수 있도록 도우는 라이브러리다. 복잡하지만 가독성이 좋은 비동기적 코드를 더 쉽게 작성할 수 있도록 도운다.

publish, subscribe방식

[https://hyunseob.github.io/2016/10/09/understanding-reactive-programming-and-rxjs/](https://hyunseob.github.io/2016/10/09/understanding-reactive-programming-and-rxjs/)

[https://xgrommx.github.io/rx-book/why\_rx.html](https://xgrommx.github.io/rx-book/why_rx.html)



```js
//버튼이 클릭될떄마다 실행
// Get stream of button clicksconst btnClickStream =Rx.Observable.fromEvent($addLocationBtn, 'click')
.map(() =>true)
.forEach(val =>console.log('btnClickStream val', val)); //foreach:subscribe -스트림의 구독(subscriber)를 추가 
.debouceTime(300) //시간지연
.distinct() //이전값과 현재값비교등등 의 메소드가 있음.

```









