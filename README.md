# ETL_Project

                                            ETL_Project Report 
               Analysis of Collegiate Football Penalties and Fines: Overall report 
				             Arthurs of Report:
                                    Kajavia Ramsey, Sandy Stoudemire, Mahan Abbasian

  For our analysis we decided to gather information in regard to football player statistics. With the football draft just recently ending, some questions arose that initiated our choice of subject. Some of the questions that arose were, “Which collegiate football team has the highest amount of penalties and fines”?, “What factors play a key component in these penalties, is it age, position etc? To gather the data, we used two different sites, kaggle.com and data.world. From the sites were able to use two datasets, (https://www.kaggle.com/zynicide/nfl-football-player-stats) and (https://data.world/alice-c/nfl-fines-and-suspensions ). Once our datasets were chosen, we created data frames within Jupyter Notebook using Pandas. With the data frames we created, we were able to merge and combine the data into one table. Once merged, we extracted the columns that we felt were unnecessary to include in the data we were trying to gather. 

After extracting the data, we began the transformation by utilizing pandas. The two CSV files “NFL_draft and “Players_penalties” were merged into pandas and renamed Players_Penalties The data was merged by an inner join on “Players”. We attempted to drop duplicates and after this process, we identified no duplicates were shared in the two databases. After the attempt to drop duplicates, we made a decision to drop other columns such as Wikipedia profile, images, biography, and unnamed: 32. A removal of commas and dollar signs also took place in the “Fined Amount” column so we could pull this data into a data frame as a integer and not a string. We focused on the fined amounts provided to get an idea of where the highest or lowest amounts triggered a specific college/universities and age group with the comparison of the years. After manipulation through pandas, an installation of MySQL database was required to convert the data from pandas to MySQL. The merged tables were uploaded into Workbench. We attempted to drop the null but found this process unless because it didn’t provide a great visualization for the table.

The final step of our data manipulation process was to load the data into a database. For our data we chose a relational database because the data is structured and through our transform process we made sure the data is being stored as the right types. To load the data from our ipython notebook to MySQL we used SQLAlchemy along with PymySQL. SQLAlchemy allowed us to link our python notebook to MySQL and by using the DataFrame.to_sql function we were able to load the data into our MySQL database. Once loaded we checked the MySQL Workbench to make sure the data loaded correctly and we were pleased to see that our data was loaded into our relational database entirely and as the correct data type.
