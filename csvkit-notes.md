# Sample csvkit commands
### Docs: https://csvkit.readthedocs.io

# `csvcut` Filter CSV files

### See the data
`csvcut us_counties_2010.csv`

### See CSV schema
`csvcut -n us_counties_2010.csv`

### Retrieve first three columns ...
`csvcut -c 1-3 us_counties_2010.csv`

### ... or cherry-pick columns
`csvcut -c 1,2,10 us_counties_2010.csv`

# `csvgrep` Search CSV files

### Find counties whose names begin with "Mill"
`csvgrep -c 1 -m "Mill" us_counties_2010.csv`

### Use regex
`csvgrep -c 1 -r "T.y" us_counties_2010.csv`

# `csvjson` Output JSON from a CSV

### Pipe your output to JSON
`csvcut -c 1,2,10 us_counties_2010.CSV | csvjson -i 4`

# `csvstat` Generate stats from CSV files

### Stats on all your columns
`csvstat us_counties_2010.csv`

### For just one column
`csvstat -c 4 us_counties_2010.csv`

# `csvsql` Build table definitions and load data

### Get a SQL table statement
`csvsql -i postgresql us_counties_2010.csv`

### Avoid trying to infer data types
`csvsql -i postgresql --no-inference us_counties_2010.csv`

### Load a CSV straight into a PostgreSQL database
`createdb testing`
`csvsql --db postgresql:///testing --table us_counties_2010 --no-inference --insert us_counties_2010.csv`
