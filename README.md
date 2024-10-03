# Duke-AI-XAI-Assignment5
I used the **BERT model** in combination with the **SHAP** tool to generate a local interpretation of textual sentiment categorization. The specific process is as follows:

### Model loading:
I used the pre-trained **BERT model textattack/bert-base-uncased-SST-2** to categorize the sentiment of the input text. The model is specialized for binary classification tasks for positive or negative sentiment.

### Text input: 
A text “Congratulations to Duke University on its 100th anniversary! Go Blue Devils!” was input and a prediction function f(x) was defined to classify the text by the BERT model. Sentiment classification prediction.

### SHAP Interpretation Generation:
The model's predictions are interpreted using SHAP's Explainer function, which calculates the contribution of each word to the final prediction (SHAP value) The SHAP value reflects how each word contributes to or inhibits the model's positive or negative predictions.

### Visualization:
I generated three kinds of interpretation plots through SHAP's visualization tools:

**Text Interpretation Map:** shows the impact of each word on the final sentiment prediction, with red indicating a positive contribution and blue indicating a negative contribution.

**Decision diagram:** shows the gradual cumulative impact of the features (words) on the prediction, illustrating how the model arrived at the final prediction.

**Waterfall diagram:** shows in detail the gradual influence of words on the model output through the accumulation of feature contributions, visualizing the transition of the model from the baseline value to the final predicted value.

### Results: 
The baseline value of the model is -1.86255, indicating that its initial tendency is negative sentiment. With the input text, the final predicted value is -1.70586, which still favors negative emotions but is slightly more optimistic than the baseline value.




