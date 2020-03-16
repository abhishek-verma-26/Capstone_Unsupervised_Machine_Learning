This is Capstone project on Unsupervised Machine Learning on Palm trait Dataset covering 2500 species of palm tree.

Datasets is available from the link below.
https://datadryad.org/stash/dataset/doi:10.5061/dryad.ts45225

Nature Article citing the Data
https://www.nature.com/articles/s41597-019-0189-0

# Introduction
Plam tree are an important plant group contributing to the bio diversity and to the global economy, in general, by providing raw materials for food, oil, fuel etc. Based on the region, climate and ecosystem a variety of palm tree species can be grow globally. Knowing the physical triats and the taxonomy of each species can help evaluate the interrelationships between species belongs to a different taxonomical group like Palm Subfamily or Plam Tribe.

The dataset used for this excercise is based on the derived measurement of over 2500 species of palm tree. As cited from https://www.nature.com/articles/s41597-019-0189-0#Tab1 , the dataset contains the global species compilation of functional traits of palm tree (Arecaceae) which predominantly grows in tropical and subtropical ecosystem

# Objective

In this excercise we will attempt to form clusters unsupervised based on the palm tree traits and cross reference it with the taxonomy labels. We test the hypothesis that the clustering based on plants traits or physical properties is in agreement with the taxonomical group.


# Summary of Unsupervised Learning
The unsupervised Machine learning flow on Palm Tree Species dataset is summarized as follows:

1)The dataset was trimmed to removed the missing traits account for 65% of palm species. The input contains binary, continuous and categorical type features that were standardized for modelling.
2)Taxonomy labels of Palm Subfamily and Palm Tribe were used to cross validate the clustering in the form of visualization QC and ARI score
3)Dimensional Reduction analysis from t-SNE and UMAP shows more elaborate grouping of 6 to 10 clusters. PCA showed three linearly separable clusters. UMAP dimensional reduction overall gave the best separation (visually) with tuned hyperparameters.
4)Four clustering techniques were used for modelling (K Means, Agglomerate, DBSCAN and GMM). The derived silhouette scores were in the range of 0.4 for clustering between 6 to 8.
5)In contrast, ARI score using Palm SubFamily were between 0.20 to 0.25 for ncluster 3 to 4.
6)Cluster analysis on Palm Subfamily shows overall consistent distribution of datapoints. Arecoideae Subfamily is shown to be dominant in 2 cluster where as Calamoideae Subfamily is dominant in 1 cluster.
7)Bivariate distribution for each predicted cluster is similar among the models.
8)The predicted clusters and taxonomical grouping (Subfamily and Tribe) are not in agreement. This implies that datapoint sharing the same physical traits (fruit properties, stem, growth etc) could potentially originate from different Subfamily or Tribes. This information can be used to advantage in plantation planning or forest regeneration as certain region (or ecosystem or natural habitat) could support specific plant species to grow.
