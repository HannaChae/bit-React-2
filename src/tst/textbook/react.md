챕터
p.19
서버 사이드 언어가 주관했던 시대-스프링 MVC
디자이너와 개발자 중간 프론트
nodejs를 이용한 서버 사이드 구현
server는 data의 제공
p.20
모던과 레거시
p.22
css 문제점 - 취약한 이유 모두 전역 범위이다
JS: var 이것이 전역개념이어서 ... ES6에서는
var -> const, let 지역개념으로 전환
p.24, p.25
제이쿼리 라이브러리 등장
리액트란? 페이스북에서 개발한 라이브러리
자바스크립트에서 발생하는 문제를 줄일 수 있다.
선언적이다-declare(js는 클래스가 없음)
component 기반(계속 작게 쪼개는 이유 - 서로 연결하는 route가 필요)
구성요소를 부품(atom) 단위로
p.33
상태를 철저히 관리(redux)
그림 2-2 vr
권장표준 ES6
바닐라스크립트(제이쿼리는바닐라가아님)
p.36
에크마(자바스크립트보다는제품명으로얘기함)는 표준권고사항이다.
const에는 값을 대입할 수 없기 때문에 상수 정의한다.
p.38
p.40
$:템플릿 리터럴 이용한 코드
p.42
구조분해 할당을 이용한 데이터 일괄처리
npm이라 불리는 패키지 관리 시스템으로 이용한다
전부 nodejs 기반이라는 것
p.48
역할 package.json
JRE와 JDK
바벨에서 사용하는 라이브러리
p.49
-S 
하나하나 하지 않고 package.json에 넣고 npm install로 한번에
팀원들과 공유
p.58
jsx란 확장(extands) 
jsx를 이용하면
p.63
return해서 던지는 것
transfile 방법
트랜스파일이란 특정 프로그램언어를 다른 프로그램언어로 변환하는 방법(ex.바벨)
바벨이란 term 알아놓기
p.65
npm을 이용하여 command line interface
https://blog.cometkim.kr/posts/start-modern-javascript-with-babel/=
p.70
바벨을 실행하는 명령을 입력합니다
p.71
리액트 작성방법
component
render
엔트리포인트(export default)
p.76
render 와 return type
유닉스 철학을 염두에 두어라
p.77
클래스형 선언
p.78
함수형
functional componenet
react - functional componenet,
js - functional interface로 바뀌는 추세
props는 component 속성
(자바에서는 parameter)
p.80 그림 props
p.81
p.83
두번째 줄 프론트 data.map
p.84
밑에서 세번째 줄 배열로 전달받은 props에 의해서
map method를 실행하여 반환
$.each(arr, (i,j)=>{}) ajax 방식
props.data.map( (i,j) => { {i} {j} } )
p.85
props.childeren
p.88
props vs state
props는 변하지 않는 객체이다 := constant
state는 변경 가능한 객체이다 := (variable  ->) mutable
let a = ''
p.89
class this.state
컴포넌트가 (자체적으로 보관하는 this.state => class 기반 리액트시절
(redux가 보관하는 state) 가 있기 때문에
별도의 props를 전달하지 않아도 date 전송이 가능하다.
p.92
p.94
on~으로 바뀌는게 state
p.98
p.99 key 목록
props.data.map(i, j) => return <key={data.id}><>
p.100
mount는 상태의 CRUD 이다
unmount
마운트 개념 : no event일 때
p.102
component update 값을 변환하지 않는
p.103
https://reactjs.org/docs/hooks-faq.html#gatsby-focus-wrapper
componentWillMount hook (Hook: lifeCycle methode, lifeCycle: state CRUD)
componentDidMount
componentWillReceiveMount
...
useEffect(() => { // componentDidMount
    //Your code here
    }, []);
p.104
단순한 스크립트 = 바닐라 스크립트 (제이쿼리 등등)
외부 cdn에 의존하게 됨
p.105
@ 없는 건 쓰지 않는다??
p.108
material 디자인
material ui
atomic 디자인
p.109
페이지 단위로 목업(옛날 방식 jsp)
p.114
page vs component
차이점은 data의 유무
있으면 page 없으면 component
목업이라고 불리는 상태를 만든다
p.115
p.118
p.120
p.127 
밑에서 네번째 줄
맹목적인 anti pattern을 피하는게 좋다
https://wikidocs.net/597
https://rapidapi.com/collection/airport
airport json data
https://raw.githubusercontent.com/mwgg/Airports/master/airports.json
덕 타이핑
덕 타이핑으로 처리하면 term을 줌으로써 면죄부가 된다?
p.287 리덕스
p.292 flux는 흐름(stream)
java - stream
js - flux
p.293
flux에서 store/action/dispath
Action은 필요에 따라 해당 시점(이벤트 + 마운트 )에서
데이터의 흐름(flux)이 시작됩니다.
store에서 인식할 수 있는 type을 가집니다.
flux 데이터 흐름은 관리할 수 있는 하나의 방법이지만 만능은 아니다.
p.295
리덕스는 flux를 기반으로 단방향으로 상태를 구현하는 라이브러리
리액트 자체의 기본구조는 props를 전달하는 것이 기본구조
네번쨰 줄 액션은 간단한 객체다.({type: ...})
자바스크립트의 객체는 json
상태 객체와 액션 객체를 연결시켜주는 것이 reducer
상태(state) 객체, {}
{} - function<P,R> - {type: '', ...}
state - reducer - action
function({type:...,}){return {state} } // reducer 
p.300 리덕스의 3원칙
single source - state
const action - action
pure function : param ok, return ok
디바운스 https://webclub.tistory.com/607
p.306
밑에서 네번째 줄
p.313
npm i -D throttle-debounce
npm i -D react-redux redux
p.319
p.295
리덕스는 플럭스(흐름)
p.296
플럭스는 내장된 스트림 자바는 스트림화시키는건데
내부의 흐름구조를 만듦
p.297