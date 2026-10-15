# Tecnia Online Slitting Optimizer

在线分切计算器（Online Slitting Calculator）：客户输入订单规格（宽 mm × 长 M × 卷数）与产品型号，
基于母卷规格 **1650 mm × 6000 M**（可在「高级设置」中调整）自动计算最优分切方案。

## 功能

- 宽度向上取整至标准档位（默认 5mm，可调）
- 长度按母卷长度整段取整（刀数 ≤ 6，可调）
- 同型号同规格合并数量排产
- 同型号多规格组合套切（混排），最小化边料损耗
- 排刀示意（按毫米等比）、损耗分析、材料利用率
- 导出 Excel / CSV、打印存 PDF
- 中 / 英双语切换

## 使用

纯静态单文件应用（`index.html`），无任何依赖。

**在线访问（GitHub Pages）**：仓库 Settings → Pages → Source 选择 *GitHub Actions* 即可，
推送后自动部署（工作流见 `.github/workflows/deploy.yml`）。

也可以直接双击 `index.html` 离线使用。

## 计算原则

1. 优化后宽度略大于需求宽度（不计分切刀具材料损耗）
2. 长度按 6000M 分段取整，长度方向取刀数一般不超过 6 刀
3. 尽量减少切后废料损耗
