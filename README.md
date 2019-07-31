
# Importing Data Using Pandas - Lab

## Introduction

In this lab, you'll get some practice with loading files with summary or metadata, and if you find that easy, the optional "level up" content covers loading data from a corrupted csv file!

## Objectives
You will be able to:
* Import data from csv files and Excel files
* Understand and explain key arguments for imports
* Save information to csv and Excel files
* Access data within a Pandas DataFrame (print() and .head())

##  Loading Files with Summary or Meta Data

Load either of the files Zipcode_Demos.csv or Zipcode_Demos.xlsx. What's going on with this dataset? Clean it up into a useable format and describe the nuances of how the data is currently formatted.

All data files are stored in a folder titled 'Data'.


```python
#Your code here
```


```python
# __SOLUTION__ 
import pandas as pd
```


```python
# __SOLUTION__ 
df = pd.read_csv('Data/Zipcode_Demos.csv')
df.head()
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
      <th>Average Statistics</th>
      <th>Unnamed: 2</th>
      <th>Unnamed: 3</th>
      <th>Unnamed: 4</th>
      <th>Unnamed: 5</th>
      <th>Unnamed: 6</th>
      <th>Unnamed: 7</th>
      <th>Unnamed: 8</th>
      <th>Unnamed: 9</th>
      <th>...</th>
      <th>Unnamed: 37</th>
      <th>Unnamed: 38</th>
      <th>Unnamed: 39</th>
      <th>Unnamed: 40</th>
      <th>Unnamed: 41</th>
      <th>Unnamed: 42</th>
      <th>Unnamed: 43</th>
      <th>Unnamed: 44</th>
      <th>Unnamed: 45</th>
      <th>Unnamed: 46</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1</td>
      <td>NaN</td>
      <td>0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2</td>
      <td>JURISDICTION NAME</td>
      <td>10005.8</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>2</th>
      <td>3</td>
      <td>COUNT PARTICIPANTS</td>
      <td>9.4</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>3</th>
      <td>4</td>
      <td>COUNT FEMALE</td>
      <td>4.8</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>4</th>
      <td>5</td>
      <td>PERCENT FEMALE</td>
      <td>0.404</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
  </tbody>
</table>
<p>5 rows × 47 columns</p>
</div>




```python
# __SOLUTION__ 
df.tail()
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
      <th>Average Statistics</th>
      <th>Unnamed: 2</th>
      <th>Unnamed: 3</th>
      <th>Unnamed: 4</th>
      <th>Unnamed: 5</th>
      <th>Unnamed: 6</th>
      <th>Unnamed: 7</th>
      <th>Unnamed: 8</th>
      <th>Unnamed: 9</th>
      <th>...</th>
      <th>Unnamed: 37</th>
      <th>Unnamed: 38</th>
      <th>Unnamed: 39</th>
      <th>Unnamed: 40</th>
      <th>Unnamed: 41</th>
      <th>Unnamed: 42</th>
      <th>Unnamed: 43</th>
      <th>Unnamed: 44</th>
      <th>Unnamed: 45</th>
      <th>Unnamed: 46</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>52</th>
      <td>53</td>
      <td>10006</td>
      <td>6</td>
      <td>2</td>
      <td>0.33</td>
      <td>4</td>
      <td>0.67</td>
      <td>0</td>
      <td>0</td>
      <td>6</td>
      <td>...</td>
      <td>6</td>
      <td>100</td>
      <td>0</td>
      <td>0</td>
      <td>6</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>6</td>
      <td>100</td>
    </tr>
    <tr>
      <th>53</th>
      <td>54</td>
      <td>10007</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>...</td>
      <td>1</td>
      <td>100</td>
      <td>1</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>100</td>
    </tr>
    <tr>
      <th>54</th>
      <td>55</td>
      <td>10009</td>
      <td>2</td>
      <td>0</td>
      <td>0</td>
      <td>2</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>2</td>
      <td>...</td>
      <td>2</td>
      <td>100</td>
      <td>0</td>
      <td>0</td>
      <td>2</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>2</td>
      <td>100</td>
    </tr>
    <tr>
      <th>55</th>
      <td>56</td>
      <td>10010</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>...</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>56</th>
      <td>57</td>
      <td>10011</td>
      <td>3</td>
      <td>2</td>
      <td>0.67</td>
      <td>1</td>
      <td>0.33</td>
      <td>0</td>
      <td>0</td>
      <td>3</td>
      <td>...</td>
      <td>3</td>
      <td>100</td>
      <td>0</td>
      <td>0</td>
      <td>3</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>3</td>
      <td>100</td>
    </tr>
  </tbody>
</table>
<p>5 rows × 47 columns</p>
</div>




```python
# __SOLUTION__ 
# Comment: Dataframe is really two table views, one on top of the other. 
# The first is a summary view of the raw data below. 
# There is also a blank row at row 1 in the file.
```


```python
# __SOLUTION__ 
prev_count = 10**3
for row in df.index:
    count = 0
    for entry in df.iloc[row].isnull():
        if entry:
            count += 1
    if count != prev_count and row!=0:
        print('On row {} there are {} null values. The previous row had {} null values.'.format(row, count, prev_count))
    prev_count = count
```

    On row 1 there are 44 null values. The previous row had 45 null values.
    On row 46 there are 0 null values. The previous row had 44 null values.



