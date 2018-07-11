자료형
======
변수에 저장할 수 있는 값의 종류
------------------------------
### 자료형의 종류
1. ##### Number
    숫자를 나타내는 자료형    
    64bit로 실수와 정수 모두 표현 가능  
    정상적이지 않는 숫자나 표현할 수 없는 범위의 수를 표시하는 NaN, Infinity 
    "1"은 문자열이고 1은 숫자형
    ```js
    var a = 100, b = 3.14, c = 1e-3;
    ```
2. ##### String
    작은 따옴표나('), 큰따옴표(")로 감싸서 문자열을 표현    
    문자열 안에 따옴표, 큰따옴표 등의 문자를 활용 하려면 이스케이프 문자 활용  
    이스케이프 문자 역슬래시(\) 사용 `줄바꿈 \n, 작은 따옴표 \', 큰따옴표 \", 역슬래시 \\`
    ```js
    var a = 'abcde';
    var b = "abcde";
    var c = "abc'de";
    var d = 'abc"de';
    var e = "ab\'c\"de";
    var f = 'ab\'c\"de';
    var g = "\\abcde";
    var h = "abc\nde";
    var i = a+b;
    ```
3. ##### Boolean
    참 거짓
    ```js
    var e = true, f = false;
    ```
4. ##### Object
    Number, String, Boolean의 단순 자료형보다 더 복잡한 자료를 표현할 때 사용    
    객체는 숫자형이나 문자열로 표현할 수 없는 복잡한 값을 관리할 수 있는 데이터타 타입
    + 객체 생성  
    객체는 속성의 집합으로 이루어져 있으며, 속성은 `속성이름:속성값` 형태로 정의  
        - 중괄호 {}를 사용해 정의 가능
        - 각 속성은 이름과 값으로 구성
        - 속성의 값은 모든 자료형이 가능, object 포함
    + 객체 속성 접근
        - 마침표 이용방법
        ```js
        객체이름.속성이름
        object.propertyname
        ```
        - 대괄호 이용방법
        ```js
        객체이름[속성이름]
        object[propertyname]
        ```
    + 객체 속성 값 변경    
    객체 속성에 접근해서 변수에 값을 저장하듯이 사용
    ```js
    object.propertyname = abc;
    object[propertyname] = abc;
    ```