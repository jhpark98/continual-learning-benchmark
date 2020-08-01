# Continual Learning Benchmark [![forthebadge made-with-python](http://ForTheBadge.com/images/badges/made-with-python.svg)](https://www.python.org/)

This repo contains the code for reproducing the results of the following papers:

1. [Continual Learning in Human Activity Recognition: An Emperical Analysis of Regularization](https://drive.google.com/file/d/1B-p_xzlA2j56LtzxQyUHA34QwxedJosJ/view) [Accepted at ICML 2020 workshop on Continual Learning]
2. Benchmarking Continual Learning in Sensor-based Human Activity Recognition: an Empirical Analysis [Submitted to the Pervasive and Mobile Computing Journal]

![Incremental learning](https://github.com/srvCodes/continual-learning-benchmark/blob/master/utils/img/incremental_learning.png)

A sub-total of 11 recent continual learning techniques have been implemented so far:

1. Maintaining Discrimination and Fairness in Class Incremental Learning [[Paper](https://openaccess.thecvf.com/content_CVPR_2020/papers/Zhao_Maintaining_Discrimination_and_Fairness_in_Class_Incremental_Learning_CVPR_2020_paper.pdf)]
2. Adjusting Decision Boundary for Class Imbalanced Learning [[Paper](https://ieeexplore.ieee.org/document/9081988)]
3. Large Scale Incremental Learning [[Paper](https://openaccess.thecvf.com/content_CVPR_2019/papers/Wu_Large_Scale_Incremental_Learning_CVPR_2019_paper.pdf)]
4. Learning a Unified Classifier Incrementally via Rebalancing [[Paper](http://dahualin.org/publications/dhl19_increclass.pdf)]
5. Incremental Learning in Online Scenario [[Paper](https://openaccess.thecvf.com/content_CVPR_2020/papers/He_Incremental_Learning_in_Online_Scenario_CVPR_2020_paper.pdf)]
6. Gradient Episodic Memory for Continual Learning [[Paper](https://papers.nips.cc/paper/7225-gradient-episodic-memory-for-continual-learning.pdf)]
7. Efficient Lifelong Learning with A-GEM [[Paper](https://openreview.net/forum?id=Hkf2_sC5FX)]
8. Elastic Weight Consolidation [[Paper](https://arxiv.org/pdf/1612.00796.pdf)]
9. Rotated Elastic Weight Consolidation [[Paper](https://arxiv.org/abs/1802.02950)]
10. Learning without Forgetting [[Paper](https://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=8107520)]
11. Memory Aware Synapses [[Paper](https://link.springer.com/chapter/10.1007/978-3-030-01219-9_9)]

Additionally, the following six exemplar-selection techniques are available (for memory-rehearsal):

1. Herding from ICaRL [[Paper](https://openaccess.thecvf.com/content_cvpr_2017/papers/Rebuffi_iCaRL_Incremental_Classifier_CVPR_2017_paper.pdf)]
2. Frank-Wolfe Sparse Regression [[Paper](https://arxiv.org/abs/1811.02702)]
3. K-means sampling
4. DPP sampling 
5. Boundary-based sampling [[Paper](https://ieeexplore.ieee.org/document/8986833)]
6. Sensitivity-based sampling [[Paper](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=8949290)]

## Running the code

For training, please execute the `runner.sh` script that creates all the directories required for logging the outputs. One can add further similar commands for running further experiments.

For instance, training on *ARUBA* dataset with FWSR-styled exemplar selection:

```python
>>> python runner.py --dataset 'aruba' --total_classes 11 --base_classes 2 --new_classes 2 --epochs 160 --method 'kd_kldiv_wa1' --exemplar 'fwsr' # e.g. for FWSR-styled exemplar selection

```

## Evaluating the logs

For evaluation, please uncomment the lines per the instructions in `runner.py`. This can be used to measure forgetting scores [1], base-new-old accuracies, and average report by holdout sizes.

## Verification

The implementations have been verified through their runs on Permumted-MNIST.

## Personal Note 

_This work was done as my **EMJMD Master's thesis** at the University of St Andrews._ :smiley:

## Acknowledgement

Special thanks to [sairin1202](https://github.com/sairin1202)'s implementation of [BiC](https://github.com/sairin1202/BIC) and [Electronic Tomato](https://github.com/ElectronicTomato)'s implementation of [GEM/AGEM/EWC/MAS](https://github.com/ElectronicTomato/continue_leanrning_agem/tree/master/agents). 

## References

[1] Chaudhry, A., Dokania, P.K., Ajanthan, T., & Torr, P.H. (2018). Riemannian Walk for Incremental Learning: Understanding Forgetting and Intransigence. ECCV.


[![forthebadge made-with-python](https://github.com/pytorch/pytorch/blob/master/docs/source/_static/img/pytorch-logo-dark.svg)](https://pytorch.org/)
