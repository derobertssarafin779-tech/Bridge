# 候选评估预算／迭代次数

## 完整代码包

[Automatic-Bridge-Sequence-Search--main-four-model-original-bridge-main-iter-length-v1.zip](Automatic-Bridge-Sequence-Search--main-four-model-original-bridge-main-iter-length-v1.zip)

本目录中的 ZIP 是现有代码包的原样副本，没有修改任何实验代码。解压后项目目录为 `Automatic-Bridge-Sequence-Search--main`。

## 实验入口

`util_scripts/run_candidate_evaluation_0_5.sh`

脚本默认设置：默认 Qwen non-thinking；K=2；最多 E=5。候选索引 0–4 对应预算 1–5；不是运行索引 0–5 共六次。

除迭代与新消融脚本默认仅 Qwen non-thinking 外，其他分类脚本默认遍历四种 DeepSeek/Qwen thinking/non-thinking 配置。各脚本默认覆盖 banking、slack、travel、workspace。脚本默认值不是历史运行参数的证明。

## 使用示例

以下为已有脚本的调用方式，不是已执行的命令，也不自动代表论文全部实验范围。请先按包内依赖文件配置环境和自己的凭据。

```bash
cd Automatic-Bridge-Sequence-Search--main
export PYTHONPATH=src
MODELS="QWEN_PLUS_NON_THINKING" MAX_EVALUATIONS="5" bash util_scripts/run_candidate_evaluation_0_5.sh
```

以上为 Bash/Linux 运行示例。保持入口脚本原样，并在解压后的项目根目录运行。凭据通过环境变量设置，勿写入公开代码。目标模型与 bridge 文本生成模型的配置需分别核对。

## 与其他分类的关系

主实验、长度、迭代使用同一个完整代码包，只是入口与参数不同；三个目录内的 ZIP 校验值相同。防御和新消融使用各自独立代码包。

本次只分类现有代码，不补写缺失的历史实现。实验数据、原始日志及图表数据由作者另行整理，本目录不包含这些材料。

原包 SHA-256：`18010541c4f631ae87a3c149b6a8d8290474311935d5605ef832e4789a2c6b93`
