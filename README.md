### Problem statement: 
For your current project, you need to create a visualization that shows the CO2 emissions per capita for each country from 2000-2011. You need to provide a visual presentation that not only allows someone to visually compare CO2 emissions between countries from year to year, but also provides information about each county’s population, GDP, and energy use. 
#### Step 1:
Access the datasets
Link to datasets
- CO2: https://docs.google.com/spreadsheets/d/1LwGHDgJkXSm8b0ziSDyC8pQGqjYVGpX9mAEVPs2KQgY/template/preview
- energy: https://docs.google.com/spreadsheets/d/1C3tnheC5Qd8deHaSMNjWLZPApLwaGQkpx-Sv-1mDwv0/template/preview
- total population: https://docs.google.com/spreadsheets/d/1yfbxSmFOUhH1FHoxYpOl3ir982HA_lsPchLAt60xbss/template/preview
- gdp total: https://docs.google.com/spreadsheets/d/1WbrxXDLKxAxDpwNSAQg2PdIEbtnjGwGe3bPHyCN7GlM/template/preview


#### Step 2
Load the data
1. Go to your profile on Tableau public and click Create a Viz.
2. From the Connect to Data window, go to the Files tab and open the CO2 dataset you downloaded earlier.
3. From the Data Source tab on the bottom of the interface, go to the Connections header at the top of the left-side column.
4. Click the + icon to add another data source. Start with the energy dataset.
5. Repeat step 4 for the other datasets, gdptotal and totalpopulation.
Now, you should have all four datasets loaded into Tableau. The datasets will be on the left-hand side of your screen under Connections.
![connections](https://github.com/PoojaParab-DA/Tableau/assets/172165136/39ce8fa6-d917-4aff-a406-1c26cce650eb) 

#### Step 3
Make connections with join
1. Click on CO2 under Connections. 
2. Under Sheets, you will notice all the different sheets in the CO2 dataset. Find CO2 Data Cleaned and double-click on it to load it.
3. Hover your cursor over the right side of the CO2 Data Cleaned box and click on the arrow.
4. Select Open to open the CO2 Data Cleaned dataset. Make sure you complete this step. This allows you to change the physical table, which will allow you to create JOINs. Otherwise, you will only be able to edit Relationships. Usually, you could use either option to accomplish the same goal. But for the purposes of this activity, we specifically want to use JOINs.
5. Click on the energy dataset under Connections.
6. Drag the energy sheet across to the CO2 Data Cleaned box under Multiple Connections. A Join pop-up window will appear.
7. The popup window may automatically populate with Year from CO2 Data Cleaned and Year1 from Energy. If not, put Year on the left side of the chart and Year1 on the right side.
8. Click on Add new join clause under Year. A dropdown menu will appear.
9. Select Country Name on the left side and Country on the right side.
10. Click the X to close the dropdown menu.

![join1](https://github.com/PoojaParab-DA/Tableau/assets/172165136/a34aac19-bbbf-4eec-b538-2ae972605b44)

11. Click Update now to examine the dataset. You will notice that Year and Year1 have a number sign above them. Change the data type to date for each of these columns. 
12. In the column, Year click on the # (not the arrow next to it) and select Date from the available options. 
After completing the first field, you will notice a red exclamation mark between CO2 Data Cleaned and Energy. This indicates that the columns you have joined are no longer of the same data type. One is formatted as date, and the other numeric.
You will also notice that after changing Year (CO2 Data Cleaned) to a Date type, the data preview pane will no longer display properly.
13. To fix this, go to the column list in the lower left of the screen. 



