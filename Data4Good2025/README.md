This is my competition entry for the data4good challenge 2025/2026. 

Task: 
Classify AI responses as factual, contradiction (false), or irrelevant based on a question, answer, and context. 

Model: 
Rather than use a pre-trained model and the standard NLP libraries (TFIDF etc), I wanted to write the functions to get a useful numerical representation of the data. I used PyTorch for modelling since I wanted to practice with this library and its logic. 

Due to class imbalances, I used a class-weighted focal loss function for training. To note, SMOTE and other over/under sampling techniques did not aid the model. The model's main issue during the final phases of testing was the close similarity between contradictions and factual responses (especially when no context was given). This can be seen since the model predicted most of the factual and irrelevant responses correctly, but the contradiction responses only correct ~50-60% of the time. 
