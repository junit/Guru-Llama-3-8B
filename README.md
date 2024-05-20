# Guru-Llama-3-8B 中文增强预训练基座模型

[Guru-Llama-3-8B](https://modelscope.cn/models/wifibaby4u/Guru-Llama-3-8B)中文增强预训练基座模型，使用多种不同类型的中文语料进行增强预训练。

## 项目概述

本项目使用 `LLaMA-Factory` 对 `Llama3-8b` 模型进行了中文增强预训练。

微调对话模型下载：[Guru-Llama-3-8B-Chat](https://modelscope.cn/models/wifibaby4u/Guru-Llama-3-8B-Chat)

## 评测

### CMMLU

| Name | Average | STEM | Social Sciences | Humanities | Other |
|-------|---------|------|-----------------|------------|-------|
| Five-shot | 49.59 | 42.28 | 51.37 | 51.87 | 51.79 |
| Zero-shot | 40.53 | 36.31 | 41.13 | 40.82 | 43.20 |

### MMLU

| Name | Average | STEM | Social Sciences | Humanities | Other |
|-------|---------|------|-----------------|------------|-------|
| Five-shot | 60.88 | 49.77 | 71.62 | 55.22 | 69.24 |
| Zero-shot | 58.97 | 48.30 | 69.62 | 52.75 | 67.81 |

## 训练数据集

| 资源名称               | 描述                             | 记录数量 | 文件名               | 文件大小(MB)     | 文件占比(%)  |
|-----------------------|---------------------------------|----------|----------------------|--------------|------------|
| 新闻联播内容           | 2016-2024年的新闻联播        | 31,637篇   | cctv_news.jsonl              | 43           | 0.029       |
| 中华古诗词数据库       | 古诗词数据库                 | 390,904篇  | poetry.jsonl                 | 110          | 0.074       |
| 诗人数据库             | 诗人数据库                   | 10,477条   | poet.jsonl                   | 3.7          | 0.002       |
| 中国古典小说数据库     | 中国古典小说数据库           | 431本      | novel.jsonl                  | 242          | 0.163       |
| 金庸小说               | 金庸小说                     | 15本       | jinyong.jsonl                | 25           | 0.017       |
| 中国近现代历史文献选集 | 中国近现代历史文献选集       | 131篇      | bibliography.jsonl           | 2.3          | 0.002       |
| 成语数据库             | 成语数据库                   | 23,148条   | idiom.jsonl                  | 2.5          | 0.002       |
| 中国近代史-徐中约      | 中国近代史-徐中约            | 上、下两册 | modern_chinese_history.jsonl | 1.9          | 0.001       |
| 高质量中英文翻译数据   | 中英文高质量翻译对           | 69,206条   | translation.jsonl            | 44           | 0.030       |
| 维基百科               | 中文维基百科 (2023年7月20日) | 254,547条  | wikipedia-cn-20230720.jsonl  | 488          | 0.329       |
| 作文                   | 作文集                       | 269,370篇  | composition.jsonl            | 517          | 0.349       |
| 散文                   | 散文作品集                   | 658篇      | prose.jsonl                  | 2.9          | 0.002       |

## 使用指南

### 环境配置

确保您的机器已经安装了以下软件：

- Python 3.8+
- PyTorch 1.8+

### 安装

首先安装所需依赖：

```bash
pip install modelscope
```

### 模型下载

使用以下命令加载并运行模型：

```python
from modelscope import snapshot_download
model_dir = snapshot_download('wifibaby4u/Guru-Llama-3-8B')
```

## 贡献

我们欢迎社区开发者的贡献！如果您有兴趣参与本项目的开发或有任何建议，欢迎通过 Issue 或 Pull Request 的方式与我们联系。
