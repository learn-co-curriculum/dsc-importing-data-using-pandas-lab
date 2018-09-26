
#  Loading Files with Summary or Meta Data

Load either of the files Zipcode_Demos.csv or Zipcode_Demos.xlsx. What's going on with this dataset? Clean it up into a useable format and describe the nuances with how the data is currently formatted.

All data files are stored in a folder titled 'Data'.


```python
#Your code here
```

# Level-Up: Loading Corrupt CSV files

Occassionally, you encountered some really ill formatted data. One example of this can be data that has strings containing commas in a csv file. Under the standard protocol, when this occurs, one is suppossed to use quotes to differentiate between the commas denoting fields and commas within those fields themselves. For example, we could have a table like this:  

ReviewerID,Rating,N_reviews,Review,VenueID
123456,4,137,This restuarant was pretty good, we had a great time.,98765

Which should be saved like this if it were a csv (to avoid confusion with the commas in the Review text):
"ReviewerID","Rating","N_reviews","Review","VenueID"
"123456","4","137","This restuarant was pretty good, we had a great time.","98765"

Attempt to import the corrupt file, or at least a small preview of it. It is appropriately titled **Yelp_Reviews_corrupt.csv**. Then, write a function that loads as much as the file as possible until it hits an error. Once it hits the error, have the function save that many rows (up to the error) as a dataframe. Load the next part of the dataframe starting from just after the error row. Continue on until you have reached the end of the file and merge all of these into a single dataframe. Also return the indices of the corrupt rows from the original file.


```python
#Hint: here's a useful programming pattern to use.
try:
    #do something
except Exception as e:
    #handle your exception e
```


```python
#Your code here
```
