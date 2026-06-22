# 材料科学数据资源大全

[English](README.md) | **简体中文**

> 一份面向**材料科学 / 计算材料 / 材料信息学与机器学习**的精选数据资源清单：涵盖数据库、数据集、ML 基准、通用仓库、表征与光谱、软件工具等。持续扩充。

这份清单按"用途"而非"材料类别"组织，方便快速定位。每条目都标注了**可获取性**（开放 / 半开放 / 商业）和**数据性质**（计算 / 实验）。本清单受 [`sedaoturak/data-resources-for-materials-science`](https://github.com/sedaoturak/data-resources-for-materials-science) 启发，并在其基础上大幅补全了晶体学三大库、光谱与表征、ML 基准、2D / 电池 / 热电 / 超导等领域库、软件工具链与文献挖掘资源。

---

## 图例

| 标签 | 含义 |
|---|---|
| 🟢 | 开放免费 |
| 🟡 | 半开放（需注册 / 部分付费） |
| 🔴 | 商业订阅 |
| 🧮 | 以计算数据为主（DFT、MD、ML） |
| 🧪 | 以实验 / 实测数据为主 |

---

## 目录

1. [计算与 DFT 数据库](#1-计算与-dft-数据库)
2. [晶体学与结构数据库](#2-晶体学与结构数据库)
3. [实验与工程性能数据库](#3-实验与工程性能数据库)
4. [光谱与表征数据库](#4-光谱与表征数据库)
5. [专题领域数据库](#5-专题领域数据库)
6. [机器学习数据集与基准](#6-机器学习数据集与基准)
7. [通用数据仓库](#7-通用数据仓库)
8. [显微与图像数据集](#8-显微与图像数据集)
9. [原子间势与力场](#9-原子间势与力场)
10. [软件与工具](#10-软件与工具)
11. [文献挖掘与文本资源](#11-文献挖掘与文本资源)
12. [书籍与手册](#12-书籍与手册)
13. [学习资源与教学数据集](#13-学习资源与教学数据集)
14. [贡献与许可](#14-贡献与许可)

---

## 1. 计算与 DFT 数据库

大规模第一性原理 / 高通量计算数据库，是 ML 势函数与材料筛选的主力数据源。

- 🟢 🧮 **[Materials Project](https://materialsproject.org/)** — DFT 计算的无机化合物（数十万），含生成能、能带、弹性/压电张量、X 射线吸收谱与电池浏览器；提供 REST + Python API（`mp-api`）。
- 🟢 🧮 **[OQMD — Open Quantum Materials Database](https://oqmd.org/)** — ~100 万+ 材料的 DFT 热力学与结构性质；整库可下载。
- 🟢 🧮 **[AFLOW](http://aflowlib.org/)** — 350 万+ 化合物、7 亿+ 计算属性，含属性预测与原型搜索工具。
- 🟢 🧮 **[JARVIS (NIST)](https://jarvis.nist.gov/)** — 集成多种模拟的仓库：DFT、力场、ML、STM 数据集，外加用于基准测试的 JARVIS-Leaderboard。
- 🟢 🧮 **[NOMAD](https://nomad-lab.eu/)** — 遵循 FAIR 原则的仓库，收录 1 亿+ 第一性原理计算的原始与解析输入输出；支持自定义 AI 工具与 NOMAD 百科。
- 🟢 🧮 **[Materials Cloud](https://www.materialscloud.org/)** — 基于 AiiDA 工作流的策展 / 归档 / 交互板块，溯源完全可复现。
- 🟢 🧮 **[Alexandria Materials Database](https://alexandria.icams.rub.de/)** — 数百万 DFT 弛豫结构（3D/2D/1D），PBE/PBEsol/SCAN，含可用于训练 MLIP 的轨迹。
- 🟢 🧮 **[NRELMatDB](https://materials.nrel.gov/)** — NREL 的计算材料数据库，聚焦能源相关材料。
- 🟢 🧮 **[Computational Materials Repository (CMR)](https://cmr.fysik.dtu.dk/)** — DTU 策展的 DFT 数据集（ASE/GPAW 配套），每个都附文档与下载。
- 🟢 🧮 **[OPTIMADE](https://www.optimade.org/)** — 不是数据库，而是一套*统一的 API 规范*，让你用一套接口查询 Materials Project、OQMD、AFLOW、COD、NOMAD、JARVIS 等众多库。
- 🔴 🧮🧪 **[Pauling File / MPDS](https://mpds.io/)** — 无机化合物的晶体结构、相图与物性；大型策展商业库，提供开放 API 档位。

## 2. 晶体学与结构数据库

晶体结构（CIF）的权威来源——做结构识别、XRD 物相、生成模型训练时绕不开。

- 🟢 🧪 **[Crystallography Open Database (COD)](http://www.crystallography.net/cod/)** — 50 万+ 有机 / 无机 / 金属有机化合物与矿物晶体结构的开放集合。
- 🔴 🧪 **[ICSD — 无机晶体结构数据库](https://icsd.products.fiz-karlsruhe.de/)** — 最大的全鉴定无机晶体结构策展库（FIZ Karlsruhe）。订阅制。
- 🔴 🧪 **[CCDC / 剑桥结构数据库 (CSD)](https://www.ccdc.cam.ac.uk/)** — 120 万+ 实验测定的有机与金属有机晶体结构。订阅制，沉积者可免费访问 WebCSD。
- 🔴 🧪 **[ICDD PDF（粉末衍射文件）](https://www.icdd.com/)** — 用于物相鉴定的标准粉末衍射图谱。商业。
- 🟢 🧪 **[American Mineralogist Crystal Structure Database (AMCSD)](http://rruff.geo.arizona.edu/AMS/amcsd.php)** — 矿物学期刊发表的开放晶体结构。
- 🟢 🧮 **[Bilbao Crystallographic Server](https://www.cryst.ehu.es/)** — 关于空间群、对称性、能带表示与拓扑分析的免费程序与数据库。

## 3. 实验与工程性能数据库

工程材料的力学 / 热 / 物理性能——选材、对标、数据挖掘常用。

- 🟢 🧪 **[NIST Standard Reference Data (SRD)](https://www.nist.gov/srd)** — 数十个权威参考数据库的总目录（热物性、动力学、合金、陶瓷、扩散等）。
- 🟡 🧪 **[MatWeb](https://www.matweb.com/)** — 10 万+ 金属 / 聚合物 / 陶瓷 / 复合材料数据表；免费检索，批量导出收费。
- 🟡 🧪 **[Matmatch](https://matmatch.com/)** — 工程选材数据库（~3 万+ 材料），含供应商链接。
- 🟡 🧪 **[NIMS MatNavi / DICE](https://mits.nims.go.jp/en/)** — NIMS 系列材料库：聚合物（PoLyInfo）、无机、金属、超导、扩散、蠕变等。
- 🔴 🧪 **[Springer Materials](https://materials.springer.com/)** — Landolt-Börnstein 及跨材料类的策展物性数据，含可视化工具。
- 🔴 🧪 **[Ansys Granta (MaterialUniverse / MI)](https://www.ansys.com/products/materials)** — 业界标准的材料物性数据库与选材软件。
- 🔴 🧪 **[Total Materia](https://www.totalmateria.com/)** — 全球金属数据库：标准、成分、性能、牌号互查。
- 🟢 🧪 **[MakeItFrom](https://www.makeitfrom.com/)** — 免费、易读的典型工程材料性能概览。
- 🟢 🧪 **[The Engineering ToolBox](https://www.engineeringtoolbox.com/)** — 面向工程计算的气体 / 流体 / 固体性质。
- 🟢 🧪 **[HTEM DB（高通量实验材料库）](https://htem.nrel.gov/)** — 组合法生长薄膜的成分、结构、光学与电学性质（NREL）。

## 4. 光谱与表征数据库

谱图与表征数据（IR / Raman / XRD / XAS / UV-Vis 等）——结构鉴定、谱图反演与谱-性质学习的基础。

- 🟢 🧪 **[RRUFF](https://rruff.info/)** — 矿物的参考 Raman、红外、XRD 与化学数据；事实标准的矿物光谱库。
- 🟢 🧪 **[NIST Chemistry WebBook](https://webbook.nist.gov/chemistry/)** — 数万种化合物的 IR、质谱、UV-Vis 谱及热化学数据。
- 🟢 🧪 **[SDBS（有机化合物谱库）](https://sdbs.db.aist.go.jp/)** — 有机化合物的 IR、¹H/¹³C NMR、MS、Raman、ESR 谱（日本 AIST）。
- 🟢 🧪 **[HITRAN](https://hitran.org/)** — 气相吸收的高分辨分子光谱线表（大气与燃烧科学）。
- 🟢 🧮 **[Materials Project XAS](https://next-gen.materialsproject.org/xas)** — FEFF 计算的 X 射线吸收谱（XANES + EXAFS，K/L 边）：50 万+ 谱、4 万+ 材料，可经 `mp-api`（`mpr.materials.xas.search`）查询。
- 🟢 🧮 **[ORNL AISD-Ex](https://www.osti.gov/biblio/1969001)** — ~1000 万有机分子的计算 UV/Vis（TD-DFT）吸收谱。

## 5. 专题领域数据库

按应用领域分组的数据库。

### 聚合物
- 🟡 🧪 **[PoLyInfo (NIMS)](https://polymer.nims.go.jp/en/)** — 最大的聚合物物性库：来自文献的结构、加工与性能。
- 🟡 🧮 **[Polymer Genome](https://www.polymergenome.org/)** — 基于 ML 的聚合物性能预测平台（Ramprasad 组）。
- 🟢 🧮 **[Khazana](https://khazana.gatech.edu/)** — 聚合物与分子数据仓库，附 ML 就绪描述符（佐治亚理工）。
- 🟢 🧪 **[Polymer Property Predictor and Database (PPPDB)](https://pppdb.uchicago.edu/)** — 从文献抽取并策展的 χ 参数与玻璃化转变温度。

### 玻璃与陶瓷
- 🟢 🧪 **[SciGlass](https://github.com/epam/SciGlass)** — 42 万+ 玻璃成分及性能；现已在 GitHub 开源。
- 🟢 🧮 **[Python for Glass Genomics (PyGGi)](https://pyggi.iitd.ac.in/)** — 玻璃性能建模与优化平台（IIT Delhi）。

### MOF 与多孔材料
- 🟢 🧮 **[CoRE MOF](https://zenodo.org/records/3370144)** — 由 CSD 衍生、清洗到可直接模拟的"计算就绪"实验 MOF 结构（4 万+）。
- 🟢 🧮 **[QMOF Database](https://github.com/Andrew-S-Rosen/QMOF)** — 2 万+ MOF，含 DFT 计算的电子性质；也可在 Materials Project 浏览。
- 🟢 🧮 **[Open DAC (ODAC23)](https://open-dac.github.io/)** — 面向直接空气捕集的 MOF 中 CO₂/H₂O 吸附大规模 DFT 数据集（Meta FAIR Chemistry）。

### 催化与表面
- 🟢 🧮 **[Catalysis-Hub.org](https://www.catalysis-hub.org/)** — DFT 表面反应能学，含交互可视化与 GraphQL API。
- 🟢 🧮 **[Open Catalyst Project / FAIR Chemistry](https://opencatalystproject.org/)** — OC20、OC22、OCx24 催化数据集与预训练模型（`fairchem`）。

### 钙钛矿
- 🟢 🧪 **[The Perovskite Database Project](https://www.perovskitedatabase.com/)** — 从 16000+ 篇钙钛矿太阳能电池论文中手工抽取的器件与材料数据。

### 二维材料
- 🟢 🧮 **[C2DB — Computational 2D Materials Database](https://cmr.fysik.dtu.dk/c2db/c2db.html)** — 4000+ 原子级薄材料，含结构、电子、磁性与光学性质（DTU）。
- 🟢 🧮 **[2DMatPedia](http://www.2dmatpedia.org/)** — 自上而下与自下而上筛选得到的 6000+ 二维结构。

### 电池与能源
- 🟢 🧪 **[Battery Archive](https://batteryarchive.org/)** — 标准化的公开电池循环与安全数据仓库，内置可视化与 CSV 导出。
- 🟢 🧮 **[Materials Project Battery Explorer](https://next-gen.materialsproject.org/)** — 计算的嵌入 / 转化电极性质（电压、容量、稳定性）。

### 热电
- 🟢 🧪 **[Starrydata2](https://www.starrydata2.org/)** — 从 13000+ 篇论文数字化提取的 19 万+ 性能曲线（Seebeck、电阻率、热导率）；文献曲线数据共享的范例。

### 超导
- 🟢 🧪 **[SuperCon (NIMS)](https://supercon.nims.go.jp/en/)** — 经典超导数据库；清洗后的 2.6 万条版本在 [MDR](https://mdr.nims.go.jp/collections/5712mb227)。
- 🟢 🧮🧪 **[3DSC](https://github.com/aimat-lab/3DSC)** — 将 SuperCon 条目匹配到三维晶体结构，可直接做基于结构的 ML。

### 相图与热力学
- 🔴 🧪 **[ASM Alloy Phase Diagram Database](https://matdata.asminternational.org/apd/)** — 数万张经评估的二元 / 三元合金相图。
- 🟢 🧪 **[NIST Self-Diffusion and Impurity Diffusion Database](https://www.nist.gov/srd)** — 扩散系数与 Arrhenius 参数（属 NIST SRD）。

## 6. 机器学习数据集与基准

可直接喂给模型的数据集与标准化基准——做属性预测、势函数、生成模型时优先看这些。

- 🟢 🧮 **[Matbench](https://matbench.materialsproject.org/)** — 材料性能预测的标准 13 任务监督学习基准。
- 🟢 🧮 **[Matbench Discovery](https://matbench-discovery.materialsproject.org/)** — 评测通用 ML 原子间势在高通量稳定性预测上的排行榜。
- 🟢 🧮 **[MoleculeNet](https://moleculenet.org/)** — 分子机器学习基准套件（量子、物理、生物物理、生理任务）。
- 🟢 🧮 **[Quantum-Machine 数据集 (QM7 / QM9 / MD17 / rMD17)](http://quantum-machine.org/datasets/)** — 经典的小分子量子化学数据集，用于能量 / 力学习。
- 🟢 🧮 **[ANI-1 / ANI-1x](https://github.com/isayev/ANI1_dataset)** — 数百万非平衡 DFT 构象，用于神经网络势。
- 🟢 🧮 **[GNoME](https://github.com/google-deepmind/materials_discovery)** — Google DeepMind 发现的 38 万+ 稳定晶体，含结构与能量。
- 🟢 🧮 **[OMat24 / OMol25 / OC20-22（Hugging Face 上的 FAIR Chemistry）](https://huggingface.co/facebook)** — Meta FAIR 的大规模开放 DFT 数据集与基础模型。
- 🟢 🧮 **[Mechanical MNIST](https://github.com/elejeune11/Mechanical-MNIST)** — 非均质材料形变的基准数据集，用于代理模型。
- 🟢 🧮🧪 **[Hugging Face Datasets — materials 标签](https://huggingface.co/datasets?search=materials)** — 社区上传的材料与化学数据集，持续增长。

## 7. 通用数据仓库

跨学科数据托管平台——很多论文的补充数据 / 原始数据集就挂在这些地方，按 DOI 检索。

- 🟢 **[Zenodo](https://zenodo.org/)** — CERN 支持的开放仓库；可为任何数据集 / 代码 / 补充材料分配 DOI。
- 🟢 **[Figshare](https://figshare.com/)** — 通用科研产出仓库，广泛用于材料补充数据。
- 🟢 **[Mendeley Data](https://data.mendeley.com/)** — Elsevier 的科研数据仓库，常被期刊文章引用。
- 🟢 **[Dryad](https://datadryad.org/)** — 策展的开放科研数据仓库（CC0）。
- 🟢 **[Kaggle Datasets](https://www.kaggle.com/datasets)** — 社区数据集与竞赛，部分聚焦材料 / 化学。
- 🟢 **[Harvard Dataverse](https://dataverse.harvard.edu/)** — 大型通用机构数据仓库。
- 🟢 🧮🧪 **[Materials Data Facility (MDF)](https://www.materialsdatafacility.org/)** — 发布与发现大型材料数据集，为 ML 流水线设计。
- 🟢 🧮🧪 **[Materials Commons](https://materialscommons.org/)** — 存储与共享实验 / 计算材料数据的协作平台，带溯源。

## 8. 显微与图像数据集

图像类数据——做计算机视觉 / 显微图像分割与分类的素材。

- 🟢 🧪 **[DoITPoMS Micrograph Library](https://www.doitpoms.ac.uk/miclib/)** — 数百张带标注的光学与电子显微图（剑桥）。
- 🟢 🧪 **[UHCSDB — 超高碳钢显微组织库](http://uhcsdb.materials.cmu.edu/)** — 带元数据的超高碳钢显微组织 SEM 图（CMU）。
- 🟢 🧮🧪 **[NOMAD AI Toolkit / Encyclopedia](https://nomad-lab.eu/)** — 在计算归档之外提供可视化的计算材料数据。

## 9. 原子间势与力场

势函数与基础模型——分子动力学和大尺度模拟的核心。

- 🟢 🧮 **[OpenKIM](https://openkim.org/)** — 策展、经测试的原子间模型，含模拟器无关的 API 与可复现性测试。
- 🟢 🧮 **[NIST Interatomic Potentials Repository](https://www.ctcms.nist.gov/potentials/)** — 经审核的经典势（EAM、MEAM、ReaxFF……），附评估数据。
- 🟢 🧮 **[MatPES](https://matpes.ai/)** — 用于训练通用 MLIP 的基础势能面数据集（Materials Virtual Lab）。

## 10. 软件与工具

读取 / 处理这些数据库、做特征工程与训练模型的常用库。

- 🟢 **[pymatgen](https://pymatgen.org/)** — 材料分析与访问 Materials Project 的标准 Python 库。
- 🟢 **[matminer](https://hackingmaterials.lbl.gov/matminer/)** — 数据挖掘与特征化工具包，内置大量现成数据集加载器。
- 🟢 **[ASE — Atomic Simulation Environment](https://wiki.fysik.dtu.dk/ase/)** — 搭建、运行、分析原子模拟，桥接多数 DFT/MD 程序。
- 🟢 **[JARVIS-Tools](https://github.com/usnistgov/jarvis)** — JARVIS 数据库、描述符与 ML 的 Python 工具包。
- 🟢 **[AiiDA](https://www.aiida.net/)** — 自动溯源的工作流引擎；Materials Cloud 的底座。
- 🟢 **[automatminer](https://github.com/hackingmaterials/automatminer)** — 材料性能预测的自动化 ML 流水线。
- 🟢 **[MatGL (M3GNet / MEGNet)](https://github.com/materialsvirtuallab/matgl)** — 材料的图深度学习模型与通用势。
- 🟢 **[CHGNet](https://github.com/CederGroupHub/chgnet)** — 含电荷信息的预训练通用神经网络势。
- 🟢 **[MACE](https://github.com/ACEsuit/mace)** — 高精度等变消息传递原子间势。
- 🟢 **[DScribe](https://github.com/SINGROUP/dscribe)** — 用于原子体系 ML 的描述符库（SOAP、MBTR、库仑矩阵……）。

## 11. 文献挖掘与文本资源

从论文里"挖"数据、做 NLP / 知识图谱的工具与语料入口。

- 🟢 **[Matscholar](https://matscholar.com/)** — 基于对 500 万+ 摘要做 NLP 的材料感知文献检索（材料 / 性质 / 方法的命名实体识别）。
- 🟢 **[ChemDataExtractor](http://www.chemdataextractor.org/)** — 从文本自动抽取化学信息与性质表的工具包。
- 🟢 **[OpenAlex](https://openalex.org/)** — 完全开放的学术索引，收录 2.5 亿+ 文献、作者与概念，含免费 API。
- 🟢 **[Semantic Scholar API](https://www.semanticscholar.org/product/api)** — 免费编程访问论文元数据、摘要、引用与嵌入向量。

## 12. 书籍与手册

权威纸质 / 电子手册——查标准数值和经验关联式时仍然是金标准。

- **Materials Handbook**, 15th Edition — Brady, Clauser & Vaccari
- **Smithells Metals Reference Book**, 8th Edition — Gale & Totemeier
- **Materials Science and Engineering Handbook**, 3rd Edition — Shackelford & Alexander
- **MMPDS Handbook**（Metallic Materials Properties Development and Standardization）
- **Handbook of Materials Structures, Properties, Processing and Performance** — Murr
- **ASM Handbook Set**（38 卷）— ASM International
- **CASTI Metals Handbook — Nonferrous Metals**, 4th Edition
- **Materials Handbook: A Concise Desktop Reference**, 2nd Edition — Cardarelli

## 13. 学习资源与教学数据集

入门练手用的小数据集、教程与 notebook。

- 🟢 **[JARVIS-Tools Notebooks](https://github.com/JARVIS-Materials-Design/jarvis-tools-notebooks)** — 用 JARVIS 做材料 ML 的实操 Colab notebook。
- 🟢 **[matminer dataset loaders](https://hackingmaterials.lbl.gov/matminer/dataset_summary.html)** — 一行代码获取数十个策展基准数据集，适合教学与原型。
- 🟢 **[nanoHUB](https://nanohub.org/)** — 模拟工具、课程与已发布的纳米材料数据集。
- 🟢 **[Materials Project Workshop](https://workshop.materialsproject.org/)** — 关于 pymatgen、MP API 与高通量工作流的免费教程。

## 14. 贡献与许可

**贡献**
发现死链、过期条目或值得收录的资源，欢迎提 Issue 或 PR。请保持一行一条目，标注可获取性（🟢/🟡/🔴）与数据性质（🧮/🧪），并归入最贴切的章节。

**免责声明**
本清单只是对**外部资源的索引**。每个数据库 / 数据集都有各自的许可与使用条款，使用前请自行核对。链接与可用性可能随时间变化。

**许可**
本清单（README 本身）以 [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/) 公有领域方式释出。
