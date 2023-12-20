# Glossary of Terms

* Divergence - "I compare the probability distributions for each token in a sequence of 500 tokens when I did this test." - kalomaze
  -  In general, lower values are better.
* Layer - A large language model is made of a large number of layers.
* Model - a set of weights, organized into layers.
* Perplexity - What this actually means is not straightforward to understand, but in general, lower values are better.
* Quantization - FIXME
* Tensor - FIXME

# Common Abbreviations

* AI - Artificial Intelligence
* AGI - Artificial General Intelligence. Question: What separates AGI from AI?
  -  (naptastic's opinion) AGI won't be restricted by different modalities for input and output. Seeing, hearing, touching, reading, will all feed into an input layer of the same model. That model will be able to output text, audio, images, video, gcode, **whatever**.
* BPW - Bits Per Weight: An **average** of how many bits are given to each weight across a full model. A lower BPW means a model will take less RAM to run, potentially with lower speed or performance. A full exploration of this topic is beyond the scope of a glossary and deserves its own page.
* DRAM - See RAM
* exl2 - One format for LLMs, based on GPTQ. Its main benefits are both faster generation and lower perplexity when using fewer bits per weight.
* HBM - see RAM
* GAN - Generative Adversarial Network: Early image generation method where two networks compete, a generator and discriminator. The generator tries to fool the discriminator into thinking what it made is part of the dataset.
* GGML - One format for LLMs. It is **obsolete** and replaced by GGUF.
* GGUF - One format for LLMs. It supports CPU and GPU inference by offloading some layers from the CPU. While I have not tested this myself, I've heard that fully-offloaded GGUF is still not as fast as GPTQ. If you have info please share.
* GPTQ - One format for LLMs. It only supports GPU inference. Speed is good. It is slowly being replaced by exl2.
* LSTM - Long Short Term Memory: Predecessor to the transformer model architecture, what powers ChatGPT. Its weakness was that it does not scale well.
* ML - Machine Learning
* ppl - Perplexity. (See definitions.)
* RAM - Random-Access Memory
  -  DRAM - CPU-attached RAM. DRAM memory tends to be less expensive than VRAM but is much slower.
  -  VRAM - GPU-attached RAM. It generally has a much faster and wider bus to the GPU.
  -  HBM - High-Bandwidth Memory. In these situations, a GPU will be on the same substrate as its VRAM, allowing for much faster and wider connections. 
* RNN - Recurrent Neural Network: Can be thought of as the predecessor to an LSTM, though an LSTM is a type of RNN. In an RNN, part of its output is fed to a copy of itself at a later time step or token.
* RVC - Retrieval-based Voice Conversion, which is a fork of SVC (singing voice conversion)
* TTS - Text-To-Speech
* VRAM - See RAM 
* xttsv2 - Text-To-Speech software that doesn't work with a base local file (FIXME this needs to be written as a positive) 
