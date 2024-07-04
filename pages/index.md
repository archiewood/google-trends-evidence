# Hit Google Trends API with DuckDB

```sql fourth_of_july
select 
  strptime(Time, '%Y-%m-%dT%H') as timestamp,
  "fourth of july: (United States)" as fourth_of_july_volume
from read_csv_auto('https://trends.google.com/trends/api/widgetdata/multiline/csv?req=%7B%22time%22%3A%222024-06-27T19%5C%5C%3A21%5C%5C%3A51%202024-07-04T19%5C%5C%3A21%5C%5C%3A51%22%2C%22resolution%22%3A%22HOUR%22%2C%22locale%22%3A%22en-US%22%2C%22comparisonItem%22%3A%5B%7B%22geo%22%3A%7B%22country%22%3A%22US%22%7D%2C%22complexKeywordsRestriction%22%3A%7B%22keyword%22%3A%5B%7B%22type%22%3A%22BROAD%22%2C%22value%22%3A%22fourth%20of%20july%22%7D%5D%7D%7D%5D%2C%22requestOptions%22%3A%7B%22property%22%3A%22%22%2C%22backend%22%3A%22CM%22%2C%22category%22%3A0%7D%2C%22userConfig%22%3A%7B%22userType%22%3A%22USER_TYPE_LEGIT_USER%22%7D%7D&token=APP6_UEAAAAAZohHz29acv4CWw6nLrHn-ki_5SoWfkoc&tz=240')
```


```sql sperm_donation
select 
  strptime(Time, '%Y-%m-%dT%H') as timestamp,
  "Sperm donation: (United States)" as sperm_donation_volume
from read_csv_auto('https://trends.google.com/trends/api/widgetdata/multiline/csv?req=%7B%22time%22%3A%222024-06-27T19%5C%5C%3A19%5C%5C%3A14%202024-07-04T19%5C%5C%3A19%5C%5C%3A14%22%2C%22resolution%22%3A%22HOUR%22%2C%22locale%22%3A%22en-US%22%2C%22comparisonItem%22%3A%5B%7B%22geo%22%3A%7B%22country%22%3A%22US%22%7D%2C%22complexKeywordsRestriction%22%3A%7B%22keyword%22%3A%5B%7B%22type%22%3A%22ENTITY%22%2C%22value%22%3A%22%2Fm%2F07mwt4%22%7D%5D%7D%7D%5D%2C%22requestOptions%22%3A%7B%22property%22%3A%22%22%2C%22backend%22%3A%22CM%22%2C%22category%22%3A0%7D%2C%22userConfig%22%3A%7B%22userType%22%3A%22USER_TYPE_LEGIT_USER%22%7D%7D&token=APP6_UEAAAAAZohHMnA71Z-2Hz1edZj_0IyJbD9wHAXZ&tz=240')
```



<LineChart
  data={fourth_of_july}
  x="timestamp"
  y="fourth_of_july_volume"
  title="Fourth of July - Search Volume"
  xLabel="Time"
/>

<LineChart
  data={sperm_donation}
  x="timestamp"
  y="sperm_donation_volume"
  title="Sperm Donation - Search Volume"
  xLabel="Time"
/>

