## Snippets

# KWU Computer Vision AI Challenge

### 🏆🏆🏆 **3rd Place** 🏆🏆🏆

## 팀원
김재윤 (https://github.com/kimjaeyoonn)
김태영 (https://github.com/kty4119)

## Dataset
<img src=./imgs/dataset.png width="600" height="400" />

1.dirty_mnist.zip (3.05 GB)
- (256,256)크기의 .png 파일 50,000 개
- 월간데이콘 7의 알파벳 데이터를 합성한 이미지
- (256, 256)크기의 이미지 속에 10 ~ 15개의 글자(알파벳 a – Z, 중복 제외)가 배치
- 노이즈 추가

2.test_dirty_mnist.zip (313 MB)
- (256,256)크기의 .png 파일 5,000 개
- dirty_mnist와동일한 형태로 구성

3.dirty_mnist_answer.csv(2.80 MB)
- dirty_mnist에 존재하는 5만장의 이미지에 대한 정답 파일
- 알파벳이 존재할 경우 1, 존재하지 않을 경우 0로 채움

## Training
- 사용 모델 : Efficientnet-b7

- 5-fold로 나누어 학습 / Augmentation은 RandomRotation만 적용할 때 가장 좋은 성능을 보임.

- Fold 별로 생성된 모델의 loss와 accuracy를 비교하면서 Fold당 모델을 11개씩 선정하여 앙상블을 진행.
