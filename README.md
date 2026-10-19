<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0F766E,50:0EA5E9,100:6366F1&height=200&section=header&text=%EC%A0%95%EC%8A%B9%ED%98%B8&fontSize=54&fontColor=ffffff&desc=Vision%20AI%20%EC%97%94%EC%A7%80%EB%8B%88%EC%96%B4%20%C2%B7%20%EB%8D%B0%EC%9D%B4%ED%84%B0%EC%99%80%20%EB%AA%A8%EB%8D%B8%EC%9D%98%20%ED%95%9C%EA%B3%84%EB%A5%BC%20%EB%B6%84%EC%84%9D%ED%95%A9%EB%8B%88%EB%8B%A4&descSize=16&descAlignY=72&animation=fadeIn" alt="정승호 프로필 배너" />

<br />

<img src="https://img.shields.io/badge/%ED%8F%AC%EC%A7%80%EC%85%98-%EC%8B%A0%EC%9E%85%20Vision%20AI-0EA5E9?style=for-the-badge" alt="포지션 신입 Vision AI" />
<img src="https://img.shields.io/badge/%EA%B5%90%EC%9C%A1-%EC%BD%94%EB%93%9C%EC%9E%87%20AI%20%EC%97%94%EC%A7%80%EB%8B%88%EC%96%B4%2010%EA%B8%B0-6366F1?style=for-the-badge" alt="코드잇 AI 엔지니어 10기" />
<a href="mailto:wjdtmdgh87@gmail.com">
  <img src="https://img.shields.io/badge/%EC%9D%B4%EB%A9%94%EC%9D%BC-%EB%AC%B8%EC%9D%98-0F766E?style=for-the-badge&logo=gmail&logoColor=white" alt="이메일 문의" />
</a>

</div>

---

## 소개

데이터와 모델의 한계를 분석해 실제 문제를 해결하는 Vision AI 엔지니어 정승호입니다.<br />
이미지 라벨링부터 모델 선정까지 맡아 왔고, 모델을 바꾸기 전에 데이터와 평가 기준부터 확인합니다.

---

## 프로젝트

