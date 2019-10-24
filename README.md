# SmartWork (스마트 업무처리 시스템)

## 설치 안내 (Installation Process)

### 사용 버전 안내
- Django (2.2.6)
django-allauth (0.40.0)
django-crispy-forms (1.8.0)
django-markdownx (2.0.28)

#### BackEnd로 Django 이용
- apt-get install python3-pip
- pip3 install Django
- pip3 install django-allauth
- pip3 install django-crispy-forms
- pip3 install django-markdownx

## 사용법 (Getting Started)
- source venv/bin/activate
python3 manage.py makemigrations
python3 manage.py migrate
python3 manage.py migrate --run-syncdb
 python3 manage.py createsuperuser
- python3 manage.py runserver 0:8000 --insecure



## 개발 계획
1. 게시판 기능 구현하기
(글쓰기, 수정, 댓글, 카테고리 구성하기)
2. 게시판 커스텀 관리자 페이지 만들기
3. markdown 에디터, 이미지 업로더 구현
4. 출타 신청 페이지 구성하기
5. 출타 승인 / 관리 페이지 구성
6. 인원 현황 기능
7. 로그인, 회원가입 기능 구현

## 개발 동기


군부대나 일반 회사에는 대부분 업무 처리를 할 수 있는 인트라넷 시스템들이 갖추어져 있습니다.
하지만 시스템이 해당 기관의 업무에 특화되어 있지 않은 경우가 많아 협업과 최신화에 어려움이 있으며 중복적으로 업무를 하게 되는 불편함이 생기기도 합니다. 결국 시간과 비용적으로 큰 손해를 보는 결과가 발생하게 됩니다.
이를 해결하기 위해 공유, 협업, 자동화, 맞춤성과 통합 관리 등을 극대화하여 업무를 간소화할 수 있는 신개념의 스마트 업무 처리 시스템을 기획하였습니다.

## 프로젝트 구조
- 첫 번째로는 "스마트 국방업무"로 이름 붙인 국방부 분야입니다.
스마트 국방업무에는 아래와 같이 크게 4가지 메뉴로 구성되어있습니다.


1. 부대 관리 업무(휴가/출타 관리, 근무관리, 인원 현황, 부대일지)
2. 부대 활동(공지사항, 감사 나눔 1·2·3 운동, 1·1·30·30 캠페인)
3. 편의 기능(청소/임무분담제, 출타 행선지 공유, 부대 일정, 전역/진급일 계산)
4. SNS(부대 밴드, 친구 찾기, 메일/쪽지함, 미니게임)


- 두 번째로는 타 기관 연계사업입니다.
스마트 국방업무 처리 시스템의 구성과 기능들을 활용하여 다른 유관기관에서도 변형하여 이용할 수 있도록 배포할 것입니다. 해당 기관의 관리자가 권한을 부여받게 되면 관리자 페이지에서 사이트의 UI를 편집하여 재배치하고 필요한 기능들을 추가하고 변경할 수 있게 됩니다. 업무처리 시스템에서 공유경제를 활성화시키는 무한한 능력을 갖게 될 것입니다.

## 이용 가능성
해당 프로젝트는 군부대, 회사, 학교 등 여러 기관에서 이용이 가능하고 자료만 입력하면 대부분의 업무를 자동화하여 수행하므로 4차 산업혁명에 걸맞게 사업 전망 또한 매우 좋습니다.

실례로 부대에서 휴가 신청을 하게 되면 출타 비율과 빈도를 수기로 계산 후 엑셀 파일로 출타를 종합하고, 출력하여 문서로 공지하게 됩니다. 이를 근거로 상황판에 휴가 인원을 기재하고, 해당 날의 근무와 청소구역을 찾아 다시 교체하여 작성하는 등 여러 작업을 반복하는 비효율적인 면들이 존재합니다.  이런 상황에서 휴가 일정이 변경되기라도 하면 모든 문서를 다시 초기화해야 하며 기존 자료와 혼선이 발생하기도 합니다. 
여기에 스마트 국방업무처리 시스템을 이용하면 휴가자는 휴가/출타 관리 페이지에서 실시간 출타율을 보며 원하는 날짜에 휴가를 신청할 수 있습니다. 물론 훈련 등의 이유로 휴가 불가 기간을 지정해 두면 휴가 신청은 불가능합니다. 휴가를 신청하면 지휘관의 계정에 승인 요청이 뜨며 승인 시에 자동으로 출타 인원 현황이 종합되어 부대 일정과 부대일지에 등록이 됩니다. 또한 해당 일의 근무와 청소구역에 변경 표시가 활성화되어 교체 요청이나 자동 재편성이 가능해집니다. 필요시에는 휴가 행선지를 공유하여 카풀이나 배차를 이용할 수도 있습니다.

이러한 기능들은 군부대뿐만이 아니라 타 기관에서도 특성에 맞게 배치해 사용할 수 있으며 개인이 새로운 기능을 만들었을 경우에 깃허브의 Pull requests를 통해 commit을 하게 되면 프로그래밍 기술이 없지만 해당 기능이 필요한 다른 기관에서도 관리자 페이지의 GUI를 통해 손쉽게 추가하여 사용할 수 있는 강점이 있습니다.
