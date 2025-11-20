# 📘 GPT-2 Fine-Tuning — Football Dataset

This project demonstrates how to fine-tune **GPT-2** on a custom text dataset using Hugging Face Transformers. 

The model is trained on `football.txt`, a curated list of facts about football rules, famous players, and major tournaments.

## 📂 Project Structure

```text
├── finetune.py          # The main training script
├── football.txt         # Dataset (general facts & rules)
└── README.md            # Project documentation
🧠 Dataset Details
The dataset (football.txt) contains text data regarding:

Core Rules: Objectives, duration, and team structure.

Key Figures: Mentions of Lionel Messi, Cristiano Ronaldo, etc.

Competitions: FIFA World Cup, UEFA Champions League.

Gameplay elements: Tactics, VAR, and goalkeeping.

📦 Installation
1. Create a virtual environment (Windows)
Bash

python -m venv venv
venv\Scripts\activate
2. Install dependencies
Bash

pip install transformers datasets torch
▶️ Running the Fine-Tuner
Ensure football.txt is in the same folder as the script.

Run the training script:

Bash

python finetune.py
Output: The script trains for 3 epochs. Once finished, the model is saved to:

Plaintext

./finetuned-football-model
✨ Using the Trained Model
Create a new python file (e.g., run_model.py) or use a notebook to generate text:

Python

from transformers import GPT2LMHeadModel, GPT2TokenizerFast

# Load the fine-tuned model
model = GPT2LMHeadModel.from_pretrained("./finetuned-football-model")
tokenizer = GPT2TokenizerFast.from_pretrained("./finetuned-football-model")

# Define the prompt
prompt = "The FIFA World Cup is"
inputs = tokenizer(prompt, return_tensors="pt")

# Generate output
output = model.generate(
    inputs["input_ids"],
    max_length=50,
    do_sample=True,
    temperature=0.7,
    top_k=50
)

print("-" * 20)
print(tokenizer.decode(output[0], skip_special_tokens=True))
print("-" * 20)
🎯 Why This Project?
Minimal Code: Uses the Trainer API for a clean implementation.

Custom Data: Shows how to load local text files (.txt).

Beginner Friendly: Perfect for learning the mechanics of LLM fine-tuning.


---

### 💡 Optional Quick Tip for your Code
Since your `football.txt` is very small (15 lines), your model might finish training in just a few seconds. If you want the model to learn those specific sentences better, you can increase the epochs in your `finetune.py` slightly:

```python
# In finetune.py
args = TrainingArguments(
    ...
    num_train_epochs=10,  # Changed from 3 to 10 for better learning on tiny data
    ...
)