```python
# __SOLUTION__ 
df1 = pd.read_csv('Data/Zipcode_Demos.csv', skiprows=[1], nrows=45, usecols=[0,1,2])
df1.head()
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
      <th>Average Statistics</th>
      <th>Unnamed: 2</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>2</td>
      <td>JURISDICTION NAME</td>
      <td>10005.800</td>
    </tr>
    <tr>
      <th>1</th>
      <td>3</td>
      <td>COUNT PARTICIPANTS</td>
      <td>9.400</td>
    </tr>
    <tr>
      <th>2</th>
      <td>4</td>
      <td>COUNT FEMALE</td>
      <td>4.800</td>
    </tr>
    <tr>
      <th>3</th>
      <td>5</td>
      <td>PERCENT FEMALE</td>
      <td>0.404</td>
    </tr>
    <tr>
      <th>4</th>
      <td>6</td>
      <td>COUNT MALE</td>
      <td>4.600</td>
    </tr>
  </tbody>
</table>
</div>




```python
# __SOLUTION__ 
df1.tail()
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
      <th>Average Statistics</th>
      <th>Unnamed: 2</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>40</th>
      <td>42</td>
      <td>COUNT NRECEIVES PUBLIC ASSISTANCE</td>
      <td>7.100</td>
    </tr>
    <tr>
      <th>41</th>
      <td>43</td>
      <td>PERCENT NRECEIVES PUBLIC ASSISTANCE</td>
      <td>0.649</td>
    </tr>
    <tr>
      <th>42</th>
      <td>44</td>
      <td>COUNT PUBLIC ASSISTANCE UNKNOWN</td>
      <td>0.000</td>
    </tr>
    <tr>
      <th>43</th>
      <td>45</td>
      <td>PERCENT PUBLIC ASSISTANCE UNKNOWN</td>
      <td>0.000</td>
    </tr>
    <tr>
      <th>44</th>
      <td>46</td>
      <td>COUNT PUBLIC ASSISTANCE TOTAL</td>
      <td>9.400</td>
    </tr>
  </tbody>
</table>
</div>




```python
# __SOLUTION__ 
df2 = pd.read_csv('Data/Zipcode_Demos.csv', skiprows=47)
df2.head()
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
      <th>47</th>
      <th>JURISDICTION NAME</th>
      <th>COUNT PARTICIPANTS</th>
      <th>COUNT FEMALE</th>
      <th>PERCENT FEMALE</th>
      <th>COUNT MALE</th>
      <th>PERCENT MALE</th>
      <th>COUNT GENDER UNKNOWN</th>
      <th>PERCENT GENDER UNKNOWN</th>
      <th>COUNT GENDER TOTAL</th>
      <th>...</th>
      <th>COUNT CITIZEN STATUS TOTAL</th>
      <th>PERCENT CITIZEN STATUS TOTAL</th>
      <th>COUNT RECEIVES PUBLIC ASSISTANCE</th>
      <th>PERCENT RECEIVES PUBLIC ASSISTANCE</th>
      <th>COUNT NRECEIVES PUBLIC ASSISTANCE</th>
      <th>PERCENT NRECEIVES PUBLIC ASSISTANCE</th>
      <th>COUNT PUBLIC ASSISTANCE UNKNOWN</th>
      <th>PERCENT PUBLIC ASSISTANCE UNKNOWN</th>
      <th>COUNT PUBLIC ASSISTANCE TOTAL</th>
      <th>PERCENT PUBLIC ASSISTANCE TOTAL</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>48</td>
      <td>10001</td>
      <td>44</td>
      <td>22</td>
      <td>0.50</td>
      <td>22</td>
      <td>0.50</td>
      <td>0</td>
      <td>0</td>
      <td>44</td>
      <td>...</td>
      <td>44</td>
      <td>100</td>
      <td>20</td>
      <td>0.45</td>
      <td>24</td>
      <td>0.55</td>
      <td>0</td>
      <td>0</td>
      <td>44</td>
      <td>100</td>
    </tr>
    <tr>
      <th>1</th>
      <td>49</td>
      <td>10002</td>
      <td>35</td>
      <td>19</td>
      <td>0.54</td>
      <td>16</td>
      <td>0.46</td>
      <td>0</td>
      <td>0</td>
      <td>35</td>
      <td>...</td>
      <td>35</td>
      <td>100</td>
      <td>2</td>
      <td>0.06</td>
      <td>33</td>
      <td>0.94</td>
      <td>0</td>
      <td>0</td>
      <td>35</td>
      <td>100</td>
    </tr>
    <tr>
      <th>2</th>
      <td>50</td>
      <td>10003</td>
      <td>1</td>
      <td>1</td>
      <td>1.00</td>
      <td>0</td>
      <td>0.00</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>...</td>
      <td>1</td>
      <td>100</td>
      <td>0</td>
      <td>0.00</td>
      <td>1</td>
      <td>1.00</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>100</td>
    </tr>
    <tr>
      <th>3</th>
      <td>51</td>
      <td>10004</td>
      <td>0</td>
      <td>0</td>
      <td>0.00</td>
      <td>0</td>
      <td>0.00</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>...</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0.00</td>
      <td>0</td>
      <td>0.00</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>4</th>
      <td>52</td>
      <td>10005</td>
      <td>2</td>
      <td>2</td>
      <td>1.00</td>
      <td>0</td>
      <td>0.00</td>
      <td>0</td>
      <td>0</td>
      <td>2</td>
      <td>...</td>
      <td>2</td>
      <td>100</td>
      <td>0</td>
      <td>0.00</td>
      <td>2</td>
      <td>1.00</td>
      <td>0</td>
      <td>0</td>
      <td>2</td>
      <td>100</td>
    </tr>
  </tbody>
</table>
<p>5 rows × 47 columns</p>
</div>



## Level Up (Optional) - Loading Corrupt CSV files

Occasionally, you encountered some really ill formatted data. One example of this can be data that has strings containing commas in a csv file. Under the standard protocol, when this occurs, one is supposed to use quotes to differentiate between the commas denoting fields and commas within those fields themselves. For example, we could have a table like this:  

ReviewerID,Rating,N_reviews,Review,VenueID
123456,4,137,This restaurant was pretty good, we had a great time.,98765

Which should be saved like this if it were a csv (to avoid confusion with the commas in the Review text):
"ReviewerID","Rating","N_reviews","Review","VenueID"
"123456","4","137","This restaurant was pretty good, we had a great time.","98765"

Attempt to import the corrupt file, or at least a small preview of it. It is appropriately titled Yelp_Reviews_corrupt.csv. Investigate some of the intricacies of skipping rows to then pass over this error and comment on what you think is going on.


```python
#Hint: here's a useful programming pattern to use.
try:
    #do something
