# 🧠 전이학습 기반 뇌종양 분류

본 프로젝트는 MRI 뇌 영상 데이터를 기반으로 딥러닝 모델을 활용해  
**뇌종양의 존재 여부 및 종류를 분류**하는 모델을 개발한 실험 노트북입니다.

최종적으로 ResNet50V2 기반 전이학습 모델에 Fine-tuning을 적용하여  
높은 정확도와 오분류 최소화를 달성했습니다.

---

## 📁 주요 파일
- **출처**: Kaggle의 [Brain Tumor MRI Dataset](https://www.kaggle.com/datasets/masoudnickparvar/brain-tumor-mri-dataset/data) 공개 데이터셋 사용

| 파일명 | 설명 |
|--------|------|
| `brain_tumor_classification.ipynb` | 전체 실험 흐름, 시각화 결과 포함 |
| `brain_tumor_classification.html` | 노트북 고정 시각화 버전 (다운로드 후 열람 권장) |

> 📝 학습된 모델 파일(`.h5`)은 포함되어 있지 않으며,  
> 본 노트북을 실행하면 동일한 모델 구조와 성능을 재현할 수 있습니다.

---

## 🧪 실험 구성 요약

- **입력 전처리**: 512×512 Grayscale 이미지로 변환 및 정규화
- **기본 CNN 모델 성능 한계(93~95%)** 확인 후 개선 시도
- **13종 전이학습 모델 비교 실험** → ResNet50V2 선택
- **Fine-tuning 적용 후** 최종 성능 대폭 향상

---

## 📊 최종 결과 요약

- **Validation Accuracy**: 99%
- **F1-score**: 99%
- **종양을 정상으로 오분류한 사례 없음 (Confusion Matrix 기준)**

---

## 🔗 데이터셋 정보

- 출처: [Kaggle - BBrain Tumor MRI Dataset](https://www.kaggle.com/datasets/masoudnickparvar/brain-tumor-mri-dataset/data)
- 클래스: `no_tumor`, `glioma`, `meningioma`, `pituitary`
- 제공된 `Testing` 데이터를 **Validation 용도**로 사용함

---

## 🚀 데모 체험

- Hugging Face Demo (실시간 민원 분류 + 부처 정보 제공)  
  👉 [전이학습 기반 뇌종양 분류](https://huggingface.co/spaces/JohnYim0213/project-note)
