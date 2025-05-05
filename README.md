1.  t-SNE projected the data into four distinct clusters, although the original data had some overlap between a few clusters.
    You can see that some of the points ended up in the "wrong" cluster, although to be fair, t-SNE has no knowledge of which clusters the points actually belong to.
    All the clusters have similar densities.
    Two of the blobs are distinct from each other but "gave up" some of their points to the blob they originally had overlapped with.
    A "perfect" result would not completely separate the overlaps between blobs.
    Notice that the distance between the blobs is consistent with the degree to which they were originally separated.


2.  UMAP correctly projected the data into four partially distinct clusters, with one cluster completely distinct from the others.
    Unlike t-SNE, it has preserved the connectedness that the original data had with the partially overlapping clusters.
    You can see that, like t-SNE, some of the points ended up in the "wrong" cluster.
    Again, like t-SNE, all the clusters have similar densities.
    A "perfect" result would not completely separate the overlaps between blobs, because they actually do overlap in the original feature space.
    The distance between the clusters is again consistent with the degree to which they were originally separated.

3.  PCA  faithfully preserved the relative blob densities.
    PCA also preserved the relative separation between blobs.
    The distance between the clusters is very consistent with the degree to which they were originally separated.
    PCA and t-SNE took very little time to complete compared to UMAP.
    IMNSHO, PCA outperformed both t-SNE and UMAP in this experiment. This points to a common tendency to want to implement more advanced algorithms. The default result is not always an improvement over the simpler established methods.



