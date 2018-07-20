DOM
===
> Document Object Model
### DOM 이란?
+ 컴퓨터가 문서를 잘 처리할 수 있도록 문서의 구조를 약속한 문서 객체 모델
    - Tree 형태를 따름, 족보나 가계도와 비슷함
#### Document Object
+ JavaScript에서 `document`로 접근 가능
    - children에는 문서의 최상위 엘리먼트인 html이 존재
### Element API
+ .innerHTML : 엘리먼트 안의 HTML 코드 변경
+ .innerText : 엘리먼트 안의 텍스트 변경
+ .style : CSS 변경
+ .getAttribute
    - element의 속성 값을 반환
    - 하나의 attribute 매개변수 필요
    - 직접 객체에 동기화 되지 않는 속성에 대해서도 접근 가능
+ .setAttribute
    - element의 속성 값을 설정
    - 두개의 attribute 매개변수 필요 이름, 설정할 속성의 값
    - 직접 객체에 동기화 되지 않는 속성에 대해서도 설정 가능
#### 자식, 부모 엘리먼트에 접근하는 방법
+ .children : 해당 object의 자식 노드에 대한 배열
+ .parentNode : 부모 노드
+ .firstElementChild : 첫 자식 엘리먼트
+ .lastElementChild : 마지막 자식 엘리먼트
#### 같은 레벨의 형제 엘리먼트에 접근하는 방법
+ .nextElementSibling
+ .previousElementSibling
### Document API
+ document.getElementByTg : 단일 엘리먼트를 선택하는 메소드
+ document.getElementsBy~ : 다중 엘리먼트를 선택하는 메소드
+ document.getElementById : 인자로 html element 태그의 id를 전달하면 해달 엘리먼트가 반환