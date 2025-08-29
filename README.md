🩺 Chest X-Ray 폐렴 진단 AI 실습
📊 데이터셋 소개
데이터 출처

Dataset: Chest X-Ray Images (Pneumonia)
제공: Kaggle / Paul Timothy Mooney
원본 연구: Guangzhou Women and Children's Medical Center, Guangzhou

데이터 구성
이 데이터셋은 소아 환자(1-5세)의 흉부 X-Ray 이미지로 구성되어 있습니다.
chest_xray/
├── train/
│   ├── NORMAL/       (1,341장)
│   └── PNEUMONIA/    (3,875장)
├── val/
│   ├── NORMAL/       (8장)
│   └── PNEUMONIA/    (8장)
└── test/
    ├── NORMAL/       (234장)
    └── PNEUMONIA/    (390장)
클래스 설명

NORMAL: 정상 흉부 X-Ray 이미지
PNEUMONIA: 폐렴이 있는 흉부 X-Ray 이미지

세균성 폐렴 (Bacterial)
바이러스성 폐렴 (Viral)



데이터 특징

총 이미지 수: 5,863장
이미지 형식: JPEG
이미지 크기: 다양함 (대부분 1000x1000 픽셀 이상)
컬러: Grayscale (흑백)
클래스 불균형: 폐렴 이미지가 정상보다 약 3배 많음

🎯 실습 목표

의료 영상 데이터 전처리 방법 학습
이진 분류 모델 구축 (정상 vs 폐렴)
전이학습(Transfer Learning) 활용 - DenseNet121
클래스 불균형 문제 다루기
모델 성능 평가 - 정확도, 민감도, 특이도

🔬 의료 데이터의 특수성
왜 이 데이터가 중요한가?

폐렴은 전 세계적으로 5세 미만 어린이 사망의 주요 원인
조기 진단이 치료 성공률을 크게 높임
의료진 부족 지역에서 AI 보조 진단 도구로 활용 가능

주의사항

이 모델은 교육 목적으로만 사용
실제 의료 진단은 반드시 전문 의료진이 수행해야 함
AI는 의사를 대체하는 것이 아닌 보조 도구

📝 데이터 전처리 과정

이미지 크기 통일: 224x224 픽셀로 리사이즈
정규화: 픽셀 값을 0-1 범위로 조정
데이터 증강 (선택사항):

회전, 이동, 줌 등을 통한 데이터 다양성 확보


클래스 균형 맞추기:

실습에서는 각 클래스당 600장으로 제한



🚀 실습 진행 순서

환경 설정: 필요한 라이브러리 설치
데이터 로드: 이미지 읽기 및 확인
전처리: 크기 조정 및 정규화
모델 구축: DenseNet121 전이학습
학습: 모델 훈련
평가: 성능 측정 및 분석
예측: 새로운 X-Ray 이미지 진단

📊 예상 성능 지표

정확도(Accuracy): 90% 이상 기대
민감도(Sensitivity/Recall): 폐렴 환자를 정확히 찾는 능력
특이도(Specificity): 정상을 정상으로 판단하는 능력

⚠️ 윤리적 고려사항

개인정보 보호: 모든 X-Ray 이미지는 익명화됨
편향 방지: 다양한 인구집단에 대한 검증 필요
투명성: AI 판단 근거를 설명할 수 있어야 함
책임: 최종 진단 책임은 의료진에게 있음

🔗 참고 자료

Original Paper
Kaggle Competition
DenseNet Paper
Transfer Learning Guide

💡 추가 학습 제안

다중 분류: 정상 vs 세균성 폐렴 vs 바이러스성 폐렴
Grad-CAM: AI가 주목한 영역 시각화
앙상블 모델: 여러 모델 조합으로 성능 향상
Cross-validation: 더 견고한 성능 평가
