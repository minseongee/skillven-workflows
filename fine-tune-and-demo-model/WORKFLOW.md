---
name: fine-tune-and-demo-model
description: Fine-tune an open model on Hugging Face - check the dataset, train with TRL on HF Jobs, evaluate the result and publish a Gradio demo on Spaces.
when_to_use: Adapting an open language model to a task with your own or a Hub dataset, and showing the result to others.
steps:
  - id: goal
    title: Agree on the task, base model and budget
    checkpoint: true
  - id: data
    title: Inspect the dataset
    skill: huggingface/skills/skills/huggingface-datasets
    output: the splits, size and a sample of rows, with any problems noted
  - id: train
    title: Fine-tune the model
    skill: huggingface/skills/skills/huggingface-llm-trainer
    checkpoint: true
    output: a trained model pushed to the Hub
  - id: eval
    title: Evaluate against the base model
    skill: huggingface/skills/skills/huggingface-community-evals
  - id: demo
    title: Publish a demo
    skill: huggingface/skills/skills/huggingface-spaces
---
## goal
Ask what the model should do better, which base model and dataset to start from, how the
result will be judged, and how much GPU time can be spent. Training jobs cost money: get a
clear yes before starting one.

## eval
Run the same evaluation on the base model and the fine-tuned one and report both, so the
gain (or loss) is clear.
