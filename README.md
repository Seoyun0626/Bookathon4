# 💻2021 SKKU AI x Bookathon 4rd📚


## 1. Introduction
Book(책)과 Hackathon(해커톤)의 합성어로 인간과 AI가 협업하여 글을 쓰는 대회

성균관대학교에서 주최하는 AI x Bookathon 대회로 인공지능 모델을 사용하여 주제가 '대담한'인 수필을 작성하는 것이 목적


### 🏆 reward

📖"6월의 피는 한련화"라는 제목을 가진 수필을 생성하여 본선에서 장려상 수상

[>> 발표자료 보러가기](./당당!_발표자료.pdf)

[>> 최종작품 보러가기](./당당!_6월의%20피는%20한련화.pdf)


## 1차 예선 -> 인공지능 관련 시험
    2번의 사전교육과정을 수행한 후  gpt와 여러가지 ai와 관련한 객관식, 주관식, T/F문제를 풀어서 예선통과
    다른 팀들의 답변과의 차별성을 두기위해 답변에 틀린 이유를 근거로 작성하는 것과 추가설명을 위한 그림을 첨부
    예선 과정을 통해서 이 대회에서 어떠한 것을 활용하여 어떠한 결과물을 도출해야할지 숙지하고 이해
    
    
## 2차 본선
    2차 본선은 오후 3시부터 시작하여 다음날 오전11시까지 총 21시간동안 무박 2일로 진행
    성균관 대학교 삼성학술정보관에서 각 팀들이 모여서 진행
    수필의 키워드 발표 후 각 팀들이 모여 어떠한 주제를 발표할지 회의 후 각 팀마다 팀 소개 후 
    본격적인 수필작성을 위한 팀별 활동 시작
    주제 선정 후 이와 관련된 데이터를 추가적으로 크롤링 후 데이터 전처리 후 
    모델을 추가적으로 학습시켜 원하는 문장이 생성될 수 있도록 함
    한 명이 서버에 접속하여 글을 쓰기에는 시간이 부족할 것이라고 판단하여 모델이 일부를 freezing시켜 
    GPU데이터 확보 하여 여러 명이 서버에 접속하여 글을 쓸 수 있도록 함


## 2. Data Preprocessing Strategy
    대회 키워드를 알기 전에는 브런치(감성 ESSAY), 신춘문예, 글틴에서 크롤링 대회 키워드를 알고 난 후는 주제에 적합한 데이터 추가적 크롤링
    크롤링한 데이터(.txt)를 파일 형식 변환 후(.json) 정규화 표현을 이용한 기계전처리 후 세밀한 전처리를 위해 사람 전처리 과정을 통하여 데이터 정제
    ![데이터 전처리](https://user-images.githubusercontent.com/104416283/213632907-26d485e7-a044-4b31-b58f-78facfe19ac2.PNG)
    ![.txt -> .json 형식변환](https://user-images.githubusercontent.com/104416283/213633422-38fa96d3-3cf4-444c-aa85-6e53a64a042b.PNG)


## 3. Model Training Strategy
    마인즈랩에서 제공하는 사전학습된 GPT3 모델을 사용하는 대신, EleutherAI/polyglot-ko-1.3b5를 한 번 더 사전학습을 진행한 후 
    fine-tuning 하는 방법으로 생성 모델을 학습
    ![모델 학습](https://user-images.githubusercontent.com/104416283/213633570-19530ccc-1e7b-4a86-b16d-4859642c4a3c.PNG)

    GPU 메모리 확보를 위한 전략
    1. Gradient Checkpointing
    2. 8-bit optimizer
    3. Gradient Accumulation
    4. Mixed/Half precision
    ![GPU메모리 확보 전략](https://user-images.githubusercontent.com/104416283/213633577-15a490e2-57a7-432c-a66d-7f27549d5799.PNG)
    


## 4. Model Inference Strategy
    top-k sampling, top-p sampling, temperature 방법을 이용하여 대회 조건에 맞는 문장이 생성될수있도록 파라미터 조정


# 👀 팀 소개-

    * **김서윤** - *Data Preprocess + Writing* - (tjdbs0626@gmail.com)
    * **김효정** - *Data Crawling + Writing* - (hyojeong9888@gmail.com)
    * **이상민** - *Fine-Tuning + Model Training* - (l.alex6095@gmail.com)
    * **이창훈** - *Writing* - (rheasis0115@gmail.com)
    

## 🙋‍♀️소감
    인공지능을 학습시켜 글을 생성하고 최상의 글을 쓰기 위해 인간의 개입이 들어가 결국 인간과 AI가 협업한다는 것이 흥미로운 경험이었다.
    
    
    처음에는 팀원 한명이 서버에 접속하여 글을 집중적으로 작성하고 나머지는 다음 소제목을 구성하고 내용을 구성하였지만 
    팀원 한명만 서버에 접속하면 2만자라는 분량을 채우기 힘들 것이라고 판단하여 모델을 freezing을 사용하여 GPU확보 후 
    팀원 3명이서 글을 작성했기에 분량을 채울 수 있었다고 생각하고 이 과정에서 freezing해야겠다는 판단이 중요했다고 생각한다.
    
    또한 주제가 정해진 후에 인공지능이 팀에서 원하는 내용을 생성하기 위해서 추가적을 데이터를 수집해야겠다는 판단을 했는데
    주제와 관련된 데이터를 추가적으로 수집하여 학습시켰기때문에 인공지능이 팀에서 요구하는 내용을 도출할 수 있었다고 생각하여
    이 판단이 최상의 결과물이 나올 수 있는 결정적인 이유라고 생각한다.
    
    잠을 자지않고 밤새 팀원 모두가 글을 쓰느라 마지막에는 힘들어했지만 서로 응원하고 할 수 있다고 계속 생각한 덕분에
    마지막까지 지치지않고 글을 쓸 수 있었다고 생각한다.
    
    장려상을 수상해서 행복하고, 우리 팀원 모두에게 감사하다❤❤!!






