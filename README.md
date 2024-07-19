# MemoryWipeML: Enhancing Model Adaptability via Machine Unlearning

## Introduction

Machine Unlearning is focused on selectively removing or forgetting specific data or patterns from trained models. The process involves selectively modifying existing models to discard unwanted information or patterns, ensuring minimal computational load and maintaining overall performance. Machine unlearning plays a crucial role in data privacy, security, and compliance.

## Proposed Unlearning Framework

### Two Teachers:
- **Competent Teacher (Ts):** Possesses accurate knowledge.
- **Incompetent Teacher (Td):** Contains "bad" information.

### Student Model:
- Train a student model (S) on the entire dataset initially.

### Selective Forgetting:
- Aim to remove information about unwanted data (Df) while keeping desired data (Dr).

### Teacher-Student Interaction:
- **Td** helps **S** forget **Df** by providing misleading information.
- **Ts** helps **S** retain **Dr** by providing accurate knowledge.

### Loss Function (L):
- Minimize KL-divergence between **S** and **Ts** for **Dr**.
- Maximize KL-divergence between **S** and **Ts** for **Df** (using lu weight).

### Training Data:
- Train **S** on **Df** and a small subset of **Dr**.

### Student Learning:
- **S** learns to mimic **Td** for **Df**, achieving selective forgetting while retaining generic **Dr** knowledge.

## Block Diagram

![Unlearning Framework Block Diagram](https://github.com/user-attachments/assets/5905d124-fd68-4e63-80c1-01f90305b0c4)

---

By using this framework, we can effectively enhance the adaptability of models through machine unlearning, ensuring that specific information can be discarded while maintaining overall performance and compliance with data privacy and security standards.

---

