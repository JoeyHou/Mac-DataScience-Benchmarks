## About
This is a personal project to test several daily tasks in the field of data science on the new Apple M1/M1-Pro macs. The project is inspired by [
this Medium article by
Dario Radečić](https://towardsdatascience.com/are-the-new-m1-macbooks-any-good-for-data-science-lets-find-out-e61a01e8cad1).

## Test Environment
- Python: 3.6.13
- Pandas: 1.1.5
- Numpy: 1.19.2
- PyTorch: 1.10.0

## Test Machines
- MacBook Pro (14' Late 2021): MBP 14
- MacBook Air (14' Late 2020): MBP 13
- MacBook Pro (13' Mid 2020): MBA 13

| Spec    | MBP 14 			| MBP 13		  | MBA 13|
| -------	| --------------	| ------------ | -------- |
| CPU 		| M1 Pro (8 Core)| Intel I5 2 GHz | M1 (8 Core) |
| Memory	| 16 GB			| 16 GB		| 8 GB |
| Storage	| 512 GB			| 512 GB		| 256 GB |
| Year		| Late 2021 		| Mid 2020 	| Late 2020|

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

| Task       						| MBP 14 	| MBP 13 | MBA 13 |
| ---------------------			| ------ 	| ------ | ------ |
| Pure Python 			 		| 138s		| 182s | 163s|
| Pandas - Loading   			| 74s		| 149s | 138s|
| Pandas - Data Manipulation  | 91s 		| 100s | 112s|
| Pandas - Groupby 				| 6.96s   | 10s | 9s |
| Pandas - Query   				| 91s 		| 177s| 92s |
| Numpy   						| 147s 	| 77s | 151s|
| SkLearn - DT (fit)			| 8s		| 14s | 8s|
| SkLearn - DT (grid earch)			| 48s		| 92s | 102s|
| SkLearn - SVM (fit) 			| 26s	 	| 35s | 27s|
| SkLearn - SVM (grid search) 		| 797s    | 1089s | 859s|
| SkLearn - SVM (grid search - 8 thread parallel) 		| 197s    | 328s | 292s|
| PyTorch - MLP 					| 66s 		| 96s| 69s|

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
