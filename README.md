# Build A Large Language Model (From Scratch) — 中英双语版

> 本仓库是 [rasbt/LLMs-from-scratch](https://github.com/rasbt/LLMs-from-scratch) 的中英双语版本。

📖 **原书**: [Build a Large Language Model (From Scratch)](https://mng.bz/lZ5B) by Sebastian Raschka (Manning, 2024)

## 翻译说明

- **翻译模式**: 中英双语对照 — 每个 Markdown 单元格保留英文原文，附中文翻译
- **未翻译内容**: 代码单元格、LaTeX 公式、URL 保持原样
- **技术术语**: 采用「中文(English)」格式，如：注意力机制 (Attention Mechanism)
- **翻译工具**: 使用 OpenAI 兼容 API 自动翻译，每 24 小时同步上游更新

## 章节目录

| 章节 | 主题 | 主要 Notebook | 练习解答 |
|------|------|--------------|---------|
| 第 2 章 | 处理文本数据 | `ch02/01_main-chapter-code/ch02.ipynb` | `exercise-solutions.ipynb` |
| 第 3 章 | 编写注意力机制 | `ch03/01_main-chapter-code/ch03.ipynb` | `exercise-solutions.ipynb` |
| 第 4 章 | 从零实现 GPT 模型 | `ch04/01_main-chapter-code/ch04.ipynb` | `exercise-solutions.ipynb` |
| 第 5 章 | 在无标注数据上预训练 | `ch05/01_main-chapter-code/ch05.ipynb` | `exercise-solutions.ipynb` |
| 第 6 章 | 针对分类的微调 | `ch06/01_main-chapter-code/ch06.ipynb` | `exercise-solutions.ipynb` |
| 第 7 章 | 针对指令遵循的微调 | `ch07/01_main-chapter-code/ch07.ipynb` | `exercise-solutions.ipynb` |
| 附录 A | PyTorch 入门 | `appendix-A/01_main-chapter-code/` | `exercise-solutions.ipynb` |
| 附录 D | 参数高效微调 | `appendix-D/01_main-chapter-code/appendix-D.ipynb` | — |
| 附录 E | 高效训练技术 | `appendix-E/01_main-chapter-code/appendix-E.ipynb` | — |

### Bonus Notebooks

各章节还包含丰富的扩展 notebooks，涵盖：

- BPE 分词器实现、数据加载器原理 (ch02)
- 高效多头注意力、缓冲区理解 (ch03)
- FLOPs 性能分析 (ch04)
- 多种 LLM 架构实现：LLaMA、Qwen3、Gemma3/4、OLMo3、Tiny-Aya (ch05)
- 情感分类、DPO 偏好调优、指令数据集生成 (ch06-07)

## 自动同步

本仓库通过 GitHub Action 每日自动同步上游仓库的更新：

1. 每天北京时间 00:00 检查上游是否有新提交
2. 对比 `.ipynb` 文件，定位变更的 Markdown 单元格
3. 仅重新翻译**内容有变化**的单元格（增量翻译，节省 token）
4. 自动创建 PR 等待人工审核合并

```
上游更新 → 检测变更 → 增量翻译 → 生成 PR → 人工审核 → 合并
```

## 本地运行

```bash
# 克隆仓库
git clone https://github.com/xbsheng/LLMs-from-scratch-zh.git
cd LLMs-from-scratch-zh

# 配置 API
cp .env.example .env
# 编辑 .env 填入 API key

# 安装依赖
pip install openai

# 首次全量翻译（或使用 --incremental 增量翻译）
python scripts/translate_notebook.py . . --incremental
```

## 贡献翻译

欢迎提 PR 改善翻译质量！特别关注：

- 技术术语翻译是否准确
- 长句是否通顺
- 格式是否保持一致

## 致谢

感谢 [Sebastian Raschka](https://sebastianraschka.com/) 创建了这个优秀的开源教程。

## 引用

```bibtex
@book{build-llm-from-scratch,
  author       = {Sebastian Raschka},
  title        = {Build A Large Language Model (From Scratch)},
  publisher    = {Manning},
  year         = {2024},
  isbn         = {9781633436947},
  url          = {https://mng.bz/lZ5B},
  github       = {https://github.com/rasbt/LLMs-from-scratch}
}
```