except Exception as e:
    #handle your exception e
```


```python
# __SOLUTION__ 
#Your code here
try:
    df = pd.read_csv('Data/Yelp_Reviews_Corrupt.csv')
except Exception as e:
    print(e)
```

    Error tokenizing data. C error: Expected 10 fields in line 2331, saw 11
    



```python
# __SOLUTION__ 
# # Iteration 1 
for i in range(1500,2000):
    try:
        df = pd.read_csv('Data/Yelp_Reviews_Corrupt.csv', nrows=i)
    except:
        print('First failure at: {}'.format(i))
        break
df1 = pd.read_csv('Data/Yelp_Reviews_Corrupt.csv', nrows=i-1)
print(len(df))
df1.head()
```

    First failure at: 1962
    1961





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
      <th>Unnamed: 0</th>
      <th>business_id</th>
      <th>cool</th>
      <th>date</th>
      <th>funny</th>
      <th>review_id</th>
      <th>stars</th>
      <th>text</th>
      <th>useful</th>
      <th>user_id</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1</td>
      <td>pomGBqfbxcqPv14c3XH-ZQ</td>
      <td>0</td>
      <td>2012-11-13</td>
      <td>0.0</td>
      <td>dDl8zu1vWPdKGihJrwQbpw</td>
      <td>5.0</td>
      <td>I love this place! My fiance And I go here atl...</td>
      <td>0.0</td>
      <td>msQe1u7Z_XuqjGoqhB0J5g</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2</td>
      <td>jtQARsP6P-LbkyjbO1qNGg</td>
      <td>1</td>
      <td>2014-10-23</td>
      <td>1.0</td>
      <td>LZp4UX5zK3e-c5ZGSeo3kA</td>
      <td>1.0</td>
      <td>Terrible. Dry corn bread. Rib tips were all fa...</td>
      <td>3.0</td>
      <td>msQe1u7Z_XuqjGoqhB0J5g</td>
    </tr>
    <tr>
      <th>2</th>
      <td>4</td>
      <td>Ums3gaP2qM3W1XcA5r6SsQ</td>
      <td>0</td>
      <td>2014-09-05</td>
      <td>0.0</td>
      <td>jsDu6QEJHbwP2Blom1PLCA</td>
      <td>5.0</td>
      <td>Delicious healthy food. The steak is amazing. ...</td>
      <td>0.0</td>
      <td>msQe1u7Z_XuqjGoqhB0J5g</td>
    </tr>
    <tr>
      <th>3</th>
      <td>5</td>
      <td>vgfcTvK81oD4r50NMjU2Ag</td>
      <td>0</td>
      <td>2011-02-25</td>
      <td>0.0</td>
      <td>pfavA0hr3nyqO61oupj-lA</td>
      <td>1.0</td>
      <td>This place sucks. The customer service is horr...</td>
      <td>2.0</td>
      <td>msQe1u7Z_XuqjGoqhB0J5g</td>
    </tr>
    <tr>
      <th>4</th>
      <td>10</td>
      <td>yFumR3CWzpfvTH2FCthvVw</td>
      <td>0</td>
      <td>2016-06-15</td>
      <td>0.0</td>
      <td>STiFMww2z31siPY7BWNC2g</td>
      <td>5.0</td>
      <td>I have been an Emerald Club member for a numbe...</td>
      <td>0.0</td>
      <td>TlvV-xJhmh7LCwJYXkV-cg</td>
    </tr>
  </tbody>
</table>
</div>




```python
# __SOLUTION__ 
df1.tail()
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
      <th>Unnamed: 0</th>
      <th>business_id</th>
      <th>cool</th>
      <th>date</th>
      <th>funny</th>
      <th>review_id</th>
      <th>stars</th>
      <th>text</th>
      <th>useful</th>
      <th>user_id</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>1956</th>
      <td>4993</td>
      <td>u8C8pRvaHXg3PgDrsUHJHQ</td>
      <td>0</td>
      <td>2016-08-08</td>
      <td>0.0</td>
      <td>gXmHGBSBBz2-uHdvGf4lZQ</td>
      <td>2.0</td>
      <td>just went to a retirement party upstairs and t...</td>
      <td>1.0</td>
      <td>tFa-r1pxZh04FjxNSEQgcQ</td>
    </tr>
    <tr>
      <th>1957</th>
      <td>4998</td>
      <td>-9nai28tnoylwViuJVrYEQ</td>
      <td>0</td>
      <td>2015-03-22</td>
      <td>0.0</td>
      <td>u-zqCN_IXfypJIUzIVUuzw</td>
      <td>5.0</td>
      <td>Great restaurant and great atmosphere.</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>1958</th>
      <td>I had an awesome great time with friends.</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>1959</th>
      <td>I loved the tapas and the excellent paella.</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>1960</th>
      <td>I can't wait to come back soon.</td>
      <td>0</td>
      <td>otDVyX37h61WEbqPLEjCmQ</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
  </tbody>
