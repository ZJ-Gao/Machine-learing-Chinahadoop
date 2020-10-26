# Stacking

![](../.gitbook/assets/image%20%2818%29.png)

![](../.gitbook/assets/image%20%2815%29.png)

## Process

1. Choose machine learning model
2. Fitting

```python
from sklearn.linear_model import LogisticRegression
from sklearn.neighbors import KNeighborsClassifier
from sklearn.tree import DecisionTreeClassifier
from sklearn.svm import SVC
from mlxtend.classifer import StackingClassifier
# choose models
clf1 = KNeighborsClassifier()
clf2 = SVC()
clf3 = DecisionTreeClassifier()
lr1 = LogisticRegression()
# fit
 
# stack
sclf = StackingClassifier(classifiers = [], meta_classifier = )
```

