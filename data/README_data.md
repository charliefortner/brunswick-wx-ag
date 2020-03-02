By Charlie Fortner\
2020-03-01


# Data Sources

`ga_field_crops_2000-2020.csv`\
`ga_ag_commodities_1866-1970.csv`\
`ga_field_crops_1866-1999.csv`\
were downloaded from the USDAs [National Agricultural Statistical Service](https://quickstats.nass.usda.gov/) Quick Stats webppage. The data for field crops was split between two files because the webpage does not allow datasets >50,000 rows.

`qs.crops_20200229.txt.gz` is the raw data for the entire crop census downloaded from their [FTP](ftp://ftp.nass.usda.gov/quickstats/) site. This is how you get around that 50,000 row limit. This file is **Tab Delimited**. I suggest loading it using (python) pandas:
`pd.read_csv('qs.crops_20200229.txt.gz', compression='gzip', header=0, sep='\t', quotechar='"', error_bad_lines=False)`
Their documentation is pretty bad. The best explanation of the column names and codes is in the [glossary](https://quickstats.nass.usda.gov/src/glossary.pdf).

