# Workshop Spielen mit LLM part 2

In diesem Workshop lernt man: 

1. VLM (Vision-Language-Model), wie GPT-4o-mini, kennenlernen
1. Eigene Anwendung mit LLM oder VLM planen und programmieren
1. Unterschiedliche LLMs kennenlernen
1. Eventuell kann man die für Digital Humanities essentiellen Technologie wie IIIF kennenlernen 


## Beispiele

### VLM (GPT-4o-mini) und Structured Output
[Notebook-beispiel](https://colab.research.google.com/drive/1JUBrPdwjDWxceEiQ_LTj65fLHzZ7k5vh?usp=sharing)


### RAG

### Andere LLM


#### <img src="https://huggingface.co/allenai/MolmoE-1B-0924/resolve/main/molmo_logo.png" width="500">


[Notebook-Beispiel](https://colab.research.google.com/drive/1XPUyZpQJkzsosHqDO45ZWIrmnvHi0cN1?usp=sharing)

##### Zu Molmo

>Molmo is a family of open vision-language models developed by the Allen Institute for AI. Molmo models are trained on PixMo, a dataset of 1 million, highly-curated image-text pairs. It has state-of-the-art performance among multimodal models with a similar size while being fully open-source. You can find all models in the Molmo family here. Learn more about the Molmo family in our announcement blog post or the paper.
>MolmoE-1B is a multimodal Mixture-of-Experts LLM with 1.5B active and 7.2B total parameters based on OLMoE-1B-7B-0924. It nearly matches the performance of GPT-4V on both academic benchmarks and human evaluation, and achieves state-of-the-art performance among similarly-sized open multimodal models.

##### GPU 
Um ein Model Molmo (hier MolmoE 1B) auf Colaboratory zu betätigen, braucht man GPU (Tesla A100) für Runtime, weil A100 am meisten RAM hat.
Die anderen GPU haben folgende RAM-Kapazität:

- Tesla A100 : 40GB
- Tesla V100 : 16GB
- Tesla P100 : 16GB 
- Tesla K80 : 12GB

Um GPU für Runtime zu ändern: "Runtime" > "Change runtime type" > "A100"

Als ich MolmoE 1B auf Colab betätigt habe, hat das Model 34.4 GB RAM gebraucht:

![](./img/runtime_vram.png)


#### LLM durch Huggingface-PipeLine von Langchain

[Notebook-Beispiel mit Gemma](https://colab.research.google.com/drive/1kWYFrTCEpdEIULwSiJPhQEmnz9qY3IMW#scrollTo=DV7SZMtUCLXX)

[Huggingfache]() bietet sehr viele KI-Models. Diese Model kann man über Huggingface-PipeLine geholt werden.

1. Dafür zuerst einen Account von Huggingface erstellen
1. Dann ein Access-Token von Huggingface erstellen (wie unten)

<img src="./img/hf_token.png" width="500">

3. Eventuell Agreement für ein Model abschliessen (siehe unten)

<img src="./img/hf_agreement.png" width="500">


Das Access-Token in Colaboratory eingeben ... wie immer.
Danach dieses Token in Umgebungsvariable "HUGGING_FACE_HUB_TOKEN" eintragen:

```
from google.colab import userdata
import os

os.environ["HUGGING_FACE_HUB_TOKEN"] = userdata.get("[secretName von deinem Token]")
```




### Sonstige Anwendung


