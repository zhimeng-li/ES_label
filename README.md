# Experiments 1–2: Data and Analysis Guide

## Overview

This repository contains the processed data and analysis outputs for Experiments 1 and 2.
Both experiments follow the same general structure:

**Level 1 → Level 2 → final analysis outputs**

Level 1 contains derived behavioral measures created from the cleaned task data. Level 2 combines these measures into participant-level datasets used for statistical analysis. The final analysis stage uses those datasets to generate the reported tests, tables, figures, and model summaries.

Experiment 1 includes two conditions: `WithLabel` and `NoLabel`. Experiment 2 includes those same conditions plus a `Counting` condition.

## Level 1: Derived measures

`Processed Data/Level1_output/` contains intermediate measures derived from the cleaned behavioral data.

The main measure families are:

- **Segmentation / MLU measures** — summaries of how participants segmented each video.
- **Consensus Event Agreement (CEA)** — measures of how closely participants’ event boundaries aligned with consensus event boundaries.
- **Signal Detection Theory (SDT) measures** — measures derived from responses to critical-event and non-critical-event intervals, including sensitivity, response bias, and accuracy.
- **Optimal-bias measures** — comparisons between observed response bias and an estimated optimal criterion.
- **Emotion-word / semantic measures** — participant-level language measures used in supplementary analyses.

Files labeled `full` use consensus events defined from the pooled sample. Files labeled `LAB`, `SEG`, and, in Experiment 2, `COUNT` use condition-specific consensus-event definitions.

## Level 2: Participant-level analysis datasets

`Processed Data/Level2_output/` contains the main datasets used for participant-level statistical analyses.

These files combine relevant Level 1 measures and apply the study’s outlier-screening procedures. Rather than removing an entire participant when a value is flagged, the workflow generally treats the affected measure as missing.

Level 2 includes two complementary analysis approaches:

- **Pooled-event analyses**, based on consensus events defined using the full sample.
- **Within-condition analyses**, based on consensus events defined separately within each experimental condition.

These datasets provide the main inputs for the analyses reported in the project.

## Final analysis outputs

The final analysis scripts use the Level 2 datasets, along with selected Level 1 summaries where needed, to produce the study results.

Outputs include:

- descriptive summaries;
- statistical tests and effect-size estimates;
- supplementary model results;

