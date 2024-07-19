<div align="center">

<h1> GraphRAG Visualization Tutorial </h1>
這個 repo 提供你已經做過 Indexing pipeline 的文件，讓你可以快速 Microsoft GraphRAG 進行知識圖譜的建立和問答；另外提供視覺化的文檔，方便你快速實作。
<br><br>

[**English**](../../README.md) | **中文**

</div>

## 事前準備

確保你已經閱讀過 Microsoft GraphRAG 的[文檔-英文](https://microsoft.github.io/graphrag/posts/get_started/)，或我的[文章-中文](https://medium.com/@cch.chichieh/knowledge-graph-rag-microsoft-graphrag-%E5%AF%A6%E4%BD%9C%E8%88%87%E8%A6%96%E8%A6%BA%E5%8C%96%E6%95%99%E5%AD%B8-ac07991855e6)。

## 環境變數

將 OpenAI API 或 Azure OpenAI 的 API key 輸入到 `.env.sample` 中，便將其重新命名為 `.env`

## 視覺化使用

### 方法 1: 使用 yFiles Graphs

安裝 requirements.txt 套件，注意 Python 版本要在 3.10 到 3.12 之間。

```bash
pip install -r requirements.txt
```

接著打開 [graph-visualization.ipynb](../../graph-visualization.ipynb) 並修改 INPUT_DIR 為你的的索引結果目錄，如果你下載了整個 repo，使用預設即可。

### 方法 2: 使用 GraphML 和第三方軟體

在 settings.yaml 中啟用 GraphML 輸出：

```bash
snapshots:
  graphml: True
```

完成 Indexing pipeline 後，使用如 Gephi 或 yEd Graph Editor 等工具開啟生成的 GraphML 文件。
