# 材料科学数据资源大全

[English](README.md) | **简体中文**

> 一份面向**材料科学 / 计算材料 / 化学 / 材料信息学与机器学习**的精选数据资源清单：涵盖数据库、数据集、ML 基准、通用仓库、表征与光谱、化学信息学、软件工具等。持续扩充。

这份清单按"用途"而非"材料类别"组织，方便快速定位。每条目都标注了**可获取性**（开放 / 半开放 / 商业）和**数据性质**（计算 / 实验）。本清单受 [`sedaoturak/data-resources-for-materials-science`](https://github.com/sedaoturak/data-resources-for-materials-science) 启发并大幅扩充——补全了晶体学三大库、光谱与表征、化学信息学、分子与量子化学数据集、ML 基准，以及 2D / 电池 / 热电 / 超导 / 磁性 / 拓扑 / 沸石等领域库、软件工具链与文献挖掘资源。

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
5. [化学信息学与分子库](#5-化学信息学与分子库)
6. [专题领域数据库](#6-专题领域数据库)
7. [晶体与材料 ML 数据集和基准](#7-晶体与材料-ml-数据集和基准)
8. [分子与量子化学数据集](#8-分子与量子化学数据集)
9. [通用数据仓库](#9-通用数据仓库)
10. [显微与图像数据集](#10-显微与图像数据集)
11. [原子间势与力场](#11-原子间势与力场)
12. [软件与工具](#12-软件与工具)
13. [文献挖掘与文本资源](#13-文献挖掘与文本资源)
14. [书籍与手册](#14-书籍与手册)
15. [学习资源与教学数据集](#15-学习资源与教学数据集)
16. [贡献与许可](#16-贡献与许可)

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
- 🟢 🧮 **[Carolina Materials Database (CMD)](http://www.carolinamatdb.org/)** — 由深度生成模型（CubicGAN、PGCGM）生成、经 DFT 验证的 21.4 万+ 无机化合物，含 25 万+ 计算属性。
- 🟢 🧮 **[Organic Materials Database (OMDB)](https://omdb.mathub.io/)** — 4 万+ 已合成三维有机晶体的 DFT 电子结构（能带、态密度），含数据挖掘工具。
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

谱图与表征数据（IR / Raman / XRD / XAS / XPS / NMR / EELS / UV-Vis 等）——结构鉴定、谱图反演与谱-性质学习的基础。

- 🟢 🧪 **[RRUFF](https://rruff.info/)** — 矿物的参考 Raman、红外、XRD 与化学数据；事实标准的矿物光谱库。
- 🟢 🧪 **[NIST Chemistry WebBook](https://webbook.nist.gov/chemistry/)** — 数万种化合物的 IR、质谱、UV-Vis 谱及热化学数据。
- 🟢 🧪 **[SDBS（有机化合物谱库）](https://sdbs.db.aist.go.jp/)** — 有机化合物的 IR、¹H/¹³C NMR、MS、Raman、ESR 谱（日本 AIST）。
- 🟢 🧪 **[NIST X 射线光电子能谱数据库（XPS, SRD 20）](https://srdata.nist.gov/xps/)** — 3.35 万+ 经评估的结合能、化学位移与俄歇参数。
- 🟢 🧪 **[Raman Open Database (ROD)](https://solsa.crystallography.net/rod/)** — 开放（CC0）的 Raman 谱，与 COD 晶体结构互联。
- 🟢 🧪 **[NMRShiftDB](https://nmrshiftdb.nmr.uni-koeln.de/)** — 开放、社区共建的 ¹H/¹³C（及其他核）NMR 数据库，支持谱预测。
- 🟢 🧪 **[EELS Database (eelsdb.eu)](https://eelsdb.eu/)** — 电子能量损失谱与 X 射线吸收谱的开放仓库。
- 🟢 🧪 **[HITRAN](https://hitran.org/)** — 气相吸收的高分辨分子光谱线表（大气与燃烧科学）。
- 🟢 🧪 **[refractiveindex.info](https://refractiveindex.info/)** — 数千种材料跨波段的光学常数（n、k）。
- 🟢 🧮 **[Materials Project XAS](https://next-gen.materialsproject.org/xas)** — FEFF 计算的 X 射线吸收谱（XANES + EXAFS，K/L 边）：50 万+ 谱、4 万+ 材料，可经 `mp-api`（`mpr.materials.xas.search`）查询。
- 🟢 🧮 **[ORNL AISD-Ex](https://www.osti.gov/biblio/1969001)** — ~1000 万有机分子的计算 UV/Vis（TD-DFT）吸收谱。

## 5. 化学信息学与分子库

大型分子结构 / 生物活性数据库——化学 ML、虚拟筛选，以及作为量化数据集的来源。

- 🟢 🧪 **[PubChem](https://pubchem.ncbi.nlm.nih.gov/)** — 1 亿+ 化合物，含结构、性质、生物测定与专利（NIH）。
- 🟢 🧪 **[ChEMBL](https://www.ebi.ac.uk/chembl/)** — 人工策展的生物活性分子，含成药性质与测定数据（EMBL-EBI）。
- 🟢 🧮 **[ZINC20](https://zinc20.docking.org/)** — 数十亿可商购化合物的即用三维对接格式，用于虚拟筛选。
- 🟢 🧮 **[GDB 系列 (GDB-11/13/17)](http://gdb.unibe.ch/)** — 枚举式小有机分子库（GDB-17 达 1660 亿），用于化学空间探索。
- 🟢 🧪🧮 **[Open Reaction Database (ORD)](https://open-reaction-database.org/)** — 开放、结构化的有机反应数据仓库，用于反应结果 ML。
- 🟢 🧪 **[Therapeutics Data Commons (TDC)](https://tdcommons.ai/)** — 覆盖药物发现全流程的 ML 就绪数据集与基准。

## 6. 专题领域数据库

按应用领域分组的数据库与数据集。

### 聚合物
- 🟡 🧪 **[PoLyInfo (NIMS)](https://polymer.nims.go.jp/en/)** — 最大的聚合物物性库：来自文献的结构、加工与性能。
- 🟡 🧮 **[Polymer Genome](https://www.polymergenome.org/)** — 基于 ML 的聚合物性能预测平台（Ramprasad 组）。
- 🟢 🧮 **[Khazana](https://khazana.gatech.edu/)** — 聚合物与分子数据仓库，附 ML 就绪描述符（佐治亚理工）。
- 🟢 🧪 **[Polymer Property Predictor and Database (PPPDB)](https://pppdb.uchicago.edu/)** — 从文献抽取并策展的 χ 参数与玻璃化转变温度。

### 玻璃与陶瓷
- 🟢 🧪 **[SciGlass](https://github.com/epam/SciGlass)** — 42 万+ 玻璃成分及性能；现已在 GitHub 开源。
- 🟢 🧮 **[Python for Glass Genomics (PyGGi)](https://pyggi.iitd.ac.in/)** — 玻璃性能建模与优化平台（IIT Delhi）。

### 金属有机框架（MOF）
- 🟢 🧮 **[CoRE MOF](https://zenodo.org/records/3370144)** — 由 CSD 衍生、清洗到可直接模拟的"计算就绪"实验 MOF 结构（4 万+）。
- 🟢 🧮 **[QMOF Database](https://github.com/Andrew-S-Rosen/QMOF)** — 2 万+ MOF，含 DFT 计算的电子性质；也可在 Materials Project 浏览。
- 🟢 🧮 **[Open DAC (ODAC23)](https://open-dac.github.io/)** — 面向直接空气捕集的 MOF 中 CO₂/H₂O 吸附大规模 DFT 数据集（Meta FAIR Chemistry）。

### 沸石与多孔材料
- 🟢 🧪 **[IZA Database of Zeolite Structures](https://www.iza-structure.org/databases/)** — 国际沸石协会认证的参考骨架类型。
- 🟢 🧮 **[Deem PCOD 假想沸石库](https://mwdeem.org/PCOD/)** — ~290 万预测沸石结构及计算能量。
- 🟢 🧮 **[MOFX-DB](https://mof.tech.northwestern.edu/)** — 16 万+ 真实与假想 MOF / 沸石（hMOF、ToBaCCo、CoRE）的计算吸附等温线（Snurr 组）。

### 催化与表面
- 🟢 🧮 **[Catalysis-Hub.org](https://www.catalysis-hub.org/)** — DFT 表面反应能学，含交互可视化与 GraphQL API。
- 🟢 🧮 **[Open Catalyst Project / FAIR Chemistry](https://opencatalystproject.org/)** — OC20、OC22、OCx24 催化数据集与预训练模型（`fairchem`）。

### 钙钛矿与光伏
- 🟢 🧪 **[The Perovskite Database Project](https://www.perovskitedatabase.com/)** — 从 16000+ 篇钙钛矿太阳能电池论文中手工抽取的器件与材料数据。

### 二维材料
- 🟢 🧮 **[C2DB — Computational 2D Materials Database](https://cmr.fysik.dtu.dk/c2db/c2db.html)** — 4000+ 原子级薄材料，含结构、电子、磁性与光学性质（DTU）。
- 🟢 🧮 **[2DMatPedia](http://www.2dmatpedia.org/)** — 自上而下与自下而上筛选得到的 6000+ 二维结构。

### 电池与能源
- 🟢 🧪 **[Battery Archive](https://batteryarchive.org/)** — 标准化的公开电池循环与安全数据仓库，内置可视化与 CSV 导出。
- 🟢 🧪 **[Severson / 斯坦福–丰田 快充数据集](https://data.matr.io/1/projects/5c48dd2bc625d700019f3204)** — 124 颗商用 LFP 电池在 72 种快充策略下循环至失效；经典的循环寿命基准。
- 🟢 🧪 **[Oxford 电池退化数据集](https://ora.ox.ac.uk/objects/uuid:03ba4b01-cfed-46d3-9b1a-7d4a7bdf6fac)** — 8 颗锂离子软包电池的长期老化数据，定期表征。
- 🟢 🧪 **[NASA PCoE 锂离子电池老化数据集](https://www.nasa.gov/intelligent-systems-division/discovery-and-systems-health/pcoe/pcoe-data-set-repository/)** — 充放电 / EIS 的跑到失效数据，用于寿命预测。
- 🟢 🧪 **[CALCE 电池数据](https://calce.umd.edu/battery-data)** — 马里兰大学 CALCE 组的循环与表征数据集。
- 🟢 🧮 **[Materials Project Battery Explorer](https://next-gen.materialsproject.org/)** — 计算的嵌入 / 转化电极性质（电压、容量、稳定性）。

### 热电
- 🟢 🧪 **[Starrydata2](https://www.starrydata2.org/)** — 从 13000+ 篇论文数字化提取的 19 万+ 性能曲线（Seebeck、电阻率、热导率）；文献曲线数据共享的范例。

### 超导
- 🟢 🧪 **[SuperCon (NIMS)](https://supercon.nims.go.jp/en/)** — 经典超导数据库；清洗后的 2.6 万条版本在 [MDR](https://mdr.nims.go.jp/collections/5712mb227)。
- 🟢 🧮🧪 **[3DSC](https://github.com/aimat-lab/3DSC)** — 将 SuperCon 条目匹配到三维晶体结构，可直接做基于结构的 ML。

### 磁性与拓扑材料
- 🟢 🧪 **[MAGNDATA](https://www.cryst.ehu.es/magndata/)** — 2000+ 已发表的公度与非公度磁结构（Bilbao 服务器，可导出 magCIF）。
- 🟢 🧮 **[Topological Materials Database](https://topologicalquantumchemistry.com/)** — 用拓扑量子化学对全部可处理 ICSD 条目做拓扑分类；含 2D 与磁性版本。

### 声子与热输运
- 🟢 🧮 **[Phonon Database at Kyoto (phonondb)](http://phonondb.mtl.kyoto-u.ac.jp/)** — 数千种化合物的第一性原理声子计算（phonopy）。

### 相图与热力学
- 🔴 🧪 **[ASM Alloy Phase Diagram Database](https://matdata.asminternational.org/apd/)** — 数万张经评估的二元 / 三元合金相图。
- 🟢 🧪 **[NIST Self-Diffusion and Impurity Diffusion Database](https://www.nist.gov/srd)** — 扩散系数与 Arrhenius 参数（属 NIST SRD）。

## 7. 晶体与材料 ML 数据集和基准

可直接喂给模型的固态数据集与标准化基准——属性预测、通用势、生成模型。

- 🟢 🧮 **[Matbench](https://matbench.materialsproject.org/)** — 材料性能预测的标准 13 任务监督学习基准。
- 🟢 🧮 **[Matbench Discovery](https://matbench-discovery.materialsproject.org/)** — 评测通用 ML 原子间势在高通量稳定性预测上的排行榜。
- 🟢 🧮 **[WBM 数据集](https://www.nature.com/articles/s41524-020-00481-6)** — 由化学相似性元素替换 + DFT 弛豫得到的 25.7 万结构；Matbench Discovery 背后的分布外测试集。
- 🟢 🧮 **[OMat24 (Open Materials 2024)](https://huggingface.co/facebook)** — 1 亿+ DFT 单点计算与轨迹，用于训练通用 MLIP（Meta FAIR）。
- 🟢 🧮 **[GNoME](https://github.com/google-deepmind/materials_discovery)** — Google DeepMind 发现的 38 万+ 稳定晶体，含结构与能量。
- 🟢 🧮 **[Mechanical MNIST](https://github.com/elejeune11/Mechanical-MNIST)** — 非均质材料形变的基准数据集，用于代理模型。
- 🟢 🧮🧪 **[Hugging Face Datasets — materials 标签](https://huggingface.co/datasets?search=materials)** — 社区上传的材料与化学数据集，持续增长。

## 8. 分子与量子化学数据集

分子层面的参考数据集（能量、力、几何、性质），用于 ML 原子间势与性质模型。

- 🟢 🧮 **[QM7 / QM8 / QM9 (Quantum-Machine)](http://quantum-machine.org/datasets/)** — 经典的小分子量子化学数据集（原子化能、性质等）。
- 🟢 🧮 **[MD17 / rMD17](http://quantum-machine.org/datasets/)** — 含能量与力的分子动力学轨迹，用于势函数基准。
- 🟢 🧮 **[ANI-1 / ANI-1x / ANI-1ccx](https://github.com/isayev/ANI1_dataset)** — 数百万非平衡 DFT（及 CCSD(T)）构象，用于神经网络势。
- 🟢 🧮 **[PubChemQC](http://pubchemqc.riken.jp/)** — 数百万 PubChem 分子的 DFT（及 TD-DFT）电子结构；PM6 版本覆盖 2.21 亿分子。
- 🟢 🧮 **[OE62](https://www.nature.com/articles/s41597-020-0385-y)** — 6.2 万有机分子在 PBE、PBE0 与 GW 水平的轨道能 / 谱。
- 🟢 🧮 **[QMugs](https://www.research-collection.ethz.ch/handle/20.500.11850/482129)** — 来自 ChEMBL 的 66.5 万成药分子 / 200 万构象的 QM 性质（GFN2-xTB + DFT）。
- 🟢 🧮 **[tmQM](https://github.com/uiocompcat/tmQM)** — 来自 CSD 的 10 万+ 过渡金属配合物的几何与量子性质。
- 🟢 🧮 **[SPICE](https://github.com/openmm/spice-dataset)** — 110 万+ 成药分子、肽与离子的构象，用于 ML 势（15 种元素）。
- 🟢 🧮 **[Transition1x](https://www.nature.com/articles/s41597-022-01870-w)** — 沿反应路径（NEB）的 960 万 DFT 能量 / 力，用于反应性 ML 势。
- 🟢 🧮 **[GEOM](https://github.com/learningmatter-mit/geom)** — 45 万分子的 3700 万能量标注构象；构象生成与性质预测。
- 🟢 🧮 **[OGB-LSC PCQM4Mv2](https://ogb.stanford.edu/docs/lsc/pcqm4mv2/)** — 370 万分子的 DFT HOMO–LUMO 带隙；大规模图 ML 基准。
- 🟢 🧮 **[MoleculeNet](https://moleculenet.org/)** — 分子机器学习基准套件（量子、物理、生物物理、生理任务）。
- 🟢 🧮 **[OMol25 (Open Molecules 2025)](https://huggingface.co/facebook)** — 1 亿+ 生物分子、金属配合物与电解质的 DFT 计算（Meta FAIR）。

## 9. 通用数据仓库

跨学科数据托管平台——很多论文的补充数据 / 原始数据集就挂在这些地方，按 DOI 检索。

- 🟢 **[Zenodo](https://zenodo.org/)** — CERN 支持的开放仓库；可为任何数据集 / 代码 / 补充材料分配 DOI。
- 🟢 **[Figshare](https://figshare.com/)** — 通用科研产出仓库，广泛用于材料补充数据。
- 🟢 **[Mendeley Data](https://data.mendeley.com/)** — Elsevier 的科研数据仓库，常被期刊文章引用。
- 🟢 **[Dryad](https://datadryad.org/)** — 策展的开放科研数据仓库（CC0）。
- 🟢 **[Kaggle Datasets](https://www.kaggle.com/datasets)** — 社区数据集与竞赛，部分聚焦材料 / 化学。
- 🟢 **[Harvard Dataverse](https://dataverse.harvard.edu/)** — 大型通用机构数据仓库。
- 🟢 **[OpenML](https://www.openml.org/)** — 共享 ML 数据集、任务与基准结果的开放平台。
- 🟢 **[Open Science Framework (OSF)](https://osf.io/)** — 面向开放研究的免费项目管理与数据托管平台。
- 🟢 🧮🧪 **[Materials Data Facility (MDF)](https://www.materialsdatafacility.org/)** — 发布与发现大型材料数据集，为 ML 流水线设计。
- 🟢 🧮🧪 **[Materials Commons](https://materialscommons.org/)** — 存储与共享实验 / 计算材料数据的协作平台，带溯源。

## 10. 显微与图像数据集

图像类数据——做计算机视觉 / 显微图像分割与分类的素材。

- 🟢 🧪 **[DoITPoMS Micrograph Library](https://www.doitpoms.ac.uk/miclib/)** — 数百张带标注的光学与电子显微图（剑桥）。
- 🟢 🧪 **[UHCSDB — 超高碳钢显微组织库](http://uhcsdb.materials.cmu.edu/)** — 带元数据的超高碳钢显微组织 SEM 图（CMU）。
- 🟢 🧪 **[EELS Database (eelsdb.eu)](https://eelsdb.eu/)** — 谱图及配套 TEM/STEM 上下文，用于表征 ML。
- 🟢 🧮🧪 **[NOMAD AI Toolkit / Encyclopedia](https://nomad-lab.eu/)** — 在计算归档之外提供可视化的计算材料数据。

## 11. 原子间势与力场

势函数与基础模型——分子动力学和大尺度模拟的核心。

- 🟢 🧮 **[OpenKIM](https://openkim.org/)** — 策展、经测试的原子间模型，含模拟器无关的 API 与可复现性测试。
- 🟢 🧮 **[NIST Interatomic Potentials Repository](https://www.ctcms.nist.gov/potentials/)** — 经审核的经典势（EAM、MEAM、ReaxFF……），附评估数据。
- 🟢 🧮 **[MatPES](https://matpes.ai/)** — 用于训练通用 MLIP 的基础势能面数据集（Materials Virtual Lab）。

## 12. 软件与工具

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
- 🟢 **[RDKit](https://www.rdkit.org/)** — 标准的开源化学信息学工具包，处理分子与描述符。
- 🟢 **[DScribe](https://github.com/SINGROUP/dscribe)** — 用于原子体系 ML 的描述符库（SOAP、MBTR、库仑矩阵……）。

## 13. 文献挖掘与文本资源

从论文里"挖"数据、做 NLP / 知识图谱的工具与语料入口。

- 🟢 **[Matscholar](https://matscholar.com/)** — 基于对 500 万+ 摘要做 NLP 的材料感知文献检索（材料 / 性质 / 方法的命名实体识别）。
- 🟢 **[ChemDataExtractor](http://www.chemdataextractor.org/)** — 从文本自动抽取化学信息与性质表的工具包。
- 🟢 **[OpenAlex](https://openalex.org/)** — 完全开放的学术索引，收录 2.5 亿+ 文献、作者与概念，含免费 API。
- 🟢 **[Semantic Scholar API](https://www.semanticscholar.org/product/api)** — 免费编程访问论文元数据、摘要、引用与嵌入向量。

## 14. 书籍与手册

权威纸质 / 电子手册——查标准数值和经验关联式时仍然是金标准。

- **Materials Handbook**, 15th Edition — Brady, Clauser & Vaccari
- **Smithells Metals Reference Book**, 8th Edition — Gale & Totemeier
- **Materials Science and Engineering Handbook**, 3rd Edition — Shackelford & Alexander
- **MMPDS Handbook**（Metallic Materials Properties Development and Standardization）
- **Handbook of Materials Structures, Properties, Processing and Performance** — Murr
- **ASM Handbook Set**（38 卷）— ASM International
- **CASTI Metals Handbook — Nonferrous Metals**, 4th Edition
- **Materials Handbook: A Concise Desktop Reference**, 2nd Edition — Cardarelli

## 15. 学习资源与教学数据集

入门练手用的小数据集、教程与 notebook。

- 🟢 **[JARVIS-Tools Notebooks](https://github.com/JARVIS-Materials-Design/jarvis-tools-notebooks)** — 用 JARVIS 做材料 ML 的实操 Colab notebook。
- 🟢 **[matminer dataset loaders](https://hackingmaterials.lbl.gov/matminer/dataset_summary.html)** — 一行代码获取数十个策展基准数据集，适合教学与原型。
- 🟢 **[nanoHUB](https://nanohub.org/)** — 模拟工具、课程与已发布的纳米材料数据集。
- 🟢 **[Materials Project Workshop](https://workshop.materialsproject.org/)** — 关于 pymatgen、MP API 与高通量工作流的免费教程。

## 16. 贡献与许可

**贡献**
发现死链、过期条目或值得收录的资源，欢迎提 Issue 或 PR。请保持一行一条目，标注可获取性（🟢/🟡/🔴）与数据性质（🧮/🧪），并归入最贴切的章节。

**免责声明**
本清单只是对**外部资源的索引**。每个数据库 / 数据集都有各自的许可与使用条款，使用前请自行核对。链接与可用性可能随时间变化。

**许可**
本清单（README 本身）以 [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/) 公有领域方式释出。
