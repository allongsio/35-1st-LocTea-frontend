<h1>Wecode 35기 1차 프로젝트 - 1팀 LOCTEA</h1>

![스크린샷 2022-07-29 오후 4 58 12](https://user-images.githubusercontent.com/106301980/181713092-f83ac4cb-9098-484a-8afe-7141db81fce7.png)

<h2>사이트 주소</h2>
http://1st-loctea.s3-website.ap-northeast-2.amazonaws.com/
<h2>개요</h2>
<ul>
  <li>오설록 웹페이지 클론코딩 프로젝트</li>
  <li>프로젝트는 2주동안 진행되며, 1주차에는 필수 구현사항 위주로 아래 항목들을 구현하였습니다.
    <ul>
      <li>Nav, Footer</li>
      <li>메인페이지</li>
      <li>상품 목록</li>
      <li>상품 상세</li>
      <li>장바구니</li>
      <li>로그인, 회원가입</li>
    </ul>
  </li>
  <li>2주차에는 추가 구현사항과 코드 리팩토링, 서버 통신 위주로 진행하였습니다.
    <ul>
      <li>주문서 작성</li>
      <li>로그인, 회원가입 시 비밀번호 확인 가능 기능 구현</li>
      <li>라이브러리 사용 없이 슬라이드 구현</li>
      <li>로그아웃</li>
    </ul>
  </li>
</ul><br>

<h2>팀원</h2>
<strong>Front-end</strong><br>
- 김익현, 류승연, 이금관, 최재홍<br>
<strong>Back-end</strong><br>
- 박정용, 조민지, 조예슬<br><br>

<h2>사용한 기술</h2>
<strong>Front-end</strong><br>
- HTML, CSS(SASS), Javascript, React<br>
<strong>Back-end</strong><br>
- Django, Python, JWT, Bcrypt, Miniconda, dbdiagram.io, MySQL, Postman<br>
<strong>Cowork</strong><br>
- Git, Slack, Trello<br><br>

<h2>시연 영상</h2>
https://youtu.be/grWXHlKwkyY<br><br>

<h2>구현 기능</h2>
<ul>
  <li>Nav, Login, Register, Main Banner (이금관)
    <ul>
      <li>Login & Register</li>
      <img src="https://user-images.githubusercontent.com/106301980/182009824-2cedf437-272d-4886-8f97-e26ffee083d6.gif"/>    
      
    - BE와 회원가입 조건을 맞춰 정규표현식을 활용한 유효성 검사가 되는 회원가입 페이지 기능 구현
    - input의 조건이 충족되지 않을 시 조건부 렌더링으로 표시되는 text 추가
    - 비밀번호가 올바르게 작성되었는지 확인할 수 있는 버튼 추가
    - 유저 정보가 올바르게 입력되었는지의 여부에 따른 로그인/회원가입 버튼 활성화
      
</ul>
<ul>
  <li>Nav</li>
  <img src="https://user-images.githubusercontent.com/106301980/182009841-6cd2b753-7aff-4dbb-a1b5-2117134bee88.gif"/>

  
    - BE에서 카테고리 데이터를 받아와 Nav 구현
    - 대분류와 중분류를 정렬하기 위해 이중 map 함수를 적용하여 카테고리 구현
    - 토큰 유무에 따른 로그인 및 로그아웃 액션 변화
    

</ul>
<ul>
  <li>Main Banner</li>
  <img src="https://user-images.githubusercontent.com/106301980/182009888-c9b49c3c-cfac-465c-bbdc-16441f97531c.gif"/>
</ul>

    - 라이브러리를 사용하지 않고 useState를 활용한 메인 이벤트배너 구현
    
  </li>
  
  <li>Item List (최재홍)</li>
  <img src="https://user-images.githubusercontent.com/106301980/182009990-b3f23cb6-9c1d-4bd3-a984-2455ff937824.gif"/>

      
    - 라이브러리를 사용하지 않고 useState를 활용하여 끝단이 있는 carousel 구현
     
  <li>
  <img src="https://files.slack.com/files-pri/TH0U6FBTN-F03R3S4177H/________________________________2022-07-29______________5_19_55_adobeexpress.gif"/>
  
    - 1차 카테고리, 2차 카테고리 선택에 따라 상이한 제품군, 제품리스트 랜더링
    - 제품배열에 대한 탭 활성화 여부로 state변화, 제품 리스트업 순서 변경
    - BE로부터 상이한 제품데이터 획득, 제품 타입에 대한 버튼 클릭에 따라 해당되는 제품들만 선별적으로 호출
    - 랜더링된 개별적 상품에 대해 개별적 아이디 부여하여 클릭에 따라 해당되는 페이지로 이동
    
    
  </li>
  <li>Main Page, Item Detail, Order (김익현)</li>
 <img src="https://user-images.githubusercontent.com/106301980/182010125-0472c645-8db1-4106-884f-9f09abb00b39.gif"/>
      
    - 라이브러리를 사용하지 않고 useState를 활용한 무한 슬라이드 구현
    
 <img src="https://user-images.githubusercontent.com/106301980/182010197-0e3e1619-9bc3-4905-ab85-002cb17e3a02.gif"/>

    
    - 각 조건에 따른 조건부 렌더링을 통해 할인 가격 및 재고 여부에 따른 일시품절, 바로구매/장바구니로 이동 가능한 상품 상세 페이지 구현    
    - 각 input마다 조건을 받아 BE로 전달할 수 있게 구현, 조건에 따른 가격 및 배송비 계산하여 반영
    - Cart 페이지에서 fetch() 함수를 활용하여 BE와 통신 가능하도록 하여 상품 삭제 및 수량 변경 등의 기능을 구현
    
     
  <li>Footer, Cart (류승연)</li>
  <img src="https://user-images.githubusercontent.com/106301980/182009975-0f7ca780-4392-45fa-99aa-318fa59e8b68.gif"/>

      
    - 반복되는 구성에 상수데이터를 활용하여 Component 나누어 구현
    - useState를 활용하여 스크롤 위치를 확인, 부드럽게 스크롤되도록 scrollTop 버튼 구현
    - 서버에서 전달받은 상품리스트를 장바구니에서 보여줌
    - 체크 박스로 원하는 아이템을 선택할 수 있으며 선택된 아이템에 한해 할인율과 배송비를 반영한 결제 예상 금액을 실시간으로 보여줌
    - 선택 삭제를 통한 아이템 삭제 기능 구현, 해당 데이터는 DELETE로 BE와 통신
    - 같은 아이템을 담을 시 수량 변경으로 담기도록 해당 데이터를 PATCH로 BE와 통신

  </li>
</ul>
