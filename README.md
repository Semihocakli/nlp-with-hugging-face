
# Natural Language Processing With Hugging Face

## Yol haritası

- [Transformer Mimarisine Giriş](https://github.com/Semihocakli/nlp-with-hugging-face/tree/main/01)

- [Duygu Analizi Çıkarımı Projesi](https://huggingface.co/ocaklisemih/distilbert-emotion)

- [Token Sınıflandırma (NER) Projesi](https://huggingface.co/ocaklisemih/multilingual-xlm-roberta-for-ner)

- [Metin Üretme Projesi](https://github.com/Semihocakli/nlp-with-hugging-face/tree/main/4.)

- [LLM Projesi](https://huggingface.co/ocaklisemih/mistral-7b-dolly)

## DistilBERT Emotion Recognition Model

Bu Hugging Face modeli, duyguları tanımlamak için DistilBERT modelini kullanır. Model, metin girdisine dayalı olarak duyguları tahmin etme yeteneğine sahiptir.

### Kullanım

Modeli kullanmak için aşağıdaki adımları takip edebilirsiniz.

```python
from transformers import pipeline

# Duygu tanıma modelini yükle
emotion_model = pipeline("sentiment-analysis", model="ocaklisemih/distilbert-emotion")

# Metin üzerinde duyguyu tahmin et
text = "Bugün harika bir gün!"
emotion = emotion_model(text)

print(emotion)
```
---

## NER Demo

Bu demo için Spaces üzerinde çalıştırmak için aşağıdaki adımları izleyebilirsiniz.

1. Spaces sayfasına gidin: [NER-Demo](https://huggingface.co/spaces/ocaklisemih/NER-Demo)

2. Demo alanını açmak için "NER-Demo" düğmesine tıklayın.

3. Demo başladığında, metin girişi yaparak NER modelini deneyebilirsiniz.

### Örnek Kullanım

Demo alanını kullanmak için gerekli adımlar Spaces üzerinde otomatik olarak yapılmaktadır. Ancak, modeli yerel olarak kullanmak istiyorsanız, şu örnek kullanımı inceleyebilirsiniz:

```python
from transformers import pipeline

# NER modelini yükle
ner_model = pipeline("ner", model="ocaklisemih/ner-demo")

# Metin üzerinde adlandırılmış varlıkları tanımla
text = "Hugging Face, yapay zeka alanında öncü bir şirkettir."
entities = ner_model(text)

print(entities)
```
---

## Multilingual XLM-RoBERTa for Named Entity Recognition (NER)

Bu Hugging Face modeli, çok dilli metinler üzerinde adlandırılmış varlık tanıma (NER) görevi için XLM-RoBERTa modelini kullanır. Model, farklı dillerdeki metinlerdeki adlandırılmış varlıkları tanımlama yeteneğine sahiptir.

### Kullanım

Modeli kullanmak için aşağıdaki adımları takip edebilirsiniz.

```python
from transformers import pipeline

# NER modelini yükle
ner_model = pipeline("ner", model="ocaklisemih/multilingual-xlm-roberta-for-ner")

# Metin üzerinde adlandırılmış varlıkları tanımla
text = "Hugging Face, yapay zeka alanında öncü bir şirkettir."
entities = ner_model(text)

print(entities)
```
---
## Mistral-7B-Dolly: Turkish Language Model

Bu Hugging Face modeli, Türkçe dilinde geniş bir dil modeli olan Mistral-7B-Dolly'yi içermektedir.

### Kullanım

Modeli kullanmak için aşağıdaki adımları takip edebilirsiniz.

```python
from transformers import pipeline

# Dil modelini yükle
language_model = pipeline("text-generation", model="ocaklisemih/mistral-7b-dolly")

# Metin üret
generated_text = language_model("Merhaba, bu bir örnek metindir. ")
print(generated_text)
```
