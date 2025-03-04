# **정성호 vs 임재범**
이 파이선 스크립트는 크롤링으로 데이터를 수집한 뒤 새로운 영상을 입력하면 정성호 또는 임재범의 영상을 분류하는 프로그램입니다.
딥러닝을 활용한 이미지 분류 모델을 개발하여, 특정 인물(정성호 vs 임재범)을 정확하게 분류하는 것을 목표로 합니다.

### 기능 
* 정성호, 임재범의 영상을 수집합니다
* 정성호, 임재범의 영상을 분류합니다

## 사용된 라이브러리
▶️ 기본 라이브러리
* numpy, random, os, shutil → 데이터 처리 및 파일 관리
* matplotlib.pyplot → 시각화
* tqdm → 학습 진행 상황 표시

▶️ 딥러닝 & 이미지 처리
* torch, torchvision → 딥러닝 모델 학습
* timm → 전이 학습을 위한 사전 학습된 모델 제공
* cv2, PIL → 이미지 데이터 로드 및 전처리

## 프로젝트 구조
📁 프로젝트 폴더
│── 📄 정성호 vs 임재범.ipynb  # 이미지 분류 모델 학습

│── 📄 Crawling.ipynb           # (예상) 데이터 수집을 위한 웹 크롤링

│── 📁 data                     # 원본 데이터 저장 폴더

│── 📁 train                    # 학습 데이터

│── 📁 valid                    # 검증 데이터

│── 📁 test                     # 테스트 데이터



## 작동방식
'''

    train_root = f'{data_root}/train'

    valid_root = f'{data_root}/valid'

    test_root = f'{data_root}/test'

    for folder in [train_root, valid_root, test_root]:]
  
    if not os.path.exists(folder):
    
        os.makedirs(folder) 
'''
        
➡️ 데이터셋을 학습(train) / 검증(valid) / 테스트(test) 폴더로 분할합니다.

'''

    import timm

    model = timm.create_model('resnet50', pretrained=True)
'''

➡️ timm 라이브러리를 활용하여 ResNet-50 모델을 불러오고 전이 학습을 적용합니다.

## 실행방법 
▶️  Colab에서 실행하는 경우
- 위 코드처럼 google.colab을 이용하여 Google Drive를 마운트하고
- 데이터를 data/ 폴더에 저장한 후 실행합니다!

▶️  로컬 환경에서 실행하는 경우
-  data/ 폴더에 데이터를 저장 후, torch, timm 등을 설치하고 실행합니다!

'''

    pip install timm torch torchvision opencv-python matplotlib tqdm
'''
        
