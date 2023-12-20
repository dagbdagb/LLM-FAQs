# Intro
What follows is an attempt at creating the document we wanted to have at hand when we started messing around with LLMs. It tries to give you a kickstart when it comes to understanding the shape, color and taste of *a lot* of brand new technology and terminology/lingo.  

Please understand that the introduction of Large-Language Models (LLMs) to the masses is an event which in scale and importance mirrors the introduction of the Internet itself to the masses. Stuff is currently happening at an absolute breakneck speed, and what is written here was likely true at the point in time it was written. It may no longer be (completely) true by the time you are reading it, or some essential technology/software/model/concept/whatever may have been invented or discovered after this was written.

Also, this is not intended to be a deep-dive into any particular concept within Large Language Models. Consider it a kind of "coloring book" where you get to decide the color (shape, taste, size, texture) of each individual sub-topic.

We have tried to order sections and sub-topics in a somewhat logic or pedagogic order. Feel free to tell us where we fail at this.

Finally, it is not our intention to promote any particular hardware, software, company, brand, person or other entity. We just want this to be a guide for your personal journey, and not to guide you down a particular path.  

Good luck.

## The Very High-level Stuff

### What is an LLM?

### Is ChatGPT an LLM?

### What can an LLM do for me?

### What can't LLMs do? (particularly well. yet.)

### Can I run my own LLM?

### Can I create my own LLM?
Yes. But not yet, young padavan. You don't know what what that means yet. And we don't know what *you* mean by 'create' exactly. So hold that thought for a while.

### Why would I want to run my own LLM?
Well. Would you like to? You don't need to have a reason. And even if you do, you don't owe neither us nor anyone else to state your reason(s) publicly.  

### What is required to run my own LLM at home?
Yes. In order to......

### Can I run my own LLM in the Cloud?
Yes. There are plenty options.....

### How is the quality of an LLM measured?
Also known as Benchmarking, statistics and other lies.

### How is the performance of an LLM measured?
More Benchmarking, statistics and other lies.


## Basic Terminology
The terminology you find in this section may be some of the first stumbling blocks when starting out.

### LLM families

### LLM formats

### LLM quantization

### Loader

### Front-end

### Prompt/template

### Training

### Fine-tuning

### Reinforcement Learning from Human Feedback (RLHF)

### Inference

### Context

### API

### Multi-modality





## Hardware for hosting a local LLM

### High-level overview - what hardware capabilities and performance *matters* for running local LLMs?

Any computer has a multitude of bottlenecks. If we focus on the hardware *only*, the following is a good list:
* storage
* network
* memory
* CPU
* GPU
* interconnects (buses)

And while a sports car is both fast *and* quick, it may not have a lot of capacity for moving *lots of stuff*. In other words, the actual bottleneck for *each item* in the list above *may* be either one of:
* speed
* latency
* capacity

And while all of the above is important, software optimization and adaption to the hardware at hand is just as important. Now, most of us do not have the budget to buy custom hardware for playing with LLMs. So we largely all have access to buy the same hardware. If you are a gamer, you optimize for framerate and buy a shiny GPU. For other stuff, you may want a CPU with a few very speedy cores. Or a CPU with less speedy, but many cores.  

What matters for running LLMs?    

For running a local LLM, the primary bottleneck is memory (RAM) *size*. You need enough memory to load the model of your choice into memory, in order to play with it. Using a pagefile/swap as a substitute for real memory has been the solution for decades. Technically, his also works for LLMs, but you don't want to. 

Because when the requirement for memory size has been fulfilled, memory bandwidth is *the* most important hardware parameter to optimize for. And while system memory (DIMMs) in combination with a current Intel or AMD CPU may give ~20x better bandwidth (and latency( than your fancy M.2 NVME drive, it is still ~10x slower than the memory bandwidth of a high-end GPU. Current high-end GPUs for the consumer market tops out at 24GB. This allows for running decent sized ("quality") models at decent speed ("tokens per second"). GPUs with less memory (than the top-end) mostly also have less memory bandwidth. I.e. they are slower. But still faster than your system memory (DIMMs in your motherboard).

And finally, when you have sufficient memory bandwidth to get acceptable (to you) speed (tokens per second) out of your model, you will likely want to increase the amount of memory in order to be able to load a bigger model or get more context. 

TODO: internal link.

More stuff ......xxx current requirement to have decent performance from a model of decent quality (enough parameters at a sufficiently high level of quantization

### CPU vs GPU

### CPU

### GPU

### Motherboard

### Memory


## Software for hosting a local LLM

### Operating Systems

### Libraries and toolkits for particular hardware

#### Nvidia Cuda

#### AMD ROCm

#### Intel OneAPI

### PyTorch

## Medium Advanced Terminology

### Perplexity

### Merged model

### Rope scaling or something.


## Advanced Terminology and other Magic

## How do I.....

## This FAQ is lame. It totally forgets to say something about.....

### Big Claims require Big Evidence

### The Laws of Physics still apply

## Resources and pointers
May have to split this into multiple sections.








