# ProteinMechanicsGNN: Rapid Prediction of Protein Natural Frequencies using Graph Neural Networks

Kai Guo, Markus J. Buehler

The primary sequence and distance matrix of test proteins are fed as input to the trained GNN models to predict the natural frequencies.

## Requisites

PyTorch == 1.6.0

PyTorch Geometric

pickle == 4.0

biopython

Datafile: https://www.dropbox.com/s/54y7ihxdxibbilw/all_proteins_freqs_no_ratios.zip?dl=0 (place into Notebooks/data)

## Training and Inference

1. run get_pdb.sh in the "PDB" folder to download PDB files

2. run the Jupyter notebooks in the "Notebooks" folder

## Test new protein sequences on pre-trained models

1. put the sequence file (domain.fasta) and distance matrix file (domain_dist.pickle) into the folder "data"

2. open jupyter notebook "Pre-trained Models/Test.ipynb"
 
3. modify the list "test_domains" so that it contains all domain names to be predicted

4. modify "idx_mode"; to predict the first natural frequency, idx_mode = 0; to predict the 64th natural frequency, idx_mode = 63

5. if idx_mode == 0, epochs = 100; if idx_mode > 0, epochs = 50

6. run the notebook and see the predicted frequencies at the end of the notebook
