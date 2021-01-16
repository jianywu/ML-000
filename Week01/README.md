
## 概述
主要学习了机器学习的行业现状，以及需要的知识背景，比如python，比如数学，比如神经网络，lightbgm。复习了python，以及部分数学知识。

## python复习
1. []列表是全局的，要注意尽量不要作为入参，而是入参用None代替，如果为None，初始化为空，不为None，用原始的。
python'''
def __init__(self, passengers=None):
    if passengers == None:
        self.passengers = []
    else
        self.passengers = passengers
'''
可以避免passengers下次进来已经存了之前运行了的值的情况。

2. dataclass: 存数据用，是带有默认值的可变的named tuple。类中含有该属性相关的类方法。可以理解为既有数据，也有方法，是一种充血模型。主要用途是可以区分key和value，管理数据很方便。

3. python的slice
是左闭右开的。
[1:3]，表示index为1和2个元素，其中index从0开始。
[:-1]，表示最开始到倒数第二个元素。

## 学新语言的步骤
变量和赋值
控制循环
函数定义
类定义
常见函数，数据结构

## 数学知识复习
1. 概率Probability
概率是一种函数，把样本空间sample space的事件event发生的情况映射到值域[0, 1]。
条件概率：
P(A|B) = P(AB) / P(B)
P(AB)是AB交集的probability。

推论:
P(A|B) = P(A) * P(B|A) / P(B)
其中P(A) * P(B|A)为A和B交集发生的probablity，除以P(B)就是B发生的情况下，A发生的概率。

全概率：
P(B) = sum(P(B|Ai) * P(Ai))

贝叶斯定理:
P(Ai|B) = P(Ai) * P(B|Ai) / sum(P(B|Aj) * P(Aj))
其中P(Ai)表示先验概率prior probability，而P(Ai|B)表示后验概率，B事件发生时，Ai事件发生的概率。先验概率是根据样本统计出来的，后验概率是用于预测的。