</table>
</div>




```python
# __SOLUTION__ 
# # Iteration 2 
for i in range(0,500):
    try:
        temp = pd.read_csv('Data/Yelp_Reviews_Corrupt.csv', skiprows=1962, nrows=i, names=df1.columns)
    except:
        print('First failure at: {}'.format(i))
        break
df2 = pd.read_csv('Data/Yelp_Reviews_Corrupt.csv', skiprows=1962, nrows=i-1, names=df1.columns)
print(len(df2))
df2.head()
```

    498





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
      <th>Unnamed: 0</th>
      <th>business_id</th>
      <th>cool</th>
      <th>date</th>
      <th>funny</th>
      <th>review_id</th>
      <th>stars</th>
      <th>text</th>
      <th>useful</th>
      <th>user_id</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>STAY AWAY FROM THIS PLACE!!!!!!</td>
      <td>5</td>
      <td>sDofYImMQQmu4Le5G9zmpQ</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>1</th>
      <td>3948</td>
      <td>GAKFx4jFUtTOTpp_jDJnuA</td>
      <td>0</td>
      <td>2017-09-01</td>
      <td>0</td>
      <td>OUZWMw7EgO7D596pUelSlA</td>
      <td>5</td>
      <td>Nice relaxing atmosphere. Friendly service and...</td>
      <td>1</td>
      <td>6vJY67yve43Ijvn8RKVUow</td>
    </tr>
    <tr>
      <th>2</th>
      <td>3949</td>
      <td>0QzCeORfF8EY34UODWRV9A</td>
      <td>0</td>
      <td>2017-09-03</td>
      <td>0</td>
      <td>7lbykaWFD8YBwT0mU1Rexw</td>
      <td>4</td>
      <td>Very pleased with our experience. Great off th...</td>
      <td>0</td>
      <td>6vJY67yve43Ijvn8RKVUow</td>
    </tr>
    <tr>
      <th>3</th>
      <td>3950</td>
      <td>tlt8zNrZ6_A3DmXiM-cnBA</td>
      <td>0</td>
      <td>2016-06-12</td>
      <td>0</td>
      <td>Nd_soHwCYi8adcNIT2w9LQ</td>
      <td>1</td>
      <td>Wife went to this location and was horrible. N...</td>
      <td>0</td>
      <td>S0dnPb1OzaqdBSOxyLr7BQ</td>
    </tr>
    <tr>
      <th>4</th>
      <td>3952</td>
      <td>XD0LjNuPPwJPsTAHecUh7A</td>
      <td>0</td>
      <td>2015-08-23</td>
      <td>0</td>
      <td>FUUTAr5CECrkfRa9Y2-MSg</td>
      <td>1</td>
      <td>Not baby friendly anymore.</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
  </tbody>
</table>
</div>




