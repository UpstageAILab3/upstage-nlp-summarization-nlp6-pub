# DialoguSum summarization competition 

DialogSum 데이터의 dialogue와(한국어 대화문) summary(한국어 요약문)를 학습한 모델로     summarization model 만들고 평가하기.
  
# Data len
  
train : 12457, dev : 499, test : 250, hidden-test : 249

# Data columns

fname : 대화 고유번호 입니다. 중복되는 번호가 없습니다.

dialogue : 최소 2명에서 최대 7명이 등장하여 나누는 대화 내용입니다. 각각의 발화자를 구분하기 위해#Person”N”#: 을 사용하며, 발화자의 대화가 끝나면 \n 으로 구분합니다. 이 구분자를 기준으로 하여 대화에 몇 명의 사람이 등장하는지 확인해보는 부분은 EDA 에서 다루고 있습니다.

summary : 해당 대화를 바탕으로 작성된 요약문입니다.

# Evaluation Metric

Final Score
=Sum{Sum(ROUGE-1-F1(pred,gold)+Sum(ROUGE-2-F1(pred,gold))+Sum(ROUGE-L-F1(pred,gold)}/Data len(N)

