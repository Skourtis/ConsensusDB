Input files:

Should be added as in the examples in the Dataset Folder
code is:
POI_list <- read.xlsx("./../Project_Datasets/POIS.xlsx", colNames = F)
Go_terms_OI <- read.xlsx("./../Project_Datasets/Go_terms_OI.xlsx", colNames = F)$X1



EnrichGO can only occur for gene lists >10 so some are excluded
EnrichmentGo clusterProfiler Explanation from https://www.biostars.org/p/220465/
I will give an example to explain this that helped me understand it. I also was looking for the answer and Guangchuang link helped.


Let is suppose I have a collection of genesets called : HALLMARK Now let is suppose there is a specific geneset there called: E2F_targets

BgRatio, M/N.

M = size of the geneset (eg size of the E2F_targets); (is the number of genes within that distribution that are annotated (either directly or indirectly) to the node of interest).

N = size of all of the unique genes in the collection of genesets (example the HALLMARK collection); (is the total number of genes in the background distribution (universe)

GeneRatio is k/n.

k = size of the overlap of 'a vector of gene id' you input with the specific geneset (eg E2F_targets), only unique genes; (the number of genes within that list n, which are annotated to the node.

n = size of the overlap of 'a vector of gene id' you input with all the members of the collection of genesets (eg the HALLMARK collection),only unique genes; is the size of the list of genes of interest
