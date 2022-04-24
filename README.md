# DnD-Statistics
Throw 4 machine learning models at DnD creature statblocks. Just to see if there are any correlations...

My final project for my Data Mining class.

Note: The test set (unseen data) was 10% of the data set. This may be adjusted in train_test_split().

# Requirements

Python 3, numpy, pandas, scikit (sklearn)

# Credit

Dataset: https://www.kaggle.com/datasets/travistyler/dnd-5e-monster-manual-stats

# Results

```
##############################   Testing against: ac   ##############################

[0.291970802919708, 0.24963503649635038, 0.2321167883211679, 0.291970802919708]
[RandomForestClassifier(max_depth=25, min_samples_split=8, n_estimators=50), KNeighborsClassifier(algorithm='kd_tree', metric='euclidean',
                     weights='distance'), SGDClassifier(alpha=0.1), SVC(C=10, gamma=0.1)]

Best model accuracy: 29.20%, RandomForestClassifier(max_depth=25, min_samples_split=8, n_estimators=50)
Accuracy against unseen data: 35.06%

##############################   Testing against: hp   ##############################

[0.09781021897810219, 0.07883211678832117, 0.06569343065693431, 0.12116788321167885]
[RandomForestClassifier(max_depth=20, min_samples_split=10, n_estimators=50), KNeighborsClassifier(algorithm='ball_tree', leaf_size=40, metric='euclidean'), SGDClassifier(), SVC(C=100, gamma=0.01, kernel='sigmoid')]

Best model accuracy: 12.12%, SVC(C=100, gamma=0.01, kernel='sigmoid')
Accuracy against unseen data: 9.09%

##############################   Testing against: cr   ##############################

[0.3751824817518249, 0.3167883211678832, 0.32992700729927005, 0.35474452554744523]
[RandomForestClassifier(max_depth=25, min_samples_split=10, n_estimators=75), KNeighborsClassifier(algorithm='kd_tree', leaf_size=40, metric='euclidean'), SGDClassifier(alpha=0.001), SVC(C=10, gamma=0.1)]

Best model accuracy: 37.52%, RandomForestClassifier(max_depth=25, min_samples_split=10, n_estimators=75)
Accuracy against unseen data: 33.77%

##############################   Testing against: str   ##############################

[0.15766423357664233, 0.13576642335766426, 0.14306569343065692, 0.17664233576642335]
[RandomForestClassifier(max_depth=25, min_samples_split=8, n_estimators=25), KNeighborsClassifier(algorithm='ball_tree', leaf_size=40, metric='euclidean',
                     weights='distance'), SGDClassifier(alpha=0.001), SVC(C=10, gamma=0.1, kernel='sigmoid')]

Best model accuracy: 17.66%, SVC(C=10, gamma=0.1, kernel='sigmoid')
Accuracy against unseen data: 10.39%

##############################   Testing against: dex   ##############################

[0.21021897810218979, 0.19416058394160582, 0.15182481751824817, 0.2131386861313868]
[RandomForestClassifier(max_depth=15, min_samples_split=8, n_estimators=75), KNeighborsClassifier(algorithm='ball_tree', metric='euclidean'), SGDClassifier(alpha=0.001, penalty='elasticnet'), SVC(C=1000, gamma=0.0001)]

Best model accuracy: 21.31%, SVC(C=1000, gamma=0.0001)
Accuracy against unseen data: 24.68%

##############################   Testing against: con   ##############################

[0.2583941605839416, 0.2175182481751825, 0.18248175182481752, 0.2423357664233577]
[RandomForestClassifier(max_depth=15, min_samples_split=10, n_estimators=25), KNeighborsClassifier(algorithm='ball_tree', metric='manhattan',
                     weights='distance'), SGDClassifier(penalty='elasticnet'), SVC(C=1, gamma=0.1)]

Best model accuracy: 25.84%, RandomForestClassifier(max_depth=15, min_samples_split=10, n_estimators=25)
Accuracy against unseen data: 19.48%

##############################   Testing against: int   ##############################

[0.25401459854014596, 0.2204379562043796, 0.18978102189781024, 0.256934306569343]
[RandomForestClassifier(criterion='entropy', max_depth=25, min_samples_split=8), KNeighborsClassifier(algorithm='ball_tree', metric='manhattan',
                     weights='distance'), SGDClassifier(alpha=0.001), SVC(C=1000, gamma=0.01)]

Best model accuracy: 25.69%, SVC(C=1000, gamma=0.01)
Accuracy against unseen data: 27.27%

##############################   Testing against: wis   ##############################

[0.310948905109489, 0.2846715328467153, 0.23357664233576642, 0.291970802919708]
[RandomForestClassifier(criterion='entropy', max_depth=15, min_samples_split=8,
                       n_estimators=50), KNeighborsClassifier(algorithm='ball_tree', leaf_size=40, metric='euclidean'), SGDClassifier(alpha=1.0), SVC(C=1, gamma=1)]

Best model accuracy: 31.09%, RandomForestClassifier(criterion='entropy', max_depth=15, min_samples_split=8,
                       n_estimators=50)
Accuracy against unseen data: 23.38%

##############################   Testing against: cha   ##############################

[0.22043795620437953, 0.20145985401459857, 0.14306569343065695, 0.21897810218978103]
[RandomForestClassifier(max_depth=20, min_samples_split=8, n_estimators=25), KNeighborsClassifier(algorithm='ball_tree', leaf_size=40, metric='euclidean',
                     weights='distance'), SGDClassifier(alpha=0.001, penalty='elasticnet'), SVC(C=1000, gamma=0.01)]

Best model accuracy: 22.04%, RandomForestClassifier(max_depth=20, min_samples_split=8, n_estimators=25)
Accuracy against unseen data: 18.18%

##############################   Testing against: legen   ##############################

[0.9562043795620438, 0.9518248175182482, 0.9532846715328468, 0.9518248175182482]
[RandomForestClassifier(max_depth=10, min_samples_split=10, n_estimators=25), KNeighborsClassifier(algorithm='ball_tree', leaf_size=40, metric='euclidean'), SGDClassifier(alpha=0.001, penalty='elasticnet'), SVC(C=1000, gamma=0.01)]

Best model accuracy: 95.62%, RandomForestClassifier(max_depth=10, min_samples_split=10, n_estimators=25)
Accuracy against unseen data: 92.21%

##############################   Testing against: nalign   ##############################

[0.4233576642335767, 0.38832116788321164, 0.3839416058394161, 0.41605839416058393]
[RandomForestClassifier(max_depth=25, min_samples_split=10, n_estimators=75), KNeighborsClassifier(algorithm='ball_tree', leaf_size=40, metric='manhattan'), SGDClassifier(alpha=0.001, penalty='l1'), SVC(C=1, gamma=0.1)]

Best model accuracy: 42.34%, RandomForestClassifier(max_depth=25, min_samples_split=10, n_estimators=75)
Accuracy against unseen data: 31.17%

##############################   Testing against: nsize   ##############################

[0.6175182481751824, 0.5795620437956204, 0.6102189781021898, 0.6116788321167883]
[RandomForestClassifier(max_depth=10, min_samples_split=6, n_estimators=50), KNeighborsClassifier(algorithm='brute', metric='euclidean'), SGDClassifier(alpha=0.001, penalty='l1'), SVC(C=1000, gamma=0.001, kernel='sigmoid')]

Best model accuracy: 61.75%, RandomForestClassifier(max_depth=10, min_samples_split=6, n_estimators=50)
Accuracy against unseen data: 51.95%

##############################   Testing against: ntype   ##############################

[0.5021897810218978, 0.47153284671532847, 0.4613138686131387, 0.4875912408759124]
[RandomForestClassifier(max_depth=15, min_samples_split=6, n_estimators=75), KNeighborsClassifier(algorithm='brute', metric='manhattan', weights='distance'), SGDClassifier(alpha=0.01), SVC(C=1, gamma=1)]

Best model accuracy: 50.22%, RandomForestClassifier(max_depth=15, min_samples_split=6, n_estimators=75)
Accuracy against unseen data: 45.45%

##############################   Testing against: nlaw   ##############################

[0.5912408759124088, 0.5357664233576643, 0.5605839416058395, 0.5868613138686131]
[RandomForestClassifier(criterion='entropy', max_depth=10, min_samples_split=10), KNeighborsClassifier(algorithm='brute', metric='manhattan', weights='distance'), SGDClassifier(alpha=0.001, penalty='elasticnet'), SVC(C=1, gamma=0.1)]

Best model accuracy: 59.12%, RandomForestClassifier(criterion='entropy', max_depth=10, min_samples_split=10)
Accuracy against unseen data: 45.45%

##############################   Testing against: nmoral   ##############################

[0.7313868613138685, 0.6715328467153284, 0.7007299270072993, 0.7124087591240876]
[RandomForestClassifier(criterion='entropy', max_depth=15, min_samples_split=10,
                       n_estimators=75), KNeighborsClassifier(algorithm='ball_tree', metric='euclidean'), SGDClassifier(alpha=0.001, penalty='elasticnet'), SVC(C=1, gamma=1)]

Best model accuracy: 73.14%, RandomForestClassifier(criterion='entropy', max_depth=15, min_samples_split=10,
                       n_estimators=75)
Accuracy against unseen data: 70.13%
```
