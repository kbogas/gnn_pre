17/02/2020

First finalised the list of drugs. We started from the 3679 unique drugs of 16/12/2019.

They were picked as the following:
- They all had full details from textual metadata (1914 drugs)
- The nodes where found at least once in both train and test edges (2242 drugs)

The intersection of those were: 1476 drugs finally.

Updated the corresponding train/test files only with these drugs in mind.


~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~ BIOBERT GNN ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Will re-create the train/test/embeddings file to be used by the torchkge platform.

- train.txt
Drug pairs from DB 5.0.3 that are in the list of the final drugs. 170381 triples. 41.39% reduction from 16/12.



- test.txt
Drug pairs from DB 5.1.3 that are in the list of the final drugs. 304597 triples. 69.67 %
 reduction from 16/12.


- DB_Bert_Emb_INT.csv
The corresponding embedding file with the integer mapping. All other drugs have been dropped. 769 columns (with header, no index). The last column is the incremental ID.

-DB_Bert_Emb_INT__MAPPING.csv
The .csv file containing the mapping from the DB_ID to the incremental ID.
Comma separated, 2 columns with header (no index), ["DB_ID", "INDEX"]

