# 🧬 MMD-GAN: Enhancing Generative Adversarial Networks with Maximum Mean Discrepancy

This repository contains the code and evaluation tools for our collaborative deep learning project on **MMD-GANs**, developed as part of the **Modèles génératifs, méthodes par patchs, photographie computationnelle** at **Télécom Paris**.

The objective was to explore and implement **GAN architectures using kernel-based statistical distances**, in particular **Maximum Mean Discrepancy (MMD)**, and compare their performance with classical WGANs.

---

## 📚 Project Overview

Generative Adversarial Networks (GANs) have made significant strides in producing realistic synthetic data. However, training stability, convergence guarantees, and mode collapse remain persistent challenges.

This project investigates an alternative formulation of GANs by replacing the discriminator with a **kernel-based statistical distance: MMD**. The key ideas are:

- Replace the adversarial min-max loss with a **kernel two-sample test**
- Use the **Maximum Mean Discrepancy (MMD)** to measure divergence between generated and real samples
- Evaluate the impact of **learnable kernel functions**, **gradient penalties**, and **encoder mappings**

We implemented both MMD-GAN and WGAN baselines, compared them on **synthetic datasets** and **MNIST**, and analyzed results using a unified evaluation framework.

---

## 📈 Results Summary

- On synthetic data, MMD-GAN showed better **diversity** and **mode coverage**
- On MNIST, **WGAN** retained an edge in **visual sharpness**, but MMD-GAN delivered smoother training dynamics
- The impact of using a **learned kernel** and **repulsive loss** in MMD-GAN improved robustness to mode collapse

More details, plots, and training curves can be found in the full project report included below.

---

## 🧠 Methods Used

- 🌀 **MMD-GAN** with:
  - Gaussian kernels
  - Encoder-based input mapping
  - Gradient penalties (GP)
- 🆚 **Wasserstein GAN** (WGAN) baseline
- ✏️ Statistical metrics and loss visualization
- 🔍 Kernel learning experiments

---

## 🔗 Dataset & Evaluation

We evaluated on:
- 🧪 **Synthetic Toy Datasets**: 2D Gaussian Mixtures
- 🔢 **MNIST**: Handwritten digit dataset

---
## 🧾 Accessing the Project Code

The complete project code is available in a Colab-compatible format and can be accessed using the following link:

👉 **[MMD-GAN Project Code (Google Drive - Colab)](https://drive.google.com/file/d/1F80mNEMlabiuxPWyej7MhY9OFO43AZJa/view?usp=drive_link)**

---

## 📂 Repository Structure

```bash
├── WGAN_evaluation_file_mnist/      # Evaluation and generation on MNIST
├── WGAN_evaluation_file_toy/        # Evaluation and generation on Toy Data
├── Rapport_MMD_GAN.pdf              # Full project report (Télécom Paris)
├── README.md                        # Project overview (this file)
```

---

## 💾 Requirements

* Python ≥ 3.7
* PyTorch ≥ 1.12
* NumPy, Matplotlib, torchvision

---

## 🧑‍🤝‍🧑 Team & Contributions

This project was developed in collaboration as part of the **Modèles génératifs, méthodes par patchs, photographie computationnelle** module at Télécom Paris.

* Amir Loris Ben El Ghali
* Rayan Fatnassi
* Atef Bouzid
* Malek Feki

Everyone contributed to the literature review, model implementation, and experimentation.

---

## 🙏 Acknowledgments

This project was conducted under the guidance of the **Modèles génératifs, méthodes par patchs, photographie computationnelle** course at Télécom Paris.

Special thanks to the instructors and peers for insightful discussions and support throughout.


