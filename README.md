# api_test
DB에 쓰이는 데이터 중 OPEN API에서 불러오는 것들을 구현한 코드입니다.

## 금융상품 정보 (Product)
1. 채권 관련<br>
   bond_list: 채권 상품 리스트 (금융위원회)<br>
   bond_list_price: 채권 시세 정보 (금융위원회)<br>
2. 코인 관련 (빗썸 API)<br>
   coin_list: 코인 종목 정보<br>
   coin_list_price: 코인 종목 가격<br>
   coin_price: 코인 종목 가격<br>
3. 예금/적금<br>
  deposite_list: 정기예금 상품 (금융감독원)<br>
  saving_list: 적금 상품 (금융감독원)<br>
4. 주식 관련<br>
  stock_list: 유가증권 종목 리스트 (한국거래소)<br>
  stock_price: 유가증권 가격 정보 (금융위원회)<br>
  stock_list_price: 유가증권 가격 정보 (금융위원회)<br>

## 개인 자산 정보 (Asset)<br>
1. stock: 개인 주식 자산 (한국투자증권 private API)<br>
2. coin: 개인 코인 자산 (빗썸 private API)<br>

<br><br>
* 모든 데이터는 JSON 형태로 받아와서 전처리 후 해당 테이블에 저장되는 방식으로 구현되었습니다.<br>
* 1,000건이 넘어 오래 걸리는 것들에 한해서 멀티 스래드를 사용했습니다.
