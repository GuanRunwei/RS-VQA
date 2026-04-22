# RoadSceneVQA: Benchmarking Visual Question Answering in Roadside Perception Systems for Intelligent Transportation System


Welcome to the official repository for **RoadSceneVQA**, a large-scale and richly annotated visual question answering (VQA) dataset specifically tailored for roadside scenarios]This dataset is introduced in our AAAI 2026 paper: *"RoadSceneVQA: Benchmarking Visual Question Answering in Roadside Perception Systems for Intelligent Transportation System"*.

🔗 **Dataset Link**: [baidu disk download link](https://pan.baidu.com/s/1D3MZLe4cQff52DVti7Kr0w)      Password: 48a8

## 💡 Introduction

Current roadside perception systems mainly focus on instance-level perception, which fall short in enabling interaction via natural language and reasoning about traffic behaviors in context. To bridge this semantic gap, we introduce **RoadSceneVQA**.

Unlike existing benchmarks that merely measure perceptual accuracy, RoadSceneVQA challenges models to perform both explicit recognition and implicit commonsense reasoning, grounded in real-world traffic rules and contextual dependencies. It shifts traffic intelligence evaluation from simple perceptual recognition to regulation-aware cognitive reasoning from a roadside view.

## 📊 Dataset Features

  ***Large Scale**: The dataset comprises a total of **34,736** diverse QA pairs.
  * **Data Split**: It includes 30,058 samples for the training set and 4,677 samples for the test set.
  * **Diverse Conditions**: QA pairs are collected under varying weather, illumination, and traffic conditions.
  * **Comprehensive Reasoning**: Targets not only object attributes but also the intent, legality, and interaction patterns of traffic participants. For example, it demands models to answer complex compliance judgments like "Is the pedestrian violating traffic rules given current signal states and crosswalk topology?".
  * **High-Quality Annotation**: Constructed using an agile Collaborative Human-Machine Annotation (CH-MA) system, which combines the expansive reasoning space of MLLMs (QwenVL-Max) with rigorous manual correction and semantic objectivity assessment by human panels.
  * **Foundation Data**: Leverages the rich object distributions and contextual diversity of the Rope3D dataset.

## 🧠 Baseline Model: RoadMind

Alongside the dataset, we propose **RoadMind**, a multi-modal large language model specifically tailored for roadside traffic perception and reasoning.

RoadMind integrates two key innovative components:

1.  **CogniAnchor Fusion (CAF)**: A plug-and-play visual-language fusion module inspired by human-like scene anchoring mechanisms. It pre-anchors potential regions of interest and enables the LLM to reason precisely and efficiently.
2.  **Assisted Decoupled Chain-of-Thought (AD-CoT)**: A novel method designed to enhance reasoned thinking via CoT prompting and multi-task learning, supporting reliable scene understanding on lightweight edge MLLMs.

Experiments show that RoadMind achieves state-of-the-art performance in structural traffic perception and reasoning tasks across both RoadSceneVQA and CODA-LM benchmarks.

## 📁 Dataset Structure

*(Note: Please update the directory structure based on your actual data release format)*

```text
RoadSceneVQA/
├── img_pool/                  # Roadside camera images (resized to 448x448 for training) 
├── rope3d_merged_sft_data.json   # 30,058 QA pairs for training
├── test_sft_data.json    # 4,677 QA pairs for testing
```

## 📝 Citation

If you find our dataset or models useful in your research, please consider citing our work:

```bibtex
@inproceedings{DBLP:conf/aaai/GuanHCXXLCTOLFS26,
  author       = {Runwei Guan and
                  Rongsheng Hu and
                  Shangshu Chen and
                  Ningyuan Xiao and
                  Xue Xia and
                  Jiayang Liu and
                  Beibei Chen and
                  Ziren Tang and
                  Ningwei Ouyang and
                  Shaofeng Liang and
                  Yuxuan Fan and
                  Wanjie Sun and
                  Yutao Yue},
  editor       = {Sven Koenig and
                  Chad Jenkins and
                  Matthew E. Taylor},
  title        = {RoadSceneVQA: Benchmarking Visual Question Answering in Roadside Perception
                  Systems for Intelligent Transportation System},
  booktitle    = {Fortieth {AAAI} Conference on Artificial Intelligence, Thirty-Eighth
                  Conference on Innovative Applications of Artificial Intelligence,
                  Sixteenth Symposium on Educational Advances in Artificial Intelligence,
                  {AAAI} 2026, Singapore, January 20-27, 2026},
  pages        = {4366--4375},
  publisher    = {{AAAI} Press},
  year         = {2026},
  url          = {https://doi.org/10.1609/aaai.v40i6.42434},
  doi          = {10.1609/AAAI.V40I6.42434},
  timestamp    = {Wed, 08 Apr 2026 16:53:54 +0200},
  biburl       = {https://dblp.org/rec/conf/aaai/GuanHCXXLCTOLFS26.bib},
  bibsource    = {dblp computer science bibliography, https://dblp.org}
}
```
