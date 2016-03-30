# remap-pwr
Transform ranking data-set to binary data-set for multi-partite pairwise ranking with binary classifiers

This script transforms a ranking data set into a binary data set 
suitable to perform multi-partite pairwise ranking with binary
classifiers. For each ranking in the input file the corresponding
data vectors are partitioned by their rank. For each pair of vectors
from different partitions their vector difference is written to the
output file. A target value of +1 (or -1) means that the minuend
(or the subtrahend) is ranked higher. The data format is SVMlight's
sparse data format for ranking and for binary classification,
respectively (cf. http://www.cs.cornell.edu/people/tj/svm_light/).
The output file name is the input file name appended with ".pwr".
Each line is terminated by a comment string holding the original qid
and the original line numbers of the minuend and the subtrahend.

