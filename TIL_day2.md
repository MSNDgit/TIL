import matplotlib.pyplot as plt
import seaborn as sns

titanic = sns.load_dataset('titanic')

sns.set_style('whitegrid')

j1 = sns.jointplot (x='fare', y='age', data =titanic)

j2 = sns.jointplot(x='fare', y='age', kind='reg', data=titanic)

j3 = sns.jointplot(x='fare', y='age', kind = 'hex', data=titanic)

j4 = sns.jointplot(x='fare', y='age', kind = 'kde', data=titanic)

j1.fig.suptitle('titanic fare - scatter', size = 15)
j2.fig.suptitle('titanic fare - rag', size = 15)
j3.fig.suptitle('titanic fare - hex', size = 15)
j4.fig.suptitle('titanic fare - kde', size = 15)
plt.show()

