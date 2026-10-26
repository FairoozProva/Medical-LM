Medical LLM Fine-tuning with QLoRA (Unsloth)

This project fine-tunes a 4-bit quantized DeepSeek-R1-Distill-Llama-8B model on clinical question-and-answer data from the medical-o1-reasoning-SFT dataset. It uses Unsloth for memory-efficient training, a rank-16 LoRA adapter on all projection layers (0.52% of parameters trainable), and runs on a single free Google Colab T4 GPU, peaking at about 7.2 GB of memory.

The notebook covers model loading, adapter setup, dataset formatting, epoch-based training, saving the adapter, and comparing the base model with the fine-tuned model on a set of medical questions. Results are modest: on an 8-question keyword checklist, the fine-tuned model did not beat the base model, and some diagnoses are incorrect. This is a learning prototype and not suitable for clinical use.
