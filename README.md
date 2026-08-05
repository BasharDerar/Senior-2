# Senior-2: Concept-Guided Medical Image Caption Generation

This repository contains the implementation notebooks and final thesis report for Senior Project II.

## Project Title

Concept-Guided Medical Image Caption Generation Using UMLS Concept Detection and Image–Concept Fusion

## Student

Bashar Alsaleh  
Faculty of Artificial Intelligence Engineering  
Syrian Private University

## Supervisors

Dr. Riad Sonbol  
Eng. Zeinab Baghdadi

## Overview

This project studies medical image caption generation using UMLS-based concept guidance. The work investigates how different sources of semantic and visual information affect caption quality, including ground-truth concepts, predicted concepts, image-only features, and final image-concept fusion.

The experiments are based on ImageCLEFmedical Caption 2026 data and build upon a previous concept detection model developed in Senior Project I.

## Experiments

| Experiment | Description |
|---|---|
| Exp1 | T5-base using raw ground-truth CUI codes |
| Exp2 | T5-base using ground-truth CUI codes enriched with UMLS terms |
| Exp3 | Predicted-concept fine-tuning using noisy predicted UMLS concepts |
| Exp4 | Mixed training using ground-truth and predicted concepts |
| Exp5 | Image-only captioning using BiomedCLIP visual prefix and T5 |
| Exp6 | Final image-concept fusion using BiomedCLIP visual prefix and UMLS concept text |

## Repository Structure

```text
notebooks/
  01_exp1_gt_cui_only_t5.ipynb
  02_exp2_gt_cui_umls_terms_t5.ipynb
  03_exp3_predicted_concept_finetuning.ipynb
  04_exp4_mixed_gt_predicted_training.ipynb
  05_exp5_image_only_biomedclip_visual_prefix.ipynb
  06_exp6_image_concept_fusion.ipynb

reports/
  Senior2_Graduation_Project_Thesis_Bashar_Alsaleh.pdf

## Dataset Note

The dataset files, medical images, checkpoints, and trained model weights are not included in this repository because of size and access restrictions. The notebooks contain the experimental pipeline and expected Google Drive paths used during development.

## Main Methodology

The project follows a controlled experimental design:

1. Study raw CUI-based caption generation.
2. Add readable UMLS term enrichment.
3. Evaluate the effect of predicted concept noise.
4. Improve robustness using mixed ground-truth and predicted concept training.
5. Evaluate visual-only caption generation using BiomedCLIP.
6. Combine visual features and UMLS concepts in the final fusion model.

## Important Evaluation Note

Ground-truth concept settings are treated as oracle upper-bound experiments. Predicted-concept settings represent the practical deployment scenario. Dictionary-based UMLS F1 is used as an internal medical concept consistency metric and should not be interpreted as identical to official MedCAT-based UMLS evaluation.

## License

No license is currently provided. This repository is intended for academic review purposes.
