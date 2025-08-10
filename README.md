project/
├── backend/
│   ├── main.py            # FastAPI 백엔드 (PGVector 검색 API 포함)
│   ├── db.py              # PostgreSQL 연결 유틸
│   ├── storage.py         # SHA256 저장/중복 제거 유틸
│   └── embedding.py       # CLIP 임베딩 처리
├── streamlit_app.py       # COCO 관리 & 유사도 검색 UI
├── init_pgvector.sql      # PGVector 확장 + images 테이블 생성 스크립트
└── requirements.txt


./process.py extract (5×80 경량화)
→ Tab 1: “🚀 경량화 + DB 저장 실행”

annotation JSON + 이미지 ZIP 업로드

샘플 개수 지정 → 경량화 JSON 저장 + 이미지 복사 + SHA256 스토리지 + DB/임베딩 저장

./process.py json (커스텀/CID 스키마 변환)
→ Tab 3: “커스텀 JSON 생성” 버튼

./process.py split (coco.json / a9.json 생성)
→ Tab 3: “스플릿 생성” 버튼


1탭 = 데이터 전처리 & DB 저장

2탭 = 어노테이션 기반 시각화

3탭 = 의미(임베딩) 기반 검색

