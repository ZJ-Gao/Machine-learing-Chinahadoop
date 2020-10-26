---
description: Gradient Boosting Decision Tree；To eliminate residual quicker
---

# GBDT

## CART \(Classification and RegressionTree\)

{% hint style="success" %}
Decsion tree  can not only be used to do classification, but also prediction.
{% endhint %}

![Geometry Explaination of decision tree\(Axis is dimension\)](../.gitbook/assets/image%20%2813%29.png)

![Principle of using decision tree to predict\(2D\) ](../.gitbook/assets/image%20%2816%29.png)

![Principle of using decision tree to predict\(3D\) ](../.gitbook/assets/image%20%285%29.png)

![Key Point of GBDT](../.gitbook/assets/image%20%2811%29.png)

![](../.gitbook/assets/image%20%288%29.png)

## Coding

* GradientBoostingClassifier
* GradientBoostingRegressor

| Parameter | Meaning |
| :--- | :--- |
| n\_estimators | iterations |
| learning\_rate | step size |
| max\_depth |  |
| min\_samples\_split |  |
| min\_samples\_leaf |  |

{% hint style="info" %}
n\_estimators and learning\_rate decide the fitting effect. If learning\_rate increases, n\_estimators will decrease accordingly. If n\_estimators too small, the model will underfitting.  If n\_estimators too big, the model will overfitting
{% endhint %}

