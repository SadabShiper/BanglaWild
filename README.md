<div align="center">

# BanglaWild:  An In-the-Wild Bengali Scene Text Recognition Benchmark for OCR and <br> Vision-Language Models
</div>

<p align="center">
  <strong>Sadab Shiper*</strong>, <strong>Tawsif Tashwar Dipto*</strong>, <strong>Mir Md Inzamam</strong>, <strong>Eshat Tanzeem</strong>
</p>
<div align="center">

[![arXiv](https://img.shields.io/badge/arXiv-2608.03884-b31b1b?logo=arXiv&logoColor=white)](https://arxiv.org/abs/2608.03884) [![GitHub](https://img.shields.io/badge/Code-Under%20Construction-orange?logo=GitHub)](https://github.com/SadabShiper/BanglaWild) [![Kaggle](https://img.shields.io/badge/Datasets-sadabshiper/banglawild--in--the--wild--bengali--scene--text--dataset-20BEFF?logo=Kaggle&labelColor=white&logoSize=auto)](https://www.kaggle.com/datasets/sadabshiper/banglawild-in-the-wild-bengali-scene-text-dataset)

</div>

---

## Overview

**BanglaWild** is a real-world Bangla OCR benchmark of **2,535 annotated images** collected from real-world scenes (signboards, posters, nameplates, products, vehicles, documents, graffiti, and more). It evaluates how well modern vision-language models (VLMs) and conventional OCR systems can read Bengali text "in the wild".

Each image comes with:

- a verbatim gold transcription,
- two categorical axes and four diagnostic attributes,
- an orthographically standard form, for cases where the text in the image deviates from canonical spelling.

### Dataset Categories

Each image is labeled along two orthogonal categorical axes:

| Axis | Description | Values |
|------|-------------|--------|
| **Context** | Physical medium on which the text appears | Vehicle, Signboard, Packaging, Wall, Printed Material |
| **Content** | Communicative intent of the text | Religious, Political, Advertisement, Instructional, Creative, Colloquial |

### Diagnostic Attributes

| Attribute | Value (images) |
|-----------|----------------|
| **Curved Text** | No (2,335), Yes (200) |
| **Font Style** | Handwritten (1,436), Printed (644), Artistic (455) |
| **Occlusion** | None (2,009), Partial (503), Heavy (23) |
| **Background Complexity** | Clean (2,158), Moderate (279), Cluttered (98) |

Labels were assigned by two annotators, with disagreements resolved by an expert. 87 images (3.43%) contain non-standard spelling and carry a separate orthographically standard form.

### Benchmark

- **15 VLMs** and **3 conventional OCR systems**, each evaluated under **3 prompting strategies**
- **LoRA fine-tuning** of 6 open-source models
- Edit-distance metrics plus an **LLM-as-a-Judge** evaluation
- A **15-class error taxonomy**

### Key Findings

- Larger models within the same family do not necessarily outperform smaller ones.
- Visual mis-recognition accounts for roughly 60% of errors in the strongest systems, while conjunct-related errors contribute under 2%.
- Prompt language mainly affects cross-script drift.
- LoRA reduces catastrophic failures in weak models but does not raise the ceiling of already competent ones.


