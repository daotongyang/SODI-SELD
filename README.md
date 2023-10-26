# SODI-SELD
## DATASETS
The dataset can be downloaded from the link-[https://zenodo.org/records/6387880](https://zenodo.org/records/6387880) and [https://zenodo.org/records/6406873](https://zenodo.org/records/6406873)  
Please look at the following links in detail about dataset:[https://dcase.community/challenge2022/task-sound-event-localization-and-detection-evaluated-in-real-spatial-sound-scenes](https://dcase.community/challenge2022/task-sound-event-localization-and-detection-evaluated-in-real-spatial-sound-scenes)
## Getting Started
This repository consists of multiple Python scripts forming one big architecture used to train the SELDnet.
The `batch_feature_extraction.py` is a standalone wrapper script, that extracts the features, labels, and normalizes the training and test split features for a given dataset. Make sure you update the location of the downloaded datasets before.
The parameter.py script consists of all the training, model, and feature parameters. If a user has to change some parameters, they have to create a sub-task with unique id here. Check code for examples.
The cls_feature_class.py script has routines for labels creation, features extraction and normalization.
The cls_data_generator.py script provides feature + label data in generator mode for training.
The seldnet_model.py script implements the SELDnet architecture.
The SELD_evaluation_metrics.py script implements the metrics for joint evaluation of detection and localization.
The train_seldnet.py is a wrapper script that trains the SELDnet. The training stops when the SELD error (check paper) stops improving.
The cls_compute_seld_results.py script computes the metrics results on your DCASE output format files. You can switch between using polar or Cartesian based scoring. Ideally both should give identical results.
Additionally, we also provide supporting scripts that help analyse the results.

visualize_seldnet_output.py script to visualize the SELDnet output
