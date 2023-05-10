# 4Week_LeeSangSu.md

## Title: [4Week] 이상수

### 미션 요구사항 분석 & 체크리스트

---

- [ ] **필수 미션**
  - [ ] 네이버 클라우드 플랫폼을 통한 배포,도메인,HTTPS까지
  - [x] 호감리스트 성별필터링기능 구현
- [ ] **선택 미션**


### 4주차 미션 요약

---
**[접근 방법]**

1. 호감리스트 성별필터링기능
https://localhost/usr/likeablePerson/toList?gender=M&attractiveTypeCode=&sortCode=1
해당 링크의 gender를 매핑하는게 중요할 듯
likeablePerson/toList - likeableController 부터 체크
if(gender)의 조건에 W와 M에 따른 각 성별에 따른 리스트를 갖도록 로직변경
stream().filter.equals()를 활용해서 특정 성별을 필터링 -> 리스트 출력
2. 네이버 클라우드 배포
네이버 클라우드에 CentOS7.8버전으로 생성 후 java, 도커, sql등등 설치 후에 배포!
**[특이사항]**

어떻게 필터를 걸어야 할지 고민을 했는데 멘토님께 힌트를 받아서 일부 해결
로직을 제대로 이해하지 못해서 발생한 문제였다.
멘토님의 힌트에 도움받아 stream().filter().equals()를 통해서 하나의 성별을 필터해서 걸 수 있었다.
조건문의 else를 최대한 활용하지 않으며 직관성 향상에 신경썼다

네이버 클라우드 배포하는 부분은 필수미션1을 해결하기 위해 NotProd 부분을 수정해서 체크했었는데 
이 때문에 리눅스에서 Test Build할 때 문제가 생기게 되어 실패하는 상황이 있었다.
