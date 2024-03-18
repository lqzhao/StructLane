# StructLane
> StructLane: Leveraging Structural Relations for Lane Detection (Under Peer Review)
> 
> Linqing Zhao, Wenzhao Zheng, Yunpeng Zhang, Jie Zhou, Jiwen Lu

## Introduction
Accurately detecting the lanes plays a significant role in various autonomous and assistant driving scenarios. It is a highly structured task as lanes in the 3D world are continuous and parallel to each other. While most existing methods focus on how to inject structural priors into the representation of each lane, we propose a StructLane method to further leverage the structural relations among lanes for more accurate and robust lane detection. To achieve this, we explicitly encode the structural relations using a set of relational templates in a learned structural space. We then employ the attention mechanism to enable interactions between templates and image features to incorporate structural relational priors. Our StructLane can be applied to existing lane detection methods as a plug-and-play module to improve their performance. Extensive experiments on the widely used CULane, TuSimple, and LLAMAS datasets demonstrate that StructLane consistently improves the performance of state-of-the-art models across all datasets and backbones. Visualization results also demonstrate the robustness of our StructLane compared with existing methods due to the leverage of structural relations.

## Method
<p align='center'>
<img src="./assets/layout_pipeline.png" width="720px">
</p>


泛化性实验：
| target\source           | CULane   | LLAMAS    | TuSimple    |
| :----------------------- | :----: | :-----: | :-----: | 
| CULane | -  | 43.14/50.88   | 29.85/37.32 |
| LLAMAS| 57.31/62.46  | -  |90.27/92.84 |
| TuSimple | 68.94/74.11  | 94.47/96.27  |- |

We used templates of source dataset since the templates of real-world scenes are inaccessible.
