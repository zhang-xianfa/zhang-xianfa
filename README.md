# 张现发

**山东科技大学 · 数据科学与大数据技术 · 2027 届本科**

AI 应用开发　｜　数据分析与开发　｜　后端开发

**在线简历与作品集 → <https://zhangxianfa.pages.dev>**　·　邮箱　1849363242@qq.com

---

## 关于我

数据科学与大数据技术专业 2027 届本科生，GPA 3.47/4.0，专业排名前 12%。

做过 **2 项企业横向课题并担任第一负责人**（煤矿采空区自燃风险预警、油罐车工业计量偏差校正），
习惯在不完整、不规范的真实数据里把问题拆开、定位到根因。也独立完成过从数据采集、
模型训练到服务部署的完整链路。

主要方向：**LLM 应用（RAG / Agent 工作流）**、**机器学习建模**、**大数据平台开发**。

---

## 荣誉奖项

| 级别 | 奖项 |
| --- | --- |
| 省部级 | 全国大学生市场调查与分析大赛 **一等奖**（山东省赛区）<br>全国大学生数学建模竞赛（高教社杯）**二等奖**<br>全国大学生统计建模大赛 **二等奖**<br>五一数学建模竞赛 **二等奖**<br>山东省数学建模竞赛 **三等奖**<br>第八届「鲲鹏杯」山东新动能·软件创新创业大赛 **三等奖**（AI 视觉硬件项目）<br>全球校园人工智能算法精英大赛 算法创新奖 · 蓝桥杯程序设计竞赛 省奖 |
| 国家级 | 国家励志奖学金 |
| 院校级 | 一等奖学金 · 优秀学生干部 · 优秀共青团员 · 优秀学生标兵 · 三好学生 · 数学九五奖学金 |
| 科研 | 参与国家级大创 1 项（机器视觉方向）、校级大创 3 项，均已结项 |

---

## 项目

### AI 与大模型应用

