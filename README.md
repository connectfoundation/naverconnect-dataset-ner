#### This dataset is created by NAVER Connect Foundation. 


# NER (Named Entity Recognition)

## Overview

NER 데이터셋은 개체명 인식(Named Entity Recognition) 데이터셋입니다. 

(*해당 데이터셋은 한국어 자연어 이해 평가 벤치마크인 [KLUE](https://klue-benchmark.com/) 데이터셋의 일부이나, 기존 벤치마크와는 다름을 알립니다.*)

<br>

## 목차
1. 특징
2. 포맷
3. 구성
4. 라이센스

<br>
## 1. 특징

NER 데이터셋은 TTA 개체명 태그 세트 및 태깅 말뭉치 가이드라인(https://nanum.etri.re.kr/file/002.%EA%B0%9C%EC%B2%B4%EB%AA%85%EC%9D%B8%EC%8B%9D_%EA%B0%80%EC%9D%B4%EB%93%9C%EB%9D%BC%EC%9D%B8.pdf) 의 일부 태그 셋인 PS (Person), LC (Location), OG (Organization), DT (Date), TI (Time), QT (Quantity)과 주석 원칙을 기반으로 주석되었습니다. TTA에서 제시된 태그 중 MUC-7(http://ai-center.botik.ru/Airec/images/stories/Articles/Collections/muc-guidelines/MUC_7_NER_markup.pdf)에서 제시된 ORGANIZATION, PERSON, LOCATION, DATE, TIME, MONEY, PERCENT에 해당하는 여섯 가지 태그를 선정하였습니다.
 
상세한 정보는 [KLUE 논문](https://arxiv.org/abs/2105.09680)의 Named Entity Recognition 섹션에서 확인하실 수 있습니다.

<br>

## 2. 포맷

NER 데이터셋은 다음과 같은 구조를 가지고 있습니다. ##뒤에 개체명이 주석된 문장이 제시되며, 문장을 음절 단위로 분석하고 있습니다. 각 음절은 BIO 주석이 되어 있습니다.

    ## klue-ner-v1_train_00001_nsmc <한군데:QT>서 필름을 너무 낭비한 작품입니다.
    한 B-QT
    군 I-QT
    데 I-QT
    서 O
      O
    필 O
    름 O
    을 O
      O
    너 O
    무 O
      O
    낭 O
    비 O
    한 O
      O
    작 O
    품 O
    입 O
    니 O
    다 O
    . O

개체명 주석에 활용된 태그에 대한 설명은 다음과 같습니다.

| Label   | Description   |
|---  |---  |
| PS    | Person, 개인 및 단체의 고유명  |
| LC    | Location, 행정구역 및 지역 관련 고유명  |
| OG    | Organization, 기관, 단체, 회사 등의 고유명   |
| DT  | Date, 날짜, 기간, 시대 관련 표현  |
| TI  | Time, 시간 관련 표현  |
| QT    | Quantity, 수량이나 숫자 관련 표현   |

<br>

## 3. 구성 
 
다음은 데이터의 구성입니다.
```
# 전체 데이터
./dataset/
  # 학습에 사용할 데이터셋. train 제공.
  ./train/
    # 학습용 train set
    ./train.csv
```

학습 데이터로는 총 21,008개의 문장이 제공됩니다.

<br>
 
## 4. 라이센스
 
 [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/)
 
 ### Contact
 
 작성자: 한지윤 jiyoonhan@upstage.ai