```python
# __SOLUTION__ 
temp = pd.read_csv('Data/Yelp_Reviews_Corrupt.csv')
print(len(temp))
temp.head()
```


    ---------------------------------------------------------------------------

    ParserError                               Traceback (most recent call last)

    <ipython-input-15-d6af0e7ded24> in <module>()
          1 # __SOLUTION__
    ----> 2 temp = pd.read_csv('Data/Yelp_Reviews_Corrupt.csv')
          3 print(len(temp))
          4 temp.head()


    ~/anaconda3/lib/python3.6/site-packages/pandas/io/parsers.py in parser_f(filepath_or_buffer, sep, delimiter, header, names, index_col, usecols, squeeze, prefix, mangle_dupe_cols, dtype, engine, converters, true_values, false_values, skipinitialspace, skiprows, skipfooter, nrows, na_values, keep_default_na, na_filter, verbose, skip_blank_lines, parse_dates, infer_datetime_format, keep_date_col, date_parser, dayfirst, cache_dates, iterator, chunksize, compression, thousands, decimal, lineterminator, quotechar, quoting, doublequote, escapechar, comment, encoding, dialect, error_bad_lines, warn_bad_lines, delim_whitespace, low_memory, memory_map, float_precision)
        683         )
        684 
    --> 685         return _read(filepath_or_buffer, kwds)
        686 
        687     parser_f.__name__ = name


    ~/anaconda3/lib/python3.6/site-packages/pandas/io/parsers.py in _read(filepath_or_buffer, kwds)
        461 
        462     try:
    --> 463         data = parser.read(nrows)
        464     finally:
        465         parser.close()


    ~/anaconda3/lib/python3.6/site-packages/pandas/io/parsers.py in read(self, nrows)
       1152     def read(self, nrows=None):
       1153         nrows = _validate_integer("nrows", nrows)
    -> 1154         ret = self._engine.read(nrows)
       1155 
       1156         # May alter columns / col_dict


    ~/anaconda3/lib/python3.6/site-packages/pandas/io/parsers.py in read(self, nrows)
       2046     def read(self, nrows=None):
       2047         try:
    -> 2048             data = self._reader.read(nrows)
       2049         except StopIteration:
       2050             if self._first_chunk:


    pandas/_libs/parsers.pyx in pandas._libs.parsers.TextReader.read()


    pandas/_libs/parsers.pyx in pandas._libs.parsers.TextReader._read_low_memory()


    pandas/_libs/parsers.pyx in pandas._libs.parsers.TextReader._read_rows()


    pandas/_libs/parsers.pyx in pandas._libs.parsers.TextReader._tokenize_rows()


    pandas/_libs/parsers.pyx in pandas._libs.parsers.raise_parser_error()


    ParserError: Error tokenizing data. C error: Expected 10 fields in line 2331, saw 11




```python
# __SOLUTION__ 
temp = pd.read_csv('Data/Yelp_Reviews_Corrupt.csv', names=df1.columns, skiprows=1)
print(len(temp))
temp.head()
```

    4651





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
      <th>Unnamed: 0</th>
      <th>business_id</th>
      <th>cool</th>
      <th>date</th>
      <th>funny</th>
      <th>review_id</th>
      <th>stars</th>
      <th>text</th>
      <th>useful</th>
      <th>user_id</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1</td>
      <td>pomGBqfbxcqPv14c3XH-ZQ</td>
      <td>0</td>
      <td>2012-11-13</td>
      <td>0</td>
      <td>dDl8zu1vWPdKGihJrwQbpw</td>
      <td>5</td>
      <td>I love this place! My fiance And I go here atl...</td>
      <td>0</td>
      <td>msQe1u7Z_XuqjGoqhB0J5g</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2</td>
      <td>jtQARsP6P-LbkyjbO1qNGg</td>
      <td>1</td>
      <td>2014-10-23</td>
      <td>1</td>
      <td>LZp4UX5zK3e-c5ZGSeo3kA</td>
      <td>1</td>
      <td>Terrible. Dry corn bread. Rib tips were all fa...</td>
      <td>3</td>
      <td>msQe1u7Z_XuqjGoqhB0J5g</td>
    </tr>
    <tr>
      <th>2</th>
      <td>4</td>
      <td>Ums3gaP2qM3W1XcA5r6SsQ</td>
      <td>0</td>
      <td>2014-09-05</td>
      <td>0</td>
      <td>jsDu6QEJHbwP2Blom1PLCA</td>
      <td>5</td>
      <td>Delicious healthy food. The steak is amazing. ...</td>
      <td>0</td>
      <td>msQe1u7Z_XuqjGoqhB0J5g</td>
    </tr>
    <tr>
      <th>3</th>
      <td>5</td>
      <td>vgfcTvK81oD4r50NMjU2Ag</td>
      <td>0</td>
      <td>2011-02-25</td>
      <td>0</td>
      <td>pfavA0hr3nyqO61oupj-lA</td>
      <td>1</td>
      <td>This place sucks. The customer service is horr...</td>
      <td>2</td>
      <td>msQe1u7Z_XuqjGoqhB0J5g</td>
    </tr>
    <tr>
      <th>4</th>
      <td>10</td>
      <td>yFumR3CWzpfvTH2FCthvVw</td>
      <td>0</td>
      <td>2016-06-15</td>
      <td>0</td>
      <td>STiFMww2z31siPY7BWNC2g</td>
      <td>5</td>
      <td>I have been an Emerald Club member for a numbe...</td>
      <td>0</td>
      <td>TlvV-xJhmh7LCwJYXkV-cg</td>
    </tr>
  </tbody>
</table>
</div>




