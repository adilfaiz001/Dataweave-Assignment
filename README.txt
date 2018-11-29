1) Pandas library is used to analyze the two given data files in json format.

2) Other library used are json, gzip and ast. gzip is used to read gzip files and then their content as of json form then json lib is used to get from gzip files and then ast is used to convert json into python dictionary.

3) Following procedure for each problem :
	** Here t_file represent today's dataset and y_file represent yesterday's dataset.
	1. Number of overlapping urlh is found by taking equality of each rows and urlh column in t_file and y_file.
	2. Drop null values from mrp column, and create table of mrp and url with condition on http_status being 200.Then drop duplicates of urlh keeping first of valid urlh.Now iterarte over today's new Mrp_x table compare against yesterday's new table of Mrp_y and generate data of dictionary of price difference and make new dataframe of price difference.
	3. Create t_category and y_category from t and y dataframe with value_counts() function to get unique values.
	4. 
	5.Taxonomy dataframe created using groupby method and its grouped on category,subcategory.Then count method is perfomed on this dataframe to get taxonomy of it.
	6.Get min and max of column and normalize with formula x = (x - x_min) / (x_max - x_min) on each row using apply method.
  