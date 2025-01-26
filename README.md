# CrohnsPred: Deep Neural Network For Crohn Disease (CD) Prediction
This repository holds the CrohnsPred model for Genetic Risk prediction of Crohn's Disease.
Trained on 10000+ individual synthetic genomic samples, this model can approximately predict a higher genetic susceptibility to CD.


## Requirements
The project is written in `python`. The following third party packages are required to ensure full project functionality:

- [**numpy**](https://numpy.org/doc/stable/index.html): python package for mathematical and scientific computing. 
- [**pandas**](https://pandas.pydata.org/): python package for data analysis, particularly suitable for handling relational and labelled data. 
- [**pytorch**](https://pytorch.org): python package for machine learning and deep learning algorithms.

All necessary imports, libraries and modules are specified at the top of each .ipynb file.

## Model
[**Deep Neural Network**](https://pytorch.org/tutorials/beginner/blitz/neural_networks_tutorial.html):

The model architecture, training and testing is available at [__CrohnsPred.ipynb__](CrohnsPred.ipynb). \
To run the train and test pipelines from scratch, simply acces the up stated _.ipynb_ file and run the cells in order. \
To use the Web Dashboard created to visualize the model predictions on real data, visit the [__belfioreasia/WebApp__](https://github.com/belfioreasia/WebApp) repository.

## Data
All genetic data preprocessing is described in the data_preprocessing.ipynb file. \
All mutations data from the PGS Catalog is described in the mutations_preprocessing.ipynb file. \
The formatting process for the 100k dataset is described in the [*one_million_dataset_formatting.ipynb*](one_million_dataset_formatting.ipynb) file.

To enable prediction, the input *.vcf* data must include:
- Chromosome (column 'chrom'): an Integer
- Position (column 'pos'): an Integer
- SNP name (column 'rsid' or 'ID'): as a string 'rsXXYY...'
- Reference Allele (column 'ref'): a character (A/C/T/G) or string
- ALternative Allele (column 'alt'): a character (A/C/T/G) or string

The model output will contain a value in the range [0,1], wether a higher risk has not been detected or otherwise. 


**Model Hyperparameters**
- '*PReLU*': hidden layer activation function.
- '*Sigmoid*': output activation function.
- '*Adam*': optimizer with learning rate = 0.001.
- '*20*': number of max hidden layers.
- '*300*': number of epochs.
- '*250*': training batch size.


## Example Usage
> [!Note]
> Usage commands coming soon!

## Authors

- Belfiore Asia (*ec21414*)
    
    CID:210471618\
    BSc Computer Science and Mathematics,
    Queen Mary University of London

