# История экспериментов


## 1-st iteration
### Preprocessing
1. Сделал для начала "дубовую" предобработку для данных:
 - Удалил все объекты, имеющие пропуски
 - Не нормализовывал данные
 - Удалил стобцы **Name, Ticket, Cabin**
2. Замена пропусков возраста медианой и модой по всей выборке (**Age, port_name, ticket_cost**).
3.  Кодирование:
- **port_name, Sex** через One-Hot Encoding с удалением неинформативного признака
- **Pclass** через Target Encoding *с удалением исходного столбца*

### Model choosing 
sklearn - LogisticRegression 

### Замечания
- 
### Идеи на будущее
- Нормализовать вещественные признаки
- Сделать замену медианой по группам
- Оставить искомый порядковый признак **Pclass**
### Metrics
*Kaggle - 0.75837*


## 2-nd iteration
### Preprocessing
1. Нормализовал через StandartScaler **Age** и **ticket_cost**
2. Замена пропусков возраста медианой по каждой из групп в **Pclass** для признака **Age**.
3.  Кодирование:
- **Pclass** через Target Encoding **без** удаления исходного столбца

### Model choosing
sklearn - LogisticRegression
### Замечания
-

### Идеи на будущее
- Попробовать реализовать SVM, DT, RF, GBM на этой задаче
- Попробовать сгруппировать (SibSp и Parch) в общую колонку с количеством родственников (family_count) на корабле. Возможно это даст лучшее качество. 

### Metrics
*Accuracy - 0.93779904*
*Kaggle - 0.77033*


## 3-rd iteration
### Preprocessing
- Cгруппировал (SibSp и Parch) в общую колонку с количеством родственников (family_count) на корабле
- Добавлю target encoding для **family_num** и **Age**.
### Model choosing
sklearn - LogisticRegression
### Замечания
-

### Идеи на будущее
- Попробовать реализовать SVM, DT, RF, GBM на этой задаче
- Попробовать сгруппировать (SibSp и Parch) в общую колонку с количеством родственников (family_count) на корабле. Возможно это даст лучшее качество. 

### Metrics
*Accuracy - 0.949760765*
*Kaggle - 0.76315*


## 4-rd iteration
### Preprocessing
- 
### Model choosing
sklearn - SVC
### Замечания
- Лучшая регуляризация - `C=1.8`
Модель SVM с kernel RBF показала лучшие резальтаты относительно логистической регрессии.

### Идеи на будущее
- Попробовать реализовать DT, RF, GBM на этой задаче.
- Поиграться с регуляризацией и ядрами.
### Metrics
*Accuracy - 0.95454*
*Kaggle - 0.78468*


## 5-rd iteration
### Preprocessing
- 
### Model choosing
sklearn - DecisionTree
### Замечания
- 
### Идеи на будущее
- Попробовать реализовать RF, GBM на этой задаче.
### Metrics
*Accuracy - 0.95454*
*Kaggle - 0.78468*