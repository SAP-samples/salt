<!--
SPDX-FileCopyrightText: 2017 Free Software Foundation Europe e.V. <https://fsfe.org>

SPDX-License-Identifier: CC-BY-NC-4.0
-->

# SALT: Sales Autocompletion Linked Business Tables Dataset
[![made-with-python](https://img.shields.io/badge/Made%20with-Python-red.svg)](#python)
[![License](https://img.shields.io/badge/license-CC--BY--NC--SA--4.0-blue)]()
[![REUSE status](https://api.reuse.software/badge/github.com/sap-samples/salt)](https://api.reuse.software/info/github.com/sap-samples/salt)




#### News
- **12/19/2024:** :confetti_ball: Train/test split will be provided :tada:
- 12/15/2024: Preliminatry dataset available on Hugging Face.
- 12/13/2024: Provided data 
- 10/29/2024: Preliminary repository created


## Description
This repository contains the dataset from our paper [**SALT: Sales Autocompletion Linked Business Tables Dataset**](https://openreview.net/forum?id=UZbELpkWIr#discussion) presented at [NeurIPS'24 Table Representation Workshop](https://table-representation-learning.github.io/).

### Abstract
Foundation models, particularly those that incorporate Transformer architectures, have demonstrated exceptional performance in domains such as natural language processing and image processing. Adapting these models to structured data, like tables, however, introduces significant challenges. These difficulties are even more pronounced when addressing multi-table data linked via foreign key, which is prevalent in the enterprise realm and crucial for empowering business use cases. Despite its substantial impact, research focusing on such linked business tables within enterprise settings remains a significantly important yet underexplored domain.
To address this, we introduce a curated dataset sourced from an Enterprise Resource Planning (ERP) system, featuring extensive linked tables. This dataset is specifically designed to support research endeavors in table representation learning. By providing access to authentic enterprise data, our goal is to potentially enhance the effectiveness and applicability of models for real-world business contexts.

### Dataset on Hugging Face

The dataset is now also available via the Hugging Face dataset platform. Check-out: [SALT](https://huggingface.co/datasets/sap-ai-research/SALT)

```python
from datasets import load_dataset

ds = load_dataset("sap-ai-research/SALT")
```

### Usage

#### Example of loading the tables with Hugging Face datasets
Unless pandas library is already installed, install it with:

```bash
pip install pandas
```

```python
from datasets import load_dataset

dataset_name = "sap-ai-research/SALT"
split = "train"  # use "train" or "test"
salesdocuments = load_dataset(dataset_name, "salesdocuments", split=split)
salesdocument_items = load_dataset(dataset_name, "salesdocument_items", split=split)
customers = load_dataset(dataset_name, "customers", split=split)
addresses = load_dataset(dataset_name, "addresses", split=split)

# you can also load the joined table which combines the four tables in one
joined_table = load_dataset(dataset_name, "joined_table", split=split)
```

#### Example of loading the tables with pandas
Unless pandas library is already installed, install it with:

```bash
pip install pandas
```

```python
import pandas as pd

# load the table data from the parquet files
salesdocuments = pd.read_parquet("I_SalesDocument_train.parquet")
salesdocument_items = pd.read_parquet("I_SalesDocumentItem_train.parquet")
customers = pd.read_parquet("I_Customer.parquet")
addresses = pd.read_parquet("I_AddrOrgNamePostalAddress.parquet")
joined = pd.read_parquet("JoinedTables_train.parquet")

# show the first elements
salesdocuments.head()
```


### Information
![Table Schema of SALT Dataset](images/schema.svg?raw=true "SALT Schema")
*Table Schema of SALT Dataset*

![Screenshot of a Salesorder Input Mask](images/SAP_S4HANA_SalesOrder_App.png?raw=true "Salesorder Input Mask")
*Example Input Mask of a Salesorder App using SAP S/4HANA*

## Requirements
N/A

## Known Issues
No known issues

### Authors:
 - [Tassilo Klein](https://tjklein.github.io/)
 - [Clemens Biehl](https://www.linkedin.com/in/clemens-biehl-43a39a117/)
 - [Margarida Costa](https://www.linkedin.com/in/mariamargaridacosta/)
 - [André Sreš](https://www.linkedin.com/in/andr%C3%A9-sre%C5%A1-937096160/)
 - [Jonas Kolk](https://www.linkedin.com/in/jonas-kolk-b8a94b123/)
 - [Johannes Hoffart](https://www.linkedin.com/in/johanneshoffart/)

## Citations
If you use this code in your research or want to refer to our work, please cite:

```
@inproceedings{
klein2024salt,
title={{SALT}: Sales Autocompletion Linked Business Tables Dataset},
author={Tassilo Klein and Clemens Biehl and Margarida Costa and Andre Sres and Jonas Kolk and Johannes Hoffart},
booktitle={NeurIPS 2024 Third Table Representation Learning Workshop},
year={2024},
url={https://openreview.net/forum?id=UZbELpkWIr}
}
```

## Roadmap
- [ ] Integration into [RelBench](https://relbench.stanford.edu/), Feb'25
- [x] Release dataset

## How to obtain support
[Create an issue](https://github.com/SAP-samples/SALT/issues) in this repository if you find a bug or have questions about the content.
 
For additional support, [ask a question in SAP Community](https://answers.sap.com/questions/ask.html).

## Contributing
If you wish to contribute code, offer fixes or improvements, please send a pull request. Due to legal reasons, contributors will be asked to accept a DCO when they create the first pull request to this project. This happens in an automated fashion during the submission process. SAP uses [the standard DCO text of the Linux Foundation](https://developercertificate.org/).

## License
Copyright (c) 2024 SAP SE or an SAP affiliate company. All rights reserved. This project is licensed under the CC-BY-NC-SA Software License, version 4.0 except as noted otherwise in the [LICENSE](LICENSES/CC-BY-NC-4.0.txt) file.

