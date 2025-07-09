[ML Roadmap](https://roadmap.sh/ai-engineer)


**AI Venn Diagram**

<img src="https://github.com/user-attachments/assets/eda348bc-9fd7-4661-8bdb-01a383bed3e8" width="500"/>


# Math Foundations

* **Linear Algebra** → Vectors, matrices, dot product, eigenvalues
* **Calculus** → Derivatives, gradients (focus on chain rule)
* **Probability & Statistics** → Bayes’ theorem, distributions, expectation, variance
* **Optimization** → Gradient descent, loss functions

# Deep Learning

* Neural networks (perceptrons → deep nets)
* Backpropagation
* CNNs (for images)
* RNNs / LSTMs (for sequences)
* Loss functions, optimizers

# LLMs and Foundation Models

## **Fundamentals of LLMs**

* What is a Language Model?
* History and evolution (n-grams → RNN → Transformer → LLMs)
* Key properties of LLMs (zero-shot, few-shot, in-context learning)


## Transformer Architecture (Core of LLMs)

* Attention mechanism
* Scaled dot-product attention
* Multi-head attention
* Positional encoding
* Encoder vs Decoder vs Encoder-Decoder architecture
* Layer normalization & residual connections
* Feedforward layers
* Self-attention vs Cross-attention


## Pretraining & Objective Functions

* Causal language modeling (CLM)
* Masked language modeling (MLM)
* Next sentence prediction (NSP)
* Training datasets (Common Crawl, The Pile, etc.)
* Tokenization (Byte Pair Encoding, WordPiece, SentencePiece)


## LLM Architectures & Variants

* GPT (OpenAI)
* BERT (Google)
* T5 (Text-To-Text Transfer Transformer)
* LLaMA, PaLM, Falcon, Mistral, Claude, Gemini
* Decoder-only vs Encoder-only vs Encoder-Decoder models

## Fine-Tuning & Adaptation

* Supervised fine-tuning (SFT)
* Instruction tuning
* Parameter-efficient fine-tuning (PEFT)

  * LoRA (Low-Rank Adaptation)
  * QLoRA
  * Adapters
* Domain-specific fine-tuning

## Prompt Engineering

* Zero-shot, one-shot, few-shot prompting
* Chain-of-thought prompting
* Role-based prompting (system/user prompts)
* Context window management
* Token limits and prompt formatting

## Retrieval-Augmented Generation (RAG)

* What is RAG and why it's needed
* Vector embeddings
* Vector databases (e.g., FAISS, Chroma, Weaviate)
* Semantic search
* Chunking & document loaders


## LLM Internals & Scaling

* Transformer scaling laws
* Emergent capabilities
* Memory & compute requirements
* Attention bottlenecks & sparse attention
* Model quantization, pruning, distillation

## Tools & Frameworks for LLMs

* Hugging Face Transformers
* OpenAI API
* LangChain
* LLamaIndex
* Vector databases: FAISS, ChromaDB, Pinecone
* Libraries: Transformers, Accelerate, BitsAndBytes
