# LLM-for-User-Intent
## A Population-to-individual Tuning Framework for Adapting Pretrained LM to On-device User Intent Prediction
### KDD 2024 ACCEPTED
This repository is the official PyTorch implementation for the paper: A Population-to-individual Tuning Framework for Adapting Pretrained LM to On-device User Intent Prediction
## Framework
![OverallFramework](https://github.com/zhazhahui7//LLM-for-User-Intent/blob/main/Figs/Framework.png "Overall framework")


Mobile devices, especially smartphones, can support rich functions and have developed into indispensable tools in daily life. With the rise of generative AI services, smartphones can potentially transform into personalized assistants, anticipating user needs and scheduling services accordingly. Predicting user intents on smartphones, and reflecting anticipated activities based on past interactions and context, remains a pivotal step towards this vision. Existing research predominantly focuses on specific domains, neglecting the challenge of modeling diverse event sequences across dynamic contexts. Leveraging pre-trained language models (PLMs) offers a promising avenue, yet adapting PLMs to on-device user intent prediction presents significant challenges. To address these challenges, we propose PITuning, a Population-to-Individual Tuning framework. PITuning enhances common pattern extraction through dynamic event-to-intent transition modeling and addresses long-tailed preferences via adaptive unlearning strategies. Experimental results on real-world datasets demonstrate PITuning’s superior intent prediction performance, highlighting its ability to capture long-tailed preferences and its practicality for on-device prediction scenarios.

## Installation
### Environment
- Tested OS: Linux
- Pytorch == 1.8.0
- Python  >= 3.8.10
- mlflow >= 2.2.2
- numpy >= 1.23.5
- pandas >= 2.0.0
- transformers >= 4.28.1

### Pretrained Language Model
GPT2-small can be downloaded from [HERE](https://huggingface.co/openai-community/gpt2).

## Code
The code is under internal review, coming soon.

## Dataset
Here we provide the Mobile dataset for reproducibility. As for the Honor dataset, we are currently implementing additional measures to ensure compliance with disclosure requirements. 

## Training
### Population level
 `python main_pretrain.py`
 ### Model Distilling
 `python main_distilling.py`
 ### Individual level
 `python main_unlearning_finetune.py`

## Performance
- Our framework steadily achieves the best performance.
- Our model has the smallest difference between weighted metrics and macro metrics.
- The method of LLM-based model with device-cloud collaboration is necessary for user behavior modeling.
![OverallPerformance](https://github.com/zhazhahui7//LLM-for-User-Intent/blob/main/Figs/overall_performance.png "Overall performance")

## License
The software in this repository is freely available under MIT license.

