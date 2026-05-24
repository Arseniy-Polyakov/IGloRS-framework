# IGloRS framework
## Introduction
IGloRS framework is used for automatic text-to-gloss translation via GUI interface.

## Functional method
The functional method scheme is provided here:
![Link](images\functional_method_scheme.jpg)

## Experiments
### Training arguments for encoder-decoder models are shown here: 

| Hyperparameter                 | Value |
|--------------------------------|-------|
| Train batch size               | 1     |
| Gradient accumulation steps    | 4     |
| Epochs                         | 10    |
| Learning rate                  | 2e-5  |
| Optimizer                      | Adafactor |

### Experimental results with various encoder-decoder models are provided here:

| Model                              | BLEU-1 | BLEU-2 | BLEU-3 | BLEU-4 |
|-------------------------------------|--------|--------|--------|--------|
| google/byt5-small                   | 0.3182 | 0.0963 | 0.0371 | 0.0040 |
| Helsinki-NLP/opus-mt-ru-en          | 0.6588 | 0.4165 | 0.2697 | 0.1325 |
| facebook/nllb-200-distilled-600M    | 0.8815 | 0.7640 | 0.6589 | 0.4434 |
| facebook/mbart-large-50             | 0.9103 | 0.8395 | 0.7500 | 0.5179 |
| facebook/m2m100_418M                | **0.9427** | **0.8891** | **0.8119** | **0.5819** |