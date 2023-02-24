# ABSLearn
Inferring aliasing and buffer-size information is important to understanding a C program's memory layout, which is critical to program analysis and security-related tasks. However, traditional static and dynamic program analysis methods suffer from certain limitations: static alias analysis methods suffer from precision loss and have poor scalability. Meanwhile, although dynamic analysis can achieve high precision, there is no soundness guarantee, and an online analysis may cause non-negligible runtime overhead. Besides, the current methods can only capture aliasing information. As for the buffersize relational information, which is the specific variable storing the size of the buffer pointed by the pointers, it is tough to analyze by traditional methods. Moreover, we observe that most methods are designed for specific information. To address these limitations, we present ABSLearn, a deep learning framework that is capable of retrieving both aliasing and buffersize information from C programs. The core idea of ABSLearn is to formulate the information retrieval as a link prediction problem, where a Graph Neural Network (GNN) model is applied to solve the problem. We developed the first related dataset that contains 285 C program samples to train ABSLearn. Then, the trained model is applied to infer the information on three practical benchmarks: Gzip-1.2.4, Make-3.80, and Tar-1.15.1. The results show that ABSLearn achieves comparable performance and excellent runtime performance. As the first attempt at applying GNN to infer aliasing and buffer-size information, ABSLearn can potentially benefit future program analysis frameworks.

Codes will be released ASAP.

🌻  If the paper and datasets is also useful for you, please cite: 
```
@Article{ABSLearn,
author={Liang, Ke and Tan, Jim and Zeng, Dongrui and Huang, Yongzhe and Huang, Xiaolei and Tan, Gang},
title={ABSLearn: a GNN-based framework for aliasing and buffer-size information retrieval},
journal={Pattern Analysis and Applications},
year={2023},
month={Feb},
day={19},
issn={1433-755X},
doi={10.1007/s10044-023-01142-2},
url={https://doi.org/10.1007/s10044-023-01142-2}
}
```
