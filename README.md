### Amharic Sentiment Classification

The following models were finetuned using the [amharic-sentiment](https://huggingface.co/datasets/rasyosef/amharic-sentiment) dataset. The *finetuning notebooks* can be found in the `notebooks` folder. 

The reported precision, recall, and f1 metrics are macro averages.

|Model|Size (# params)| Accuracy | Precision | Recall | F1 |
| --- | ------------- | -------- | --------- | ------ | -- |
|[roberta-base-amharic](https://huggingface.co/rasyosef/roberta-base-amharic)|110M|**0.88**|**0.88**|**0.88**|**0.88**|
|[bert-medium-amharic](https://huggingface.co/rasyosef/bert-medium-amharic)|40.5M|0.83|0.83|0.82|0.83|
|[bert-small-amharic](https://huggingface.co/rasyosef/bert-small-amharic)|27.8M|0.83|0.83|0.82|0.83|
|[bert-mini-amharic](https://huggingface.co/rasyosef/bert-mini-amharic)|10.7M|0.81|0.81|0.81|0.81|
|[bert-tiny-amharic](https://huggingface.co/rasyosef/bert-tiny-amharic)|4.18M|0.79|0.79|0.79|0.79|
|[xlm-roberta-base](https://huggingface.co/FacebookAI/xlm-roberta-base)|279M|0.83|0.83|0.83|0.83|
|[afro-xlmr-base](https://huggingface.co/Davlan/afro-xlmr-base)|278M|0.83|0.83|0.83|0.83|
|[afro-xlmr-large](https://huggingface.co/Davlan/afro-xlmr-large)|560M|0.86|0.86|0.86|0.86|
|[am-roberta](https://huggingface.co/uhhlt/am-roberta)|443M|0.82|0.83|0.82|0.82|

### Fine-tuned Model
A finetuned `bert-medium-amharic` model is available on HuggingFace:

[rasyosef/bert-medium-amharic-finetuned-sentiment](https://huggingface.co/rasyosef/bert-medium-amharic-finetuned-sentiment)

#### How to use
You can use the model directly with a pipeline for text classification:

```python
>>> from transformers import pipeline
>>> bert_sentiment = pipeline("text-classification", model="rasyosef/bert-medium-amharic-finetuned-sentiment")
>>> bert_sentiment(["አሪፍ ፊልም ነው።", "ዩክሬን እና ሩስያ ከባድ ውግያ ላይ ናቸው።"])

[{'label': 'positive', 'score': 0.9863048791885376},
 {'label': 'negative', 'score': 0.9570127129554749}]
```

### References

[Fine-tuning a model with the Trainer API](https://huggingface.co/learn/nlp-course/chapter3/3?fw=pt)
