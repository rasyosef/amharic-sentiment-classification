### Amharic Sentiment Classification

The following models were finetuned using the [amharic-sentiment](https://huggingface.co/datasets/rasyosef/amharic-sentiment) dataset. The *finetuning notebooks* can be found in the `notebooks` folder. 

The reported precision, recall, and f1 metrics are macro averages.

|Model|Size (# params)| Accuracy | Precision | Recall | F1 |
| --- | ------------- | -------- | --------- | ------ | -- |
|[bert-medium-amharic](https://huggingface.co/rasyosef/bert-medium-amharic)|40.5M|0.83|0.83|0.82|0.83|
|[bert-small-amharic](https://huggingface.co/rasyosef/bert-small-amharic)|27.8M|0.83|0.83|0.82|0.83|
|[bert-mini-amharic](https://huggingface.co/rasyosef/bert-mini-amharic)|10.7M|0.81|0.81|0.81|0.81|
|[bert-tiny-amharic](https://huggingface.co/rasyosef/bert-tiny-amharic)|4.18M|0.79|0.79|0.79|0.79|
|[xlm-roberta-base](https://huggingface.co/FacebookAI/xlm-roberta-base)|279M|0.83|0.83|0.83|0.83|
|[am-roberta](https://huggingface.co/uhhlt/am-roberta)|443M|0.82|0.83|0.82|0.82|