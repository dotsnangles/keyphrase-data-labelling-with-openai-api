# keyphrase-data-labelling-with-openai-api


## Dev Objective

- portal_news_scraper DB의 최신 기사 5만건을 가져와 GPT 3.5 Turbo를 활용해 key-phase 생성 모델 훈련을 위한 데이터셋을 구축합니다.


## Progress

- 최신 기사 5만건 추출 후 제목이 중복되는 데이터 삭제
- 모델의 입력으로 사용할 신문기사의 적절한 길이 조사 중
- 라벨링을 위한 전처리 계획 중
- 훈련 데이터의 입력으로 제목과 본문 내용을 사용할 계획
- 토큰화 후 시퀀스의 길이가 500~1000 사이인 샘플만 훈련에 사용
- 제목과 본문 앞뒤의 공백 제거 외 정제를 진행하지 않음 (PLM 모델 사전학습 데이터의 전처리 고려)