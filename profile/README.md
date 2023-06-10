## DeltaVML is a collection of open source software to facilitate the exploration of local language models for machine learning experiments. Goals include AI assistants for all aspects of digital lifestyle enhancements.
One working model is provided by koboldai. First inception of a local language model was using GPT4ALL and the alpaca model provided by Stanford university. Kobaldcpp provides my first experience finding a model that runs on both the graphics card and the cpu. DeltaVML believes in a decentralized modular open source future for local langauge models.

The following is the output from a build using Ubuntu 23 on an i7 Desktop with 12 GB of ram and an Nvidia GeForce GTX 970 representing average consumer grade hardware in 2023. Replies currently take 2-3 minutes. Parameter settings and fine tuning
is being done to increase the performance.


~/koboldcpp$ python koboldcpp.py --threads 8 --blasthreads 8 --useclblast 0 0 --highpriority --contextsize 4096 --blasbatchsize 64 --smartcontext --gpulayers 8 --debugmode --model ggml-gpt4all-j-v1.3-groovy.bin


Welcome to KoboldCpp - Version 1.29
Setting process to Higher Priority - Use Caution
High Priority for Linux Set: 0 to 1
Attempting to use CLBlast library for faster prompt ingestion. A compatible clblast will be required.
Initializing dynamic library: koboldcpp_clblast.so
==========
Loading model: /home/codephreak/koboldcpp/ggml-gpt4all-j-v1.3-groovy.bin 
[Threads: 8, BlasThreads: 8, SmartContext: True]

---
Identified as GPT-J model: (ver 102)
Attempting to Load...
---
System Info: AVX = 0 | AVX2 = 0 | AVX512 = 0 | AVX512_VBMI = 0 | AVX512_VNNI = 0 | FMA = 0 | NEON = 0 | ARM_FMA = 0 | F16C = 0 | FP16_VA = 0 | WASM_SIMD = 0 | BLAS = 1 | SSE3 = 1 | VSX = 0 |

gptj_v2_model_load: loading model from '/home/codephreak/koboldcpp/ggml-gpt4all-j-v1.3-groovy.bin' - please wait ...

gptj_v2_model_load: n_vocab = 50400
gptj_v2_model_load: n_ctx   = 2048
gptj_v2_model_load: n_embd  = 4096
gptj_v2_model_load: n_head  = 16
gptj_v2_model_load: n_layer = 28
gptj_v2_model_load: n_rot   = 64
gptj_v2_model_load: ftype   = 2
gptj_v2_model_load: qntvr   = 0
gptj_v2_model_load: ggml ctx size = 4505.52 MB

Initializing LEGACY CLBlast (First Run)...
Attempting to use: Platform=0, Device=0 (If invalid, program will crash)

Using Platform: NVIDIA CUDA Device:
NVIDIA GeForce GTX 970

gptj_v2_model_load: memory_size =   896.00 MB, n_mem = 57344
gptj_v2_model_load: ................................... done
gptj_v2_model_load: model size =  3609.38 MB / num tensors = 285

Load Model OK: True
Embedded Kobold Lite loaded.
Starting Kobold HTTP Server on port 5001
Please connect to custom endpoint at http://localhost:5001

---------------------------------

Who is the greek god hermes?

Output: 

The Greek God Hermes was the messenger of the gods, responsible for guiding souls to the afterlife after they died. He was depicted with wings, carrying a caduceus staff, and wearing a winged hat. In mythology, he was often associated with trade and commerce, and his name was given to various professions such as merchants, traders, and messengers.

Time Taken - Processing:45.0s (529ms/T), Generation:124.8s (1580ms/T), Total:169.8s


<!--

**Here are some ideas to get you started:**

🙋‍♀️ A short introduction - what is your organization all about?
🌈 Contribution guidelines - how can the community get involved?
👩‍💻 Useful resources - where can the community find your docs? Is there anything else the community should know?
🍿 Fun facts - what does your team eat for breakfast?
🧙 Remember, you can do mighty things with the power of [Markdown](https://docs.github.com/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)
-->
