<div align="center">
<h1>Two-stage Pruning During Training for Artificial Neural Networks</h1>

</div>
<div align="center">
<b>Pelinsu Sarac</b><sup>1*</sup>,
<br>
</div>
<div align="center">
<sup>1</sup>Carnegie Mellon University
</div>

## Context
This project was done for the course 18-662: Principles and Engineering Applications of AI at Carnegie Mellon University. 

## Abstract
Deep learning has achieved remarkable success in various domains such as Computer Vision and Natural Language Processing. However, the deployment of these high-performance models on edge and mobile devices remains a challenge due to their large number of parameters. Model pruning has emerged as an effective solution to reduce model size while maintaining accuracy. Most of the pruning methods in literature follow the conventional approach of pruning after training, which involves training a model to convergence, removing low-importance weights, and fine-tuning. In contrast, pruning during training has been explored less due to its dynamic nature and additional computational complexity. In this paper, a simple pruning technique is proposed that removes unnecessary weights dynamically during training using a two-stage scoring approach, applied both to MLPs or at the filter level for CNNs. In the first stage, weights are evaluated based on their gradient magnitudes, under the assumption that smaller gradients indicate less need for updates, hence proximity to the values in convergence. In the second stage, weights with both low magnitude and small gradients are pruned. This method is periodically applied during training, reducing the number of parameters without significantly affecting accuracy. Experiments on MNIST with MLP and on CIFAR-10 with ResNet18 and VGG16 show that this approach effectively sparsifies the model with minimal accuracy degradation under appropriate hyperparameter settings.  Additionally, the results highlight how architectural choices and pruning intervals influence both sparsity and performance.

## File Organization
- Midterm_Progress
  - AI_Project_Progress.ipynb: Includes preliminary experiments (MNIST and MLP) done **without regularization**
  - AI_Project_Progress_Regularization.ipynb: Includes preliminary experiments (MNIST and MLP) done **with regularization**
- Final_Report
  - AI_Project_CNN.ipynb: Includes experiments done using ResNet18 and CIFAR-10, **without regularization**
  - AI_Project_CNN_Regularization.ipynb: Includes experiments done using ResNet18 and CIFAR-10, **with regularization**
  - AI_Project_Ablation.ipynb: Includes experiments done using VGG16 and CIFAR-10, **without regularization**
