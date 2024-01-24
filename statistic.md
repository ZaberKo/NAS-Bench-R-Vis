# NasBenchRobust

- [NasBenchRobust](#nasbenchrobust)
  - [Note](#note)
    - [Current (2024/01/20):](#current-20240120)
  - [Arch distribution](#arch-distribution)
  - [Performance Metric Comparison](#performance-metric-comparison)
    - [params _vs._ accs:](#params-vs-accs)
    - [macs _vs._ accs:](#macs-vs-accs)
    - [accs _vs._ accs:](#accs-vs-accs)
    - [accs correlation:](#accs-correlation)
  - [Best Arch distribution](#best-arch-distribution)
    - [Best top20 Arch:](#best-top20-arch)
    - [Best top100 Arch Distribution:](#best-top100-arch-distribution)


## Note

Full Archs: 15625

### Current (2024/01/20):

Total Trained: 14935

Total Evaluated by Base Attacks: 12181

Total Evaluated by AutoAttack: 7417

Note: currently, all test metrics are evaluated on the best model during the training (by CW acc on Val Set -- CIFAR 10.1).

## Arch distribution

Full Arch:

![](fig/params_hist_full.png)
![](fig/macs_hist_full.png)

Training Complete Arch:

![](fig/params_hist.png)
![](fig/macs_hist.png)

Base Attack Complete Arch:

![](fig/params_hist_ba.png)
![](fig/macs_hist_ba.png)

## Performance Metric Comparison

### params _vs._ accs:

![](fig/params_val-best-clean-acc_scatter.png)
![](fig/params_val-best-pgd-acc_scatter.png)
![](fig/params_val-best-cw-acc_scatter.png)

![](fig/params_test-clean-acc_scatter.png)
![](fig/params_test-fgsm-acc_scatter.png)
![](fig/params_test-pgd-acc_scatter.png)
![](fig/params_test-cw-acc_scatter.png)

### macs _vs._ accs:

![](fig/macs_val-best-clean-acc_scatter.png)
![](fig/macs_val-best-pgd-acc_scatter.png)
![](fig/macs_val-best-cw-acc_scatter.png)

![](fig/macs_test-clean-acc_scatter.png)
![](fig/macs_test-fgsm-acc_scatter.png)
![](fig/macs_test-pgd-acc_scatter.png)
![](fig/macs_test-cw-acc_scatter.png)

### accs _vs._ accs:

Note: ignore outlier points during regression and calculating tau

val-best-clean-acc:

![](fig/val-best-clean-acc_test-clean-acc_regress.png)
![](fig/val-best-clean-acc_test-fgsm-acc_regress.png)
![](fig/val-best-clean-acc_test-pgd-acc_regress.png)
![](fig/val-best-clean-acc_test-cw-acc_regress.png)

test-clean-acc:

![](fig/test-clean-acc_test-fgsm-acc_regress.png)
![](fig/test-clean-acc_test-pgd-acc_regress.png)
![](fig/test-clean-acc_test-cw-acc_regress.png)


### accs correlation:

Note: include outliers

Kendall Rank Correlation:

![](fig/corr_ba.png)


## Best Arch distribution

### Best top20 Arch:

Based on Test_PGD_ACC:

![](fig/best-top20-arch.png)

### Best top100 Arch Distribution:

![](fig/best-top100-arch_Depth1_test-clean-acc.png)
![](fig/best-top100-arch_Depth1_test-clean-acc_dist.png)
![](fig/best-top100-arch_Depth1_test-fgsm-acc.png)
![](fig/best-top100-arch_Depth1_test-fgsm-acc_dist.png)
![](fig/best-top100-arch_Depth1_test-pgd-acc.png)
![](fig/best-top100-arch_Depth1_test-pgd-acc_dist.png)
![](fig/best-top100-arch_Depth1_test-cw-acc.png)
![](fig/best-top100-arch_Depth1_test-cw-acc_dist.png)


![](fig/best-top100-arch_Depth2_test-clean-acc.png)
![](fig/best-top100-arch_Depth2_test-clean-acc_dist.png)
![](fig/best-top100-arch_Depth2_test-fgsm-acc.png)
![](fig/best-top100-arch_Depth2_test-fgsm-acc_dist.png)
![](fig/best-top100-arch_Depth2_test-pgd-acc.png)
![](fig/best-top100-arch_Depth2_test-pgd-acc_dist.png)
![](fig/best-top100-arch_Depth2_test-cw-acc.png)
![](fig/best-top100-arch_Depth2_test-cw-acc_dist.png)


![](fig/best-top100-arch_Depth3_test-clean-acc.png)
![](fig/best-top100-arch_Depth3_test-clean-acc_dist.png)
![](fig/best-top100-arch_Depth3_test-fgsm-acc.png)
![](fig/best-top100-arch_Depth3_test-fgsm-acc_dist.png)
![](fig/best-top100-arch_Depth3_test-pgd-acc.png)
![](fig/best-top100-arch_Depth3_test-pgd-acc_dist.png)
![](fig/best-top100-arch_Depth3_test-cw-acc.png)
![](fig/best-top100-arch_Depth3_test-cw-acc_dist.png)

![](fig/best-top100-arch_Width1_test-clean-acc.png)
![](fig/best-top100-arch_Width1_test-clean-acc_dist.png)
![](fig/best-top100-arch_Width1_test-fgsm-acc.png)
![](fig/best-top100-arch_Width1_test-fgsm-acc_dist.png)
![](fig/best-top100-arch_Width1_test-pgd-acc.png)
![](fig/best-top100-arch_Width1_test-pgd-acc_dist.png)
![](fig/best-top100-arch_Width1_test-cw-acc.png)
![](fig/best-top100-arch_Width1_test-cw-acc_dist.png)


![](fig/best-top100-arch_Width2_test-clean-acc.png)
![](fig/best-top100-arch_Width2_test-clean-acc_dist.png)
![](fig/best-top100-arch_Width2_test-fgsm-acc.png)
![](fig/best-top100-arch_Width2_test-fgsm-acc_dist.png)
![](fig/best-top100-arch_Width2_test-pgd-acc.png)
![](fig/best-top100-arch_Width2_test-pgd-acc_dist.png)
![](fig/best-top100-arch_Width2_test-cw-acc.png)
![](fig/best-top100-arch_Width2_test-cw-acc_dist.png)


![](fig/best-top100-arch_Width3_test-clean-acc.png)
![](fig/best-top100-arch_Width3_test-clean-acc_dist.png)
![](fig/best-top100-arch_Width3_test-fgsm-acc.png)
![](fig/best-top100-arch_Width3_test-fgsm-acc_dist.png)
![](fig/best-top100-arch_Width3_test-pgd-acc.png)
![](fig/best-top100-arch_Width3_test-pgd-acc_dist.png)
![](fig/best-top100-arch_Width3_test-cw-acc.png)
![](fig/best-top100-arch_Width3_test-cw-acc_dist.png)