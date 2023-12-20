# Intro
What follows is an attempt at creating the document we wanted to have at hand when we started messing around with LLMs. It tries to give you a kickstart when it comes to understanding the shape, color and taste of *a lot* of brand new technology and terminology/lingo.  

Please understand that the introduction of LLMs to the masses is an event which in scale and importance mirrors the introduction of the Internet itself to the masses. Stuff is currently happening at an absolute breakneck speed, and what is written here was likely true at the point in time it was written. It may no longer be (completely) true by the time you are reading it, or some essential technology/software/model/concept/whatever may have been invented or discovered after this was written.

## The Very High-level Stuff

### What is an LLM?

### Is ChatGPT an LLM?

### What can an LLM do for me?

### What can't LLMs do? (particularly well. yet.)

### Can I run my own LLM?

### Why would I want to run my own LLM?

### What is required to run my own LLM at home?
Yes. In order to......

### Can I run my own LLM in the Cloud?
Yes. There are plenty options.....

### How is the quality of an LLM measured?
Also known as Benchmarking, statistics and other lies.

### How is the performance of an LLM measured?
More Benchmarking, statistics and other lies.


## Hardware for hosting a local LLM

### High-level overview - what performance *matters* for LLMs?

Any computer has a multitude of bottlenecks. If we focus on the hardware *only*, the following is a good list:
* storage
* net
* memory
* CPU
* GPU
* interconnects (buses)

And while a sports car is both fast *and* quick, it may not have a lot of capacity for moving *lots of stuff*. In other words, the actual bottleneck for each item in the list above *may* be either one of:
* speed
* latency
* capacity

And while all of the above is important, software optimization and adaption to the hardware at hand is just as important. Now, most of us do not have the budget to buy custom hardware for playing with LLMs. So we largely all have access to buy the same hardware. If you are a gamer, you optimize for framerate and buy a shiny GPU. For other stuff, you want a speedy CPU with lots and lots of cores. What matters for running LLMs?    

For running a local LLM, the primary bottleneck is memory (RAM) *size*. You need enough memory to load the model of your choice into memory, in order to play with it. Using a pagefile/swap as substitute for memory has been the solution for decades. Technically, his also works for LLMs, but you don't want to. 

Because when the requirement for memory size has been fulfilled, memory bandwidth is *the* most important hardware parameter to optimize for. And while system memory (DIMMs) in combination with a current Intel or AMD CPU may give ~20x better bandwidth (and latency( than your fancy M.2 NVME drive, it is still ~10x slower than the memory bandwidth of a high-end GPU.

And finally, when you have sufficient memory bandwidth to get acceptable (to you) speed (tokens per second) out of your model, you will likely want to increase the amount of memory in order to be able to load a bigger model or get more context. TODO: internal link.

More stuff ......xxx current requirement to have decent performance from a model of decent quality (enough parameters at a sufficiently high level of quantization

### CPU vs GPU

### CPU

### GPU

### Motherboard

### Memory



## Basic Terminology

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


## Medium Terminology

### Perplexity

### Merged model

### Rope scaling or something.


## Advanced Terminology

## How do I.....

## Resources and pointers
May have to split this into multiple sections.








