# Baseline 与待对应项

## Baseline 代码位置

主实验完整包包含 `src/agentdojo/scripts/benchmark.py`。该入口具有 `--model`、`--suite`、`--attack`、`--defense` 等选项。攻击实现位于 `src/agentdojo/attacks/`。

可从 `../01_主实验_Bridge/` 获取完整包。本次没有另外造一个“历史 baseline 专用包”，也没有根据当前默认值补造历史运行命令。

## 需要后续对应的内容

- GPT-4o/Gemini 的论文实验对应哪个历史版本与模型标识，不能只凭当前四模型启动脚本确定。
- Table 4 中关闭／开启 failure-guided update 的两组历史实现。现有包尚未确认对应的独立关闭开关，不用新消融冒充该对比。
- 阶段／失败分析和累计 ASR/UTS 的论文统计脚本尚未在本次选定包中逐项确认；`create_results_table.py` 的存在不代表它能生成全部论文图表。
- 原包中异常分支可能将错误计作成功的代码问题未在本次修改，应结合原始日志核验影响。

以上均为版本对应与核验事项，不代表本次要重新运行实验。
