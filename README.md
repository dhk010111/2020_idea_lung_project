# Lung segmentation train project

## Project Purpose
 - Lung CT Data를 이용하여 Segmentation을 학습한다.
 - Input Data를 CT Data로 하여 Lung target mask를 예측해내는 인공지능 모델을 구현

 
## Learnging Model
  - Convolutional Encoder-Decoder model
  
 CNN(Convolutional Neural Network)를 이용한 인코더와 디코더 모델을 이용한다.
 
 Incoder : 차원 축소를 통해서 핵심 요소만 추출하는 과정 \
 (프로젝트에서는 MaxPooling2D 이용) \
 Decoder : 압축된 정보로부터 차원 확장을 통해 원하는 정보로 복원하는 과정 \
 (프로젝트에서는 UpSampling2D 이용)
  - Example \
 Input | Output \
 ![image](https://user-images.githubusercontent.com/65123546/99789709-57862600-2b66-11eb-9944-cd9ea96166bf.png)
 ![image](https://user-images.githubusercontent.com/65123546/99789494-05dd9b80-2b66-11eb-8009-2eec44a4fe1d.png)\
 Output은 Segmentation이 된 lung mask가 출력된다. (폐:1(white) 나머지:0(black))


 
 
 
 
## Dependencies
### Training
 - Python
 - numpy
 - keras
 - matplotlib
### Preprocessing
 - skimage
 - sklearn
 - pandas
### Dataset
Finding and Measuring Lungs in CT Data https://www.kaggle.com/kmader/finding-lungs-in-ct-data
