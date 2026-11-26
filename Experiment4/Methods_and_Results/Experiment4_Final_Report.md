# Experiment 4 — Final Evidence Report

## Scope

Independent threshold-aware evaluation of Visible and Infrared drone predictions on the Anti-UAV300 test split.

## Detection-level results

### Visible

- Highest observed F1: 0.9458
- Corresponding confidence threshold: 0.30
- TP: 7368; FP: 226; FN: 618
- Precision: 0.9702
- Recall: 0.9226

### Infrared

- Highest observed F1: 0.9223
- Corresponding confidence threshold: 0.40
- TP: 7428; FP: 251; FN: 1001
- Precision: 0.9673
- Recall: 0.8812

## Image-level alert analysis

Alert means at least one prediction reaches the confidence threshold. Positive-image alert coverage does not guarantee correct localization.

## Validation

- Ground-truth distribution audit: PASS for both modalities.
- Prediction-to-test-image alignment audit: PASS; no prediction IDs outside the test split.
- Bounding-box sanity audit: no invalid or non-finite boxes; two boxes per modality exceed image bounds by only approximately 0.001 pixels.
- Cross-result consistency audit: PASS for both modalities.

## Workload assumption

Estimated review time is 10 seconds per alerted image. This is a hypothetical workload estimate, not a human-subject or operator-performance measurement.

## Limitations

- Threshold analysis is exploratory on the test split.
- Adjacent video frames may repeat the same event.
- No real-world operator study or field deployment is claimed.
- This experiment evaluates drone detection only.

## Reproducibility provenance

- Source predictions: `Experiment2/Evaluation/Experiment2_Test_Evaluation_Evidence.zip`
- Original dataset combined SHA-256: `c644f40169369fb843373ae2e7ac54a0d44bffe6128b6198fa3d398bbca73ec1`
- IoU threshold: 0.50
- Confidence thresholds: 0.10–0.90 in increments of 0.10
- Generated UTC: 2026-11-24T14:52:04.248675+00:00
