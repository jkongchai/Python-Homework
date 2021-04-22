```python
import pandas as pd
```


```python
directory = "./Resources/budget_data.csv"
data = pd.read_csv(directory)
```


```python
data
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
      <th>Date</th>
      <th>Profit/Losses</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Jan-2010</td>
      <td>867884</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Feb-2010</td>
      <td>984655</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Mar-2010</td>
      <td>322013</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Apr-2010</td>
      <td>-69417</td>
    </tr>
    <tr>
      <th>4</th>
      <td>May-2010</td>
      <td>310503</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>81</th>
      <td>Oct-2016</td>
      <td>102685</td>
    </tr>
    <tr>
      <th>82</th>
      <td>Nov-2016</td>
      <td>795914</td>
    </tr>
    <tr>
      <th>83</th>
      <td>Dec-2016</td>
      <td>60988</td>
    </tr>
    <tr>
      <th>84</th>
      <td>Jan-2017</td>
      <td>138230</td>
    </tr>
    <tr>
      <th>85</th>
      <td>Feb-2017</td>
      <td>671099</td>
    </tr>
  </tbody>
</table>
<p>86 rows × 2 columns</p>
</div>



# Task 1
The total number of months included in the dataset.


```python
data
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
      <th>Date</th>
      <th>Profit/Losses</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Jan-2010</td>
      <td>867884</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Feb-2010</td>
      <td>984655</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Mar-2010</td>
      <td>322013</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Apr-2010</td>
      <td>-69417</td>
    </tr>
    <tr>
      <th>4</th>
      <td>May-2010</td>
      <td>310503</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>81</th>
      <td>Oct-2016</td>
      <td>102685</td>
    </tr>
    <tr>
      <th>82</th>
      <td>Nov-2016</td>
      <td>795914</td>
    </tr>
    <tr>
      <th>83</th>
      <td>Dec-2016</td>
      <td>60988</td>
    </tr>
    <tr>
      <th>84</th>
      <td>Jan-2017</td>
      <td>138230</td>
    </tr>
    <tr>
      <th>85</th>
      <td>Feb-2017</td>
      <td>671099</td>
    </tr>
  </tbody>
</table>
<p>86 rows × 2 columns</p>
</div>




```python
data["Date"]
```




    0     Jan-2010
    1     Feb-2010
    2     Mar-2010
    3     Apr-2010
    4     May-2010
            ...   
    81    Oct-2016
    82    Nov-2016
    83    Dec-2016
    84    Jan-2017
    85    Feb-2017
    Name: Date, Length: 86, dtype: object




```python
len(data["Date"])
```




    86




```python
Total_Months = len(data["Date"])
```


```python
Total_Months
```




    86



# Task 2
The net total amount of Profit/Losses over the entire period.


```python
data
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
      <th>Date</th>
      <th>Profit/Losses</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Jan-2010</td>
      <td>867884</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Feb-2010</td>
      <td>984655</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Mar-2010</td>
      <td>322013</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Apr-2010</td>
      <td>-69417</td>
    </tr>
    <tr>
      <th>4</th>
      <td>May-2010</td>
      <td>310503</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>81</th>
      <td>Oct-2016</td>
      <td>102685</td>
    </tr>
    <tr>
      <th>82</th>
      <td>Nov-2016</td>
      <td>795914</td>
    </tr>
    <tr>
      <th>83</th>
      <td>Dec-2016</td>
      <td>60988</td>
    </tr>
    <tr>
      <th>84</th>
      <td>Jan-2017</td>
      <td>138230</td>
    </tr>
    <tr>
      <th>85</th>
      <td>Feb-2017</td>
      <td>671099</td>
    </tr>
  </tbody>
</table>
<p>86 rows × 2 columns</p>
</div>




```python
sum(data["Profit/Losses"])
```




    38382578




```python
Net_Total = sum(data["Profit/Losses"])
```


```python
Net_Total
```




    38382578



# Task 3
The net total amount of Profit/Losses over the entire period.


```python
data
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
      <th>Date</th>
      <th>Profit/Losses</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Jan-2010</td>
      <td>867884</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Feb-2010</td>
      <td>984655</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Mar-2010</td>
      <td>322013</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Apr-2010</td>
      <td>-69417</td>
    </tr>
    <tr>
      <th>4</th>
      <td>May-2010</td>
      <td>310503</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>81</th>
      <td>Oct-2016</td>
      <td>102685</td>
    </tr>
    <tr>
      <th>82</th>
      <td>Nov-2016</td>
      <td>795914</td>
    </tr>
    <tr>
      <th>83</th>
      <td>Dec-2016</td>
      <td>60988</td>
    </tr>
    <tr>
      <th>84</th>
      <td>Jan-2017</td>
      <td>138230</td>
    </tr>
    <tr>
      <th>85</th>
      <td>Feb-2017</td>
      <td>671099</td>
    </tr>
  </tbody>
