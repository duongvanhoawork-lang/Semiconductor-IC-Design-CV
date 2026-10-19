# Rank-Collapse and Detail Re-injection for Efficient Safety-Helmet Detection

[![DOI](https://img.shields.io/badge/DOI-10.1007%2F978--981--92--6510--7__29-blue.svg)](https://doi.org/10.1007/978-981-92-6510-7_29)
[![Publisher](https://img.shields.io/badge/Publisher-Springer%20Nature-orange.svg)](https://link.springer.com/chapter/10.1007/978-981-92-6510-7_29)
[![Conference](https://img.shields.io/badge/Conference-MIWAI-brightgreen.svg)](https://link.springer.com/chapter/10.1007/978-981-92-6510-7_29)

---

## 📌 Publication Details

- **Title:** Rank-Collapse and Detail Re-injection for Efficient Safety-Helmet Detection
- **Authors:** 
  - **Hoa Van Duong** (FPT University, Can Tho Campus)
  - **Thuan Gia Nguyen** (FPT University, Can Tho Campus)
  - **Thinh Quang Nguyen** (FPT University, Can Tho Campus)
  - **Long Thanh Nguyen** (FPT University, Can Tho Campus)
  - **Hoang Tran Ngoc** (FPT University, Can Tho Campus)
- **Book Title:** *Multi-disciplinary Trends in Artificial Intelligence*
- **Conference:** International Conference on Multi-disciplinary Trends in Artificial Intelligence (MIWAI)
- **Series:** *Lecture Notes in Computer Science / Lecture Notes in Artificial Intelligence* (LNCS / LNAI), Springer, Singapore
- **Pages:** 379–391
- **ISBN:** 978-981-92-6510-7
- **DOI:** [10.1007/978-981-92-6510-7_29](https://doi.org/10.1007/978-981-92-6510-7_29)
- **Official Publisher URL:** [https://link.springer.com/chapter/10.1007/978-981-92-6510-7_29](https://link.springer.com/chapter/10.1007/978-981-92-6510-7_29)

---

## 📄 Abstract

Industrial safety monitoring is a labor-safety problem with a deployment-cost constraint. Safety-helmet detectors must flag unsafe bare heads while remaining light enough for routine operation on modest local hardware. In the Safety Helmet Wearing Dataset (SHWD), these bare-head instances are frequently COCO-small. We study a stage-aware rule for YOLO11n: keep P2 and replace the repeated C3k2 mixers from P3 onward with *Rank-Collapse and Detail Re-injection* (RCDR). RCDR uses a low-rank spatial mixer that folds to one $3 \times 3$ kernel, plus a full-width depthwise rail with ECA (Efficient Channel Attention) as a correction path. P2, the detector head, and the feature routing stay unchanged. The parts are established; what we contribute is their placement and their integration into an unchanged detector graph. On SHWD, relative to YOLO11n, RCDR reduces parameters by $13.14\%$, FLOPs by $9.21\%$, and GTX 1650 model-forward latency by $8.34\%$, while increasing FPS from 66.81 to 72.89 ($+9.10\%$). Under a declared tie threshold of 0.005 AP, the $\text{mAP}_{50:95}$ difference of 0.0043, $\text{AP}_{50}$, and $\text{AP}_{75}$ are ties, while $\text{AP}_S$ falls by 0.0075 and is the one measurable accuracy cost. The result is a cheaper operating point at accuracy we cannot separate from the baseline, not an accuracy improvement.

---

## 🔬 Key Contributions & Methodology

1. **Stage-Aware Placement:** Preserves the early P2 stage unaltered so high-resolution low-level features for COCO-small objects (e.g., distant bare heads and safety helmets) remain uncompromised.
2. **RCDR (Rank-Collapse and Detail Re-injection):** Replaces heavy C3k2 mixer modules from stage P3 onwards with a structural reparameterization low-rank branch that collapses into a single $3 \times 3$ convolution at inference.
3. **Detail Correction Rail:** Incorporates a full-width depthwise convolution paired with Efficient Channel Attention (ECA) to re-inject high-frequency spatial context without adding substantial parameter overhead.
4. **Seamless Detector Compatibility:** Retains standard YOLO11n routing and prediction heads without architectural divergence.

---

## 📊 Experimental Results (SHWD Benchmark on NVIDIA GTX 1650)

| Metric | Baseline YOLO11n | YOLO11n + RCDR (Ours) | Relative Improvement |
| :--- | :---: | :---: | :---: |
| **Parameters** | 2.59 M | **2.25 M** | **-13.14%** |
| **FLOPs** | 6.51 G | **5.91 G** | **-9.21%** |
| **Forward Latency** | 14.97 ms | **13.72 ms** | **-8.34%** |
| **Inference FPS** | 66.81 FPS | **72.89 FPS** | **+9.10%** |
| **mAP50:95** | Baseline | -0.0043 | Within tie threshold (< 0.005) |

---

## 📖 Citation

If you find this work relevant to your research, please cite it using the following format:

### BibTeX
```bibtex
@inproceedings{duong2027rank,
  title={Rank-Collapse and Detail Re-injection for Efficient Safety-Helmet Detection},
  author={Duong, Hoa Van and Nguyen, Thuan Gia and Nguyen, Thinh Quang and Nguyen, Long Thanh and Ngoc, Hoang Tran},
  booktitle={Multi-disciplinary Trends in Artificial Intelligence},
  pages={379--391},
  year={2027},
  publisher={Springer, Singapore},
  doi={10.1007/978-981-92-6510-7_29},
  url={https://link.springer.com/chapter/10.1007/978-981-92-6510-7_29}
}
```

### IEEE
```
H. V. Duong, T. G. Nguyen, T. Q. Nguyen, L. T. Nguyen, and H. T. Ngoc, "Rank-Collapse and Detail Re-injection for Efficient Safety-Helmet Detection," in Multi-disciplinary Trends in Artificial Intelligence (MIWAI), Springer, Singapore, pp. 379–391, doi: 10.1007/978-981-92-6510-7_29.
```

### APA
```
Duong, H. V., Nguyen, T. G., Nguyen, T. Q., Nguyen, L. T., & Ngoc, H. T. (2027). Rank-Collapse and Detail Re-injection for Efficient Safety-Helmet Detection. In Multi-disciplinary Trends in Artificial Intelligence (pp. 379-391). Springer, Singapore. https://doi.org/10.1007/978-981-92-6510-7_29
```

---

## 🔒 Access Policy Notice

> **Note:** In strict compliance with Springer Nature publisher licensing and academic copyrights, the complete full-text version of the paper is distributed directly via the [Springer Nature Chapter Link](https://link.springer.com/chapter/10.1007/978-981-92-6510-7_29). No unauthorized PDF documents are hosted within this repository.
