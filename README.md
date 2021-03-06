GRAPE, 블록체인 기반 티켓팅 플랫폼
===
GRAPE는 티켓팅을 할 때 포도알이라 불리우는 좌석을 어떻게 하면 공정하게 판매할 수 있을까? 라는 물음에서 생겨난 플랫폼입니다. 

 GRAPE를 통해 티켓 판매자와 구매자 사이 수수료를 줄일 수 있습니다. 또한 기존 중계만 하던 티켓팅 플랫폼이 아닌 불법적인 거래를 BlockChain 기술을 이용하여 미연에 방지되게끔 하려합니다.


목적
---
 - 불법적인 티켓 거래를 막아 문화 의식을 지킵니다.
 - 티켓 판매자와 구매자 사이 중간 과정을 최대한 줄일 수 있습니다.

문제점
---
최근 많은 사람들이 자신이 좋아하는 연예인의 콘서트, 공연등의 티켓을 구매하게 되며 문화 사업이 굉장히 증진하고 있습니다. 티켓팅 서비스는 많은 방법을 통해 불법적인 티켓팅을 막으려 노력하지만 여전히 **불법 거래가 왕성하게 이루어지고 있습니다.**

대표적으로 되팔램, 양도, 플미등으로 불리워지는 불법 티켓 거래는 정당하게 티켓을 구매하는 사람들에게 상대적으로 **박탈감**을 주게됩니다. 또한 문화 시민 의식이 하락되어 **불법적인 거래가 당연하게끔 되는 악영향**을 끼치게됩니다.

그렇기에 GRAPE는 불법 거래를 방지하기 위하여 **블록체인**을 도입하였습니다.

솔루션
---
불법거래를 방지하기 위해서는 확실한 본인인증이 필요하다고 판단하였습니다.
그렇기에 티켓을 구매한 내역을 블록체인 상에 올려 티켓 그 자체가 영수증이 되면서 누가 샀는지 확인할 수 있습니다.

티켓 **거래시 나오는 해시값**과 사용자의 **지갑 주소**를 **QR코드**로 만들어 티켓을 확인시 QR코드를 2번 찍어 불법 거래한 티켓인지 간단히 확인할 수 있습니다.

기능
---
<img width="859" alt="2018-08-13 10 51 16" src="https://user-images.githubusercontent.com/28648915/44035864-7111fbd4-9f4b-11e8-8bd4-d2eb58aaba83.png">

1. 회원가입
  - 서버에 회원가입 요청을 보내면 서버는 사용자에게 지갑을 만들어 주며 DB에는 사용자의 지갑 주소와 아이디, 비밀번호가 있다.

2. 로그인
 - 서버에서 로그인을 처리한다

3. 원하는 자리 선택
 - 사용자가 원하는 자리를 선택하고 확인 버튼을 누르면 그 자리는 다른 사람이 선택 불가능 하게끔 된다. (소켓 통신 사용)

4. 토큰 충전
 - 1GRP = 1000원으로 미리 포인트처럼 충전할 수 있다. 사용자의 지갑으로 충전됨
 - from : 서버
 - to : BlockChain

5. 티켓 결제
  - 부족한 GRP를 충전 후 티켓을 결제 할 수 있다.
  - 결제 후 분배
  - from : Smart Contract
  - to : 티켓 판매자
  - to : 서버 이용 수수료

6. 티켓 확인
  - 티켓의 QR코드와 사용자의 지갑 주소의 QR코드를 출력합니다.
  - 티켓의 구매자 주소와 사용자 지갑 주소와 동일하면 입장이 가능합니다.
  - 티켓 사용유무가 True로 바뀝니다.
   - from : 티켓 판매자
 - to : BlockChain

7. 티켓 취소
  - 티켓을 취소할 수 있습니다. 티켓의 환불 유무를 True로 바꿉니다.
 - from : 사용자
 - to : BlockChain