# Introduction

The goal of this project was to "Refine the application of the previously developed Rana draytonii BirdNET&#x20;machine learning model to reduce manual review effort of field recordings. This will be accomplished by iterating on the&#x20;existing model and by developing recommended default settings to achieve specific precision, recall and accuracy."

This goal was realized in the form of two separate models. One model was aimed at maximizing the discriminatory ability of the model in terms of AUC and F1 - the '[F1\_model\_2025](setup-workflow.md#high-f1-model)', and another at maximizing precision - the '[Precision\_model\_2025](setup-workflow.md#recommended-high-precision-model)'.

Both new models also demonstrate more stability across configuration settings, and have improved generalization to new datasets and domain shift.

#### Overview Metrics

| Configuration Goal  | F1    | Precision | Recall |
| ------------------- | ----- | --------- | ------ |
| **Best Overall F1** | 88.6% | 89.7%     | 87.5%  |
| **High-Precision**  | 76.1% | 98.5%     | 62.0%  |
| **2024**            | 80.3% | 76.0%     | 85.1%  |

In the context of daily presence/absence monitoring, the Precision model reduces false positive detections by 93.8% when compared to the 2024 baseline, while maintaining 95.5% daily detection accuracy.

***

### Where to go next

* [Usage Instructions](setup-workflow.md)\
  Pick a model, setup and run inference.
* [Final Model Analysis](results-overview/)\
  In depth performance analysis, comparison to 2024 model, and daily presence/absence calculations.
* [Audio Data Split Design](audio-data-split-design/)\
  How the labeled dataset was built and split.
* [Parameter Effects](parameter-effects/)\
  Deep dives on what moved metrics: data composition, augmentation, regularization, imbalance, and hyperparameters.
* [Alternative Methodologies Explored](other-methodologies-explored/)\
  Approaches that were explored, and either dropped or held for future development.
* [Environmental Impact](environmental-impact.md)\
  Training cost and practical compute notes.
* [Staged Sweeps Design](staged-sweeps-design/)\
  The full archive of experiments designed and evaluated over the course of this contract.

### Resources

* Custom training pipeline used for development: [https://github.com/Tyler-Schwenk/BirdNET-CustomClassifierSuite](https://github.com/Tyler-Schwenk/BirdNET-CustomClassifierSuite)
