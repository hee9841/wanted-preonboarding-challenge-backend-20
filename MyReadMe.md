## 필요한 API
1. 제품 목록 조회
2. 제품 상세 조회
3. 상세페이지에서 구매하기
4. 상세 페이지에서 판매승인하기
5. 구매한 용품 목록 조회
6. 예약중인 용품(내가 구매자/판매자 모두) 목록

## API 따른 제약 사항
1. 제품 목록 조회 (비회원도 가능)
    - 예약 상테 포함
2. 제품 상세 페이지 조회 (비회원도 가능)
   - 예약 상테 포함
   - 회원일 경우
     - 상세 페이지에서 거래 내역 확인 가능하다.
3. 상세페이지에서 구매하기
   - 회원만 가능
   - 판매자는 제외
4. 상세 페이지에서 판매승인하기
   - 판매자가 승인한다.
   - 판매 승인이 완료 되면 거래가 완료된다.
5. 구매한 용품 목록 조회
6. 예약중인 용품(내가 구매자/판매자 모두) 목록 조회

## 조건
1. 제품에는 "제품명", "가격", "예약상태"가 포함함된다.
2. 제품의 상태는 "판매중", "예약중", "완료" 세가지가 존재한다.
3. 구매취소는 고려하지 않는다.a
5. 검증이 필요한 부분에 대해 테스트코드를 작성한다.
6. API에 대한 명세를 작성

## 위의 조건의 따른 테이블 구성
- member
  - id, role, pw
- 제품
  - id, name, price, status, seller_id, content
- 거래
  - id, 제품 id, seller_id, buyer_id

## 프레임
- db h2를 사용해 간단히 구성
- 