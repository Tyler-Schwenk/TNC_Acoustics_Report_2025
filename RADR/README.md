# Introduction

The goal of this project was to refine the previous _Rana draytonii_ BirdNET&#x20;machine learning model (2024 model). The previous model had false positive detections which resulted in unacceptable manual review labor requirements to verify results. By iterating on the&#x20;existing model and developing recommended default settings we achieved improved precision, recall and accuracy through two separate models, known as the **F1** and **Precision** models.

The **F1** model was aimed at maximizing the discriminatory ability of the model in terms of AUC and F1 - the '[F1\_model\_2025](setup-workflow.md#high-f1-model)', and the **Precision** model maximized precision - the '[Precision\_model\_2025](setup-workflow.md#recommended-high-precision-model)'. Both new models also demonstrate more stability across configuration settings, and have improved generalization to new datasets and domain shift.

#### Overview Metrics

<table><thead><tr><th width="230">Model Name (Goal)</th><th width="93">F1</th><th width="100">Precision</th><th width="86">Recall</th></tr></thead><tbody><tr><td><strong>F1 (Max. AUC and F1)</strong></td><td>88.6%</td><td>89.7%</td><td>87.5%</td></tr><tr><td><strong>Precision (Max. Precision)</strong></td><td>76.1%</td><td>98.5%</td><td>62.0%</td></tr><tr><td><strong>2024</strong></td><td>80.3%</td><td>76.0%</td><td>85.1%</td></tr></tbody></table>

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
