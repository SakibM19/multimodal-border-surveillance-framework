# Border Surveillance — Manuscript Evidence

## Overview

This directory contains the manuscript-oriented evidence package for a multimodal border-surveillance research project. It organizes selected experimental results, figures, tables, metrics, audit reports, and supporting evidence archives.

This is an evidence archive for inspection and manuscript support. It is **not, by itself, a complete, self-contained reproduction environment**.

## Contents

| Directory | Contents |
|---|---|
| `Experiment1/` | Person-detection evidence: training and validation figures, test-performance figures, paper tables, threshold results, and independent AP50 audit outputs. |
| `Experiment2/` | Visible and infrared drone-detection evaluation summaries, metrics, dataset YAML files, paper figures, source CSVs, and a figure manifest. |
| `Experiment3/Corrected_Evidence/` | Corrected range-to-pixel and distance-error data, figures, technical report, figure manifest, and correction audit note. An explicitly superseded original report is retained for audit history. |
| `Experiment4/Methods_and_Results/` | Threshold-sweep and image-level alert results, methodology and limitations, ground-truth and consistency audits, final report, and SHA-256 manifest. |
| `Experiment5/Pilot100/` | Pilot-100 robustness-analysis bootstrap inputs, methodology, confidence intervals, and paired-difference results. |
| `Original_Evidence_Archives/` | Earlier experiment-specific evidence ZIP archives retained as supporting records. |

## Scope and interpretation notes

- **Experiment 5 is a 100-image pilot robustness analysis.** This package contains bootstrap inputs and reported bootstrap outputs. It does not contain the complete Experiment 5 execution notebook/scripts, all prediction outputs, or generated figures.
- The Experiment 5 pilot is exploratory; it is not a full-test-set degradation evaluation.
- Experiment 3 is an idealized geometrical distance-sensitivity analysis, not calibrated real-world ranging accuracy.
- Experiment 2 uses separate visible and infrared drone test sets. The results should not be interpreted as a controlled same-image comparison of modality superiority.
- This evidence package does not establish a fully integrated, continuously operating end-to-end surveillance system or a completed operator study.
- Person detection must not be described as armed-person recognition or weapon detection.
- The presence of a result file does not by itself establish that the experiment can be reproduced. Consult the corresponding methodology, configuration, and source-code materials.

## Suggested repository layout

Keep this evidence directory alongside, rather than instead of, the project source code:

```text
repository/
├── README.md
├── notebooks/
│   └── Border_Surveillance_Complete_Source_Code_with_Experiment5.ipynb
├── source/
│   └── experiment scripts and supporting modules
├── manuscript_evidence/
│   └── BORDER_SURVEILLANCE_MANUSCRIPT_EVIDENCE/
└── environment/
    └── requirements.txt
```

Only include source files and environment specifications that have actually been used and verified. Do not include credentials, private tokens, or datasets that you do not have permission to redistribute.

## How to use this package

1. Open the relevant experiment directory.
2. Read its methodology, final report, audit note, or manifest where available.
3. Use CSV and JSON files as machine-readable supporting results.
4. Use PDF figures for manuscript-quality inspection and PNG figures for previews.
5. Treat outputs explicitly identified as corrected as authoritative. Retain superseded files only for audit traceability, not as current results.

## Integrity and versioning

For a research release, record:
- the Git commit or release tag associated with the evidence;
- the source-code/notebook version used to produce each result;
- dataset versions and access conditions;
- software/library versions and relevant configuration settings;
- checksums for important files, especially large inputs and archives.

Do not claim that this archive is fully reproducible unless the code, data access, environment, and execution instructions needed to regenerate the outputs are also supplied.

## License and data rights

This README does not assert a license for third-party datasets or archived source materials. Check the original dataset and source-material terms before redistribution. Add an explicit project license only after deciding which materials you have the right to license.
