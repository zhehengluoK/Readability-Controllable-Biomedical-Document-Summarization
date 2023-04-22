# Readability-Controllable-Biomedical-Document-Summarization

![](https://img.shields.io/badge/Status-building-brightgreen) ![](https://img.shields.io/badge/PRs-Welcome-red) 


# Resource
This repository contains the data and readability metric implementation used in the paper "Readability Controllable Biomedical Document Summarization"

<!--
If you find this repository helpful for your work,  please consider citing our survey paper. The Bibtex are listed below:
<pre>

</pre>
-->


## Authors


Resource Contributed by [Zheheng Luo](), [Qianqian Xie](),[Sophia Ananiadou](https://www.research.manchester.ac.uk/portal/sophia.ananiadou.html).

## Data
The PLOS dataset used in the paper can be found in http://www.nactem.ac.uk/readability/
### Format
Each dataset consists of 3 files: `train.json`, `val.json`, and `test.json` - corresponding to the training, validation, and test splits. All files are in JSON format and contain a list of JSON objects, each of which contains data for a single article. The JSON objects are in the following format:

```
{
  "doi": str,                      # unique doi identifier
  "title": str,                    # title
  "abstract": str,                 # abstract
  "plain language summary": str,   # plain language summary
  "article": str                   # whole text
 }
```

Now you can also load the dataset from Huggingface.

```
from datasets import load_dataset

dataset = load_dataset("KennyLuo/RC-Sum-PLOS")
```