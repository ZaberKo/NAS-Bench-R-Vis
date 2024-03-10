# RobustNASBench Issues

## Hypothesis: There are some issues in the training stage

1. There are many models in MSU with small best_epoches for the best model.

    The best_epoch distribution:

    SUSTech:
    ![](./fig/best_epoch_sustech.png)
    MSU:
    ![](./fig/best_epoch_msu.png)

2. By comparing the metric of the same model (arch_id ~6000, #nums=169), models trained from SUSTech have better performance. 

    ![](./fig/dup_test_acc.png)
    ![](./fig/dup_test_fgsm.png)
    ![](./fig/dup_test_pgd.png)
    ![](./fig/dup_test_cw.png)

    And the training curves are different: MSU models suffer more Robust Overfitting.

    Arch_6006 training curves:
    ![](./fig/dup_Arch6006_training_curves.png)

    Arch_6028 training curves:
    ![](./fig/dup_Arch6028_training_curves.png)

    Arch_6033 training curves:
    ![](./fig/dup_Arch6033_training_curves.png)                     

    Arch_6118 training curves:
    ![](./fig/dup_Arch6118_training_curves.png)

    Arch_6327 training curves:
    ![](./fig/dup_Arch6327_training_curves.png)



Potential Reasons: 

- Different lr (different lr decay rate) or Different PGD attack hyperparams at the training stage?
  - The SUSTech training code is checked: it is as same as the github code.
  - We also found that some initially trained models in SUSTech (around Mar 2023) are also in the "vertical line" area. The training code at that time could be the same as the MSU code.
  - ![](./fig/local_train_issue.png)

- Different GPU: the training code enables optimized cuda operations by `torch.backends.cudnn.benchmark = True`
  - **Unlikely**. We found that MSU models with different GPUs during training have low accuracy.
  - ![](./fig/msu_gpu_issue.png)
  
