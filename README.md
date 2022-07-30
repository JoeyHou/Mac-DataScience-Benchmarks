## About
This is a personal project to test several daily tasks in the field of data science on the new Apple M1/M1-Pro macs. The project is inspired by [
this Medium article by
Dario Radečić](https://towardsdatascience.com/are-the-new-m1-macbooks-any-good-for-data-science-lets-find-out-e61a01e8cad1).

## Test Environment
- Python: 3.6.13
- Pandas: 1.1.5
- Numpy: 1.19.2
- PyTorch: 1.10.0

## Test Machines and Alias
- MacBook Pro (13' Mid 2020): MBP-13
- MacBook Air (13' Late 2020): MBA-M1
- MacBook Pro (14' Late 2021): MBP-14
- MacBook Air (13' Mid 2022): MBA-M2 (8GB RAM)
- MacBook Air (13' Mid 2022): MBA-M2 (16GB RAM)

| Spec    | MBP-13 | MBA M1 | MBP-14 | MBA-M2-8GB| MBA-M2-16GB |
| ------- | -------------| ------------ | -------- | -------- |  -------- |
| CPU 	  | Intel I5 (2.0 GHz) | M1 (8 Core) | M1 Pro (8 Core) | M2 (8 Core) | M2 (8 Core) |
| Memory  | 16 GB	| 8 GB	| 16 GB | 8 GB |16 GB |
| Storage | 512 GB	| 256 GB | 512 GB | 512 GB| 512 GB |
| Time    | Mid 2020 | Late 2020 | Late 2021 | Mid 2022 |Mid 2022 |


## Task Description
- Pure Python
	- List comprehension with simple math computation (100,000,000 numbers)
- Pandas
	- Loading Files: loading a csv large file (4.14 GB)
	- Data Manipulation: apply math calculation on columns
	- Groupby: groupby and apply math calculations
	- Query: query based on column values
- Numpy
	- Benchmark tests based on [this git repo](https://gist.github.com/markus-beuckelmann/8bc25531b11158431a5b09a45abd6276)
- SkLearn
	- Decision Tree: fit and grid search
	- SVM: fit and grid search (rbf kernel)
- PyTorch
	- Simple multilayer perceptron on numerical data & classification task

## Result

| Task       				| MBP-13 | MBA M1 | MBP-14 | MBA-M2-8GB| MBA-M2-16G |
| ---------------------		| ------ 	| ------ | ------ | ------ | ------ |
| Pure Python 			 	| 182s		| 163s | 138s| **121s** | 128s|
| Pandas - Loading   		| 149s		| 138s | 74s| **49s** | **49s** |
| Pandas - Data Manipulation | 100s 		| 112s | 91s|  88s | 93s |
| Pandas - Groupby 			| 10s   | 9s | 6.96s | **4s** | **4s**| 
| Pandas - Query   			| 177s 		| 92s| **91s** | 158s | 99s |
| Numpy   					| **77s** 	| 151s | 147s| 137s | 138s|
| SkLearn - DT (fit)		| 14s		| 8s | 8s| 4s | **4s** |
| SkLearn - DT (grid earch)	| 92s		| 102s | **48s** | 39s | 56s |
| SkLearn - SVM (fit) 		| 35s	 	| 27s | **26s**| 40s |
| SkLearn - SVM (grid search) | 1089s    | 859s | **797s** | 943s | 945s |
| SkLearn - SVM (grid search - 8 thread parallel) 		| 328s    | 292s | **197s**| 292s | 290s |
| PyTorch - MLP 			| 96s 		| 69s| 66s| **48s**| **48s**|
| Test Time	| Nov. 2021| Nov. 2021 | Nov. 2021 | Jul. 2022 | Jul. 2022 |





- **Note**: As noted in the table above, some of the tests are not done at the same time, which means there might be system updates on the OS level that impact task performances.

## Get Started
- Virtual Environment - **Highly recommanded**
	- Install [conda](https://docs.conda.io/projects/conda/en/latest/user-guide/install/macos.html) or [Anaconda](https://docs.anaconda.com/anaconda/install/index.html)
	- `conda create -n "py36" python=3.6 ipython`
	- `conda activate py36`
	- More detail about virtual environment can be found [here](https://stackoverflow.com/questions/56713744/how-to-create-conda-environment-with-specific-python-version)
- [Jupyter Notebook](https://jupyter.org/install)
	- `conda install -c conda-forge notebook`
- [Scikit](https://scikit-learn.org/stable/install.html)
	- `pip install -U scikit-learn`
- [Pandas](https://pandas.pydata.org/docs/getting_started/install.html)
	- `conda install pandas`
- [Pytorch](https://pytorch.org/get-started/locally)
	- `conda install pytorch torchvision -c pytorch`
- [tqdm](https://github.com/tqdm/tqdm)
	- `conda install -c conda-forge tqdm`


	## Other Related Articles
	- https://towardsdatascience.com/new-apple-silicon-m1-macbook-air-the-dream-laptop-for-machine-learning-engineers-a1590fbd170f
	- https://gist.github.com/markus-beuckelmann/8bc25531b11158431a5b09a45abd6276
	- https://wandb.ai/vanpelt/m1-benchmark/reports/Can-Apple-s-M1-help-you-train-models-faster-cheaper-than-NVIDIA-s-V100---VmlldzozNTkyMzg
