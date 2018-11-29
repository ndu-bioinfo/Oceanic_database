# Oceanic_database
Major oceanic 16S/18S databases in qiime2 format and pre-trained classifier

### Examples for using these databases  

#### Specify which region was amplified; not necessary but can improve accuracy of classification  

qiime feature-classifier extract-reads \
  --i-sequences PR2_for_qiime2.qza \
  --p-f-primer TTGTACACACCGCCC \
  --p-r-primer CCTTCYGCAGGTTCACCTAC \
  --o-reads PR2_for_qiime2_primer_trimmed.qza
  
#### Train the classifier   

qiime feature-classifier fit-classifier-naive-bayes \
  --i-reference-reads Data/PR2/PR2_for_qiime2.qza \
  --i-reference-taxonomy Data/PR2/PR2_taxonomy.qza \
  --o-classifier classifier/PR2_classifier.qza
  
  
