# 2021 SKKU AI x Bookathon 4rd

## 1. Introduction
Book(책)과 Hackathon(해커톤)의 합성어로 인간과 AI가 협업하여 글을 쓰는 대회

성균관대학교에서 주최하는 AI x Bookathon 대회로 인공지능 모델을 사용하여 주제가 '대담한'인 수필을 작성하는 것이 목적


### 🏆 st of 15 teams

"6월의 피는 한련화"라는 제목을 가진 수필을 생성하여 본선에서 장려상 수상

[>> 발표자료 보러가기](./당당!_발표자료.pdf)

[>> 최종작품 보러가기](./당당!_6월의%20피는%20한련화.pdf)

## 1차 예선 -> 인공지능 관련 시험
    2번의 사전교육과정을 수행한 후  gpt와 여러가지 ai와 관련한 객관식, 주관식, T/F문제를 풀어서 예선통과
    다른 팀들의 답변과의 차별성을 두기위해 답변에 틀린 이유를 근거로 작성하는 것과 추가설명을 위한 그림을 첨부
    예선 과정을 통해서 이 대회에서 어떠한 것을 활용하여 어떠한 결과물을 도출해야할지 숙지하고 이해
    
## 2차 본선
    2차 본선은 오후 3시부터 시작하여 다음날 오전11시까지 총 21시간동안 무박 2일로 진행
    성균관 대학교 삼성학술정보관에서 각 팀들이 모여서 진행
    수필의 키워드 발표 후 각 팀들이 모여 어떠한 주제를 발표할지 회의 후 각 팀마다 팀 소개 후 본격적인 수필작성을 위한 팀별 활동 시작
    주제 선정 후 이와 관련된 데이터를 추가적으로 크롤링 후 데이터 전처리 후 모델을 추가적으로 학습시켜 원하는 문장이 생성될 수 있도록 함
    한 명이 서버에 접속하여 글을 쓰기에는 시간이 부족할 것이라고 판단하여 모델이 일부를 freezing시켜 GPU데이터 확보 하여 여러 명이 서버에
    접속하여 글을 쓸 수 있도록 함

## 2. Data Preprocessing Strategy
    크롤링한 데이터(.txt)를 파일 형식 변환 후(.json) 정규화 표현을 이용한 기계전처리 후 세밀한 전처리를 위해 사람 전처리 과정을 통하여 데이터 정제

## 3. Model Training Strategy
    마인즈랩에서 제공하는 사전학습된 GPT3 모델을 사용하는 대신, EleutherAI/polyglot-ko-1.3b5를 한 번 더 사전학습을 진행한 후 fine-tuning 하는 방법으로 생성 모델을 학습

    이 외에도 GPU 메모리 확보를 위해 추가적인 전략(모델의 일부를 Freezing + 파라미터 조정)

## 4. Model Inference Strategy
    top-k sampling, top-p sampling, temperature 방법을 이용하여 대회 조건에 맞는 문장이 생성될수있도록 파라미터 조정

# Structure

    datacrawl/*: 데이터 크롤링 코드
    preprocess.ipynb: 전처리 코드
    elastic_search.py: Elastice Search 코드
    text_generation/train.py: 모델 학습 코드
    text_generation/inference.py: 텍스트 생성 (추론)코드
    text_generation/inference_loop.py: 짧은 텍스트를 연달아 생성하는 (추론)코드

### Team 당당!
# 👀 팀 소개-

    * **김서윤** - *Data Preprocess + Writing* - (tjdbs0626@gmail.com)
    * **김효정** - *Data Crawling + Writing* - (hyojeong9888@gmail.com)
    * **이상민** - *Fine-Tuning + Model Training* - (l.alex6095@gmail.com)
    * **이창훈** - *Writing* - (rheasis0115@gmail.com)






