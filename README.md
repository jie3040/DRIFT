# DRIFT
Code for paper "DRIFT: Difference-aware Reinforcement through Iterative Fine-Tuning for Language Model"

![image](https://github.com/jie3040/DRIFT/blob/main/figures/DRIFT.png)


## 1. Environment
```
pip install -r requirements.txt
```

## 2. Data

The dataset has been organized in following structure:

```bash
./benchmarking
├── datasets
│   ├── general_eval
│   │       ├── gsm8k
│   │       ├── hellaswag
│   │       ├── mmlu
│   │       ├── truthfulQA
│   │       └── winogrande 
│   └── summary
│           ├── chunk
│           ├── CNewsSum
│           ├── lcsts
│           ├── Samsung
│           └── XSum 
├── evaluation.py
├── __init__.py
└── rouge.py
```

## 3. Experiments
Note that all the examples are running based on Qwen2.5-3B-Instruct.

### 3.1 SFT Epoch 1
```bash
bash scripts/SFT/sft_1_epoch.sh
```
```bash
bash scripts/general_eval.sh
bash scripts/summary_eval.sh
```
### 3.2 SFT Epoch 2
```bash
bash scripts/SFT/sft_2_epoch.sh
```
```bash
bash scripts/general_eval.sh
bash scripts/summary_eval.sh
```
### 3.3 DRIFT Iteration 1
```bash
bash scripts/DRIFT/drift_iteration_1.sh
```
```bash
bash scripts/general_eval.sh
bash scripts/summary_eval.sh
```
### 3.4 DRIFT Iteration 2
```bash
bash scripts/DRIFT/drift_iteration_2.sh
```
```bash
bash scripts/general_eval.sh
bash scripts/summary_eval.sh
```
### 3.5 DRIFT Iteration 3
```bash
bash scripts/DRIFT/drift_iteration_3.sh
```
```bash
bash scripts/general_eval.sh
bash scripts/summary_eval.sh
```





