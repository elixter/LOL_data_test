
## 리그오브레전드 15분 데이터 승리예측
- 데이터셋
  - lolChaltest.csv (25617개) : 챌린저랭크 첫 15분 데이터
  - lolmaster.csv (64983개) : 마스터랭크 첫 15분 데이터(라인별 골드, 경험치 획득량 포함)
  - masterinf.csv (64983개) : 마스터랭크 경기종료 후 데이터. (feature가 다름 주의)
- 학습환경
  - RTX 3070 8GB
### Requirements
  - Python >= 3.7
  - Tensorflow >= 2.0
  - Tensorflow-addons
  - Sklearn
  - Pandas
  - re
  - Seaborn

## 실험 결과
- Train accuracy   
  ![Train accuracy](https://github.com/elixter/LOL_data_test/blob/main/graph1.png)
- Validation accuracy   
  ![Validation accuracy](https://github.com/elixter/LOL_data_test/blob/main/graph2.png)
- Train loss   
  ![Train loss](https://github.com/elixter/LOL_data_test/blob/main/graph3.png)
- Validation loss   
  ![Validation loss](https://github.com/elixter/LOL_data_test/blob/main/graph4.png)
- Comparison Best   
  ![Comparison best](https://github.com/elixter/LOL_data_test/blob/main/comparison.png)

## Demo
- 최종 실험본
  - 하드웨어 가속기(GPU) 사용을 권장합니다.
  - [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1_ydvR_gu3dVbTXNbhMCe-gFHpNpwI03r?usp=sharing)
- 학습된 파라미터 
  - [google drive](https://drive.google.com/drive/folders/1AsHGWCHmsdQ9UZ52lZhlkqZY-GYXYnOC?usp=sharing)
  - 256_2layers.h5
    - 256 Dense층 2개 (라인별 획득 골드, 경험치 없이 학습)
  - large-units_many_layers.h4
    - 4096 -> 8192 -> 8192 -> 4096 -> 1024 -> 512 -> 128 Dense층 (라인별 획득 골드, 경험치 없이 학습)
    - 파일크기가 크니 주의바랍니다.
  - 256_2layers_with_more_feature.h5
    - 256 Dense층 2개
  - many_layer_with_more_feature.h5
    - 4096 -> 8192 -> 8192 -> 4096 -> 1024 -> 512 -> 128 Dense층
    
