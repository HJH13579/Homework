# 메인페이지

## 구상
- '현재상영작', '상영예정작', '평점 높은 영화', '유명한 영화'의 영화 포스터들을 가로 스크롤 방식으로 보여주기
- 5~7개의 영화 포스터를 주고, Next/Prev 화살표 버튼을 통해 다른 포스터들을 보여주기
- 일정 시간이 지나면 자동으로 다음 리스트의 포스터들로 넘어가기
- 첫/마지막 페이지에서 더 넘어가려고 할 시 마지막/첫 페이지로 자연스럽게 넘어가기 (Loop)

## 구현
- 실시간으로 변경되는 정보들이기에, DB에서가 아닌 API를 통해 Data 받아오기
- 가로 스크롤을 가장 자연스럽게 구현 가능한 Bootstrap의 'carousel'과 Vue를 합친 라이브러리 'vue-carousel'를 이용해서 구현

## 문제점
- 'vue-carousel' 라이브러리가 제공하는 ':loop'는 이전/다음 슬라이들을 빠르게 skip하는 방식으로, skip되는 과정이 눈에 보인다.

## 개선점
- 자연스러운 Loop 구현
- 화살표 모양, 색상
- 포스터 크기 조정, 가로/세로 길이 변경
- 시간이 지나면 자동으로 다음 리스트의 포스터들로 넘어가기

> 설치 필수
- npm install -g @vue/cli
- npm install vue-carousel
- npm intall axios

<django 프로젝트 만들기>

python -m venv venv  #가상환경 생성

source ./venv/Scripts/activate  #가상환경 활성화

pip install -r required

cd my_pjt  #프로젝트가 있는 폴더로 이동 (ls로 이동이나 실행 가능한 폴더 파일 확인)

python manage.py runserver  #서버 실행


가상환경 활성화되어 있으면 서버실행


인증관련할 때

pip install dj-rest-auth
pip install 'dj-rest-auth[with_social]'
하고 해야됨

vue 관련

npm i
npm install vue bootstrap-vue bootstrap
npm runserve

부트스트랩 추가되어서 프로젝트 시작하기 전에  npm install vue bootstrap-vue bootstrap
해주셔야 오류가 안납니다!

https://github.com/SSAFY-5th-seungwoon/Moya_backend