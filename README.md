# keyphrase-data-labelling-with-openai-api


## Dev Objective

- portal_news_scraper DB의 최신 기사 5만건을 가져와 GPT 3.5 Turbo를 활용해 key-phase 생성 모델 훈련을 위한 데이터셋을 구축합니다.


## Progress

### Samples from DB
- 최초 30만건 추출
- 전처리를 거쳐 총 100886건의 raw data 확보
  - new-line 캐릭터 및 공백 정리를 해주는 간단한 전처리만 수행한 뒤 제목과 본문 내용을 연결하여 title_content 생성
  - T5 tokenizer를 활용하여 토큰화한 뒤 시퀀스의 길이가 500에서 1000 사이인 샘플만 라벨링 및 훈련에 투입

### Labelling
- GPT 3.5 Turbo 프롬프트 엔지니어링을 통해 raw data의 샘플에 대한 key-phrases를 생성 (구분자: '; ')
- 1000건의 샘플에 대해 시험 라벨링 진행 뒤 검토를 진행할 예정
  - 라벨 품질이 충분할 경우 총 10000건의 라벨링 데이터를 생성한 뒤 훈련을 진행할 예정