```python
# __SOLUTION__ 
pd.read_csv('Data/Yelp_Reviews_Corrupt.csv', skiprows=len(df1)+len(df2), names=df1.columns)
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
      <th>Unnamed: 0</th>
      <th>business_id</th>
      <th>cool</th>
      <th>date</th>
      <th>funny</th>
      <th>review_id</th>
      <th>stars</th>
      <th>text</th>
      <th>useful</th>
      <th>user_id</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Cons:</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>1</th>
      <td>-  Dusty!  Not sure if it's all of Vegas but I...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>2</th>
      <td>-  Valet parking: kinda inconvenient when you ...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>3</th>
      <td>-  Sofabed is extremely flimsy</td>
      <td>if you have more than 2 people</td>
      <td>insist on 2 queen beds.  the sofa cushions ar...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Other points:</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>5</th>
      <td>*  Should call ahead of time to make sure your...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>6</th>
      <td>*  Hotel lobby is extremely small!</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>7</th>
      <td>*  In-room food service was overpriced (and fo...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>8</th>
      <td>*  Don't go to the 7-11</td>
      <td>it's shady.  You can shop at the am/pm or the...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>9</th>
      <td>Overall</td>
      <td>it was a good experience for the price we pai...</td>
      <td>3</td>
      <td>DZYGeWwBRKHgLUSk12sCvA</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>10</th>
      <td>4058</td>
      <td>WPCgtEG-bJt0cZtnM-x7yw</td>
      <td>0</td>
      <td>2012-02-28</td>
      <td>0</td>
      <td>igf8qa4uqeApRYwnrmcnWg</td>
      <td>5</td>
      <td>Loud</td>
      <td>fun and full of excitement! This high energy</td>
      <td>audience participation show was awesome.  Gre...</td>
    </tr>
    <tr>
      <th>11</th>
      <td>1624</td>
      <td>T5R6aILLDBnHQvfejY7dgA</td>
      <td>1</td>
      <td>2012-07-09</td>
      <td>0</td>
      <td>HjYi1MBvuVf8fVsLeLx1bQ</td>
      <td>5</td>
      <td>I've gone here since I was 8 or 9 years old. N...</td>
      <td>I plan on taking my future children there. I ...</td>
      <td>2</td>
    </tr>
    <tr>
      <th>12</th>
      <td>4938</td>
      <td>53BSdnhzcCBfBH_6TgX63Q</td>
      <td>0</td>
      <td>2014-08-31</td>
      <td>0</td>
      <td>hHVBKv4nacYCphHhHt2KIA</td>
      <td>5</td>
      <td>Very courteous service</td>
      <td>very delicious cuisine</td>
      <td>and a very phenomenal experience over all. I ...</td>
    </tr>
    <tr>
      <th>13</th>
      <td>2897</td>
      <td>hOB3NHuF-iVFdEkrA-PUlg</td>
      <td>1</td>
      <td>2012-02-17</td>
      <td>0</td>
      <td>acsWXRjRWWKzITQK4KaI4w</td>
      <td>4</td>
      <td>The Gault is a wonderful destination.  My fian...</td>
      <td>but due to the cozy warmth of our home-away-f...</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>14</th>
      <td>The room was lovely</td>
      <td>we had a loft basic package and really enjoye...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>15</th>
      <td>We took part in the spa package offered throug...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>16</th>
      <td>I emailed the concierge ahead of time to reque...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>17</th>
      <td>I've given 4 stars instead of 5 for a couple o...</td>
      <td>the breakfast is not included in the room rat...</td>
      <td>and the gym is adequate but quite small.</td>
      <td>3</td>
      <td>gIWWW6w-6P2j-hTH7nantw</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>18</th>
      <td>2422</td>
      <td>vwQvDIb_F7AqwCPaQhHrwg</td>
      <td>0</td>
      <td>2012-10-29</td>
      <td>8</td>
      <td>iN83pl9IPEo6Ay8g_G5g5g</td>
      <td>1</td>
      <td>If you are looking for an over-priced dorm lik...</td>
      <td>underage drinking</td>
      <td>and plenty of side-stepping the puke left in ...</td>
    </tr>
    <tr>
      <th>19</th>
      <td>1527</td>
      <td>04u-szAykldu-caSDHQaKA</td>
      <td>0</td>
      <td>2012-02-09</td>
      <td>0</td>
      <td>VkEeSwaqHgp6VFeANMoFow</td>
      <td>4</td>
      <td>I have been looking for a good Chinese restrai...</td>
      <td>0</td>
      <td>iNSL4q8MUvZ1ItVGboPpbQ</td>
    </tr>
    <tr>
      <th>20</th>
      <td>4080</td>
      <td>EDcZRvERC22Cvw1yi4-VKg</td>
      <td>1</td>
      <td>2017-12-05</td>
      <td>0</td>
      <td>tTb_HmUXAj5UwxX6kh8k1w</td>
      <td>2</td>
      <td>Its was ok. I got the sausage meatballs and Ar...</td>
      <td>although the description said square. Friend ...</td>
      <td>clean</td>
    </tr>
    <tr>
      <th>21</th>
      <td>4237</td>
      <td>ZM-ljL_Y6bR4qEYsGHws5A</td>
      <td>0</td>
      <td>2016-11-05</td>
      <td>0</td>
      <td>bl6WJnhCl0s1Jd4TUcSX_g</td>
      <td>2</td>
      <td>Called to see if they had availability and a g...</td>
      <td>so come right over.  I said I was a 10 minute...</td>
      <td>0</td>
    </tr>
    <tr>
      <th>22</th>
      <td>4498</td>
      <td>VRTfAP2DjvUYxRY3dw37hA</td>
      <td>0</td>
      <td>2014-01-08</td>
      <td>0</td>
      <td>3CYH_03G3ZtIHoA3gIWpLA</td>
      <td>4</td>
      <td>Luxurious. But of course</td>
      <td>you'd expect that from the Bellagio.</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>23</th>
      <td>Chi</td>
      <td>my pedicurist</td>
      <td>was wonderful. Super sweet and very attentive...</td>
      <td>it was heavenly. When it was all over</td>
      <td>I was kicking myself for not scheduling addit...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>24</th>
      <td>Four stars instead of five because:</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>25</th>
      <td>- The ladies in reception were a bit rude</td>
      <td>both over the phone and more so in person.</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>26</th>
      <td>- My pedicure only lasted two days! A pedicure...</td>
      <td>even 3 weeks without a single chip.</td>
      <td>7</td>
      <td>ETmpBain2s02PqHGwSr7hQ</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>27</th>
      <td>2716</td>
      <td>4VHp2gei1bpY68ZzEZE9Bg</td>
      <td>2</td>
      <td>2013-05-22</td>
      <td>9</td>
      <td>m0eO3358SKkzY7isf6kEpg</td>
      <td>1</td>
      <td>Not impressed at all. I paid 200 to go up and ...</td>
      <td>which was good. Unfortunately</td>
      <td>the other 1/2 was spent bad mouthing the comp...</td>
    </tr>
    <tr>
      <th>28</th>
      <td>3426</td>
      <td>8g3u6g7J93nIOF8owARxew</td>
      <td>0</td>
      <td>2014-08-13</td>
      <td>0</td>
      <td>JVwa-qaFERoa2dg0poiBcg</td>
      <td>3</td>
      <td>If you're looking for a shawarma in this area</td>
      <td>this is your only option. Better tasting opti...</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>29</th>
      <td>Had the traditional chicken shawarma. one of m...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>2552</th>
      <td>Starting off with drinks</td>
      <td>Bamburger serves beer</td>
      <td>wine</td>
      <td>and old-fashioned Stewart's soda</td>
      <td>but what is a burger joint without milkshakes...</td>
      <td>including the usual vanilla and chocolate sus...</td>
      <td>as well a special flavour each day for the ni...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>2553</th>
      <td>The menu is varied</td>
      <td>offering up soup</td>
      <td>salads</td>
      <td>sandwiches and desserts</td>
      <td>as well as a kid's menu</td>
      <td>but almost everyone here is in it for the bur...</td>
      <td>from the type of bun</td>
      <td>burger patty (beef</td>
      <td>chicken</td>
      <td>turkey</td>
    </tr>
    <tr>
      <th>2554</th>
      <td>We went with the Bambamburger ($11.50)</td>
      <td>which is 2/3 of a pound of prime ground chuck</td>
      <td>and the chicken burger ($9.95) for myself</td>
      <td>on whole-wheat buns. Both of us outfitted our...</td>
      <td>including mushrooms</td>
      <td>onions</td>
      <td>garlic mayo and cheese sauce for the Bambambu...</td>
      <td>and avocado</td>
      <td>chipotle mayo</td>
      <td>dill pickles and jalapeno peppers for the chi...</td>
    </tr>
    <tr>
      <th>2555</th>
      <td>Bamburger serves up great burgers</td>
      <td>fries and shakes at a fairly good price</td>
      <td>although if you go a little overboard with th...</td>
      <td>you might quickly end up with a $20 burger</td>
      <td>without realizing it. The service was friendl...</td>
      <td>and the atmosphere was very comfortable and n...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>2556</th>
      <td>If you are hunting for a real deal on a burger</td>
      <td>Bamburger might not be what you are looking for</td>
      <td>but if you are more on the adventurous side</td>
      <td>and want to have fun creating your own burger...</td>
      <td>Bamburger will deliver.</td>
      <td>8</td>
      <td>YHWsLBS8jzZiPjKHMFOaAA</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>2557</th>
      <td>3225</td>
      <td>iyyWYpWm8X-6i7kBR3JHuw</td>
      <td>0</td>
      <td>2014-01-27</td>
      <td>0</td>
      <td>yLKMQNn8VE3CEDX-TF5CfA</td>
      <td>1</td>
      <td>Tried to attend a recent basketball game. Purc...</td>
      <td>two parents and two kids. Arrived 45 min earl...</td>
      <td>1</td>
    </tr>
    <tr>
      <th>2558</th>
      <td>4674</td>
      <td>4KfDcE9iU2isFpoaKeDpgw</td>
      <td>0</td>
      <td>2012-06-14</td>
      <td>0</td>
      <td>rFH9iSvRmdm5LtDdsYwwpA</td>
      <td>5</td>
      <td>Great place to take your kids and interesting ...</td>
      <td>0</td>
      <td>9gYbRvijurhrnC6yPRlaUw</td>
    </tr>
    <tr>
      <th>2559</th>
      <td>4719</td>
      <td>P4Plzlfm4uJjNmH3wY4W1Q</td>
      <td>0</td>
      <td>2014-01-14</td>
      <td>0</td>
      <td>IobIRp1mGJiLg4B6wHAvqQ</td>
      <td>2</td>
      <td>While I will continue to eat at this establish...</td>
      <td>I will only do so because it is the closet Ch...</td>
      <td>otherwise I would completely avoid this place...</td>
    </tr>
    <tr>
      <th>2560</th>
      <td>3440</td>
      <td>nW45ez1L6U4PsYhV1BTrGQ</td>
      <td>0</td>
      <td>2012-05-19</td>
      <td>0</td>
      <td>abStF7f3_IyfZmOP82baZQ</td>
      <td>5</td>
      <td>H&amp;F Jewellery is amazing!</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>2561</th>
      <td>I had given my husband some ideas of engagemen...</td>
      <td>a friend of ours recommended H&amp;F.</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>2562</th>
      <td>The customer service here is great - they are ...</td>
      <td>attentive</td>
      <td>honest and the prices are very reasonable! My...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>2563</th>
      <td>We went back for our wedding bands and I worke...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>2564</th>
      <td>We've recommended 5 other friends to H&amp;F - the...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>2565</th>
      <td>Go to H&amp;F for all your jewellery needs - you w...</td>
      <td>1</td>
      <td>PkRFSQgSfca9Tamq7b2LdQ</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>2566</th>
      <td>4812</td>
      <td>e13SEvJud_vgeDR_doL4sQ</td>
      <td>0</td>
      <td>2013-03-01</td>
      <td>0</td>
      <td>lUV1KEm4cl4mluSEFharFQ</td>
      <td>4</td>
      <td>We loved the food. The service was good and we...</td>
      <td>0</td>
      <td>NW6gHZ8PlYl1STK1A1Ixeg</td>
    </tr>
    <tr>
      <th>2567</th>
      <td>1970</td>
      <td>9NBkIExYYz3w9O5JdzDOMA</td>
      <td>0</td>
      <td>2013-11-03</td>
      <td>0</td>
      <td>RT20_fUNJJNqMNvvjviNbQ</td>
      <td>1</td>
      <td>Hit or miss. I used these guys twice in a day ...</td>
      <td>no call nothing. So I call the dispatch to le...</td>
      <td>$20 to go 4 miles? I'll be renting a car tomo...</td>
    </tr>
    <tr>
      <th>2568</th>
      <td>689</td>
      <td>BTcY04QFiS1uh-RpkR7rAg</td>
      <td>1</td>
      <td>2013-06-02</td>
      <td>0</td>
      <td>6_A58CCY8SHB7r-Wu7-A5g</td>
      <td>5</td>
      <td>Came here with my 2 year old daughter for our ...</td>
      <td>she asked if everything was ok.  We old her w...</td>
      <td>great seating!</td>
    </tr>
    <tr>
      <th>2569</th>
      <td>4874</td>
      <td>t0T_4MM4EUHbCzBTF11FHA</td>
      <td>0</td>
      <td>2016-08-14</td>
      <td>0</td>
      <td>KqQwNyfoFiJOw911mrULIg</td>
      <td>5</td>
      <td>Great little restaurant. Not to many tables an...</td>
      <td>which is awesome. We had the Pad Thai and the...</td>
      <td>0</td>
    </tr>
    <tr>
      <th>2570</th>
      <td>564</td>
      <td>5XYR6doRa5Nj1JMfSDei6A</td>
      <td>1</td>
      <td>2016-06-14</td>
      <td>0</td>
      <td>xlGJkxoIBl8XH8wVsPZpnw</td>
      <td>5</td>
      <td>Always great friendly service and fresh baked ...</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>2571</th>
      <td>Highly recommend the custard cakes they are th...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>2572</th>
      <td>The rice flour cake is also really good and a ...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>2573</th>
      <td>The bean cakes are great here too!  orange</td>
      <td>almond</td>
      <td>and a few others I have tried are all good.</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>2574</th>
      <td>Can't go wrong with Nova Era</td>
      <td>0</td>
      <td>kBNFdviedCPFWyR-wVaAzw</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>2575</th>
      <td>3458</td>
      <td>aLcFhMe6DDJ430zelCpd2A</td>
      <td>0</td>
      <td>2013-10-02</td>
      <td>0</td>
      <td>kwiEG_KCpDB6aK5fTSM7iw</td>
      <td>2</td>
      <td>We were expecting amazing Thai food after all ...</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>2576</th>
      <td>This was disappointing.</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>2577</th>
      <td>First off</td>
      <td>it was really awkward sitting on the benches ...</td>
      <td>as people walked past us while to wait for ou...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>2578</th>
      <td>Second</td>
      <td>when we were seated</td>
      <td>it was so loud. It felt like we were in a hig...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>2579</th>
      <td>Finally - Food was mediocre. I was extremely d...</td>
      <td>but it wasn't flavourful.</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>2580</th>
      <td>Wasn't worth the hype</td>
      <td>unfortunately.</td>
      <td>1</td>
      <td>PkRFSQgSfca9Tamq7b2LdQ</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>2581</th>
      <td>4206</td>
      <td>WdBWhGe4Siqg3IYTc4_K4A</td>
      <td>0</td>
      <td>2016-08-15</td>
      <td>0</td>
      <td>O0ttxNGxHKtD8Cnnwc_j1g</td>
      <td>1</td>
      <td>Sunday at 8p. Not many people here at all. We ...</td>
      <td>and no one came to take our drink order. We w...</td>
      <td>0</td>
    </tr>
  </tbody>
</table>
<p>2582 rows × 10 columns</p>
</div>



## Summary

Congratulations, you now practiced your pandas-importing skills!