</table>
<p>86 rows × 2 columns</p>
</div>




```python
change = [0]
for t in range(len(data["Profit/Losses"])-1):
    change.append(int(data["Profit/Losses"][t+1])-int(data["Profit/Losses"][t]))
```


```python
len(change)-1
```




    85




```python
data["Change"] = change
```


```python
data
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
      <th>Date</th>
      <th>Profit/Losses</th>
      <th>Change</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Jan-2010</td>
      <td>867884</td>
      <td>0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Feb-2010</td>
      <td>984655</td>
      <td>116771</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Mar-2010</td>
      <td>322013</td>
      <td>-662642</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Apr-2010</td>
      <td>-69417</td>
      <td>-391430</td>
    </tr>
    <tr>
      <th>4</th>
      <td>May-2010</td>
      <td>310503</td>
      <td>379920</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>81</th>
      <td>Oct-2016</td>
      <td>102685</td>
      <td>-665765</td>
    </tr>
    <tr>
      <th>82</th>
      <td>Nov-2016</td>
      <td>795914</td>
      <td>693229</td>
    </tr>
    <tr>
      <th>83</th>
      <td>Dec-2016</td>
      <td>60988</td>
      <td>-734926</td>
    </tr>
    <tr>
      <th>84</th>
      <td>Jan-2017</td>
      <td>138230</td>
      <td>77242</td>
    </tr>
    <tr>
      <th>85</th>
      <td>Feb-2017</td>
      <td>671099</td>
      <td>532869</td>
    </tr>
  </tbody>
</table>
<p>86 rows × 3 columns</p>
</div>




```python
Average_Change = sum(change)/(len(change)-1)
```


```python
Average_Change
```




    -2315.1176470588234




```python
print(round(Average_Change, 2))
```

    -2315.12
    

# Task 4
The greatest increase in profits (date and amount) over the entire period.


```python
max(change)
```




    1926159




```python
data[data["Change"]==max(change)]
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
      <th>Date</th>
      <th>Profit/Losses</th>
      <th>Change</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>25</th>
      <td>Feb-2012</td>
      <td>1170593</td>
      <td>1926159</td>
    </tr>
  </tbody>
</table>
</div>




```python
Max_Inc=data[data["Change"]==max(change)]
```


```python
Max_Inc
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
      <th>Date</th>
      <th>Profit/Losses</th>
      <th>Change</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>25</th>
      <td>Feb-2012</td>
      <td>1170593</td>
      <td>1926159</td>
    </tr>
  </tbody>
</table>
</div>




```python
Max_Inc.iloc[0,0]
```




    'Feb-2012'




```python
Max_Inc.iloc[0,2]
```




    1926159



# Task 5
The greatest decrease in losses (date and amount) over the entire period.


```python
min(change)
```




    -2196167




```python
data[data["Change"]==min(change)]
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
      <th>Date</th>
      <th>Profit/Losses</th>
      <th>Change</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>44</th>
      <td>Sep-2013</td>
      <td>-1196225</td>
      <td>-2196167</td>
    </tr>
  </tbody>
</table>
</div>




```python
Max_Dec=data[data["Change"]==min(change)]
```


```python
Max_Dec
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
      <th>Date</th>
      <th>Profit/Losses</th>
      <th>Change</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>44</th>
      <td>Sep-2013</td>
      <td>-1196225</td>
      <td>-2196167</td>
    </tr>
  </tbody>
</table>
</div>




```python
Max_Dec.iloc[0,0]
```




    'Sep-2013'




```python
Max_Dec.iloc[0,2]
```




    -2196167



# Final Analysis


```python
print("Financial Analysis")
print("----------------------------")
print("Total Months: %d" % (Total_Months))
print("Total: $%d" % (Net_Total))
print("Average Change: $%.2f" % (Average_Change))
print("Greatest Increase in Profits: %s ($%d)" % (Max_Inc.iloc[0,0],Max_Inc.iloc[0,2]))
print("Greatest Decrease in Profits: %s ($%d)" % (Max_Dec.iloc[0,0],Max_Dec.iloc[0,2]))
```

    Financial Analysis
    ----------------------------
    Total Months: 86
    Total: $38382578
    Average Change: $-2315.12
    Greatest Increase in Profits: Feb-2012 ($1926159)
    Greatest Decrease in Profits: Sep-2013 ($-2196167)
    
