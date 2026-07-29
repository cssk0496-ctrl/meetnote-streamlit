# MeetNote — AI 회의록 자동화

음성 회의 파일을 업로드하면 Gemini API로 녹취하고, 핵심 요약·결정사항·담당 업무를 자동 작성하는 Streamlit 앱입니다.

## 로컬 실행

```bash
pip install -r requirements.txt
streamlit run app.py
```

로컬에서는 `.streamlit/secrets.toml` 파일을 만들고 다음 내용을 입력합니다.

```toml
GEMINI_API_KEY = "Google_AI_Studio에서_발급받은_API_키"
```

API 키가 포함된 `secrets.toml` 파일은 GitHub에 올리지 마세요.

## Streamlit Community Cloud 배포

1. 이 폴더의 파일을 GitHub 저장소 최상단에 업로드합니다.
2. Streamlit Community Cloud에서 **Create app**을 선택합니다.
3. 저장소, `main` 브랜치, `app.py`를 선택합니다.
4. **Advanced settings → Secrets**에 아래 내용을 등록합니다.

```toml
GEMINI_API_KEY = "Google_AI_Studio에서_발급받은_API_키"
```

5. **Deploy**를 누릅니다.

## 파일 구성

- `app.py`: Streamlit 화면 및 AI 처리 코드
- `requirements.txt`: 설치할 Python 패키지
- `.gitignore`: API 키 등 제외 파일
