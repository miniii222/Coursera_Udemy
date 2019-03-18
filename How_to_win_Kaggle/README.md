# How to win Kaggle


정리

#### -`tree-based models`
#### - `non-tree based models : linear model, KNN`



## Preprocessing
### Numeeric Feature
- Tree-based models doesn't depend on scling
- Non-tree-based models hugely depend on scaling(KNN, linear model, neural network..)
#### scaling
- MinMaxScaler, StandardScaler, Rank, np.log(1+x), np.sqrt(1+x)

### Categorical Feature
- Label and Frequency encodings are often used for `tree-based models`
- Label encoding : category -> number(알파벳 순서로 넘버링 할수도 있고, 데이터에 나온 순서도래 할 수도 있음)
- Frequency encoding : 전체 데이터에서 몇프로의 비율로 출현하는지
- One-hot encoding is often used for `non-tree-based-models`
- Interactions of categorical features can help `non-tree-based-models`
