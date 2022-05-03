# Detection-of-Fake-News
Back to Basic: Detection of Fake News Using Traditional Machine Learning Classifiers

This paper attempts to use traditional machine learning classifiers to detect fake news using the same dataset from previously published research which attains 96.7% to 100% accuracy by re-performing one dataset. We selected the dataset from the Chinese COVID-19 Fake News Dataset (CHECKED) prepared by Yang et al. 2021 which was available at https://github.com/cyang03/CHECKED. The following traditional machine learning classifiers are used in the testing:

Perceptron (PPN);
K-Nearest Neighbor (KNN);
Support vector machine (SVM);
Logistic regression; (LR)
Decision tree (DT); and
Random forest (RF).
Data Preparation

The CHECKED dataset contained 2,104 verified microblogs related to COVID-19 between December 2019 and August 2020 from Weibo, one of China's most popular social media platforms. Of the 2104 microblogs, 1760 were labelled “Real” (true news), and 344 were labelled “Fake” (fake news). Auxiliary information of each selected microblog, namely (i) number of comments (comment_num), (ii) number of re-post (repost_num), and (iii) number of likes (like_num) of each microblog from CHECKED were also extracted. Other details of the microblogs in CHECKED, including details of reposts, contend that 1,185,702 comments were not used in this paper for simplicity.

In data pre-processing, we manually verified the content of each dataset. We found that the contextual meaning of 13 out of 2104 microblogs should be classified as "opinion," i.e., neither true nor fake news. For the sake of fairness in training, we removed these 13 items. The total number of microblogs in our dataset remains 2,091 (including 344 fake news and 1,747 real news).

The pre-processed real news dataset is at real_news_modified_v2.csv, whereas the fake news dataset is at fake_news_modified_v2.csv. The source code of the testings is at analysis_v5.2.ipynb. The source codes of the 4 ablation studies investigating the effect of the accuracy by removing different features at Ablation_study_1.ipynb, Ablation_study_2.ipynb, Ablation_study_3.ipynb and Ablation_study_4.ipynb.
