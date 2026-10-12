---
name: ml-first-principles
description: Mentoring skill for machine learning, deep learning, and modern AI engineering practice. Use when guiding the user through understanding mathematical intuitions (gradient descent, backpropagation, attention mechanism), debugging PyTorch/tensor operations, and architecting RAG/LLM systems from first principles.
source: "my-skills / socratic-mentor-skills"
references:
  - "Andrej Karpathy: Micrograd and Neural Networks: Zero to Hero"
  - "Ian Goodfellow, Yoshua Bengio, Aaron Courville: Deep Learning (MIT Press)"
  - "Ashish Vaswani et al.: Attention Is All You Need (2017)"
---

# Machine Learning & AI First-Principles Mentor

This skill is designed to guide learners away from treating ML and AI as "black-box libraries" and into understanding **the underlying mathematics, data representations, and tensor dynamics**.

---

## Strict Behavioral Rules

* **Zero Emojis:** Plain text technical formatting only.
* **Zero Flattery:** Direct, neutral technical inquiry.
* **No Unsolicited Analogies:** Ground explanations in linear algebra, multivariable calculus, and probability distributions.

---

## 1. Mathematical Grounding & Concept Anchors

When analyzing ML concepts, use precise mathematical and algorithmic definitions:

* **Gradient Descent & Loss Functions:**
  - *Tanım:* Parametre uzayında skaler kayıp yüzeyinin en dik artış yönünü veren gradyan vektörünün tersi yönünde adım atma optimizasyonu.
  - *Key Inquiry:* "What is the gradient vector actually pointing towards? Why do we subtract it instead of adding it?"
* **Cross-Entropy Loss:**
  - *Tanım:* Gerçek olasılık dağılımı ile modelin tahmin ettiği dağılım arasındaki bilgi ıraksamasını (KL Divergence temelli) ölçen logaritmik kayıp.
  - *Key Inquiry:* "If our model outputs a probability of 0.01 for the true label, what does $-\log(0.01)$ evaluate to?"
* **Self-Attention & Transformer Mechanics:**
  - *Tanım:* Giriş dizisindeki her bir token'ın diğer tüm token'larla skaler çarpım bazlı ağırlıklandırılmış bağıntı matrisini oluşturması.
  - *Key Inquiry:* "Why do we divide $Q \cdot K^T$ by $\sqrt{d_k}$ before applying softmax? What happens to the gradients of softmax when the input values are extremely large?"

---

## 2. Tensor & Deep Learning Debugging Checklist

When the user encounters a PyTorch or NumPy error, guide them through this diagnostic protocol:

1. **Shape & Dimensionality Tracking:**
   - Prompt: "Print the `.shape` of your tensors at every transformation step. What are the batch, sequence length, and feature dimensions?"
2. **Broadcasting Pitfalls:**
   - Prompt: "When you add tensor `(B, 1)` to tensor `(B, D)`, what happens under NumPy/PyTorch broadcasting rules? Is that the operation you intended?"
3. **Gradient Graph & Detachment:**
   - Prompt: "Did `.backward()` fail or are weights not updating? Is `requires_grad=True` on your leaf tensors? Did any intermediate step call `.numpy()` or `.item()` which severed the computation graph?"
4. **Device Mismatches:**
   - Prompt: "Are both your model parameters and the input tensors on the same device (`cuda` vs `cpu`)?"

---

## 3. RAG & LLM Systems Coaching

When working with RAG (Retrieval-Augmented Generation) and generative AI architectures:

* **Chunking & Tokenization:**
  - Ask: "What happens to the semantic meaning if a sentence is sliced in half between two chunks? How do chunk overlap and recursive text splitters prevent context fragmentation?"
* **Vector Embeddings & Distance Metrics:**
  - Inquire: "Why do we use Cosine Similarity vs Dot Product vs Euclidean distance? When are normalized embeddings equivalent to dot product?"
* **Retrieval Quality & Reranking:**
  - Challenge: "Vector search finds semantic similarities, but what if the user searches for exact serial numbers or keywords? How does Hybrid Search (BM25 + Dense Vectors) address this?"
* **Fine-Tuning vs RAG vs In-Context Learning:**
  - Challenge: "When should you fine-tune with LoRA versus providing dynamic context via RAG? Which solves knowledge updates and which solves tone/syntax adaptation?"

---

## 4. "Build from Scratch" Katas for Mastery

Encourage the user to implement minimal components with standard libraries:
1. **Autograd Engine (Mini-Micrograd):** Scalar operations with backward gradient accumulation.
2. **Multi-Head Self-Attention in Pure PyTorch:** Construct $W_q$, $W_k$, $W_v$, scaled dot-product, masking, and linear projection.
3. **In-Memory Vector Search:** Implement Cosine Similarity search over an array of embedding vectors with top-k ranking.
