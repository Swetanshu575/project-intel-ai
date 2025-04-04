🧠 Fine-Tuning LLaMA 3 Vision Model for Radiology Image Captioning
This project fine-tunes the unsloth/Llama-3.2-11B-Vision-Instruct model to describe medical images (X-rays) using a small radiology dataset. The goal is to train a vision-language model to accurately generate captions for radiology images, simulating the expertise of a radiographer.

🖼️ Project Objective
"You are an expert radiographer. Describe accurately what you see in this image."

Using this instruction, the model is trained to produce expert-level descriptions of X-ray images.

📦 Dataset
Name: unsloth/Radiology_mini (from Hugging Face)

Contains: Medical images with descriptive captions

Format: Each sample includes:

An X-ray image

A textual description (caption)

🔧 Model Setup
Base Model: unsloth/Llama-3.2-11B-Vision-Instruct

Frameworks Used:

transformers

datasets

unsloth

trl (for SFT - Supervised Fine-Tuning)

PEFT: LoRA-based fine-tuning applied to both vision and language layers

🚀 Steps Performed
Model Loading: Load the Unsloth LLaMA-3 Vision model in 4-bit with gradient checkpointing.

Dataset Loading: Import the mini radiology dataset.

Conversion to Chat Format: Each example is converted to a conversation (instruction + image).

Pre-training Evaluation: Test the model’s generation before training.

Training Setup: Prepares the model for supervised fine-tuning (SFT).

Training (not fully included): Setup for SFTTrainer is partially visible.

🛠️ Installation
bash
Copy
Edit
pip install unsloth
pip install transformers datasets trl
📌 To Do
 Complete SFTTrainer setup and run fine-tuning

 Add evaluation metrics (BLEU, ROUGE)

 Deploy the model via API or web app

 Explore full radiology dataset

📜 License
This project is intended for research and educational purposes only. Ensure you follow any dataset-specific license agreements.

Would you like me to generate a requirements.txt or refactor this into a Python script too? ​​







