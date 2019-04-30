# ProDyn
ProDyn - Protein Dynamics Prediction

### ProDyn0
Conformational mechanics of point-mutated calponin homology domains, CH1 and CH2, connected by a tether. Different steered and fixed residues are assigned for molecular dynamics simulation of domain stretching behavior. Input is defined as a graph with node features (residue type, secondary structure, and properties), edge features (dihedrals, h-bonds, steer-to-fixed distance), and edge connections. Output is of two types: (1) force mode classification and (2) max force (magnitude and time) regression.

The zip file "prodyn0_data.zip" contains 3 Python3-pickled data files for training, validation, and test datasets. As an example, the training data can be imported to extract the input and output data as named below:
```
import numpy as np
import pickle

with open('prodyn0_train.p','rb') as fn:
    node_features, edge_features, edge_start, edge_end, y_class, y_regress = pickle.load(fn)
```
