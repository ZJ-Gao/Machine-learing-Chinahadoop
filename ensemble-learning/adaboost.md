---
description: Traditional boost algorithm
---

# Adaboost

> The  following cited from[https://medium.com/greyatom/boosting-ce84639a805d](https://medium.com/greyatom/boosting-ce84639a805d)

![Box 1: You can see that we have assigned equal weights to each data point and applied a decision stump to classify them as + \(plus\) or &#x2014; \(minus\). The decision stump \(D1\) has generated vertical line at left side to classify the data points. We see that, this vertical line has incorrectly predicted three + \(plus\) as &#x2014; \(minus\). In such case, we&#x2019;ll assign higher weights to these three + \(plus\) and apply another decision stump.](../.gitbook/assets/image%20%2812%29.png)

![](../.gitbook/assets/image%20%287%29.png)

```python
from sklearn.ensemble import AdaBoostClassifier
from sklearn.model_selection import GridSearchCV
parameters = {'n_estimators': range(100,150)} # This value is set by experience
clf = GridSearchCV(AdaBoostClassifier(), parameters, cv=5, scoring='accuracy')\
clf.fit(x_train, y_train)
clf.best_params_
clf.best_score_
clf.score(x_test, y_test)
```

