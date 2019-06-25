# sem6-lr1
6 семестр. Лабораторная работа 1
Лабораторная работа 1. Набор данных «Titanic»
Скачайте train (обучающий) набор данных о пассажирах Титаника по ссылке: https://www.kaggle.com/c/titanic/data

С использованием кода на Python найдите ответы на следующие вопросы:

Какое количество мужчин и женщин ехало на параходе? Приведите два числа через пробел.
[HW] Подсчитайте сколько пассажиров загрузилось на борт в различных портах? Приведите три числа через пробел.
Посчитайте долю погибших на параходе (число и процент)?
[HW] Какие доли составляли пассажиры первого, второго, третьего класса?
Вычислите коэффициент корреляции Пирсона между количеством супругов (SibSp) и количеством детей (Parch).
[HW] Выясните есть ли корреляция (вычислите коэффициент корреляции Пирсона) между:
возрастом и параметром survival;
полом человека и параметром survival;
классом, в котором пассажир ехал, и параметром survival.
Посчитайте средний возраст пассажиров и медиану.
[HW] Посчитайте среднюю цену за билет и медиану.
Какое самое популярное мужское имя на корабле?
[HW] Какие самые популярные мужское и женские имена людей, старше 15 лет на корабле?
Решение оформите в виде функций, в каждой функции укажите документацию с помощью pydoc.

Например:

# импорт необходимых библиотек для работы
import pandas as pd


def get_nubmer_of_pass(data = None):
""" 
    Какое количество мужчин и женщин ехало на параходе? 
    Приведите два числа через пробел
"""
    return 42


male_int = get_nubmer_of_pass(data)
female_int = get_nubmer_of_pass(data)
# Решение

# импорт необходимых библиотек для работы
import pandas as pd

def percentage(perc, whole):
    return (perc * 100) / whole

def get_nubmer_of_pass(sex, data = None):
    """
        Какое количество мужчин и женщин ехало на параходе? 
        Приведите два числа через пробел
    """
    sexratio = data.value_counts()

    if sex == 'male':
        return sexratio['male']
    else:
        return sexratio['female']
    

data = pd.read_csv('titanic.csv', index_col='PassengerId')
# print(data['Sex'])
male_int = get_nubmer_of_pass('male', data['Sex'] )
female_int = get_nubmer_of_pass('female', data['Sex'])

# print (male_int, female_int)
total_int = male_int + female_int
print (round(percentage(male_int, total_int)), round(percentage(female_int, total_int)) )
65.0 35.0
# импорт необходимых библиотек для работы
import pandas as pd

def percentage(perc, whole):
    return (perc * 100) / whole


def get_nubmer_of_survived(data = None):
    survived = data.value_counts()
    died_int = survived[0]
    surv_int = survived[1]
    return percentage(surv_int, surv_int+died_int)

data = pd.read_csv('titanic.csv', index_col='PassengerId')

surv_int = get_nubmer_of_survived(data['Survived'])
print(surv_int)
38.3838383838
import numpy as np
import pandas as pd


data = pd.read_csv('titanic.csv', index_col='PassengerId')
sibsp_arr = data['SibSp']
parch_arr = data['Parch']

pearson_int = np.corrcoef(sibsp_arr, parch_arr)

ages_lst = data['Age'].value_counts().index.tolist()
#print (type(age.value_counts().index.tolist()))
# print(age)

print(np.average(ages_lst))

#print(data.corr())
#print((pearson_int[0, 1]))
33.7169318182