- **[medical-qa-rag](https://github.com/zhang-xianfa/medical-qa-rag)**　`Python` `FastAPI` `LangGraph` `PostgreSQL` `pgvector` `Docker`
  医疗 AI 多轮问诊系统。用 LangGraph 编排「安全检测 → 基础问诊 → 专家问诊 → 诊断报告」四阶段工作流；
  「向量 + BM25」双路召回并以 RRF 融合，按来源权威度加权；封装 LLM 适配层做 embedding 三级降级、
  四重 JSON 修复与 Pydantic 校验。后端 6036 行、8 个 REST 接口、9 张数据表，
  24 个 E2E 用例 100% 自动化，Docker Compose 4 服务部署至腾讯云。

- **[fingerprint-enhancement](https://github.com/zhang-xianfa/fingerprint-enhancement)**　`PyTorch` `GAN` `OpenCV`
  潜在指纹增强 —— 多尺度 PatchGAN 条件生成对抗网络：U-Net 生成器（7 层编解码 + 跳跃连接）
  配 3 尺度判别器（谱归一化），前 2 轮热身期冻结判别器，用 L1 损失稳定早期训练。
  **山东省大学生数学建模竞赛 三等奖**。

### 机器学习与建模

- **[coal-fire-warning](https://github.com/zhang-xianfa/coal-fire-warning)**　`PyTorch` `PyG` `GNN`
  企业横向课题（第一负责人）：煤矿采空区自燃风险时空预警。设计分层时空图神经网络 ——
  微观层多头 GAT 捕捉测点间气流关联，宏观层 GCN 抽象巷道趋势，跨层双向消息传递，再用 GRU 建模时序；
  自研非对称风险感知损失对 CO 漏报加倍惩罚。产出 254 张风险热力图与 3D 巷道可视化。

- **[scvi-breast-cancer-lung-metastasis](https://github.com/zhang-xianfa/scvi-breast-cancer-lung-metastasis)**　`scVI` `Scanpy` `GSEA`
  乳腺癌肺转移机制挖掘。用 scVI 变分自编码器做单细胞转录组批次效应整合，
  与 ComBat / Harmony / CCA / fastMNN 四种方法定量对比，kBET 0.549、LISI 4.121 均为最优。
  **全国大学生统计建模大赛 省级二等奖**。

- **[str-mixture-identification](https://github.com/zhang-xianfa/str-mixture-identification)**　`XGBoost` `Pyro` `PyTorch`
  法医物证多人身份鉴定 —— STR 混合图谱解析。四个问题分别用 XGBoost 判断贡献者人数（准确率 88%）、
  Pyro 贝叶斯神经网络推断混合比例（MAE 0.0671）、分层一维 CNN 预测基因型、
  Savitzky-Golay 滤波配合峰检测抑制图谱噪声。

- **[cumcm-2025-a-smoke-interference](https://github.com/zhang-xianfa/cumcm-2025-a-smoke-interference)**　`MATLAB` `SciPy`
  2025 高教社杯全国大学生数学建模竞赛 A 题（第一负责人）。把「能否遮挡视线」的几何判定转化为
  以导弹为顶点作切锥的判据，构造平滑遮蔽质量函数把不可导的布尔判定变成可优化目标，
  用差分进化 + L-BFGS-B 求解 4~40 维投放策略。**省级二等奖**。

- **[wuyi-mcm-2025-c-social-media](https://github.com/zhang-xianfa/wuyi-mcm-2025-c-social-media)**　`TensorFlow` `LSTM` `scikit-learn`
  2025 五一数学建模竞赛 C 题。分析社交媒体平台的用户—博主交互行为：逐博主训练 **BiLSTM**
  预测新增关注，用 **LSTM + 集成学习**（随机森林 / 梯度提升）预测用户的新关注行为，
  并按 24 个时段做活跃分布分析。**二等奖**。

- **[sme-credit-risk-modeling](https://github.com/zhang-xianfa/sme-credit-risk-modeling)**　`XGBoost` `LightGBM` `scikit-learn`
  中小微企业信贷风险评估（2020 高教社杯 C 题）。把进销项发票流水聚合成企业级经营特征，
  用 **XGBoost / LightGBM / 决策树** 三套模型估计违约概率（网格搜索 + 分层交叉验证，
  以 ROC-AUC / 精确率 / 召回率 / F1 评估），再把两个强模型的输出**取平均降低小样本方差**。

- **[tank-volume-correction](https://github.com/zhang-xianfa/tank-volume-correction)**　`NumPy` `SciPy` `MATLAB`
  企业横向课题（第一负责人）：油罐车变位场景下的工业计量偏差校正。建立卧式油罐储液体积几何模型
  （200×100 网格二重数值积分），以「装车体积 = 卸车体积」为物理约束逐仓拟合校正系数，
  处理 3303 条装卸记录，整体平均相对误差 **0.736%**。

### 数据开发与大数据

- **[retail-data-warehouse](https://github.com/zhang-xianfa/retail-data-warehouse)**　`Hive` `Spark SQL` `Flume` `Sqoop`
  零售离线数仓 ODS / DWD / DWS 分层构建。设计三层逐层对账（行数、金额合计、维度基数），
  金额合计零差异；定位 HiveServer2 查询瓶颈并开启本地执行模式，
  接口响应由 **57.2 秒降至 1.6~3.2 秒**。

- **[job-crawler-analysis](https://github.com/zhang-xianfa/job-crawler-analysis)**　`curl_cffi` `Playwright` `MySQL` `Flask`
  招聘岗位数据采集与分析平台。实现 requests / curl_cffi（TLS 指纹伪装）/ Playwright 三套请求方案
  并实测拦截率，配合随机休眠、分页冷却与失败熔断；清洗入库后用 pandas 做分布统计与薪资分析，
  jieba + WordCloud 生成技能需求词云，Flask 提供检索看板。

- **[qingdao-lard-market-survey](https://github.com/zhang-xianfa/qingdao-lard-market-survey)**　`AMOS` `结构方程模型` `随机森林`
  青岛脂渣消费机制与营销策略研究（建模负责人）。面向高校学生与城市居民两个群体分别采样，
  基于 SOR 理论构建结构方程模型检验 8 个潜变量与 H1–H8 假设体系；
  用随机森林（基尼指数）对 7 类感知价值因素做重要性排序，
  并与 SEM 路径结论交叉印证。**全国大学生市场调查与分析大赛 山东省赛区一等奖**。

### Web 与后端

- **[sake-secondhand-marketplace](https://github.com/zhang-xianfa/sake-secondhand-marketplace)**　`Flask` `SQLAlchemy` `MySQL` `SocketIO`
  SAKE 校园二手交易平台（**5 人团队，本人任队长**）。基于 Flask 蓝图拆分 9 个功能模块，
  Flask-SQLAlchemy + Alembic 管理 11 张表；本人实现实时私信（会话表 + 私信表 + SocketIO 定向推送）、
  消息中心、商品多图上传与级联删除。

---

## 技术栈

| 方向 | 技术 |
| --- | --- |
| AI 与算法 | PyTorch · 图神经网络（GAT / GCN / GRU）· 时序建模 · LLM 应用（RAG / LangGraph / Prompt 工程） |
| 数据与建模 | Pandas · NumPy · SciPy · SQL · 特征工程 · 假设检验 · 时间序列分析 · SPSS / AMOS |
| 大数据平台 | Hadoop（HDFS / YARN）· Hive · Spark SQL · Flume · Sqoop |
| 后端与工程 | Python · FastAPI · Flask · RESTful · Linux / Shell · Git · Docker |
| 数据库 | PostgreSQL（pgvector）· MySQL · Redis |

---

## 联系

- 在线简历：<https://zhangxianfa.pages.dev>
- 邮箱：1849363242@qq.com
- 微信：vx19045382689
