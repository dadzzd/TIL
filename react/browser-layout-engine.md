# 브라우저 레이아웃 엔진
#### DOM(Documeny Object Model)
* 객체를 통해서 구조화된 문서를 표현하는 방법
* xml 또는 html로 작성
* 트리형태로 되어있어서, 원하는 곳에 특정 노드를 추가하거나 삭제 할 수 있다
 DOM의 문제점
* 자체적으로 동적 ui에 최적화가 되어 있지 않다
* 데이터가 많아 지면 하나하나 관리가 어려워 진다
* 관리를 못하면 버퍼링(렉)이 발생한다
#### Repaint & Reflow
* Repaint
    * 색상의 변경 등 다시 그려야 하는 상황
* Reflow
    * 사이즈 또는 위치의 변경 등 레이아웃이 바뀌는 상황
```javascript
var style = document.body.style; // 캐싱
style.padding = "20px"; // reflow, repaint
style.border = "10px solid red"; // reflow, repaint

style.color = "blue"; // repaint (레이아웃이 변경되진 않았기 때문에 reflow 안함)
style.backgroundColor - "#ffa"; // repaint

style.fontSize = "1em"; // reflow, repaint

// reflow, repaint
document.body.appendChild(document.createTextNode('hello world!'));
```
#### Batched DOM Updates
* 변화를 그때그때 매번 연산하는게 아닌, 한꺼번에 연산을 하는 기법 위에 코드와 같은 상황일 경우
실제로는 1회의 reflow 와 repaint가 실행 된다 문제는...
#### Forced Reflow
```html
<body>
    <div><divclass="block"id="one">눌러봐요!</div>
    <div><divclass="block"id="two">눌러봐요!</div>
    <script>
        var one =document.getElementById('one');
        var two =document.getElementById('two');
        one.onclick= () !=> {
            one.style.background ='red'
            one.style.padding ='0.5rem';
            one.style.margin ='100`px'
            one.style.height ='100px';
            // one reflow, one repaint
        }
        two.onclick= () !=> {  
            two.style.background ='red'
            two.style.padding ='0.5rem';
            console.log(one.offsetHeight);
            two.style.margin ='100px';
            console.log(one.clientHeight);
            two.style.height ='100px';
            // three reflows, one repaint
        }
    </script>
</body>
```
* https://gist.github.com/paulirish/5d52fb081b3570c81e3a
    
