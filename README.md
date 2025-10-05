# Generating-positive-feedbacks-for-restaurants-small-transform-model-vs-fine-tunning-Qwen3-
Collected almost 16,000 positive feedbacks from restaurants more than 4.7(out of 5) score (Russian restaurants).

🍽️Restaurant Feedback Generator
the aim was to check how far can be local small transofmer model pushed with limited parameters(6.350264 M parameters in this case).
model created based on MinGPT from https://github.com/karpathy/minGPT with small changes == > karpathy Andrej
then used same dataset to fine tune Qwen3-0.6B model from https://huggingface.co/Qwen/Qwen3-0.6B for 2 Epochs 

🎯 Key Features
Automatically generate positives reviews 
