---
description: Evaluation of standard BirdNET model for detecting bullfrogs
---

# BirdNET Evaluation

Due to our initial deployment of the ASU 2 in the field being towards the end of the bullfrog calling season, and the fact that the device malfunctioned, we were unable to properly test the device's accuracy on real bullfrog calls. For this reason we focused primarily on testing the device in terms of its reliability and functionality, rather than specific metrics for detection accuracy.

***

## Reliability

To ensure a baseline ability to detect bullfrogs we used the following 5-minute recording of various bullfrog sounds played out of a phone speaker near the device.

{% file src="../.gitbook/assets/bullfrogs_5min.wav" %}

## Bullfrog True Positive Detections

The device was able to correctly identify the bullfrog recording in all playbacks it received. It did not provide any false positives for bullfrogs during the time of our monitoring (2 months of recording with varying schedules).

| Date       | Slot | Playback Time(s)                           | Transmission Time | # Detections |
| ---------- | ---- | ------------------------------------------ | ----------------- | ------------ |
| 2025-08-27 | 9    | Playback occurred (timestamp not recorded) | 20:37             | 52           |
| 2025-09-21 | 31   | Playback occurred (timestamp not recorded) | 10:07             | 29           |
| 2025-09-21 | 40   | Playback occurred (timestamp not recorded) | 13:07             | 58           |
| 2025-09-29 | 39   | 11:50; 12:40                               | 12:47             | 7            |
| 2025-10-02 | 51   | 16:20; 16:40                               | 16:47             | 12           |
| 2025-10-09 | 11   | 05:00                                      | 05:07             | 5            |
| 2025-10-20 | 27   | 14:03                                      | 15:43             | 9            |
| 2025-10-21 | 29   | 16:30                                      | 16:43             | 22           |
| 2025-10-21 | 41   | 16:30; 22:27                               | 22:43             | 33           |
| 2025-10-24 | 11   | 08:39                                      | 08:43             | 9            |
| 2025-11-24 | 4    | 22:15                                      | 23:50             | 34           |

### False Positives

The device consistently reported false positives. Below are the top 6 reported classes over the course of our monitoring. Note that “detections” here are reported by Instinct as the number of instances where a class is identified in a 3-second audio segment. This means in a 5-minute audio recording there are 100 segments, which could each provide a ‘detection’.

* Arizona toad - 1109 detections
* Engine - 855+ detections
* Human vocal - 507+ detections
* American bullfrog - 270 detections
* Snowy tree cricket - 207 detections

All ‘arizona toad’ detections were likely false positives, as they were not present in the area of study. Some engine detections could have come from the road or washing machine that was present near the device. ‘Human vocal’ detections were likely real detections of the tester’s home. All ‘American bullfrog’ detections came as a result of playback from the user, there were no instances of bullfrogs being reported in absence of a playback. ‘Snowy tree cricket’ was likely real detections of nearby crickets.

***

## Metrics

For a more in depth analysis of BirdNET's ability to identify bullfrog calls we differ to the paper referenced [here](https://doi.org/10.1007/s10530-023-03244-8), which collected metrics from Belgium and Italy

Their setup used "default values for the sensitivity parameter (1.0), overlap of prediction segments (no overlap, 0), and confidence score (threshold of 0.1)." This resulted in the following findings:

"BirdNET was highly effective in automatically detecting the bullfrog presence, with a detection rate (compared to visual inspection of sonograms) of 89.5% using default settings (85 of 95 recordings with known presence), and 95.8% with user-specific settings (91 of 95 recordings detected). The system showed remarkable precision, correctly identifying 99.7% (612 out of 614) of the verified predictions, and with only one mislabeled recording (predicted to be present when it was absent)"

## Looking Forward

It should be noted that Brad Hollingsworth reported that the model performed worse than what was reported by those folks in his experience, though he did not conduct an experiment to determine any hard metrics. This difference in model performance could be due to regional variability in frog calls.

We advise deploying the devices in the field in the future to get a better understanding of precise performance metrics, and the best setup for the device & model when listening within our local domain.

### References

Bota, G., Manzano-Rubio, R., Fanlo, H. _et al._ Passive acoustic monitoring and automated detection of the American bullfrog. _Biol Invasions_ 26, 1269–1279 (2024). https://doi.org/10.1007/s10530-023-03244-8

