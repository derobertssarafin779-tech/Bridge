# GraphBridge 实验代码分类



## 分类索引

| 目录 | 内容 | 主要入口 |
|---|---|---|
| [01_主实验_Bridge](01_主实验_Bridge/) | 原始 GraphBridge 主实验 | run_four_models_bridge_main.sh |
| [02_加防御_Bridge](02_加防御_Bridge/) | Spotlighting 等防御配置 | run_four_models_bridge_defense.sh |
| [03_Bridge长度_1_2_3_4](03_Bridge长度_1_2_3_4/) | 长度上限 K=1、2、3、4 | run_bridge_length_sensitivity.sh |
| [04_迭代次数_候选0至4](04_迭代次数_候选0至4/) | 最多评估 5 次；候选索引 0–4 | run_candidate_evaluation_0_5.sh |
| [05_新消融_Bridge构建](05_新消融_Bridge构建/) | No Bridge / Random Bridge / GraphBridge | run_bridge_quality_ablation_full.sh |
| [06_Baseline与待对应项](06_Baseline与待对应项/) | Baseline 入口及尚待确认的历史条件 | 见目录说明 |

每个前五类目录都包含完整 ZIP 和入口说明。主实验、长度、迭代三个 ZIP 内容相同，为方便按实验取用而重复放置，并非三套不同算法。

## 原包与版本

本次使用此前保存在本地的三个版本：main-iter-length-v1、defense-bridge-v1、bridge-quality-ablation-v2。新消融包与作者提供的“论文实验代码包（含消融）.zip”字节校验一致。

这些是现存整理版代码包；是否逐一对应每次历史运行，仍需与作者整理的日志核对。旧的 template-generalization/debug 版本未混入本次分类。所有原始文件均保留，本次没有修改源码或实验逻辑，没有启动实验或调用模型。

## 核验记录

- `CODE_PACKAGE_INDEX.csv`：分类、包名、入口、默认设置、校验值。
- `SHA256SUMS.txt`：每份分类 ZIP 的 SHA-256。
- `STATIC_CHECKS.json`：压缩包完整性、Python 语法、模型注册及有限凭据模式扫描。

静态语法通过不等于完整测试通过、依赖兼容或供应商接口可用。有限凭据扫描不能替代完整隐私审查。原包保留其自身说明和许可证，旧说明中的“用于最终实验”等表述不能代替历史日志证据。

