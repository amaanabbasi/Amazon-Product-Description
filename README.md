# Amazon product description generator for [texta.ai](https://texta.ai)
[Video tutorial](https://www.youtube.com/watch?v=GzHJ3NUVtV4)

Everything is not so difficult. First, let's download the required library.

```
$ pip install happytransformer
```

We connect this library and load the selected model, pointing to it the path in the directory. [drive](https://drive.google.com/drive/folders/1a4SclxrGzdjrNlG4sUT3Wzpyn8qqxWLu?usp=sharing) 

from happytransformer import HappyGeneration `directory`.

```python
from happytransformer import HappyGeneration

happy_gen = HappyGeneration(load_path="/content/drive/MyDrive/GPT-Neo_Amazon/3/")
```

Next, you can set the generation settings. If everyone has questions about what these settings are, then you can see them[here](https://happytransformer.com/text-generation/settings/).

```python
min_length =  10
max_length = 100 
do_sample = True
early_stopping = True
num_beams = 1 
temperature = 0.6
top_k = 50
top_p = 0.8
no_repeat_ngram_size = 1

gen_args = GENSettings(min_length, max_length, do_sample, early_stopping, num_beams, temperature, top_k, no_repeat_ngram_size, top_p)
```
To generate, we run the following function, where `text` is the prompt we are using. Examples of these can be found in the Test Model tab of this file. The result of the generation is in `result.text`.

```python
result = happy_gen.generate_text(text, args=gen_args)

print(result.text)
```

Look like that's it. Thank you for your attention.
