# Generating-positive-feedbacks-for-restaurants-small-transform-model-vs-fine-tunning-Qwen3-
Collected almost 16,000 positive feedbacks from restaurants more than 4.7(out of 5) score (Russian restaurants).

🍽️Restaurant Feedback Generator
the aim was to check how far can be local small transofmer model pushed with limited parameters(6.350264 M parameters in this case).
model created based on MinGPT from https://github.com/karpathy/minGPT with small changes == > karpathy Andrej
then used same dataset to fine tune Qwen3-0.6B model from https://huggingface.co/Qwen/Qwen3-0.6B for 2 Epochs 

🎯 Key Features

Automatically generate positives reviews 
for mini-gpt added BPETokenizerSimple which creates vocab from data (the best was 3000 vocabs) and tokenize it
also added RotaryPositionalEmbedding as its the effective way instead of The "original attention positional embedding" ==> Absolute Positions

Link to get Adapter saved parameters to load locally 
https://drive.google.com/file/d/1t6SDglyGEf09YvjMp_g9wHHkS-d3J3xq/view?usp=drive_link

Additional points:

1- Use file russian_comments_corrected-2.txt for miniGPT 

2- Use file russian_comments_corrected.txt  fpr Qwen3-Tunned

3- For miniGPT with 4080 super it took around 80-90 to train 120,000 epochs (did to be sure that cant get better result))! )

4- Fine tunning Qwen for data(which has 38296 lines) took 1 hour 25 minutes 2 epochs

as shown below the fine tunned model gives much better output (as was expected) but it was cool to try both for me!

Qwen3-Tunned output :

Очень вкусная кухня, приятная атмосфера и персонал. Всем советую!

P.S : Delicious food, pleasant atmosphere and staff. I recommend it to everyone!

mini-gpt:

Повело на вкусный завтрак у дома: теперь всегда стоит подно общаться с первого раза рождения) 
 Неплохая кухня, большой выбор блюд. Персонал - всегда прислушиваются и попахти бокалы раки хватает. 
 Сегодня они покорили, видимо уютный хамит отлично пива и отменные в обламаете в осно м дома:!!!
 
 P.S : use google translate to see the meaning but its not so good as it should be
