# Portugal SQUADv1 model

## MODEL DESCRIPTION
ISEL NLP course 2023/2024 fall semester.
Portugal BERT base model (cased) fine-tuned on SQuAD v1 Portugal version.

## Model in action

- Fast usage with pipelines:

```python
from transformers import pipeline
qa_pipeline = pipeline(
    "question-answering",
    model="isel-nlp-mp05/bert-base-portuguese-cased-finetuned-squadv1-pt",
    tokenizer="isel-nlp-mp05/bert-base-portuguese-cased-finetuned-squadv1-pt"
)
predictions = qa_pipeline({
    'context': "Chamo-me Mattheo e estou a estudar em Lisboa.",
    'question': "Onde é que o Mattheo está a estudar?"
})
print(predictions)
# output:
# {'score': 0.967152, 'start': 38, 'end': 44, 'answer': 'Lisboa'}
```
