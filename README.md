# 인사, 노무 챗봇

이 프로젝트는 인사, 노무 관련 질문을 처리하는 AI 챗봇 웹 애플리케이션입니다. Flask를 기반으로 개발되었으며, OpenAI의 GPT 모델을 사용합니다.

## 요구 사항
- Python 3.10 이상
- OpenAI API 키
- LangChain API 키
- Flask
- MongoDB

## 설치 방법
```bash
git clone https://github.com/your-username/your-repo-name.git
cd your-repo-name
# 가상환경 생성
python -m venv venv
# 가상환경 활성화: 윈도우
venv\Scripts\activate
# 가상환경 활성화: 리눅스/macOS
source venv/bin/activate
# 패키지 설치
pip install -r requirements.txt
```

## 설정
1. `config.py` 파일을 생성하고 다음과 같이 설정을 추가합니다:
```python
OPENAI_API_KEY = 'your_openai_api_key'
MONGO_URI = 'mongodb://localhost:27017/'
MONGO_DBNAME = 'your_db_name'
SECRET_KEY = 'your_secret_key'
LANGSMITH_API_KEY = 'your_langsmith_api_key'
```

2. MongoDB 서버를 실행합니다.

## 실행
```bash
python app.py
```
서버는 기본적으로 `http://localhost:5000`에서 실행됩니다.

## 주요 기능
- 사용자 인증 (로그인/로그아웃/회원가입)
- AI 챗봇과의 대화
- 채팅 기록 저장 및 조회
- 사용자 프로필 관리

## 프로젝트 구조
```
.
├── app.py              # 메인 애플리케이션 파일
├── config.py           # 설정 파일
├── model.py            # 데이터베이스 모델
├── utils.py            # 유틸리티 함수
├── static/             # 정적 파일 (CSS, JS)
│   └── js/
│       └── scripts.js
└── templates/          # HTML 템플릿
    ├── base.html
    ├── chat.html
    ├── history.html
    ├── index.html
    ├── login.html
    ├── login_base.html
    ├── register.html
    └── user_profile.html
```

## 기여
프로젝트에 기여하고 싶으시다면 이슈를 열거나 풀 리퀘스트를 보내주세요.
