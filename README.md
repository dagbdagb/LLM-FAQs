# This is a Work in Progress, feel free to contribute,

# Intro
What follows is an attempt at creating the document we wanted to have at hand when we started messing around with LLMs. It tries to give you a kickstart when it comes to understanding the shape, color and taste of *a lot* of brand new technology and terminology/lingo.  

Please understand that the introduction of Large-Language Models (LLMs) to the masses is an event which in scale and importance mirrors the introduction of the Internet itself to the masses. Stuff is currently happening at an absolute breakneck speed, and what is written here was likely true at the point in time it was written. It may no longer be (completely) true by the time you are reading it, or some essential technology/software/model/concept/whatever may have been invented or discovered after this was written.

Also, this is not intended to be a deep-dive into any particular concept within Large Language Models. Consider it a kind of "coloring book" where you get to decide the color (shape, taste, size, texture) of each individual sub-topic.

We have tried to order sections and sub-topics in a somewhat logic or pedagogic order. Feel free to tell us where we fail at this.

Finally, it is not our intention to *promote* any particular hardware, software, company, brand, person or other entity. We just want this to be a guide for your personal journey, and not to guide you down a particular path. That said, we all appreciate working examples. So we will definitely *name* things we have tried and found working for us.

Good luck.

## The Very High-level Stuff

### What is an LLM?
A Large Language Model is, seen from a sufficiently large distance, kind of like a giant zipfile of a huge collection of documents. But in order to obtain better compression of our zipfile, we accept lossy compression. That is, we cannot actually recreate the orginal documents, neither the contents or the structure. But given a word or a sentence, we can calculate what words are most likely to come next. And when we have the next word, we can redo the process. This may sound absolutely crazy, so will just let an actual expert explain it instead: [Intro to Large Language Models](https://www.youtube.com/watch?v=zjkBMFhNj_g)

### Is ChatGPT an LLM?
Yes. ChatGPT is a commercial product by OpenAI, who was first to provide mass-market access to a commercial grade LLM.

### What can an LLM do for me?
Nap, this for you

### What can't LLMs do? (particularly well. yet.)
This too.

### Can I run my own LLM? Legally?
Yes. And yes. If you are allowed to own and operate a computer, you may also run your own LLM. As far as we know. None of this is legal advice, by the way.

### Can I create my own LLM?
Yes. But not yet, young padawan. You don't know what that means yet. And we don't know what *you* mean by 'create' exactly. So hold that thought for a while.

### Why would I want to run my own LLM?
Well. Would you like to? You don't need to have a reason. And even if you do, you don't owe neither us nor anyone else to state your reason(s) publicly. We respect your privacy and ability to make informed decisions. We hope you pay it forward.

### What is required to run my own LLM at home?
In order to run an LLM locally, your first order of business is to figure out the purpose it is going to serve. If it is just as a vehicle for learning a bit about LLMs, a tiny model would technically fit on your mobile phone. But almost any PC from the last 10 years or so would be a better choice and should be able to load a tiny LLM.  

If it is for a particular purpose, you need to:
* define your scope and criteria for success
* learn a bit more to figure out what kind of model you need
* research what model can fulfill that role
* research what is required to run the model (and size) you need

This document may guide you.

### Can I run my own LLM in the Cloud?
Yes. There are plenty options for that. Or even for using someone else's LLM. Like ChatGPT.

### Can I run an LLM at home, without Internet access?
Yes. You just need to get the LLM and the supporting software and libraries installed somehow. The local LLM itself does not require access the Internet. That is, most of them (at the time of writing) are not even able to access the network or even files on your computer.

### How is the quality of an LLM measured?
If we consider an LLM we interact with via text, the layman interpretation of quality may be something along the lines of "truthfulness" or "usability". As in: is the response factually true, and is it helpful. The first can really only be measured in absolute terms for binary questions. (Ones having a yes/no question). The second may be hard to give an absolute number. ("This response is 74,3% helfpul"). But by setting up LLMs to compete against each other by answering the same prompt, we can employ humans to judge which one gave the better answer. So even if we cannot trivially put an objective, absolute number to the quality of any LLM, we *can* measure the relative quality of one LLM to another.

Other aspects of an LLM may also sort under 'quality': how natural the language sounds, the ability to not give out information deemed harmful or offensive, the ability to keep track of the conversation over time. Etcetera.

### How is the performance of an LLM measured?
There are a number of factors which goes under the 'performance' label. For the trivially measurable stuff:
* required time to process the prompt
* units of output per time ("tokens per second")
* length of output

## Basic Terminology
The terminology you find in this section may be some of the first stumbling blocks when starting out. More follows in later sections.

### LLM families

### LLM sizes - tiny/small/medium/large/enterprise

### LLM formats

### LLM quantization

### Offloading
Offloading in the context of running LLMs refers to the use of both GPU VRAM **and** system RAM for holding a model. There are various ways of achieving this, and not all current model formats can support this feature. 

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

#### Text

#### Vision

#### Audio



### Function calling






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
* speed (how fast)
* latency (how quickly)
* capacity (how much)

And while all of the above is important, software optimization and adaption to the hardware at hand is just as important. Now, most of us do not have the budget to buy custom hardware for playing with LLMs. So we largely all have access to buy the same hardware. If you are a gamer, you optimize for framerate and buy a shiny GPU. For other stuff, you may want a CPU with a few very speedy cores. Or a CPU with less speedy, but many cores.  

What matters for running LLMs?    

For running a local LLM, the primary bottleneck is memory (RAM) *size*. You need enough memory to load the model of your choice into memory, in order to play with it. Using a pagefile/swap as a substitute for real memory has been the solution for decades. Technically, this also works for LLMs, but you don't want to. 

Because when the requirement for memory size has been fulfilled, memory bandwidth is *the* most important hardware parameter to optimize for, *when running LLMs*. Other computer workloads may have other requirements. And while system memory (DIMMs) in combination with a current Intel or AMD CPU may give ~20x better bandwidth (and latency( than your fancy M.2 NVME drive, it is still ~10x slower than the memory bandwidth of a high-end GPU.  

Current high-end GPUs for the consumer market tops out at 24GB *VRAM*. The type of memory used on GPUs is speedier than system memory, and as the LLM processing now happens on the GPU, processing speed is also higher (GPUs are better than CPUs at the type of math involved in LLMs) and latency is lower. This allows for running decent sized ("quality") models at decent speed ("performance"). GPUs with less memory (than the top-end GPUs) mostly also have less memory bandwidth. I.e. they are slower. But still faster than your system memory (DIMMs in your motherboard).

And finally, when you have sufficient memory *bandwidth* to get acceptable (to you) speed (tokens per second) out of your chosen model, you will likely want to increase the memory size in order to be able to load a bigger ("quality") model or get more context. This can be done a couple of ways:
* use system memory for the part of the model which doesn't fit on the GPU. See 'offloading' under Basic Terminology (TODO: link)
* get a GPU with more memory
* get a second GPU


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

### Rope scaling or something

### Tensor


## Advanced Terminology and other Magic

## How do I.....


## This FAQ is lame. It totally forgets to say something about.....

### Big Claims require Big Evidence

### The Laws of Physics still apply

## Resources and pointers
### pointers to LLM timelines (who published what when)









