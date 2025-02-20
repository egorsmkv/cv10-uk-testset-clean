# The cleaned Common Voice 10 (test set) that has been checked by a human for Ukrainian

## Overview

This repository contains the archive of CV10 (test set) with checked Ukrainian transcriptions and audios. All audios have been checked by a human to be sure that they are correct. 

This archive is used to test all ASR models listed here: https://github.com/egorsmkv/speech-recognition-uk

## Hugging Face dataset

- URL: https://huggingface.co/datasets/Yehor/cv10-uk-testset-clean

### Usage

Example with `datasets`:

```python
from datasets import load_dataset

ds = load_dataset('Yehor/cv10-uk-testset-clean', 'train')

print(ds)
```

Example with `polars`: https://colab.research.google.com/drive/1upeXw3WbLjK37b1LetpM0HxFXDdOZqSK?usp=sharing

## Download

Duration: 4.6 hours

- Rows list: https://github.com/egorsmkv/cv10-uk-testset-clean/blob/main/rows.lst
- The archive: https://github.com/egorsmkv/cv10-uk-testset-clean/releases/download/v1.0/filtered-cv10-test.zip
