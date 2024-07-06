# SuteAlbastre-at-SemEval-2024-Task4
This Github repository contains all algorithms and models used by the SuteAlbastre team at SemEval 2024 - Task4

The final submission paper: https://aclanthology.org/2024.semeval-1.68.pdf
---

### Abstract

The main goal of this year's SemEval Task $4$ is detecting the presence of persuasion techniques in various meme formats. While **Subtask 1** targets text-only posts, **Subtask 2**, subsections **a** and **b** tackle posts containing both images and captions. The first $2$ subtasks consist of **multi-class** and **multi-label** classifications, in the context of a **hierarchical** taxonomy of $22$ different persuasion techniques. 

The last subtask represents a binary classification, signifying the presence or absence of at least one of the proposed persuasion techniques.

This paper proposes a solution for persuasion detection in both these scenarios and for various languages of the caption text. Our team's main approach consists of a Multimodal Learning Neural Network architecture, having Textual and Vision Transformers as its backbone.

---

### System Description

**Subtask 1**: We fine-tuned a BERT model on the provided data.

**Subtask 2a**: The backbone of our solution is a BERT + ViT architecture where the BERT based model creates embeddings from the text data while the ViT creates features from the image data, we concatenate the two embeddings and the resulting one is passed to a Fully connected Layer to obtain the scores for each propaganda method.

**Subtask 2b**: We used a similar architecture to Subtask 2a but where the final Fully Connected Layer does a binary classification on whether the provided meme is propagandistic or non-propagandistic.

<img src="https://github.com/IonutAnghelina/SuteAlbastre-at-SemEval-2024-Task4/assets/46871581/05e0301b-bd54-4e7f-a4f4-3d75e69d2889" width="500">


---

### Citation

```
@inproceedings{SuteAlbastreSemeval2024task4, 
	title={SuteAlbastre at SemEval-2024 Task 4: Predicting Propaganda Techniques in Multilingual Memes using Joint Text and Vision Transformers },
	author={Anghelina, Ion-Marian and Buță, Gabriel-Sebastian and Enache, Alexandru},
	booktitle = {Proceedings of the 18th International Workshop on Semantic Evaluation},
	series = {SemEval 2024},
	year = {2024},
	address = {Mexico City, Mexico},
	month = {June},
	pages = {},    
	doi= {}   
}
```
