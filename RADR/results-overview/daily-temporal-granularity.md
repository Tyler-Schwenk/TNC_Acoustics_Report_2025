# Daily Temporal Granularity

## Overview

Here I compare the two new models, evaluating their performance at the task of daily presence/absence monitoring, given data from the previous year's audio monitoring.&#x20;

* 'Precision model' at Sensitivity: 1.5, Threshold: 0.3
* 'F1 focused model' at Sensitivity: 0.75, Threshold: 1.0

***

## **Context & Methodology:**

To estimate real-world performance at daily temporal granularity I analyzed calling activity from the 2024/2025 field season, collecting days where positive RADR detections occurred. This included data from 9 recorders across 139 recording nights.&#x20;

During the previous season the recording schedule used was from 5pm-11pm, 1 min on / 9 min off - producing **432 1-minute files per night**, which translates to **8,640 3-second segments** for model inference. This ground truth is used to project false positive burden and detection confidence under different model configurations.

#### **2024/2025 Calling Season Data Summary:**

During the previous season, these were quantities of audio files containing positive calls for a given night that was determined to have RADR vocalizations present.

| Files/Night | # of Nights | % of Nights | Cumulative |
| ----------- | ----------- | ----------- | ---------- |
| 1 file      | 11          | 7.9%        | 7.9%       |
| 2-10 files  | 44          | 31.7%       | 39.6%      |
| 11-25 files | 19          | 13.7%       | 53.3%      |
| 26+ files   | 65          | 46.7%       | 100%       |

***

## Evaluation

### False Absence Risk by Calling Activity

Probability of missing detection = (1 - Recall)^N, where N = number of positive files

| Calling Activity | Nights  | F1 Missed        | Precision Missed | 2024             |
| ---------------- | ------- | ---------------- | ---------------- | ---------------- |
| 1 file           | 11      | 1.4 nights       | 4.2 nights       | 1.6 nights       |
| 2-10 files       | 44      | <1 night         | \~2 nights       | <1 night         |
| 11+ files        | 84      | 0 nights         | 0 nights         | 0 nights         |
| **Total**        | **139** | **\~1.4 nights** | **\~6.2 nights** | **\~1.7 nights** |

#### Expected Missed Detections Per Season

| Model                    | Missed Nights     | Daily Detection Accuracy |
| ------------------------ | ----------------- | ------------------------ |
| **Best F1 Model**        | 1.4 / 139 (1.0%)  | **99.0%**                |
| **High Precision Model** | 6.2 / 139 (4.5%)  | **95.5%**                |
| **2024 Model**           |  1.7 / 139 (1.2%) | **98.8%**                |

***

### Expected Review Burden

Per Median Night (20 true positives, 8,640 segments processed):

Review Time = Total Flagged Files × 3 seconds

Where: Total Flagged = (20 × Recall) + (8,620 × (1 - Precision))

| Model                    | False Positives | Total Flagged | Review Time/Night | Season Total (139 nights) |
| ------------------------ | --------------- | ------------- | ----------------- | ------------------------- |
| **Best F1 Model**        | 888 files       | 906 files     | 45 minutes        | 104 hours                 |
| **High Precision Model** | 129 files       | 141 files     | 7 minutes         | 16 hours                  |
| **2024 Model**           | 2,069 files     | 2,086 files   | 104 minutes       | 241 hours                 |

***

Full calculations for 2024/2025 calling season:

{% file src="../.gitbook/assets/positive_counts_by_recorder_date (1).txt" %}