| 프로젝트 | 한 일 | 주요 스택 |
|---|---|---|
| **[PILL SIGHT](https://github.com/wjdtmdgh87-lgtm/pill-sight)**<br /><sub>경구약제 73종 탐지·식별 · PM · 6인</sub> | 팀 일정·역할 조율, 얼리스톱이 꺼진 학습 설정 발견, 브랜치 통합과 데이터 분할 검증 | YOLO12n · WBF · EfficientNet-B3 · EasyOCR |
| **[방울이](https://github.com/jaeheonki/smart-water-meter-kr)**<br /><sub>수도 계량기 자동 검침 · 데이터·모델 · 4인</sub> | 계량기 사진 약 200장 라벨링, OCR 한계 확인 후 2단계 검출 구조로 전환, YOLOX-s 선정 | YOLOX-s · ONNX Runtime · OpenCV |
| **[It's mine](https://github.com/Codeit-Part3-6Team/Codeit-Part3-6Team-Project)**<br /><sub>공공조달 RFP 분석 RAG · 데이터 엔지니어 · 4인</sub> | HWP5 파서로 RFP 본문 복원, 메타데이터 보완, 평가 골든셋 12차 개선 | HWP5 파싱 · LangChain · BM25 · RRF |
| **메뉴재판**<br /><sub>LLM 멀티 에이전트 메뉴 선정 · 에이전트·프롬프트 · 4인</sub> | 변호인·검사·판사 프롬프트와 페르소나 설계, JSON 구조화 출력과 오류 처리 | LangGraph · LiteLLM · Pydantic |
| **[광고 생성 서비스](https://github.com/Codeit-AI10-Part4-3Team/AI10-Part4-3Team-Advanced-Project)**<br /><sub>제품 사진으로 인스타그램 광고 생성 · PM·QA · 4인</sub> | 기획·회의 운영, 광고 카피 골든셋 26건과 가드레일 비교 하네스 구축 | FastAPI · OpenAI API · Docker · GCP |
| **EviRevBench** `진행 중`<br /><sub>근거 변경 시 RAG 답변 수정 벤치마크 · 독립 검증·통계 · 5인</sub> | 분석 계획과 결정 기록 작성, 팀원 PR 독립 재검증, 비교 실험의 분모·불확실성 설계 | Python · 통계 분석 · 재현성 검증 |

---

## 대표 프로젝트

### 방울이 · 수도 계량기 자동 검침

수도 계량기 사진에서 검침값을 읽어 사용량과 요금으로 바꿔 주는 Android 앱입니다. 물-에너지 융합 포럼 공모전에 제출했습니다.

<div align="center">
  <img src="https://raw.githubusercontent.com/jaeheonki/smart-water-meter-kr/main/.github/assets/readme/yolox-two-stage-pipeline.svg" alt="YOLOX-s 2단계 자동 검침 흐름" width="760" />
</div>

- OCR이 7세그먼트 숫자를 읽지 못하는 것을 확인하고, 표시부 → 숫자 0~9를 차례로 검출하는 2단계 구조로 전환
- 라이선스·추론 시간·ONNX 연동성을 기준으로 후보 5개 중 YOLOX-s 선정
- 4방향 회전 처리를 제안하고, 회전 시 6과 9가 뒤바뀌는 문제를 찾아 방향별 비교에 반영

`표시부 검출 mAP@0.50 1.000 (내부 검증)` · `추론 108.44ms` · `실기기 E2E 완료 (팀)`

<div align="center">
  <img src="https://raw.githubusercontent.com/jaeheonki/smart-water-meter-kr/main/.github/assets/readme/device-e2e/home.png" alt="방울이 홈 화면" width="23%" />
  <img src="https://raw.githubusercontent.com/jaeheonki/smart-water-meter-kr/main/.github/assets/readme/device-e2e/manual-reading.png" alt="검침 숫자 확인 화면" width="23%" />
  <img src="https://raw.githubusercontent.com/jaeheonki/smart-water-meter-kr/main/.github/assets/readme/device-e2e/water-ledger.png" alt="물 가계부 화면" width="23%" />
  <img src="https://raw.githubusercontent.com/jaeheonki/smart-water-meter-kr/main/.github/assets/readme/device-e2e/energy-report.png" alt="에너지 리포트 화면" width="23%" />
</div>

### PILL SIGHT · 경구약제 탐지·식별

사진 속 알약 73종의 위치와 이름을 찾는 4단계 파이프라인입니다. 6인 팀의 PM을 맡았습니다.

```text
YOLO12n 5-Fold → WBF 앙상블 → 후처리 → EfficientNet-B3 재분류 → EasyOCR 각인 보정
```

- 역할을 나누기 전에 전원이 데이터를 먼저 분석하도록 제안해, 라벨 누락과 클래스 불균형을 초기에 확인
- 얼리스톱이 꺼진 채 300 epoch를 학습하던 설정을 발견하고, 공동 분석 후 epochs 150 · patience 30으로 조정
- 실험·모델 브랜치를 통합하고, fold 구성과 누락 파일을 검사하는 데이터 분할 검증 스크립트 작성

`5-Fold 검증 mAP@0.50 0.994` · `테스트 832장 수동 검수: 3,229개 중 오판 3건`

---

## 기술 스택

**Vision**<br />
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)
![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=flat-square&logo=opencv&logoColor=white)
![Ultralytics YOLO](https://img.shields.io/badge/Ultralytics%20YOLO-111F68?style=flat-square)
![YOLOX](https://img.shields.io/badge/YOLOX-0F766E?style=flat-square)
![ONNX Runtime](https://img.shields.io/badge/ONNX%20Runtime-005CED?style=flat-square&logo=onnx&logoColor=white)
![EasyOCR](https://img.shields.io/badge/EasyOCR-6366F1?style=flat-square)

**LLM / RAG**<br />
![LangChain](https://img.shields.io/badge/LangChain-1C3C3C?style=flat-square&logo=langchain&logoColor=white)
![LangGraph](https://img.shields.io/badge/LangGraph-1C3C3C?style=flat-square)
![LiteLLM](https://img.shields.io/badge/LiteLLM-111827?style=flat-square)
![OpenAI API](https://img.shields.io/badge/OpenAI%20API-412991?style=flat-square&logo=openai&logoColor=white)

**협업**<br />
![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=github&logoColor=white)
![Notion](https://img.shields.io/badge/Notion-000000?style=flat-square&logo=notion&logoColor=white)
![Trello](https://img.shields.io/badge/Trello-0052CC?style=flat-square&logo=trello&logoColor=white)

---

## 학력 · 연락

| | |
| :--- | :--- |
| **학력** | 건국대학교 물리학과 (2018.03 ~ 2026.02) |
| **교육** | 코드잇 AI 엔지니어 과정 10기 |
| **이메일** | [wjdtmdgh87@gmail.com](mailto:wjdtmdgh87@gmail.com) |

<div align="center">
<br />
<sub>데이터부터 확인하고, 숫자는 무엇을 잰 값인지 함께 말합니다.</sub>
</div>
