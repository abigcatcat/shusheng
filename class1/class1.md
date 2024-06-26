第一节：书生·浦语大模型全链路开源开放体系
========
本节介绍了书生·浦语大模型全链路开源体系，包含数据处理，预训练，微调，部署，评测和应用，书生浦语2.0包含三个版本，InternLM2-base(模型基座),InternLM2-chat(增加了SFT和RLHF),InternLM2(加强版模型基座）。

![image text](https://github.com/abigcatcat/shusheng/blob/main/class1/%E5%BC%80%E6%BA%90%E4%BD%93%E7%B3%BB.png)                                                                                                                     
数据处理：
-----
书生万卷1.0包含文本数据，图像-文本数据，视频数据，并进行了多模态融合，精细化处理和价值观对齐。书生万卷CC数据集时间跨度更长，来源更丰富，安全性更高。数据集获取：https://opendatalab.org.cn/。     
![image text](https://github.com/abigcatcat/shusheng/blob/main/class1/%E6%95%B0%E6%8D%AE.png)  


预训练：
-----
使用 InternLM-Train 进行，具有并行训练并与 HuggingFace 生态系统集成以支持轻量级技术。 它允许使用易于使用的语言模型和可配置的训练设置。
![image text](https://github.com/abigcatcat/shusheng/blob/main/class1/%E9%A2%84%E8%AE%AD%E7%BB%83.png)  
微调：
-----
开发了xtuner框架，可以增量徐训（学习新知识），训练数据为书籍等；有监督微调（理解指令），训练数据为高质量对话和问答数据。XTuner适应各种微调策略和算法，支持从HuggingFace和ModelScope加载模型和数据集，提供自动加速优化，并适应不同的硬件。
![image text](https://github.com/abigcatcat/shusheng/blob/main/class1/%E5%BE%AE%E8%B0%83.png)  
部署：
------
LMDeploy 提供了在 GPU 上部署大型模型的全面解决方案，包括模型轻量化、推理和服务。
![image text](https://github.com/abigcatcat/shusheng/blob/main/class1/%E9%83%A8%E7%BD%B2.png)  
评测：
------
通过OpenCompass进行，通过CompassRank（性能排行榜）、CompassKit（全栈评估工具）和CompassHub（高质量评估基准社区）提供全面、可重复的性能评估。
![image text](https://github.com/abigcatcat/shusheng/blob/main/class1/%E8%AF%84%E6%B5%8B.png)  
应用：
------
专注于支持Lagent、AgentLego等各种代理和工具，提供支持LangChain、Transformers Agent、lagent等系统的多模态代理工具包。 它为各种输入/输出格式提供了简单的工具功能调用接口，并支持一键远程工具部署。
![image text](https://github.com/abigcatcat/shusheng/blob/main/class1/%E6%99%BA%E8%83%BD%E4%BD%93.png)  
实现思路：
------
![image text](https://github.com/abigcatcat/shusheng/blob/main/class1/%E5%85%B8%E5%9E%8B%E6%B5%81%E7%A8%8B.png) 
