# Intro
Lorem Ipsum

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

And while all of the above is important, software optimization and adaption to the hardware at hand is just as important. Now, most of us do not have the budget to buy custom hardware for playing with LLMs. So we largely all have the same hardware at our disposal. For running a local LLM, the primary bottleneck is memory *size*. (RAM) Using a pagefile/swap as substitute for memory has been the solution for decades. Technically, his also works for LLMs, but you don't want to. Because when the requirement for memory size has been fulfilled, memory bandwidth is *the* most important hardware parameter to optimize for. And while system memory (DIMMs) in combination with a current Intel or AMD CPU may give ~20x better bandwidth (and latency( than your fancy M.2 NVME drive, it is still ~10x slower than the memory bandwidth of a high-end GPU.

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

### Prompt

### Training

### Inference

### Context

### API


## Medium Terminology

### Perplexity

### Merged model

### 













