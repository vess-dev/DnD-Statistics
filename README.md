# DnD-Statistics
Throw 4 machine learning models at DnD creature statblocks. Just to see if there are any correlations...

The models used are KNeighbors, RandomForest, SGD, and the SVC classifiers.

A final soft VotingClassifier is made from the 3 best classifiers.

The final project for a Data Mining class.

Note: The test set (unseen data) was 10% of the data set. This may be adjusted in train_test_split().

# Requirements

Python 3, numpy, pandas, scikit (sklearn)

# Credit

Dataset: https://www.kaggle.com/datasets/travistyler/dnd-5e-monster-manual-stats

# Results

```
##############################   Testing against: ac   ##############################

[0.28029197080291973, 0.23649635036496347, 0.2525547445255475, 0.27007299270072993]
[RandomForestClassifier(criterion='entropy', max_depth=10, min_samples_split=10,
                       n_estimators=50), KNeighborsClassifier(algorithm='kd_tree', leaf_size=40, metric='euclidean'), SGDClassifier(alpha=0.001, loss='log'), SVC(C=1, gamma=0.1, probability=True)]

RandomForestClassifier(criterion='entropy', max_depth=10, min_samples_split=10,
                       n_estimators=50)
Best model accuracy: 28.03%
Accuracy against unseen data: 22.08%
Top 3 accuracy against unseen data: 24.68%

##############################   Testing against: hp   ##############################

[0.08759124087591241, 0.06569343065693431, 0.10218978102189782, 0.10510948905109489]
[RandomForestClassifier(max_depth=10, min_samples_split=10, n_estimators=75), KNeighborsClassifier(algorithm='kd_tree', leaf_size=40, metric='manhattan',
                     weights='distance'), SGDClassifier(alpha=0.001, loss='log', penalty='l1'), SVC(C=1000, gamma=0.001, kernel='sigmoid', probability=True)]

SVC(C=1000, gamma=0.001, kernel='sigmoid', probability=True)
Best model accuracy: 10.51%
Accuracy against unseen data: 12.99%
Top 3 accuracy against unseen data: 16.88%

##############################   Testing against: cr   ##############################

[0.3693430656934307, 0.34160583941605843, 0.33138686131386863, 0.3474452554744526]
[RandomForestClassifier(max_depth=10, min_samples_split=8), KNeighborsClassifier(algorithm='kd_tree', metric='euclidean'), SGDClassifier(alpha=0.001, loss='log', penalty='elasticnet'), SVC(C=1, gamma=1, probability=True)]

RandomForestClassifier(max_depth=10, min_samples_split=8)
Best model accuracy: 36.93%
Accuracy against unseen data: 38.96%
Top 3 accuracy against unseen data: 33.77%

##############################   Testing against: str   ##############################

[0.15766423357664236, 0.145985401459854, 0.17226277372262774, 0.1795620437956204]
[RandomForestClassifier(max_depth=10, min_samples_split=8, n_estimators=25), KNeighborsClassifier(algorithm='kd_tree', metric='euclidean'), SGDClassifier(alpha=0.01, loss='log', penalty='l1'), SVC(C=1, gamma=0.1, probability=True)]

SVC(C=1, gamma=0.1, probability=True)
Best model accuracy: 17.96%
Accuracy against unseen data: 9.09%
Top 3 accuracy against unseen data: 11.69%

##############################   Testing against: dex   ##############################

[0.21605839416058395, 0.18832116788321168, 0.20875912408759129, 0.2145985401459854]
[RandomForestClassifier(criterion='entropy', max_depth=15, min_samples_split=8,
                       n_estimators=75), KNeighborsClassifier(algorithm='ball_tree', metric='euclidean'), SGDClassifier(alpha=0.01, loss='log', penalty='elasticnet'), SVC(C=1, gamma=0.1, probability=True)]

RandomForestClassifier(criterion='entropy', max_depth=15, min_samples_split=8,
                       n_estimators=75)
Best model accuracy: 21.61%
Accuracy against unseen data: 24.68%
Top 3 accuracy against unseen data: 27.27%

##############################   Testing against: con   ##############################

[0.256934306569343, 0.22335766423357667, 0.2218978102189781, 0.23503649635036497]
[RandomForestClassifier(criterion='entropy', max_depth=15, min_samples_split=6), KNeighborsClassifier(algorithm='kd_tree', leaf_size=40, metric='euclidean',
                     weights='distance'), SGDClassifier(alpha=0.001, loss='log'), SVC(C=1, gamma=1, probability=True)]

RandomForestClassifier(criterion='entropy', max_depth=15, min_samples_split=6)
Best model accuracy: 25.69%
Accuracy against unseen data: 19.48%
Top 3 accuracy against unseen data: 14.29%

##############################   Testing against: int   ##############################

[0.2408759124087591, 0.21313868613138687, 0.2204379562043796, 0.23065693430656933]
[RandomForestClassifier(max_depth=20, min_samples_split=6, n_estimators=50), KNeighborsClassifier(algorithm='kd_tree', leaf_size=40, metric='euclidean'), SGDClassifier(alpha=0.001, loss='log'), SVC(C=1000, gamma=0.1, kernel='sigmoid', probability=True)]

RandomForestClassifier(max_depth=20, min_samples_split=6, n_estimators=50)
Best model accuracy: 24.09%
Accuracy against unseen data: 14.29%
Top 3 accuracy against unseen data: 15.58%

##############################   Testing against: wis   ##############################

[0.31678832116788325, 0.26861313868613135, 0.2788321167883212, 0.3036496350364964]
[RandomForestClassifier(max_depth=10, min_samples_split=10, n_estimators=50), KNeighborsClassifier(algorithm='kd_tree', leaf_size=40, metric='euclidean'), SGDClassifier(alpha=0.1, loss='modified_huber'), SVC(C=1, gamma=1, probability=True)]

RandomForestClassifier(max_depth=10, min_samples_split=10, n_estimators=50)
Best model accuracy: 31.68%
Accuracy against unseen data: 27.27%
Top 3 accuracy against unseen data: 27.27%

##############################   Testing against: cha   ##############################

[0.22335766423357667, 0.1854014598540146, 0.19124087591240874, 0.21021897810218979]
[RandomForestClassifier(criterion='entropy', max_depth=25, min_samples_split=10,
                       n_estimators=25), KNeighborsClassifier(algorithm='brute', metric='manhattan', weights='distance'), SGDClassifier(alpha=0.01, loss='modified_huber'), SVC(C=1, gamma=1, probability=True)]

RandomForestClassifier(criterion='entropy', max_depth=25, min_samples_split=10,
                       n_estimators=25)
Best model accuracy: 22.34%
Accuracy against unseen data: 19.48%
Top 3 accuracy against unseen data: 22.08%

##############################   Testing against: legen   ##############################

[0.9518248175182482, 0.9459854014598541, 0.9474452554744526, 0.9489051094890512]
[RandomForestClassifier(max_depth=10, min_samples_split=10, n_estimators=25), KNeighborsClassifier(algorithm='ball_tree', leaf_size=40, metric='euclidean'), SGDClassifier(alpha=0.001, loss='log', penalty='l1'), SVC(C=1, gamma=1, probability=True)]

RandomForestClassifier(max_depth=10, min_samples_split=10, n_estimators=25)
Best model accuracy: 95.18%
Accuracy against unseen data: 89.61%
Top 3 accuracy against unseen data: 89.61%

##############################   Testing against: nalign   ##############################

[0.4467153284671532, 0.41459854014598535, 0.4204379562043795, 0.4335766423357665]
[RandomForestClassifier(max_depth=20, min_samples_split=8, n_estimators=25), KNeighborsClassifier(algorithm='brute', metric='manhattan', weights='distance'), SGDClassifier(alpha=0.001, loss='log', penalty='l1'), SVC(C=10, gamma=0.1, probability=True)]

RandomForestClassifier(max_depth=20, min_samples_split=8, n_estimators=25)
Best model accuracy: 44.67%
Accuracy against unseen data: 28.57%
Top 3 accuracy against unseen data: 33.77%

##############################   Testing against: nsize   ##############################

[0.6058394160583941, 0.5883211678832116, 0.6233576642335766, 0.6116788321167882]
[RandomForestClassifier(criterion='entropy', max_depth=10, min_samples_split=10,
                       n_estimators=25), KNeighborsClassifier(algorithm='kd_tree', leaf_size=40, metric='manhattan',
                     weights='distance'), SGDClassifier(alpha=0.01, loss='modified_huber'), SVC(C=100, gamma=0.01, probability=True)]

SGDClassifier(alpha=0.01, loss='modified_huber')
Best model accuracy: 62.34%
Accuracy against unseen data: 49.35%
Top 3 accuracy against unseen data: 48.05%

##############################   Testing against: ntype   ##############################

[0.5036496350364964, 0.4569343065693431, 0.4773722627737226, 0.4875912408759124]
[RandomForestClassifier(max_depth=15, min_samples_split=10, n_estimators=75), KNeighborsClassifier(algorithm='ball_tree', leaf_size=40, metric='euclidean'), SGDClassifier(alpha=0.001, loss='log'), SVC(C=1, gamma=1, probability=True)]

RandomForestClassifier(max_depth=15, min_samples_split=10, n_estimators=75)
Best model accuracy: 50.36%
Accuracy against unseen data: 54.55%
Top 3 accuracy against unseen data: 51.95%

##############################   Testing against: nlaw   ##############################

[0.6175182481751824, 0.5751824817518247, 0.6131386861313868, 0.6116788321167883]
[RandomForestClassifier(max_depth=20, min_samples_split=8), KNeighborsClassifier(algorithm='ball_tree', metric='manhattan',
                     weights='distance'), SGDClassifier(alpha=0.001, loss='log', penalty='elasticnet'), SVC(C=1, gamma=1, kernel='linear', probability=True)]

RandomForestClassifier(max_depth=20, min_samples_split=8)
Best model accuracy: 61.75%
Accuracy against unseen data: 50.65%
Top 3 accuracy against unseen data: 45.45%

##############################   Testing against: nmoral   ##############################

[0.7124087591240875, 0.6394160583941606, 0.6861313868613138, 0.710948905109489]
[RandomForestClassifier(max_depth=10, min_samples_split=8, n_estimators=25), KNeighborsClassifier(algorithm='brute', metric='euclidean'), SGDClassifier(alpha=0.001, loss='log', penalty='l1'), SVC(C=10, gamma=0.1, probability=True)]

RandomForestClassifier(max_depth=10, min_samples_split=8, n_estimators=25)
Best model accuracy: 71.24%
Accuracy against unseen data: 59.74%
Top 3 accuracy against unseen data: 62.34%
```
