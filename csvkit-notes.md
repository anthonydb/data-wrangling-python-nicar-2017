# csvkit commands
### https://csvkit.readthedocs.io/en/1.0.1/cli.html

# csvcut -- filter csv files

### see the data
`csvcut us_counties_2010.csv`

### see csv schema
`csvcut -n us_counties_2010.csv`

### retrieve first three columns
`csvcut -c 1-3 us_counties_2010.csv`

### or cherry-pick columns
`csvcut -c 1,2,10 us_counties_2010.csv`

# csvgrep -- search csv files

### find counties whose names begin with "Mill"
`csvgrep -c 1 -m "Mill" us_counties_2010.csv`

### Use regex
`csvgrep -c 1 -r "T.y" us_counties_2010.csv`

# csvjson -- output json from a csv

### pip your output into JSON
`csvcut -c 1,2,10 us_counties_2010.csv | csvjson -i 4`

# csvstat -- get stats from csv files

### stats on all your columns
`csvstat us_counties_2010.csv`

### For just one column
`csvstat -c 4 us_counties_2010.csv`

# csvsql -- build table definitions and load data

### Get a SQL table statement
`csvsql -i postgresql us_counties_2010.csv`

### Avoid trying to infer data types
`csvsql -i postgresql --no-inference us_counties_2010.csv`
