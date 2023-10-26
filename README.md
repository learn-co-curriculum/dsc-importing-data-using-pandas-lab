# Importing Data Using Pandas - Lab

## Introduction

In this lab, you'll get some practice with loading files with summary or metadata, and if you find that easy, the optional "level up" content covers loading data from a corrupted csv file.

## Objectives
You will be able to:

- Use pandas to import data from a CSV and and an Excel spreadsheet  

##  Loading Files with Summary or Meta Data

Load either of the files `'Zipcode_Demos.csv'` or `'Zipcode_Demos.xlsx'`. What's going on with this dataset? Clean it up into a useable format and describe the nuances of how the data is currently formatted.

All data files are stored in a folder titled `'Data'`.


```python
# Import pandas using the standard alias

```


```python
# __SOLUTION__ 
# Import pandas using the standard alias
import pandas as pd
```


```python
# Import the file and print the first 5 rows
df = None

```


```python
# __SOLUTION__ 
# Import the file and print the first 5 rows
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
# Print the last 5 rows of df

```


```python
# __SOLUTION__ 
# Print the last 5 rows of df
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
# What is going on with this data set? Anything unusual?
```


```python
# __SOLUTION__ 
# Comment: Dataframe is really two table views, one on top of the other. 
# The first is a summary view of the raw data below. 
# There is also a blank row at row 1 in the file.
```


```python
# Clean up the dataset

```


```python
# __SOLUTION__ 
# Clean up the dataset
prev_count = 10**3
for row in df.index:
    count = 0
    for entry in df.iloc[row].isnull():
        if entry:
            count += 1
    if count != prev_count and row!=0:
        print(f'On row {row} there are {count} null values. The previous row had {prev_count} null values.')
    prev_count = count
```

    On row 1 there are 44 null values. The previous row had 45 null values.
    On row 46 there are 0 null values. The previous row had 44 null values.



```python
# __SOLUTION__ 
# Import the first part of the data
df1 = pd.read_csv('Data/Zipcode_Demos.csv', skiprows=[1], nrows=45, usecols=[0, 1, 2])
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
# Look at the last five rows
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
# Import the second part of the data
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

Occasionally, you encounter some really ill-formatted data. One example of this can be data that has strings containing commas in a csv file. Under the standard protocol, when this occurs, one is supposed to use quotes to differentiate between the commas denoting fields and the commas within those fields themselves. For example, we could have a table like this:  

`ReviewerID,Rating,N_reviews,Review,VenueID
123456,4,137,This restaurant was pretty good, we had a great time.,98765`

Which should be saved like this if it were a csv (to avoid confusion with the commas in the Review text):
`"ReviewerID","Rating","N_reviews","Review","VenueID"
"123456","4","137","This restaurant was pretty good, we had a great time.","98765"`

Attempt to import the corrupt file, or at least a small preview of it. It is appropriately titled `'Yelp_Reviews_Corrupt.csv'`. Investigate some of the intricacies of skipping rows to then pass over this error and comment on what you think is going on.


```python
# Hint: Here's a useful programming pattern to use
try:
    # Do something
except Exception as e:
    # Handle your exception e
```


```python
# __SOLUTION__ 
# Your code here
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
        print(f'First failure at: {i}')
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
        print(f'First failure at: {i}')
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

Congratulations, you now practiced your Pandas-importing skills.
