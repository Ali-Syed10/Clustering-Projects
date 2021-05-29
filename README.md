# Clustering-Projects
Clustering on COI and CYTB Salvelinus sequences to find fundamental differences in biomarkers

# Introduction

In the past identification of organisms were based on morphological methods and these methods
were both tedious and also highly limited in many areas especially when determining the
biodiversity in a given location (Ndong et al. 2015). However, thanks to the rise of sequencing
tools scientists can identify the biodiversity and species much more easily and quickly. The
sequencing is done on many different kinds of samples. However, for sequencing to work, one
must use primers and those primers should recognize a particular gene. Those genes that are used
to distinguish between species and measure biodiversity are called genetic markers. In the world,
there are many genetic markers and one of the most famous ones are cytochrome C oxidase
subunit 1 gene (COI) and cytochrome B gene (CYTB) (Ndong et al. 2015).
Both genes code for proteins in the mitochondria that are vital for the production of ATP (Ndong
et al. 2015). They are highly conserved and thus give a clear idea of how much evolution the
organism has gone through and also distinct between other species (Ndong et al. 2015).
Considering that these both genes are present in the mitochondrial genome this project through
clustering analysis and statistical analysis will explore which of the two is a better genetic
marker. The proposed hypothesis is that given COI is much more profoundly used than CYTB it
will perform much better when subjected to clustering. The project is interesting as it will give a
clear indication of how much the CYTB gene is behind than the COI gene when used as a
genetic marker. The type of data used is multiple nucleotide sequences of both genes that belong
to the genus Salvenius (Genus Salvenius belongs to the family Salmonidae and are composed of
what are commonly known as trout).

# Results

The database used to obtain the nucleotides for the genus Salvenius was NCBI. The CYTB gene
resulted in 598 hits or 598 sequences (that belong to a variety of species) of which 300 were
taken. This is the maximum usable value as the dataset becomes too large to be extracted from
the NCBI database when working in R software. The COI gene results in 146 hits and this was
not an extremely large dataset thus all were used. The Dunn index after the pairwise distances
was computed and clustered through hierarchical clustering method was calculated to be 0.752
for the COI gene and 0.470 for CYTB gene. The number of sequences that belong to the CYTB
gene reduced to 259 as some values generated "NaN” and these had to be omitted. The average
silhouette width (figure 1) of the CYTB gene resulted to be 0.49, and for the COI gene, it was
0.67. Some sequences pairwise distances that belong to CYTB gene in Cluster 1 and 2 (though
not a large amount) moved toward the -1-value indicating they are not compatible with those
clusters.

Figure 2 shows the internal validation graphs of the COI gene. It reveals that as the number of
clusters increases connectivity increases. The Dunn index decreases as the number of clusters
increase however by having 4 clusters or 8 clusters the Dunn index is high. The silhouette index
decreases as the number of clusters increase. With the number of clusters set to 2, the Dunn
index is approximately 0.7 with connectivity being the lowest and silhouette index the highest.
The chart reveals that stability is high when having 2 or 4 number of clusters. With the number 
of clusters set to 8, the graphs reveal marginal stability. Figure 3 shows the internal validation
graphs for CYTB gene. As the number of clusters increases the Dunn index, silhouette index
decrease and the connectivity increases (this is a general trend). With having 4 clusters the Dunn
index is high (about 0.65), connectivity is significantly low (about 4) and silhouette index is
marginally high (about 0.60). This shows that the optimum number of clusters to have is 4. Dunn
and silhouette indexes determine by other means of clustering (K-means, pam and diana) also
agree with the results.

# Discussion

