6_01. 결정트리 (Decision Tree)
import warnings
warnings.filterwarnings("ignore")

import pandas as pd
import numpy as np
import graphviz
import multiprocessing
import matplotlib.pyplot as plt
plt.style.use(['seaborn-whitegrid'])

from sklearn.datasets import load_iris, load_wine, load_breast_cancer
from sklearn.datasets import load_boston, load_diabetes
from sklearn import tree
from sklearn.preprocessing import StandardScaler
from sklearn.model_selection import cross_val_score
from sklearn.pipeline import make_pipeline

분류 - DecisionTreeClassifier()
https://scikit-learn.org/stable/modules/tree.html
DecisionTreeClassifier는 분류를 위한 결정트리 모델
두개의 배열 x, y를 입력 받음
x는 [n_samples, n_features] 크기의 데이터 특성 배열
y는 [n_samples] 크기의 정답 배열

# Github 연동 하는데 시간이 너무 오래걸렸다
# VScode Github 연결 및 python import 설치에 어려움을 겪었음
# 더 연습하고 공부할 것
# 방법을 찾기
