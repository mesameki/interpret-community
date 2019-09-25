

[![Build Status](https://dev.azure.com/responsibleai/interpret-extensions/_apis/build/status/microsoft.interpret-community?branchName=master)](https://dev.azure.com/responsibleai/interpret-extensions/_build/latest?definitionId=5&branchName=master)
![MIT license](https://img.shields.io/badge/License-MIT-blue.svg)
![versions](https://img.shields.io/badge/python-2.7%20%7C%203.6-blue)

Interpret Community Extensions SDK
=============================================================


The Interpret Community Extensions builds on [InterpretML](https://github.com/Microsoft/interpret), an open source python package from Microsoft Research for training interpretable models and helping to explain blackbox systems, by adding additional extensions from the community to interpret ML models.

This repository contains an SDK and Jupyter notebooks with examples to showcase it's use.

# Contents
(urls will be added once this is solidified)
- Try our notebooks
    - Launch them on AzureML
- Getting Started 
- Models
- Contributing
- Code of Conduct
- Build Status
- Additional Info

# Try our notebooks
[![Azure Notebooks](https://notebooks.azure.com/launch.png)](https://notebooks.azure.com/import/gh/microsoft/interpret-community)

## Getting Started

# bz todo: make getting started a separate md page. Validate steps in clean env.

This repo uses Anaconda to simplify package and environment management.

To setup on your local machine:

<details><summary><strong><em>1. Set up Environment</em></strong></summary>

    a. Install Anaconda with Python >= 3.6 
       [Miniconda](https://conda.io/projects/conda/en/latest/user-guide/install/index.html) is a quick way to get started.

 
    b. Create conda environment named interp and install packages

```
    conda create --name interp2 python=3.6 anaconda
    
```

    Optional, additional reading:, [conda cheat sheet](https://docs.conda.io/projects/conda/en/4.6.0/_downloads/52a95608c49671267e40c689e0bc00ca/conda-cheatsheet.pdf), [jupyter](https://pypi.org/project/jupyter/) and [nb_conda](https://github.com/Anaconda-Platform/nb_conda)

<details><summary><strong><em>On Windows: c. Activate conda environment</strong></em></summary>

```
    activate interp
```
</details>

<details><summary><strong><em>On Linux:</em> c. Activate conda environment</em></strong></summary>

```
    source activate interp
```
</details>

</details>
 
<details>

<summary><strong><em>2. Clone the interpret-community repo</em></strong></summary>

a. Clone and cd into the repository
```
git clone https://github.com/Microsoft/Interpret-community
cd interpret-community
```
</details>

<details>
<summary><strong><em>3. Install Python module, packages and necessary distributions</em></strong></summary>


```
pip install -e ./python 
```
a. Install additional packages for tests and more
```
pip install -r requirements.txt
```

</details>

<details>
<summary><strong><em>3. Set up and run Jupyter Notebook server </em></strong></summary>

a. Install and run Jupyter Notebook
```
if needed:
          pip install jupyter
then:
jupyter notebook
```
</details>

<!---{% from interpret.ext.blackbox import TabularExplainer %}
--->

# Models

# bz this section requires rewording
Add ref to
https://docs.microsoft.com/en-us/python/api/azureml-explain-model/azureml.explain.model?view=azure-ml-py

* The API supports both dense (numpy or pandas) and sparse (scipy) datasets

* For more advanced users, individual explainers can be used
 (details?)
* The TabularExplainer provides local and global feature importances  
    *  The best explainer is automatically chosen for the user based on the model
        - Best implies fastest execution time and highest interpretabilty accuracy.
* Local feature importances are for each evaluation row
* Global feature importances summarize the most importance features at the model-level
 * The KernelExplainer and MimicExplainer are for BlackBox models
 * The MimicExplainer is faster but less accurate than the KernelExplainer
 * The TreeExplainer is for tree-based models
 * The DeepExplainer is for DNN tensorflow or pytorch models
[shap](https://github.com/slundberg/shap) and [lime](https://github.com/marcotcr/lime) have docs

global surrogate is ???

# Contributing

# bz is CLA required when we go public?

This project welcomes contributions and suggestions.  Most contributions require you to agree to a
Contributor License Agreement (CLA) declaring that you have the right to, and actually do, grant us
the rights to use your contribution. For details, visit https://cla.opensource.microsoft.com.

When you submit a pull request, a CLA bot will automatically determine whether you need to provide
a CLA and decorate the PR appropriately (e.g., status check, comment). Simply follow the instructions
provided by the bot. You will only need to do this once across all repos using our CLA.

# Code of Conduct

This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/).
For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or
contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.

# Build Status
# bz add detailed build status
[![Build Status](https://dev.azure.com/responsibleai/interpret-extensions/_apis/build/status/microsoft.interpret-community?branchName=master)](https://dev.azure.com/responsibleai/interpret-extensions/_build/latest?definitionId=5&branchName=master)

# Additional Info
