# The cleaned Common Voice 10 (test set) that has been checked by a human for Ukrainian

## Overview

This repository contains the archive of [CV10 (test set)][1] with checked Ukrainian transcriptions and audios. All audios have been checked by a human to be sure that they are correct. 

This archive is used to test all ASR models listed here: https://github.com/egorsmkv/speech-recognition-uk

## Hugging Face dataset

- URL: https://huggingface.co/datasets/Yehor/cv10-uk-testset-clean

### Usage

Example with `datasets`:

```python
from datasets import load_dataset

ds = load_dataset('Yehor/cv10-uk-testset-clean')

print(ds)

for row in ds['train']:
  audio = row["audio"]

  sampling_rate = audio["sampling_rate"]
  audio_bytes = audio["array"]
  filename = audio["path"]

  print(len(audio_bytes), sampling_rate, filename)
  print(row["duration"], row["transcription"])

  print('---')
```

Example with `polars`: https://colab.research.google.com/drive/1upeXw3WbLjK37b1LetpM0HxFXDdOZqSK?usp=sharing

## Google Colabs

Use the following colabs to see how you can download this dataset in Python:

`datasets`:
- https://colab.research.google.com/drive/1qqnr5-WkaJi8iqHa_Pmlx7PbbXwXiimD?usp=sharing

`polars`:
- https://colab.research.google.com/drive/1upeXw3WbLjK37b1LetpM0HxFXDdOZqSK?usp=sharing

## Statistics

## Duration statistics

Duration: 4.6 hours

| Metrics | Value |
| ------ | ------ |
| mean | 5.201474 |
| std | 1.764957 |
| min | 1.704 |
| 25% | 3.816 |
| 50% | 4.896 |
| 75% | 6.384 |
| max | 10.536 |

## Download from GitHub

We recommend to use Hugging Face dataset, but in case you need raw dataset, use:

- Audio data: https://github.com/egorsmkv/cv10-uk-testset-clean/releases/download/v1.1/filtered-cv10-test.zip

- Labels list (TAB format) with absolute paths: https://github.com/egorsmkv/cv10-uk-testset-clean/blob/main/labels_absolute.lst
- Labels list (CSV format) with absolute paths: https://github.com/egorsmkv/cv10-uk-testset-clean/blob/main/labels_absolute.csv
- Labels list (CSV format) with relative paths: https://github.com/egorsmkv/cv10-uk-testset-clean/blob/main/labels_relative.csv

[1]: https://huggingface.co/datasets/mozilla-foundation/common_voice_10_0