NDONG et al 2015 reveal that the CYTB gene has greater variation and thus is a more profound
genetic marker when determining differences between species. However, Tobe et al 2009 reveal
that one is not better than the other and that both markers have significantly similar performance.
Considering these different conclusions this project has explored through clustering analysis
which performs significantly better. Considering the Dunn index and Silhouette index are
significantly much higher for the COI gene than it is for CYTB gene the hypothesis seems to be
well supported that the COI gene performs better than the CYTB gene. 8 clusters were produced
and the silhouette plots as shown in figure 1 reveal that the clusters formed based on pairwise
distances from COI sequences were of significantly higher quality than CYTB clusters. Some
part of clusters of 1 and 2 that belong to the CYTB gene was revealed to be moving towards -1
value indicating that the CYTB gene is failing to distinct as number of clusters rise. While the
COI gene did not have any part of clusters or any cluster moving towards -1 value.
The internal validation measures were calculated and plotted as shown in figure 2 and 3, and
they reveal that number of clusters chosen to be formed were appropriate and that the type of
clustering method chosen which is hierarchical clustering was also appropriate for both genes
COI and CYTB. In the case of COI gene though the degree of connectivity was significantly
higher when the clusters were set to 8 rather than 2 when compared to Dunn index validation
graph the plotted point of connectivity is much lower than the Dunn index and same when
compared to silhouette index. In the case of CYTB, the connectivity is significantly higher, and
the Dunn index is significantly lower. Considering the trends of the graphs and values, the idea
that the COI gene is significantly better performing genetic marker is further supported.

# Conclusion

In conclusion, the silhouette plots, the Dunn index values, and validation graphs all support the
hypothesis that the COI gene is significantly better performing marker that CYTB gene.
Furthermore, this evidence challenges the conclusions proposed by the NDONG et al 2015 and
Tobe et al 2009 who agree on the opposite that CYTB is equally performing or better performing
gene when compared to COI gene for discriminating between species. There is an
acknowledgement that there were limitations of the experiment such as the sample sizes were not
the same. However, given that COI gene is such as profoundly used genetic marker for
biodiversity analysis and the extreme significant difference in index values it is highly
recommended that COI should be the genetic marker of choice. 

# Acknowledgements
I would like to appreciate Jacqueline May’s NCBI R script for showing how to operate the
Entrez R package and its functions. I would also like to acknowledge www.cran.r-project.org for
the clValid function and hclust function which was required to calculate the Dunn index. I would
also to thank YouTube tutorial "Phylogenetic Analysis of ITS sequences in R” by Russ Gray for
introducing me to the distance. Alignment function. 

# References
Tobe SS, Kitchener A, Linacre A. 2009. Forensic Science International: Genetics Supplement
Series Cytochrome b or cytochrome c oxidase subunit I for mammalian species identification —
An answer to the debate 2:306–307.
Ndong A, Thiaw C, Diallo B, Sarr M, Diome T, Kane M, Sembene M. 2015. Barcoding:
Comparison of Variation Degree of COI and Cytochrome b Mitochondrial Markers in Two
Species Primary Maize Pests ( Sitophilus zeamais and Sitophilus oryzae ) 4531:373–393

# Images

![Figure 1: Shows the silhouette plots of cytochrome B (CYTB) gene and cytochrome oxidase
subunit 1 (COI) gene. N represents the number of sequences or samples. 1A) Shows the plot of
CYTB gene where 259 samples have been placed into 8 clusters. The average width of the
silhouette is 0.49. 1B) Shows the plot of COI gene where 143 samples have been placed into 8
clusters. The average width of the silhouette is 0.67.](Fish-clustering/Capture1.PNG)

![Figure 2: Represents the Internal Validation Graphs of COI gene produced by the “clValid()” function from R. Each graph shows 4
lines and each of those lines represent a clustering method. The clustering methods that were inputted for validation are
hierarchical, kmeans, pam and diana. The connections form due to values calculated from each number of clusters. 2A) shows the
validation graph of Dunn index. 2b) shows the validation graph on the basis of connectivity. 2c) shows the validation graph of the
silhouette index. ](Fish-clustering/Capture2.PNG)


![Figure 2: Represents the Internal Validation Graphs of CYTB gene produced by the “clValid()” function from R. Each graph shows 4
lines and each of those lines represent a clustering method. The clustering methods that were inputted for validation are
hierarchical, kmeans, pam and diana. The plot points connections form due to values calculated from each number of clusters. 2A)
shows the validation graph of Dunn index. 2b) shows the validation graph on the basis of connectivity. 2c) shows the validation
graph of the silhouette index. ](Fish-clustering/Capture3.PNG)
