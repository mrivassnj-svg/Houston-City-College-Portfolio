---
title: "Module 01: Introduction to Computer Vision"
module_id: "01"
course_slos: "SLOs 1, 2"
generated_at_utc: "2026-08-08T22:50:21Z"
research_status: "protocol-design"
---

# Module 01: Introduction to Computer Vision

## Executive Abstract

This module is designed as a reproducible empirical investigation within a Computer Vision and Robotics research portfolio. The objective is not merely to demonstrate an implementation, but to evaluate technical claims under an explicit protocol, document uncertainty, and make design trade-offs auditable.

## Research Question

> Evaluate preprocessing latency and quantify face/PII anonymization utility-privacy trade-offs.

## Falsifiable Hypothesis

**H1:** The optimized or proposed configuration will improve the primary task metric relative to the baseline while preserving a pre-specified operational constraint on latency, memory, robustness, or calibration.

**H0:** Any observed performance difference between configurations is not practically meaningful under the established evaluation protocol.

## Technical Scope

- **Course SLOs:** SLOs 1, 2
- **Technology stack:** OpenCV; PIL; Ethics Frameworks
- **Mechanics under study:** CV pipeline design, classical and modern workflows, ethics, privacy, bias evaluation.
- **Primary investigation:** Evaluate preprocessing latency and quantify face/PII anonymization utility-privacy trade-offs.

## Experimental Design

| Component | Specification |
|---|---|
| Unit of analysis | Image, frame, track, prompt-image pair, or agent decision event |
| Baseline | Simplest defensible reference implementation |
| Treatment | Optimized, fine-tuned, or alternative architecture |
| Controls | Dataset split, seed, hardware, preprocessing, and stopping criteria |
| Replications | Minimum 3 runs when computationally feasible |
| Primary metric | Task-specific metric defined before final evaluation |
| Secondary metrics | Latency, memory, throughput, calibration, fairness, robustness |
| Statistical reporting | Mean, standard deviation, confidence interval, and effect size |
| Error analysis | Stratified failure analysis by domain, scale, lighting, class, or motion |

## Evaluation Protocol

1. Freeze the dataset manifest and data split before comparative training.
2. Run the baseline and candidate systems under matched hardware and input conditions.
3. Capture configuration, seed, package versions, Git commit, wall-clock time, and resource use.
4. Aggregate repeated runs and report uncertainty rather than a single best run.
5. Inspect qualitative failures and document conditions under which the system should not be used.

## Benchmark Matrix

| Variant | Dataset Version | Seed | Latency (ms) | Throughput | Primary Metric | 95% CI | Memory | Notes |
|---|---|---:|---:|---:|---:|---:|---:|---|
| Baseline | TBD | TBD | TBD | TBD | TBD | TBD | TBD | Reference implementation |
| Candidate A | TBD | TBD | TBD | TBD | TBD | TBD | TBD | Proposed improvement |
| Candidate B | TBD | TBD | TBD | TBD | TBD | TBD | TBD | Ablation or deployment variant |

## Reproducibility Checklist

- [ ] Dataset source, license, consent constraints, and checksum documented
- [ ] Train/validation/test split versioned and leakage-reviewed
- [ ] Configuration committed in `configs/`
- [ ] Random seeds fixed and recorded
- [ ] Environment and hardware captured
- [ ] Raw run logs saved in `results/`
- [ ] Aggregate tables and plots exported to `figures/` and `reports/`
- [ ] Failure cases and limitations documented
- [ ] Privacy, bias, and misuse risks assessed

## Responsible AI and Governance

Assess dataset representativeness, annotation quality, privacy risk, disparate error rates, confidence calibration, and deployment failure modes. For human-centered or surveillance-adjacent applications, avoid claiming suitability without context-specific validation, lawful data handling, and meaningful human oversight.

## Directory Contract

| Path | Purpose |
|---|---|
| `configs/` | Versioned experiment configurations |
| `data/` | Raw, interim, processed, and external data references |
| `src/` | Reusable implementation code |
| `experiments/` | Experiment entrypoints and run manifests |
| `results/` | Machine-readable metrics and run metadata |
| `figures/` | Publication-quality visualizations |
| `reports/` | Technical reports, analyses, and model cards |
| `tests/` | Unit, integration, and regression tests |

---
Portfolio curator: Michael Anthony Rivas  
Generated: 2026-08-08T22:50:21Z
### 🔍 Extracted Implementation Evidence
- **File:** `L02_Rivas_Michael_ITAI1378.ipynb` (Lines 157, 184) — Image I/O via `cv2.imread` / `cv2.imwrite`
- **File:** `Lab05_CNN_Chihuahua_Muffin.ipynb` (Lines 1755, 1781, 1867) — Ethical Audit Framework (`EthicalAuditFramework`), Fairness Disparity Checks, and Privacy Impact Analysis
- **File:** `Lab_06_Michael_Rivas (1).ipynb` (Line 1547) — Local-first & Privacy Protection Architecture

