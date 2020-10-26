# HW-clustering

## Plot

```python
'''
    Historgram
'''
fig = plt.figure(figsize=(30, 150)) # Big drawing board
font = {'family' : 'Times New Roman',
'weight' : 'normal',
'size'   : 23,
}

fig = plt.figure(figsize=(30, 150))
# 将要绘制图形的每行由多少个直方图组成
column_per_line = 3
# 属性的总数
columns = len(data.columns)

# subplot format (3,3,x), layout is 3*3
# x is the location of this subplot
for i, attr in enumerate(data.columns):
    ax=fig.add_subplot((columns-columns%3)/3+1,column_per_line,i+1)
    ax.hist(data[attr])
    plt.title(attr)
    plt.rc('font', **font) # change the font according to the definition above
plt.sho
```

```python
'''
    Draw one scatter plot, but two sets(Y1,Y2).
'''
fig = plt.figure()
ax = fig.add_subplot(1, 1, 1)  
X = components[components.columns[1]] 
Y1 = components[components.columns[0]]
Y2 = components[components.columns[1]]
ax.scatter(X,Y1)
ax.scatter(X,Y2)
plt.show()
```

## Dataframe operations

### Delete certain column

```python
# Deleting columns
# Delete the "Area" column from the dataframe
data = data.drop("Area", axis=1)
# alternatively, delete columns using the columns parameter of drop
data = data.drop(columns="area")
# Delete the Area column from the dataframe in place
# Note that the original 'data' object is changed when inplace=True
data.drop("Area", axis=1, inplace=True). 
# Delete multiple columns from the dataframe
```

### Describe columns

* Type of desribe is series\#llsd

```python
result = data['habitat'].describe()
result
'''
    output:
    count     8124
    unique       7
    top          d
    freq      3148
    Name: habitat, dtype: object

'''
result['unique']
'''
    output:
    7
'''
```

## Data processing

### LabelEncoder

```python
from sklearn.preprocessing import LabelEncoder 
encoder = LabelEncoder()
x = encoder.fit_transform(x)
```

### Get dummies

Combine Label Encoder and Onehot Encoder

```python
data = pd.get_dummies(data)
```

## list

```python
# Give a list index
for i,col in enumerate(list):
```



