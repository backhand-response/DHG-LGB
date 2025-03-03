Project Setup and Usage Instructions
Recommended System Requirements:

    Memory: 16GB or more

Software Requirements:

    Python: Appropriate version compatible with the listed packages.
    dhg: 0.9.4
    flake8: 7.1.1
    nbclient: 0.10.0
    nbconvert: 7.16.4
    nbformat: 5.10.4
    nest - asyncio: 1.6.0
    networkx: 2.8.8
    numpy: 2.0.2
    Sphinx: 7.4.7
    sphinxcontrib - applehelp: 2.0.0
    sphinxcontrib - devhelp: 2.0.0
    sphinxcontrib - htmlhelp: 2.1.0
    sphinxcontrib - jsmath: 1.0.1
    sphinxcontrib - qthelp: 2.0.0
    sphinxcontrib - serializinghtml: 2.0.0

Data and File Structure

    Training Data: We use a 1:10 positive - negative sample ratio for training data. The 1 - 10 folder contains five - fold training sets.
    Data Information: The data folder records information about proteins, metabolites, diseases, GO IDs, and their corresponding codes.
    Feature Folders:
        The gofeature, metabolitefeature, and proteinfeature folders store information about the involved characterizations and their similarity matrices.
        feature.txt is a matrix that integrates the characterizations of the three types of information.
        hypermatrix is the processed hypergraph result matrix.

Data Processing and Model Execution

    Run embedding.py: This script generates disease and metabolite characterization information (X_3, Y_1) through hypergraph result operations.
    Run ranklghp.py: This script is used to obtain predicted disease - metabolite association pairs.
    Run roc5fold.py: This script generates ROC, PRC, and confusion matrices to evaluate the model.


Note: The code omits some cumbersome operations in the characterization part and the hypergraph result processing. If you need more information, please contact the author.
How to Use

    Ensure that you have installed all the required dependencies as listed above.
    Run embedding.py to generate the disease and metabolite characterization information after hypergraph result operations.
    Run ranklghp.py to get the predicted disease - metabolite association pairs.
    Finally, run roc5fold.py to evaluate the model through ROC, PRC, and confusion matrices.

Installation

To install the required dependencies, you can create a requirements.txt file with the following content:

plaintext

dhg==0.9.4
flake8==7.1.1
nbclient==0.10.0
nbconvert==7.16.4
nbformat==5.10.4
nest - asyncio==1.6.0
networkx==2.8.8
numpy==2.0.2
Sphinx==7.4.7
sphinxcontrib - applehelp==2.0.0
sphinxcontrib - devhelp==2.0.0
sphinxcontrib - htmlhelp==2.1.0
sphinxcontrib - jsmath==1.0.1
sphinxcontrib - qthelp==2.0.0
sphinxcontrib - serializinghtml==2.0.0


And then run the following command in your terminal:

bash

pip install -r requirements.txt
