.env는 깃에 올라가는 파일'
.env.local은 깃에 올라가지 않는 파일

환경변수를 추가하고 싶다면 꼭 REACT_APP로 시작해야함

p.c가 받는 데이터의 구조가 서버의 데이터 구조는 상관이 없어야 한다.
- 재서용허기 힘들어짐
p.c의 데이터 구조는 최대한 간단해야 재사용하기 쉽다
README.md에 주소 설계한 것 적기
/홈
/product/1 상품정보

ESLint에서 alt생략하면 초록줄 뜨는 에러가 있으므로 img에 alt 적어주기

match

일일히 콘솔로그 찍는것보단 
React 개발자 꼭 켜고 개발할 것

속도를 빠르게 하려면-> 서버와 통신할 때, 요청 횟수를 줄이는 게 프론트엔드 최적화의 관건


수량 입력 필드를 만들어서, 옵션이나 수량이 변경
뭐가 선택되었는지 UI상태는  p.c에 둔다


그 UI에 대한 상태라면, p.c에 둬도 된다
- 외부 세계와의 연동을 위한 상태는 Container

select, input태그는 내가 숫자를 넣어뒀더라도, 가져올 때는 문자열로 가져와짐. 숫자로 만들려면, parseInt 해야함

상태에 이상한 값이 들어있으면(옵션이 선택되었지 않거나) -> 수량이나 옵션을 확인해달라는 경고창 띄우기


- react에서는 selected를 사용하지 않는 것이 좋다. defaultValue나 value를 사용하는 것을 권장 
- option의 value= 빈문자열""을 넣으면, 초기상태에 빈문자열을 넣어 놓는다. -> 강제로 선택되도록 만듦

- value prop에 실수로 null이 넘어가면 안된다. null이 넘어가면, 제어되지 않는 컴포넌트가 됨
- 제어되는 컴포넌트를 만들려면 -> null값이 넘어가면 안된다.

옵션을 바꿨을 때, 수량을 1로 바꾸고 싶다

Redirect 컴포넌트를 호출하는 것만으로도 주소표시줄의 상태가 바뀌는 부작용이 생긴다

React의 핵심은 언제 다시 그려질지, 언제 그려지지 않을 지를 구분할 줄 알아야 한다.

**Provider에서 내려주는 값이 바뀔 때마다 화면이 다시 그려진다.**

- 엘리먼트 타입이나 key가 바뀌면 상태가 날아간다 -> 상태가 초기화되서 화면이 새로 그려진다

