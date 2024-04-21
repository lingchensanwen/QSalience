# QSalience

## :star2: Introduction
QSalience introduces the first application-agnostic salience predictor for inquisitive questions. This project is fine-tuned over our newly annotated dataset of 1,766 (context, question) pairs with salience scores. We explore the usefulness of question salience in downstream applications such as TL;DR expansion.

If you find our work useful or relevant to your research, please consider citing our paper.

```
@article{wu2024questions,
  title={Which questions should I answer? Salience Prediction of Inquisitive Questions},
  author={Wu, Yating and Mangla, Ritika and Dimakis, Alexandros G and Durrett, Greg and Li, Junyi Jessy},
  journal={arXiv preprint arXiv:2404.10917},
  year={2024}
}
```

## Salience

### Data Availability
Datasets are organized as follows:
- General data: [salience](./data/salience)
- Training, validation, and testing sets: [train_val_test](./data/train_val_test)

### Installation and Usage
Go to QSalience/code for below running code. 

The codebase is actively under construction. 🚧🚧🚧 

0. Please login into huggingface before running the code as ```mistralai/Mistral-7B-Instruct-v0.2``` now requires you to approve their policy.

1. Install necessary packages:
###### Depends on your dependency package version, you may expect very minor difference on the generation.

  ```
  pip install -q -U bitsandbytes
  pip install -q -U git+https://github.com/huggingface/transformers.git
  pip install -q -U git+https://github.com/huggingface/peft.git
  pip install -q -U git+https://github.com/huggingface/accelerate.git
  pip install -q datasets scipy evaluate peft scikit-learn torch transformers wandb
  pip install -q trl
  ```
  
  
2. To run the evaluation script and reproduce our results:
   
  ```
  python evaluate_score_final.py --model_name="MODEL_NAME"
  ```
   
   Replace `MODEL_NAME` with one of the following:
   - `mistral-ins`
   - `llama2-chat`
   - `t5`
   - `tiny-llama`

3. We also provide a [quick colab running code](https://colab.research.google.com/drive/1MmZ_M7FOBcotf22j98Ov5ADsqCFaQEYz?usp=sharing)

4. Provide your text file then predict salience of your question (Coming soon)
   
### Models
Fine-tuned models are available at the following links:
- [Salience Predict Mistral-Instruct](https://huggingface.co/lingchensanwen/mistral-ins-generation-best-balanced)
- [Salience Predict Llama2-chat](https://huggingface.co/lingchensanwen/llama2-chat-generation-best-balanced)
- [Salience Predict Flan T5-base](https://huggingface.co/lingchensanwen/t5_model_1st)
- [Salience Predict Tinyllama-chat](https://huggingface.co/lingchensanwen/tiny-llama-generation-best-balanced-new)

## Answerability
Relevant data can be found here: [answerability](./data/answerability)

## Repository Status 🚧
This repository is under construction! We will soon upload the scripts required to implement the research presented in our paper.
