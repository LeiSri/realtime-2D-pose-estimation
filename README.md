# realtime-2D-pose-estimation
paper:https://openaccess.thecvf.com/content_cvpr_2017/papers/Cao_Realtime_Multi-Person_2D_CVPR_2017_paper.pdf
Realtime Multi-Person 2D Pose Estimation using Part Affinity Fields
使用 Part Affinity Fields 的实时多人 2D 姿态估计

本文算法主要流程如下：
![image](https://user-images.githubusercontent.com/47564814/128984184-cf943feb-fd46-493d-948b-3ed0ed7ac389.png)

即输入一幅图像，经过卷积网络提取特征，得到一组特征图，然后分成两个岔路，分别使用 CNN网络提取Part Confidence Maps 和 Part Affinity Fields 。
得到这两个信息后，我们使用图论中的 Bipartite Matching 将同一个人的关节点连接起来得到最终的结果。
