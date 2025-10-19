Project Description
This project implements a computational pipeline for identifying gene driver modules from multi-omics data. The specific functions and execution order of the .py files are as follows:
1、node_impact.py - Calculates the Node Impact (NI) of genes to prepare for subsequent analysis.
2、gene_miRNA_w2_f2.py - Constructs a weighted PPI network PP2 using gene-miRNA data and extracts the feature matrix F2.
3、mutation_w1.py - Builds a weighted PPI network PP1 using PPI network and mutation data, and integrates it with PP2 to form the combined network PP.
4、feature_extraction.py - Computes the feature matrix F1 using PP1 and combines it with F2 for cluster analysis.
5、refining.py - Refines the clustering results through a heuristic algorithm to construct driver modules.

Environment Requirements:
h5py==3.13.0
mkl-service==2.4.0
networkx==2.8.8
node2vec==0.4.6
pandas==2.2.3
pyparsing==3.0.9
scanpy==1.10.3
scikit-learn==1.1.3
scipy==1.13.1
sklearn==0.0
tqdm==4.64.1
torch==2.6.0

Usage Instructions:
Execute the scripts in the following order to complete the full analysis pipeline:
1、node_impact.py
2、gene_miRNA_w2_f2.py
3、mutation_w1.py
4、feature_extraction.py
5、refining.py

Note:
Since running gene_miRNA_w2_f2.py on different devices may yield different results, there might be variations in the outcomes. For accurate reproduction, you can use the precomputed files generated on the author's machine:
w2: ../out/optimized_coef.txt
F2: ../out/final_feature_vectors.txt
