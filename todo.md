- 画图
- 跑一下MobileNet作为backbone的实验
  - 0 - pretrained 用MobileNet.pth
  - 1 - pretrained 用IR50-MS1M那个
- 跑一下F1作为各项指标的实验
- 改论文中的公式解释
- 对比加没加entropy的伪标签的准确率和对应的accuracy，在消融实验那部分加上加了entropy condition 和不加entropy condition的实验

| Method Contrast | Source set | Target set | Accuracy            | Recall              | Precision           | F1                  | My Folder  |
| --------------- | ---------- | ---------- | ------------------- | ------------------- | ------------------- | ------------------- | ---------- |
| AGRA / CGLRL    | RAF-DB     | ExpW       | 67.65 / 70.29（g）  | 47.65 / 49.91（g）  | 51.13 / 53.67（g）  | 48.48 / 50.48（g）  | 1648863452 |
| AGRA / CGLRL    | RAF-DB     | FER2013    | 57.44 / 59.30（gl） | 54.15 / 54.57（gl） | 50.98 / 54.12（gl） | 47.41 / 49.89（gl） | 1648863267 |
| AGRA / CGLRL    | RAF-DB     | SFEW2.0    | 53.21 / 56.88（g）  | 45.18 / 49.48（g）  | 50.04 / 58.86（gl） | 42.50 / 46.91（g)   | 1648863716 |
| AGRA / CGLRL    | FER2013    | ExpW       | 53.89 / 61.96（lm） | 42.93 / 44.96（gl） | 38.38 / 41.58（g）  | 35.51 / 37.48（gl)  | 1648864350 |
| AGRA / CGLRL    | FER2013    | RAF-DB     | 69.29 / 72.06（gl） | 60.74 / 58.22（gl） | 62.13 / 67.68（gl） | 53.42 / 53.89（gl） | 1648864147 |
| AGRA / CGLRL    | FER2013    | SFEW2.0    | 41.06 / 52.29（gl） | 33.43 / 44.09（g）  | 54.93 / 44.72（g）  | 29.24 / 43.02（g）  | 1648865646 |

AGRA可以不用跑得很高

Recall 、Precision、F1都是取平均值

