> 本文由 [简悦 SimpRead](http://ksria.com/simpread/) 转码， 原文地址 [mp.weixin.qq.com](https://mp.weixin.qq.com/s/bBOsuI-f7mGCt_AUZkteXA)

> ![](https://mmbiz.qpic.cn/mmbiz_png/fUBU1yiaEmJiawNBPPibQx77icD7oXRl84CpnkwdqQT8ScvgQ20ohcqCxdxoXFUCNuQlJ4McYxmicWR7HqRGfaTnD0w/640?wx_fmt=png)
> 
> 其中：
> 
> 语言模型：解决基座问题，目前包括 llama，bloom,glm 等，但这些都存在版权问题，开源协议规定禁止商用；‍‍‍‍‍‍‍‍‍‍‍‍
> 
> 指令微调数据：解决所需要的对齐 sft 数据，根据场景指定，包括 alpaca、belle、guanaco 等百万级微调数据，  
> 
> 微调加速：解决的是低资源下的训练问题，贫民玩法，其中热度最高的为 LoRA 是一种以极低资源微调大模型的方法，其来自于论文 LoRA: Low-Rank Adaptation of Large Language Models。
> 
> 由于 meta-llama 的小参数以及论文中的高性能介绍，目前已经出现系列的变体。

> ![](https://mmbiz.qpic.cn/mmbiz_png/fUBU1yiaEmJiawNBPPibQx77icD7oXRl84CpG54iafZtoQ0icDmG2jTtRSoxaQtr9uKGcaFgslTibkB1xLvxB47KUmRLw/640?wx_fmt=png)
> 
> 如上图所示，对于数据，首先通过自学方法生成了后续指导演示。从自学种子集的 175 个人工编写的指令 - 输出对开始。然后，提示 text-davinci-003 使用种子集作为上下文示例生成更多指令。通过简化生成 pipeline，改进了自我指导方法，并显著降低了成本。我们的数据生成过程产生了 52K 个独特的指令和相应的输出，使用 OpenAI API 的成本不到 500 美元。