<Text 분석 이론 정리>

NLP 와 텍스트 분석의 차이

- NLP(자연어처리) : 머신이 인간의 언어를 이해하고 해석하는데 중점을 두고 기술이 발전해 왔으며, 언어를 해석하기 위한 기계번역, Chat bot 대화 등에서 텍스트 분석과는 차별점이 존재
- 텍스트 분석(텍스트 마이닝) : 비정형 텍스트에서 의미 있는 정보를 추출하는 것에 좀 더 중점을 두고 기술을 발전


[Text Analysis Type]
    
    1. 텍스트 분류 (Text Classification) : Text Categorization 이라고도 하고 문서가 특정 분류 또는 카테고리에 속하는 것을 예측하는 기법. 예를 들어 신문기사를 카테고리별로 분류하거나 스팸 메일 검출 프로그램이 이에 속한다. 지도학습으로 볼 수 있다
    
    2. 감성분석 (Sentiment Analysis) : 텍스트에서 나타나는 감정, 판단, 의견 등의 주관적인 요소를 분석하는 기법. 소셜미디어 감정분석, 제품에 대한 리뷰 등 다양한 영역에서 적용되며 Text Analytics에서 가장 활발하게 사용되고 있는 분야. 지도학습 뿐만 아니라 비지도 학습을 이용해 적용이 가능하다. 감정 Dictionary 라고 불리우는 단어에 대해 Positive / Negative를 판단하는 지표가 있으나 잘 활용 되지는 않는다. 긍정,부정, 중립 에서 더 나아가 감성을 분석.
    방법은 크게 3가지 : Knowledge-based techniques, statistical methods, hybrid approaches 가 있다. 평가는 재현율 정밀도로 보통 측정이 된다 
    *지도학습/ 비지도, SeintWordNet, VADER 학습 수행 
    
    3. 텍스트 요약 (Summarization) : 텍스트 내에서 중요한 주제나, 중심사상을 추출하는 기법. 대표적으로 토픽 모델링이 있다. 잠재 의미 분석(LSA), 잠재 디리클레 할당 (LDA) 같은 분석이 있다. 사이킷런의 LDA 기반의 토픽모델링을 LatentDifichletAllocation클래스 제공.
    
    4. 텍스트 군집화 (Clustering) 와 유사도 측정 : 비슷한 유형의 문서에 대해 군집화를 수행하는 기법. 텍스트 분류를 비지도 학습으로 수행하는 방법 중 하나로 볼 수 있고, 유사도 측정 역시 문서들간의 유사도를 측정하여 문서끼리 모을 수 있는 방법. ex. 코사인 유사도 - 비슷한 유사도 찾기, Kmeans 이용
    
    
[Text Analysis Package]
    
    1. NLTK : 가장 대표적인 NLP 패키지, 아카데미 적인 성격인 강하고 NLP 패키지의 시조새! 패키지의 용량도 방대하다. 실제 분석 시에는 잘 사용하지는 않는다. 
    2. Gensim
    3. SpaCy
    4. 케라스, 파이토치, 텐서 플로우 .... 
    
    
[Text Analysis Process]
    
    1. 텍스트 사전 준비작업 (전처리 작업)
    2. 피처 벡터화/추출
    3. ML모델 수립 및 학습
    

[Text Preprocessing]
    
    1. 클렌징 (대/소문자 변경, 특수문자 삭제 등)
    2. 토큰화 (문장 토큰화, 단어 토큰화)
    3. 필터링
    4. 스톱 워드 제거
    nltk.corpus.stopwords.words('english')
    5. 철자수정
    6. Stemming : 원형 단어로 변환 시 일반적인 방법을 적용
    7. Lemmatization : 품사와 같은 문법적인 요소와 더 의미적인 부분을 감안해 정환한 철자로 된 어근 단어를 찾아주는 
    
[BOW] : 카운트 기반의 벡터화, TF-IDF 기반의 벡터화 
    
   
