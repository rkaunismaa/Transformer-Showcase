# Transformer-Showcase
What can be done with a Vaswani Transformer other than translation?

## Thursday, May 25, 2023

This repo will begin with the code from the [The Annotated Transformer](https://github.com/harvardnlp/annotated-transformer) 

So when I started this, I was having a problem pushing this change to github. This got me chasing down this [Connecting to GitHub with SSH](https://docs.github.com/en/authentication/connecting-to-github-with-ssh) path, which I did on KAUWITB. A quick test proved it was working. Nice!

### 11:12am

I want to provide time stamps in this log to indicate the duration between steps. 
Let's start with creating the code for the model, shall we ... 

### 6:07pm

I am thinking, how do I use this code in Transformers.ipynb to implement JUST an encoder and then JUST a decoder? The Andrej Karpathy [minGPT](https://github.com/karpathy/minGPT) code is just a decoder. I think the same can be said for his other example, [nanoGPT](https://github.com/karpathy/nanoGPT).Look at these examples for guidance on how to do this. 

## Friday, May 26, 2023

### 9:20am

Continuing with building the workflow.

### 11:08 

Studying the code found in [nanoGPT](https://github.com/karpathy/nanoGPT) which is really excellent.

### 11:53am

The [model.py](https://github.com/karpathy/nanoGPT/blob/master/model.py) code found in [nanoGPT](https://github.com/karpathy/nanoGPT) bears a striking similarity to the code found in [The Annotated Transformer](https://github.com/harvardnlp/annotated-transformer).

### 5:08pm

Studying the Shakespeare example in the nanoGPT code base because I want to try to implement something like that here.

If you peek inside the config/train_shakespeare_char.py file of the nanoGPT code base, you'll see that we're training a GPT with a context size of up to 256 characters, 384 feature channels (the width of the embeddings), and it is a 6-layer Transformer with 6 heads in each layer.

## October 4, 2023

### 4:01pm 

Yup, getting back to this cuz I want to resume my deep study of transformers. And I will once again begin with the code from [The Annotated Transformer](https://nlp.seas.harvard.edu/annotated-transformer/). I am curious to see just how much of this code can I get to run on KAUWITB. 

### 4:40pm

The docker container hfpt_Sept1 is not going to work for this repo. Gonna next try a pure pytorch docker container. 

### 4:46pm

Now trying the docker container sad_nightingale, which was spun up from the image pt1131:20230216. 