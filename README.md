# Materials Data Resources · 材料科学数据资源大全

> A curated, regularly expanded list of **databases, datasets, benchmarks, repositories and tools** for materials science, computational materials, and materials informatics / machine learning.
>
> 一份面向**材料科学 / 计算材料 / 材料信息学与机器学习**的精选数据资源清单：涵盖数据库、数据集、ML 基准、通用仓库、表征与光谱、软件工具等。持续扩充。

中文说明：这份清单整理了做材料数据驱动研究时常用的数据来源，按"用途"而非"材料类别"组织，方便快速定位。每条目都标注了**可获取性**（开放 / 半开放 / 商业）和**数据性质**（计算 / 实验）。本清单受 [`sedaoturak/data-resources-for-materials-science`](https://github.com/sedaoturak/data-resources-for-materials-science) 启发，并在其基础上大幅补全了晶体学三大库、光谱与表征、ML 基准、2D / 电池 / 热电 / 超导等领域库、软件工具链与文献挖掘资源。

---

## Legend · 图例

| Tag | Meaning · 含义 |
|---|---|
| 🟢 | Open / free to access · 开放免费 |
| 🟡 | Freemium — partly open, registration or paid tiers · 半开放（注册/部分付费） |
| 🔴 | Commercial / subscription · 商业订阅 |
| 🧮 | Primarily computational data (DFT, MD, ML) · 以计算数据为主 |
| 🧪 | Primarily experimental / measured data · 以实验数据为主 |

---

## Table of Contents · 目录

1. [Computational and DFT Databases · 计算与 DFT 数据库](#1-computational-and-dft-databases--计算与-dft-数据库)
2. [Crystallography and Structure Databases · 晶体学与结构数据库](#2-crystallography-and-structure-databases--晶体学与结构数据库)
3. [Experimental and Engineering Property Databases · 实验与工程性能数据库](#3-experimental-and-engineering-property-databases--实验与工程性能数据库)
4. [Spectroscopy and Characterization Databases · 光谱与表征数据库](#4-spectroscopy-and-characterization-databases--光谱与表征数据库)
5. [Domain-Specific Databases · 专题领域数据库](#5-domain-specific-databases--专题领域数据库)
6. [Machine Learning Datasets and Benchmarks · 机器学习数据集与基准](#6-machine-learning-datasets-and-benchmarks--机器学习数据集与基准)
7. [General-Purpose Data Repositories · 通用数据仓库](#7-general-purpose-data-repositories--通用数据仓库)
8. [Microscopy and Image Datasets · 显微与图像数据集](#8-microscopy-and-image-datasets--显微与图像数据集)
9. [Interatomic Potentials and Force Fields · 原子间势与力场](#9-interatomic-potentials-and-force-fields--原子间势与力场)
10. [Software and Tools · 软件与工具](#10-software-and-tools--软件与工具)
11. [Literature Mining and Text Resources · 文献挖掘与文本资源](#11-literature-mining-and-text-resources--文献挖掘与文本资源)
12. [Books and Handbooks · 书籍与手册](#12-books-and-handbooks--书籍与手册)
13. [Learning Resources and Toy Datasets · 学习资源与教学数据集](#13-learning-resources-and-toy-datasets--学习资源与教学数据集)
14. [Related Awesome Lists · 相关清单](#14-related-awesome-lists--相关清单)
15. [Contributing and License · 贡献与许可](#15-contributing-and-license--贡献与许可)

---

## 1. Computational and DFT Databases · 计算与 DFT 数据库

大规模第一性原理 / 高通量计算数据库，是 ML 势函数与材料筛选的主力数据源。

- 🟢 🧮 **[Materials Project](https://materialsproject.org/)** — Hundreds of thousands of DFT-computed inorganic compounds with formation energies, band structures, elastic/piezoelectric tensors, X-ray absorption spectra, and a battery explorer. REST + Python API (`mp-api`).
- 🟢 🧮 **[OQMD — Open Quantum Materials Database](https://oqmd.org/)** — DFT thermodynamic and structural properties for ~1M+ materials; full database downloadable.
- 🟢 🧮 **[AFLOW](http://aflowlib.org/)** — 3.5M+ compounds and 700M+ calculated properties, with property-prediction and prototype-search tools.
- 🟢 🧮 **[JARVIS (NIST)](https://jarvis.nist.gov/)** — Joint Automated Repository for Various Integrated Simulations: DFT, force-field, ML, and STM datasets, plus the JARVIS-Leaderboard for benchmarking.
- 🟢 🧮 **[NOMAD](https://nomad-lab.eu/)** — FAIR repository of raw and parsed inputs/outputs from 100M+ first-principles calculations; supports custom AI toolkits and the NOMAD Encyclopedia.
- 🟢 🧮 **[Materials Cloud](https://www.materialscloud.org/)** — Curated, archive, and interactive sections built on AiiDA workflows; fully reproducible provenance.
- 🟢 🧮 **[Alexandria Materials Database](https://alexandria.icams.rub.de/)** — Millions of DFT-relaxed structures (3D/2D/1D), PBE/PBEsol/SCAN, with trajectories useful for training MLIPs.
- 🟢 🧮 **[NRELMatDB](https://materials.nrel.gov/)** — NREL's computational materials database focused on energy-relevant materials.
- 🟢 🧮 **[Computational Materials Repository (CMR)](https://cmr.fysik.dtu.dk/)** — Curated DFT datasets from DTU (used by ASE/GPAW), each with documentation and download.
- 🟢 🧮 **[OPTIMADE](https://www.optimade.org/)** — Not a database but a *common API specification* that lets you query Materials Project, OQMD, AFLOW, COD, NOMAD, JARVIS, and many more through one interface.
- 🔴 🧮🧪 **[Pauling File / MPDS](https://mpds.io/)** — Crystal structures, phase diagrams, and physical properties for inorganic compounds; large curated commercial database with an open API tier.

## 2. Crystallography and Structure Databases · 晶体学与结构数据库

晶体结构（CIF）的权威来源——做结构识别、XRD 物相、生成模型训练时绕不开。

- 🟢 🧪 **[Crystallography Open Database (COD)](http://www.crystallography.net/cod/)** — Open collection of 500k+ crystal structures of organic, inorganic, metal-organic compounds and minerals.
- 🔴 🧪 **[ICSD — Inorganic Crystal Structure Database](https://icsd.products.fiz-karlsruhe.de/)** — The largest curated database of fully identified inorganic crystal structures (FIZ Karlsruhe). Subscription.
- 🔴 🧪 **[CCDC / Cambridge Structural Database (CSD)](https://www.ccdc.cam.ac.uk/)** — >1.2M experimentally determined organic and metal-organic crystal structures. Subscription, with free WebCSD-style access for deposits.
- 🔴 🧪 **[ICDD PDF (Powder Diffraction File)](https://www.icdd.com/)** — Reference powder-diffraction patterns for phase identification. Commercial.
- 🟢 🧪 **[American Mineralogist Crystal Structure Database (AMCSD)](http://rruff.geo.arizona.edu/AMS/amcsd.php)** — Open crystal structures published in mineralogical journals.
- 🟢 🧮 **[Bilbao Crystallographic Server](https://www.cryst.ehu.es/)** — Free programs and databases for space groups, symmetry, band representations, and topological analysis.

## 3. Experimental and Engineering Property Databases · 实验与工程性能数据库

工程材料的力学/热/物理性能——选材、对标、数据挖掘常用。

- 🟢 🧪 **[NIST Standard Reference Data (SRD)](https://www.nist.gov/srd)** — Catalog of dozens of authoritative reference databases (thermophysical, kinetics, alloys, ceramics, diffusion, etc.).
- 🟡 🧪 **[MatWeb](https://www.matweb.com/)** — Datasheets for 100k+ metals, polymers, ceramics, and composites; free search with paid bulk export.
- 🟡 🧪 **[Matmatch](https://matmatch.com/)** — Engineering materials selection database (~30k+ materials) with supplier links.
- 🟡 🧪 **[NIMS MatNavi / DICE](https://mits.nims.go.jp/en/)** — NIMS materials databases: polymers (PoLyInfo), inorganic, metallic, superconductors, diffusion, creep, and more.
- 🔴 🧪 **[Springer Materials](https://materials.springer.com/)** — Landolt-Börnstein and curated property data across all material classes, with visualization tools.
- 🔴 🧪 **[Ansys Granta (MaterialUniverse / MI)](https://www.ansys.com/products/materials)** — Industry-standard materials property database and selection software.
- 🔴 🧪 **[Total Materia](https://www.totalmateria.com/)** — Global metals database: standards, compositions, properties, cross-references.
- 🟢 🧪 **[MakeItFrom](https://www.makeitfrom.com/)** — Free, readable summaries of typical engineering-material properties.
- 🟢 🧪 **[The Engineering ToolBox](https://www.engineeringtoolbox.com/)** — Properties of gases, fluids, and solids for engineering calculations.
- 🟢 🧪 **[HTEM DB (High Throughput Experimental Materials)](https://htem.nrel.gov/)** — Composition, structure, optical and electrical properties of combinatorially-grown thin films (NREL).

## 4. Spectroscopy and Characterization Databases · 光谱与表征数据库

谱图与表征数据（IR / Raman / XRD / XAS / UV-Vis 等）——结构鉴定、谱图反演与谱-性质学习的基础。

- 🟢 🧪 **[RRUFF](https://rruff.info/)** — Reference Raman, infrared, XRD, and chemistry data for minerals; the de-facto standard mineral spectroscopy database.
- 🟢 🧪 **[NIST Chemistry WebBook](https://webbook.nist.gov/chemistry/)** — IR, mass, UV-Vis spectra plus thermochemical data for tens of thousands of compounds.
- 🟢 🧪 **[SDBS (Spectral Database for Organic Compounds)](https://sdbs.db.aist.go.jp/)** — IR, ¹H/¹³C NMR, MS, Raman, and ESR spectra for organic compounds (AIST, Japan).
- 🟢 🧪 **[HITRAN](https://hitran.org/)** — High-resolution molecular spectroscopic line lists for gas-phase absorption (atmospheric and combustion science).
- 🟢 🧮 **[Materials Project XAS](https://next-gen.materialsproject.org/)** — Computed X-ray absorption near-edge spectra (XANES/XES) for thousands of materials, queryable via `mp-api`.
- 🟢 🧮 **[ORNL AISD-Ex](https://www.osti.gov/biblio/1969001)** — Computed UV/Vis (TD-DFT) absorption spectra for ~10M organic molecules.

## 5. Domain-Specific Databases · 专题领域数据库

### Polymers · 聚合物
- 🟡 🧪 **[PoLyInfo (NIMS)](https://polymer.nims.go.jp/en/)** — The largest polymer property database: structures, processing, and properties from the literature.
- 🟡 🧮 **[Polymer Genome](https://www.polymergenome.org/)** — ML-based polymer property prediction platform (Ramprasad group).
- 🟢 🧮 **[Khazana](https://khazana.gatech.edu/)** — Repository of polymer and molecular data with ML-ready descriptors (Georgia Tech).
- 🟢 🧪 **[Polymer Property Predictor and Database (PPPDB)](https://pppdb.uchicago.edu/)** — Curated χ-parameters and glass-transition temperatures extracted from the literature.

### Glass and Ceramics · 玻璃与陶瓷
- 🟢 🧪 **[SciGlass](https://github.com/epam/SciGlass)** — 420k+ glass compositions with properties; now open-sourced on GitHub.
- 🟢 🧮 **[Python for Glass Genomics (PyGGi)](https://pyggi.iitd.ac.in/)** — Glass property modeling and optimization platform (IIT Delhi).

### Metal-Organic Frameworks and Porous Materials · MOF 与多孔材料
- 🟢 🧮 **[CoRE MOF](https://zenodo.org/records/3370144)** — Computation-Ready, Experimental MOF structures (40k+) derived from the CSD and cleaned for simulation.
- 🟢 🧮 **[QMOF Database](https://github.com/Andrew-S-Rosen/QMOF)** — 20k+ MOFs with DFT-computed electronic properties; also browsable on Materials Project.
- 🟢 🧮 **[Open DAC (ODAC23)](https://open-dac.github.io/)** — Large-scale DFT dataset of CO₂/H₂O adsorption in MOFs for direct air capture (Meta FAIR Chemistry).

### Catalysis and Surfaces · 催化与表面
- 🟢 🧮 **[Catalysis-Hub.org](https://www.catalysis-hub.org/)** — DFT surface-reaction energetics with interactive visualization and a GraphQL API.
- 🟢 🧮 **[Open Catalyst Project / FAIR Chemistry](https://opencatalystproject.org/)** — OC20, OC22, OCx24 catalysis datasets and pretrained models (`fairchem`).

### Perovskites · 钙钛矿
- 🟢 🧪 **[The Perovskite Database Project](https://www.perovskitedatabase.com/)** — Device and material data hand-extracted from 16,000+ perovskite solar-cell papers.

### 2D Materials · 二维材料
- 🟢 🧮 **[C2DB — Computational 2D Materials Database](https://cmr.fysik.dtu.dk/c2db/c2db.html)** — 4,000+ atomically thin materials with structural, electronic, magnetic, and optical properties (DTU).
- 🟢 🧮 **[2DMatPedia](http://www.2dmatpedia.org/)** — 6,000+ 2D structures from top-down and bottom-up screening.

### Batteries and Energy · 电池与能源
- 🟢 🧪 **[Battery Archive](https://batteryarchive.org/)** — Standardized public repository of battery cycling and safety data, with built-in visualization and CSV export.
- 🟢 🧮 **[Materials Project Battery Explorer](https://next-gen.materialsproject.org/)** — Computed insertion/conversion electrode properties (voltage, capacity, stability).

### Thermoelectrics · 热电
- 🟢 🧪 **[Starrydata2](https://www.starrydata2.org/)** — 190k+ digitized property curves (Seebeck, resistivity, thermal conductivity) extracted from 13,000+ papers; a model for literature-curve data sharing.

### Superconductors · 超导
- 🟢 🧪 **[SuperCon (NIMS)](https://supercon.nims.go.jp/en/)** — The canonical superconductor database; the cleaned 26k-record version is on [MDR](https://mdr.nims.go.jp/collections/5712mb227).
- 🟢 🧮🧪 **[3DSC](https://github.com/aimat-lab/3DSC)** — SuperCon entries matched to 3D crystal structures, ready for structure-based ML.

### Phase Diagrams and Thermodynamics · 相图与热力学
- 🔴 🧪 **[ASM Alloy Phase Diagram Database](https://matdata.asminternational.org/apd/)** — Tens of thousands of evaluated binary/ternary alloy phase diagrams.
- 🟢 🧪 **[NIST Self-Diffusion and Impurity Diffusion Database](https://www.nist.gov/srd)** — Diffusion coefficients and Arrhenius parameters (part of NIST SRD).

## 6. Machine Learning Datasets and Benchmarks · 机器学习数据集与基准

可直接喂给模型的数据集与标准化基准——做属性预测、势函数、生成模型时优先看这些。

- 🟢 🧮 **[Matbench](https://matbench.materialsproject.org/)** — The standard 13-task supervised-learning benchmark for materials property prediction.
- 🟢 🧮 **[Matbench Discovery](https://matbench-discovery.materialsproject.org/)** — Leaderboard for universal ML interatomic potentials on high-throughput stability prediction.
- 🟢 🧮 **[MoleculeNet](https://moleculenet.org/)** — Benchmark suite for molecular machine learning (quantum, physical, biophysical, physiological tasks).
- 🟢 🧮 **[Quantum-Machine datasets (QM7 / QM9 / MD17 / rMD17)](http://quantum-machine.org/datasets/)** — Canonical small-molecule quantum-chemistry datasets for energy/force learning.
- 🟢 🧮 **[ANI-1 / ANI-1x](https://github.com/isayev/ANI1_dataset)** — Millions of off-equilibrium DFT conformers for neural-network potentials.
- 🟢 🧮 **[GNoME](https://github.com/google-deepmind/materials_discovery)** — 380k+ stable crystals discovered by Google DeepMind, with structures and energies.
- 🟢 🧮 **[OMat24 / OMol25 / OC20-22 (FAIR Chemistry on Hugging Face)](https://huggingface.co/facebook)** — Massive open DFT datasets and foundation models from Meta FAIR.
- 🟢 🧮 **[Mechanical MNIST](https://github.com/elejeune11/Mechanical-MNIST)** — Benchmark dataset of heterogeneous-material deformation for surrogate modeling.
- 🟢 🧮🧪 **[Hugging Face Datasets — materials tag](https://huggingface.co/datasets?search=materials)** — Growing hub of community-uploaded materials and chemistry datasets.

## 7. General-Purpose Data Repositories · 通用数据仓库

跨学科数据托管平台——很多论文的补充数据 / 原始数据集就挂在这些地方，按 DOI 检索。

- 🟢 **[Zenodo](https://zenodo.org/)** — CERN-backed open repository; DOIs for any dataset, code, or supplementary material.
- 🟢 **[Figshare](https://figshare.com/)** — General research-output repository widely used for materials supplementary data.
- 🟢 **[Mendeley Data](https://data.mendeley.com/)** — Elsevier's research-data repository, often linked from journal articles.
- 🟢 **[Dryad](https://datadryad.org/)** — Curated open repository for research data (CC0).
- 🟢 **[Kaggle Datasets](https://www.kaggle.com/datasets)** — Community datasets and competitions, several materials/chemistry-focused.
- 🟢 **[Harvard Dataverse](https://dataverse.harvard.edu/)** — Large general-purpose institutional data repository.
- 🟢 🧮🧪 **[Materials Data Facility (MDF)](https://www.materialsdatafacility.org/)** — Publish and discover large materials datasets; designed for ML pipelines.
- 🟢 🧮🧪 **[Materials Commons](https://materialscommons.org/)** — Collaborative platform for storing and sharing experimental/computational materials data with provenance.

## 8. Microscopy and Image Datasets · 显微与图像数据集

图像类数据——做计算机视觉 / 显微图像分割与分类的素材。

- 🟢 🧪 **[DoITPoMS Micrograph Library](https://www.doitpoms.ac.uk/miclib/)** — Hundreds of annotated optical and electron micrographs (Cambridge).
- 🟢 🧪 **[UHCSDB — Ultrahigh Carbon Steel Micrograph DB](http://uhcsdb.materials.cmu.edu/)** — Labeled SEM micrographs of steel microstructures with metadata (CMU).
- 🟢 🧮🧪 **[NOMAD AI Toolkit / Encyclopedia](https://nomad-lab.eu/)** — Includes visualizable computed materials data alongside the calculation archive.

## 9. Interatomic Potentials and Force Fields · 原子间势与力场

势函数与基础模型——分子动力学和大尺度模拟的核心。

- 🟢 🧮 **[OpenKIM](https://openkim.org/)** — Curated, tested interatomic models with a simulator-agnostic API and reproducibility tests.
- 🟢 🧮 **[NIST Interatomic Potentials Repository](https://www.ctcms.nist.gov/potentials/)** — Vetted classical potentials (EAM, MEAM, ReaxFF, …) with evaluation data.
- 🟢 🧮 **[MatPES](https://matpes.ai/)** — Foundational potential-energy-surface dataset for training universal MLIPs (Materials Virtual Lab).

## 10. Software and Tools · 软件与工具

读取/处理这些数据库、做特征工程与训练模型的常用库。

- 🟢 **[pymatgen](https://pymatgen.org/)** — The standard Python library for materials analysis and Materials Project access.
- 🟢 **[matminer](https://hackingmaterials.lbl.gov/matminer/)** — Data mining and featurization toolkit; ships with many ready-to-use dataset loaders.
- 🟢 **[ASE — Atomic Simulation Environment](https://wiki.fysik.dtu.dk/ase/)** — Set up, run, and analyze atomistic simulations; bridges most DFT/MD codes.
- 🟢 **[JARVIS-Tools](https://github.com/usnistgov/jarvis)** — Python toolkit for the JARVIS databases, descriptors, and ML.
- 🟢 **[AiiDA](https://www.aiida.net/)** — Workflow engine with automatic provenance tracking; backbone of Materials Cloud.
- 🟢 **[automatminer](https://github.com/hackingmaterials/automatminer)** — Automated ML pipeline for materials property prediction.
- 🟢 **[MatGL (M3GNet / MEGNet)](https://github.com/materialsvirtuallab/matgl)** — Graph deep-learning models and universal potentials for materials.
- 🟢 **[CHGNet](https://github.com/CederGroupHub/chgnet)** — Pretrained universal neural-network potential with charge information.
- 🟢 **[MACE](https://github.com/ACEsuit/mace)** — High-accuracy equivariant message-passing interatomic potentials.
- 🟢 **[DScribe](https://github.com/SINGROUP/dscribe)** — Library of descriptors (SOAP, MBTR, Coulomb matrix, …) for ML on atomistic systems.

## 11. Literature Mining and Text Resources · 文献挖掘与文本资源

从论文里"挖"数据、做 NLP / 知识图谱的工具与语料入口。

- 🟢 **[Matscholar](https://matscholar.com/)** — Materials-aware literature search built on NLP over 5M+ abstracts (named-entity recognition for materials, properties, methods).
- 🟢 **[ChemDataExtractor](http://www.chemdataextractor.org/)** — Toolkit for automatically extracting chemical information and property tables from text.
- 🟢 **[OpenAlex](https://openalex.org/)** — Fully open index of 250M+ scholarly works, authors, and concepts, with a free API.
- 🟢 **[Semantic Scholar API](https://www.semanticscholar.org/product/api)** — Free programmatic access to paper metadata, abstracts, citations, and embeddings.

## 12. Books and Handbooks · 书籍与手册

权威纸质/电子手册——查标准数值和经验关联式时仍然是金标准。

- **Materials Handbook**, 15th Edition — Brady, Clauser & Vaccari
- **Smithells Metals Reference Book**, 8th Edition — Gale & Totemeier
- **Materials Science and Engineering Handbook**, 3rd Edition — Shackelford & Alexander
- **MMPDS Handbook** (Metallic Materials Properties Development and Standardization)
- **Handbook of Materials Structures, Properties, Processing and Performance** — Murr
- **ASM Handbook Set** (38 Volumes) — ASM International
- **CASTI Metals Handbook — Nonferrous Metals**, 4th Edition
- **Materials Handbook: A Concise Desktop Reference**, 2nd Edition — Cardarelli

## 13. Learning Resources and Toy Datasets · 学习资源与教学数据集

入门练手用的小数据集、教程与 notebook。

- 🟢 **[JARVIS-Tools Notebooks](https://github.com/JARVIS-Materials-Design/jarvis-tools-notebooks)** — Hands-on Colab notebooks for materials ML with JARVIS.
- 🟢 **[matminer dataset loaders](https://hackingmaterials.lbl.gov/matminer/dataset_summary.html)** — One-line access to dozens of curated benchmark datasets for teaching and prototyping.
- 🟢 **[nanoHUB](https://nanohub.org/)** — Simulation tools, courses, and published nanomaterial datasets.
- 🟢 **[Materials Project Workshop](https://workshop.materialsproject.org/)** — Free tutorials on pymatgen, the MP API, and high-throughput workflows.

## 14. Related Awesome Lists · 相关清单

- **[sedaoturak/data-resources-for-materials-science](https://github.com/sedaoturak/data-resources-for-materials-science)** — The original list that inspired this one (databases, datasets, handbooks).
- **[tilde-lab/awesome-materials-informatics](https://github.com/tilde-lab/awesome-materials-informatics)** — Broader awesome list covering codes, databases, and tools for materials informatics.

## 15. Contributing and License · 贡献与许可

**Contributing · 贡献**
Found a dead link, an outdated entry, or a resource that belongs here? Open an issue or a pull request. Please keep entries one line, add the access tag (🟢/🟡/🔴) and data-nature tag (🧮/🧪), and place them in the most relevant section.

发现死链、过期条目或值得收录的资源，欢迎提 Issue 或 PR。请保持一行一条目，标注可获取性（🟢/🟡/🔴）与数据性质（🧮/🧪），并归入最贴切的章节。

**Disclaimer · 免责声明**
This is a curated index of *external* resources. Each linked database/dataset retains its own license and terms of use — check them before use. Availability and URLs may change over time.

本清单只是对**外部资源的索引**。每个数据库/数据集都有各自的许可与使用条款，使用前请自行核对。链接与可用性可能随时间变化。

**License · 许可**
The list itself (this README) is released under [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/) — public domain. 本清单（README 本身）以 CC0 1.0 公有领域方式释出。
