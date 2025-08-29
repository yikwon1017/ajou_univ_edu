# 흉부 X-Ray 폐렴 진단 AI 실습

## 데이터셋 소개

### 데이터 출처
- **데이터셋**: [Chest X-Ray Images (Pneumonia)](https://www.kaggle.com/datasets/paultimothymooney/chest-xray-pneumonia)
- **제공**: Kaggle / Paul Timothy Mooney
- **원본 출처**: Guangzhou Women and Children's Medical Center, Guangzhou

### 데이터 구조
이 데이터셋은 1-5세 소아 환자의 흉부 X-Ray 이미지로 구성되어 있습니다.

```
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
```

### 클래스 설명
- **NORMAL**: 정상 흉부 X-Ray 이미지
- **PNEUMONIA**: 폐렴이 있는 흉부 X-Ray 이미지
  - 세균성 폐렴 (Bacterial)
  - 바이러스성 폐렴 (Viral)

### 데이터 특징
- **총 이미지 수**: 5,863장
- **이미지 형식**: JPEG
- **이미지 크기**: 다양함 (대부분 1000x1000 픽셀 이상)
- **색상**: 흑백 (Grayscale)
- **클래스 불균형**: 폐렴 이미지가 정상보다 약 3배 많음

## 학습 목표

1. **의료 영상 데이터 전처리** 방법 학습
2. **전이학습(Transfer Learning)** 활용 - DenseNet121
3. **모델 성능 평가** - loss curve, 정확도

## 의료 데이터의 중요성

### 이 데이터가 중요한 이유
- 폐렴은 전 세계 5세 미만 어린이 사망의 주요 원인
- 조기 진단이 치료 성공률을 크게 향상시킴
- 의료진이 부족한 지역에서 AI 보조 진단 도구로 활용 가능

### 주의사항
- 이 모델은 **교육 목적**으로만 사용
- 실제 의료 진단은 반드시 **전문 의료진**이 수행해야 함
- AI는 의사를 대체하는 것이 아닌 **보조 도구**

## 데이터 전처리 과정

1. **이미지 크기 통일**: 224x224 픽셀로 리사이즈
4. **클래스 균형 맞추기**: 
   - 실습에서는 각 클래스당 600장으로 제한을 하려고 하였으나, codespace 자원 한계 상 10장으로 제한 

## 실습 진행 순서

1. **환경 설정**: 필요한 라이브러리 설치
2. **데이터 로드**: 이미지 읽기 및 확인
3. **전처리**: 크기 조정 및 이미지 셔플 작업 
4. **모델 구축**: DenseNet121 전이학습
5. **학습**: 모델 훈련
6. **평가**: 성능 측정

## 참고 자료

- [Original Paper](http://www.cell.com/cell/fulltext/S0092-8674(18)30154-5)
- [Kaggle 데이터셋 페이지](https://www.kaggle.com/datasets/paultimothymooney/chest-xray-pneumonia)
- [DenseNet 논문](https://arxiv.org/abs/1608.06993)
- [Transfer Learning 가이드](https://www.tensorflow.org/tutorials/images/transfer_learning)

## 추가 학습 제안

1. **다중 분류**: 정상 vs 세균성 폐렴 vs 바이러스성 폐렴
2. **Grad-CAM**: AI가 주목한 영역 시각화
3. **앙상블 모델**: 여러 모델 조합으로 성능 향상

---
실습 관련 질문이 있으시면 강사에게 문의해주세요.

**즐거운 학습 되세요!**
