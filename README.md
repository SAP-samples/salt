# SALT: Sales Autocompletion Linked Business Tables Dataset
[![made-with-python](https://img.shields.io/badge/Made%20with-Python-red.svg)](#python)
[![License](https://img.shields.io/badge/license-CC--BY--NC--SA--4.0-blue)]()



#### News
- **10/29/2024:** Preliminary repository created


## Description
This repository **will contain** the data and the code for our paper [**SALT: Sales Autocompletion Linked Business Tables Dataset**](https://openreview.net/forum?id=UZbELpkWIr#discussion) to be presented at [NeurIPS'24 Table Representation Workshop](https://table-representation-learning.github.io/).

### Abstract
Foundation models, particularly those that incorporate Transformer architectures, have demonstrated exceptional performance in domains such as natural language processing and image processing. Adapting these models to structured data, like tables, however, introduces significant challenges. These difficulties are even more pronounced when addressing multi-table data linked via foreign key, which is prevalent in the enterprise realm and crucial for empowering business use-cases. Despite its substantial impact, the research focusing on such linked business tables within enterprise settings remains a significantly important yet underexplored domain.
To address this, we introduce a curated dataset sourced from an Enterprise Resource Planning (ERP) system, featuring extensive linked tables. This dataset is specifically designed to support research endeavors in table representation learning. By providing access to authentic enterprise data, our goal is to potentially enhance the effectiveness and applicability of models for real-world business contexts.


### Information
![Table Schema of SALT Dataset](images/schema.svg?raw=true "SALT Schema")
*Table Schema of SALT Dataset*

![Screenshot of a Salesorder Input Mask](images/SAP_S4HANA_SalesOrder_App.png?raw=true "Salesorder Input Mask")
*Example Input Mask of a Salesorder App using SAP S4/HANA*

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

## How to obtain support
[Create an issue](https://github.com/SAP-samples/SALT/issues) in this repository if you find a bug or have questions about the content.
 
For additional support, [ask a question in SAP Community](https://answers.sap.com/questions/ask.html).

## Contributing
If you wish to contribute code, offer fixes or improvements, please send a pull request. Due to legal reasons, contributors will be asked to accept a DCO when they create the first pull request to this project. This happens in an automated fashion during the submission process. SAP uses [the standard DCO text of the Linux Foundation](https://developercertificate.org/).

## License
Copyright (c) 2024 SAP SE or an SAP affiliate company. All rights reserved. This project is licensed under the CC-BY-NC-SA Software License, version 4.0 except as noted otherwise in the [LICENSE](LICENSES/CC-BY-NC-4.0.txt) file.

