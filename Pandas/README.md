# Pandas Quizzes

Challenge your Python pandas skills by taking the quizzes below. The quizzes will be tagged with **#PandasQuiz** on social media to help identify them.

### Become an Expert

If you are looking for a comprehensive path to help you become an expert at the python data science ecosystem, you might want to check out the following books I wrote.

* [Exercise Python][3]
* [Master Data Analysis with Python][4]
* [Master Machine Learning with Python][5]

### Take a live in-person class with me

Learn directly with me by taking an interactive and fun [in-person bootcamp in Toronto, Houston, New York City, Boston, or Chicago in 2020][6].

### Get started for free

Sample my material by taking my [free Intro to Pandas class][7].

[1]: twitter.com/tedpetrou
[2]: linkedin.com/in/tedpetrou
[3]: https://www.dunderdata.com/exercise-python
[4]: https://www.dunderdata.com/master-data-analysis-with-python
[5]: https://www.dunderdata.com/master-machine-learning-with-python
[6]: https://www.dunderdata.com/all-in-person-courses
[7]: https://www.dunderdata.com

## Quiz #1 - February 6, 2020 - difficulty (3/4)

Take a look at the following DataFrame. What is the result of `sum(df)`?

a) 1  
b) 6  
c) 30  
d) 36  



```python
import pandas as pd
df = pd.DataFrame({0: [1, 2, 3], 
                   1: [5, 10, 15]})
df
```

<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>0</th>
      <th>1</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1</td>
      <td>5</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2</td>
      <td>10</td>
    </tr>
    <tr>
      <th>2</th>
      <td>3</td>
      <td>15</td>
    </tr>
  </tbody>
</table>
</div>

```python
sum(df)
```
