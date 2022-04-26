# Exporting ACS Data
* Step 1: In the 'parseJson' class, do the following:
  Select your dataset of interest: "acs/acs5, acs/acs3,...,dec/sf1,etc."
  Next, select the publication year. For acs, you may select years as early as 2009.
  See below for an example. Here we selected 2012 ACS 5-year data set using "acs/acs5" in red and 2018 in green:
  parseJson(baseurl, "acs/acs5", 2012, variables)

* Step 2: In the 'getAll' method, do the following:
  Set "df" to True (df = True) if you want to export the data selected to your desktop.
  Select geography of interests, either "Tract" or "County".
  Select the name you want your output csv to be. (filename = 'someName')
  See below for another example. Here we selected df = True, county as our geography, and 'Putnam_SC2' as our filename.
  .getAll(df = True, geo = 'County', filename = 'Putnams_SC2')

To complete our example, the full line of code should look like

parseJson(baseurl, "acs/acs5", 2012, variables).getAll(df = True, geo = 'County', filename = 'Putnams_SC2')
