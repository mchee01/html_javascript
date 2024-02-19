## form - 사용자 입력 양식을 만든다
	- 서버에게 전송 제출(submit)
	- 주요 속성 : action은 서버의 url, method
	- 자식 요소는 입력요소를 갖습니다.

## 입력 요소
	- input : type에 따라 여려가지 모양이 만들어집니다.
	- select : 자식요소로 option 태그를 갖습니다.
	- button : type은 submit 또는 button
		: form 태그 안에 있으면 기본 타입 submit
		: 	   밖에		       button


- 입력요소가 form 태그로 서버에 제출할때 꼭 필요한 속성은? name (변수처럼 식별자)
- 사용자가 입력하거나 선택한 값을 저장하는 속성은 ? value


## 자바스크립트
- 실행 환경은 브라우저(컴파일은 브라우저의 엔진 (예시. 크롬 V8)이 합니다.)
- node.js 라이브러리는 JS로 서버단의 개발을 할수 있도록 하며 실행환경을 브라우저 밖으로 바꿉니다.
- 주요 객체 생각나는것, 제일 많이 쓴것 ? document
- document 객체의 제일 많이 사용한 메소드? getElementById ( id 값으로 요소를 가져온다.)
	=> 실행결과 <시작태그><내용</종료태그> 와 같은 하나의 요소를 가져옵니다.
- JS로 사이트를 동적으로 보이게 만든 예시 ? 속성, 스타일, 내용(innerHTML)
- 동적으로 사이트가 변화되게 사용자가 이벤트를 발생시킵니다.
	=> 이벤트 : click, drag drop, change, resize(윈도우 창 사이즈가 바뀌는 이벤트) 등등..
- 태그요소의 이벤트 속성: onXXXXX 의 값은 자바스크립트코드 1개 또는 함수
- JS의 상수 : const, 변수 : let (참고 var은 지역변수의 개념이 불명확.)
- 제어문: if, switchm for는 자바와 동일하게 사용합니다.

- 함수 정의(선언) 키워드 : function, 리턴값은 return 키워드 사용합니다.

- 각자 조사하기 : 자바 스크립트 for 에 추가된 형식
    - for(..in 배열), for(..of 배열)형식 조사
    - for (...of 배열) -> 배열 요소를 반복자가 순회
    - for (...in + 배열) -> 배열의 속성을 반복자가 순회
## ``백틱
### 자바스크립트는 템프릿 리터럴(멀티라인 문자열, 표현식) 기능이 있습니다. ``(백틱) 기호 사용.
## 요소의 집합을 다루는 메소드를 알아보자. 
 getElementById는 요소를 1개만 가져옴.
 getElementByxxxx 중에 요소를 여러개 가져오는 메소드 1) 태그이름 2)클래스이름
 ```javascript
 const lis document = document.getElementByTagName('li');
 console.log(lis);
 ```
 주의할 점 : lis 는 `<li>`요소의 집합. 배열이 아니고 Collection 임. 따라서, forEadch를 사용하려면 배열로 변환해야 함.<br>
```javascript
const liArr = Array.form(lis);
liArr.forEach((item) => document.write(`li 요소 내용 =${item.innerHtml}`))
```
    document
```html
<pre style="font-size: 1rem;font-family: inherit;"></pre>
```

pre 태그 : 

```javascript
const trOne = document.querySelector('tr')
// document에서도 존재하지만 querySelector는 나중에 후술할 NoSql(mongodb, sqllite 등) 에서도 쿼리를 조회하는 용도로 사용됨
const tr2 = document.querySelector('tr:last-child')
const newtd2 = document.createElement("td")
newtd2.innerHTML = '테스트2'
tr2.appendChild(newtd2)
```
getElementById 또는 querySelector 메소드 선택은 취향.