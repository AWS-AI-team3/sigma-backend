# Sigma Backend (MSA)

## 서비스 구조
- services/user-service : 사용자 인증, 로그인, 유저 정보 관련 API
- services/motion-service : 모션모델 관련 API
- services/face-service : 얼굴인식모델 관련 API
- services/voice-service : 음성명령모델 관련 API
- shared/ : 공통 유틸 및 예외 처리 모듈
- gateway/ : API 통합 게이트웨이 (추후 사용 예정)

## 로컬 실행
```bash
cd services/user-service
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
uvicorn app.main:app --reload