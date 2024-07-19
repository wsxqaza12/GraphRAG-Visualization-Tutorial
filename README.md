<div align="center">

<h1> GraphRAG Visualization Tutorial </h1>
This repository provides you with documents that have already undergone the Indexing pipeline, allowing you to quickly build and query knowledge graphs with Microsoft GraphRAG. Additionally, it includes documentation for visualization to facilitate quick implementation.
<br><br>

**English** | [**中文**](./docs/CN/README.md)

</div>

## Prerequisites

Ensure you have read through the Microsoft GraphRAG [documentation](https://microsoft.github.io/graphrag/posts/get_started/) in English, or my [article](https://medium.com/@cch.chichieh/knowledge-graph-rag-microsoft-graphrag-%E5%AF%A6%E4%BD%9C%E8%88%87%E8%A6%96%E8%A6%BA%E5%8C%96%E6%95%99%E5%AD%B8-ac07991855e6) in Chinese.

## Environment Setup

Enter your OpenAI API or Azure OpenAI API key into `.env.sample` and rename it to `.env`.

## Visualization Usage

### Method 1: Using yFiles Graphs

Install the packages from requirements.txt, ensuring your Python version is between 3.10 and 3.12.

```bash
pip install -r requirements.txt
```

Then open [graph-visualization.ipynb](./graph-visualization.ipynb) and modify the INPUT_DIR to your indexing results directory. If you have downloaded the entire repo, the default settings should work.

### Method 2: Using GraphML and Third-Party Software

Enable GraphML output in settings.yaml:

```bash
snapshots:
  graphml: True
```

After completing the Indexing pipeline, open the generated GraphML file using tools such as Gephi or yEd Graph Editor.
