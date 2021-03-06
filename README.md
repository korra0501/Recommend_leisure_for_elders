# 어르신 여가활동 추천 서비스 '동행'
## <서울시 거주 노인분들을 위한 여가, 복지, 교육 추천시스템>
#### 홈페이지 주소: www.dhelders.com
#### Readme in other languages: [Japanese](/README_jp.md)
![Main Page](/mainpage.jpg)
#### 문제제기
- 서울시 노인 사회활동 참가 통계에 의하면, 특별한 사회활동이 없는 노인들이 약 35%를 차지한다. 현재 독거노인의 고독사 또한 문제가 되고있을만큼 고독한 삶을 보내고 있는 노인이 많지만, 개개인의 상황에 맞추어 여가, 복지, 교육 프로그램을 추천해주는 시스템이 없다. 따라서 노인분들이 다른 사람들과 함께 소통하며, 행복한 노후생활을 보낼 수 있도록 한눈에 알기 쉽게 필요한 정보를 추천해주는 시스템을 만들고자 한다.

#### 입력정보 
- 아이디(이메일), 비밀번호, 성별, 주거지역, 설문조사 

### <사용 추천 알고리즘> 
서비스 초기 추천방식: 노인의 선호 여가 활동(2013-2017) 데이터 분석. 통계자료에 기반한 가짜 데이터를 생성하여, 코사인 유사도로 클러스터링
서비스 중반 추천방식: 선호 여가 활동 + DB에 쌓인 다른 노인분들의 여가활동을 기반으로 추천

### <제공 서비스>
1. 어르신을 위한 복지관 여가 프로그램 추천
    - 선호 여가활동에 따라 맞춤형 노인 복지/여가시설 및 시구청 여가프로그램 추천
2. 어르신을 위한 야외 활동 추천
    - 선호 여가에 따라 그에 맞춘 야외활동(ex)북한산 등산 등 추천
3. 직업 추천 
    - 서울시어르신 취업지원센터 정보를 활용하여 직종, 거리 순으로 정렬
4. 비슷한 취미를 갖는 주변 노인 소개 -> 친구 추가 및 대화 기능(현재 개발중)

### <기대효과> 
- 노인분들의 재사회화, 고독사 방지, 취업기회 제공, 노인 공동체 및 유대감 형성
- 노인들의 여가활동, 교육활동 수요 분석, 검색로그 분석을 통해 지자체 및 정부에 노인복지 제안

### <이용 데이터>
- 구청 및 시청의 노인대상 프로그램 및 여가프로그램 정보, 서울시 독거노인 현황, 어르신 교육시설 현황, 서울시 노인여가 복지시설, 서울시 노인주거 복지시설, 서울시 노인 사회활동 참가 통계, 구글맵 API 

#### 개선사항
- 4.23 AWS EC2 인스턴스를 활용해 ‘동행’ deploy, 도메인 구입 및 등록
- 4.25 Google Map API update bug fix, Enabled HTTPS with Let's Encrypt & Cerbot


#### 추후 개선사항
- 회원가입기능 개선(구글, 페이스북과 같은 SNS도 가입할 수 있도록)
- 회원가입 시 설문 문항 디자인 개선
- 불필요한 코드 삭제, Jinja2로 html 페이지의 코드 효율화
- 회원 간 쪽지 기능 구현
- 댓글 기능 개선
- 여가정보 최신화(노인복지회관 교육정보, 취업정보, 여가시설 등)
- Django로 플랫폼 이전
