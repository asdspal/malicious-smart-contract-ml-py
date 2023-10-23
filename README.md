# Malicious Smart Contract Detection ML 2.0

## Description


This detection bot detects when a suspicious non-token or non-proxy contract is deployed. It uses an offline trained machine learning model that was built based on contract creation code contained in malicious and benign smart contracts. It will improve upon the previous version.

### Model Configuration

**Data Used For Training**
- [x]  Trained on 15,443 benign and 174 malicious non-token and non-proxy Ethereum contracts. Datasets can be found at [forta-network/labelled-datasets](https://github.com/forta-network/labelled-datasets)
- [] Collect the dataset for binance and polygon in same way as done for above dataset.
- [] Use an unlablled dataset for pretraining the network example : https://huggingface.co/datasets/mwritescode/slither-audited-smart-contracts

**Algorithm**
Given that the malicious contracts are rare, we will use anomaly detection approach for the problem.
    **Featurization**
    - []  tf-idf using decompiled opcodes as done previously
    - []  Glove vectors on the decompiled opcodes
    **ML Models**
    - [] Tree based decision models( Isolation Forest )
    - [] Word2vec
    - [] Pretaining with Transformers on unlabelled datasets followed by finetuning on the smaller labelled dataset


