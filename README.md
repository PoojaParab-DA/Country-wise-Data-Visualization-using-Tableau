### Problem statement: 
For your current project, you need to create a visualization that shows the CO2 emissions per capita for each country from 2000-2011. You need to provide a visual presentation that not only allows someone to visually compare CO2 emissions between countries from year to year, but also provides information about each county’s population, GDP, and energy use. 

Tableau visualization : https://public.tableau.com/app/profile/pooja.parab4551/viz/Yearwiseco2distribution/Sheet1

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
14. Select the # icon next to the Year1 (Energy) column. Then, change the data type to Date.

Datatype changed.
![datatype change](https://github.com/PoojaParab-DA/Tableau/assets/172165136/9a3c091c-b205-4135-95c5-1cefa9853d78)

15. Click Update Now.

#### Step 4: Connect Additional datatypes

1. Click on gdptotal under Connections.

2. Under Sheets, drag the gdptotal sheet into the white space underneath the energy box.  

3. Go to the column list in the lower left of the screen, scroll until you find the column Year(Gdptotal). Click on # above it. A drop-down menu will appear.

4. Select Date from the drop-down menu.

If the data preview does not display properly, fix the date type in the lower left pane.

5. Click on the Venn diagram between energy and gdptotal. Click on Add new join clause under year. A drop-down menu will appear. 

6. Under CO2 Data Cleaned click on Country Name.

7. Click on the empty field under gdptotal across from Country Name. A dropdown menu will appear.

8. Set the right side of the join statement to Country1.

9. Close the Join pop-up by clicking on its exit button.

Now you are going to join totalpopulation, the last of the four datasets that you downloaded.

10. Click on totalpopulation under Connections.

11. Under Sheets, drag the totalpopulation sheet into the white space to the right of the energy and gdptotal boxes. 

A pop-up window will appear for the join. It should already be populated with Year under Datasource and Year(totalpopulation) under totalpopulation.

12. Go to the column list in the lower left of the screen, scroll until you find the Year(totalpopulation) column. Click on # above it. A drop-down menu will appear.

13. Select Date from the drop-down menu.

If the data preview does not display properly, fix the date type in the lower left pane.

14. Click on the Venn diagram to the left of totalpopulation. Click on Add new join clause under Year. A drop-down menu will appear. 

15. Under CO2 Data Cleaned click Country Name. 

16. Click on the empty field under totalpopulation across from Country Name. A dropdown menu will appear.

17. Click Country (totalpopulation).

18. Close the Join pop-up by clicking on its exit button.

19. Click the Update button to view your data columns.

    ![connections](https://github.com/PoojaParab-DA/Tableau/assets/172165136/ffae6a02-3992-43bc-81ee-b3678d6a1470)

If the dataset had gone beyond those dates, you would have filtered out the unneeded years in your visualization.

Reviewing the dataset, you may have noticed that some of your measurement values need to be changed. The data type for the column Energy use is listed as string data. You can tell this because of the Abc icon above the name. The column currentGDP is also formatted as type string.

20. Find the Abc icon above the Energy use column. Change it to Number (decimal).

21. Find the Abc icon above the currentGDP column. Change it to Number (whole).

If the data preview does not display properly, fix the date type in the lower left pane.

#### Step 5
Create a visualization

1. Click on the tab Sheet1.

2. Drag Country Name under CO2 Data Cleaned into the Detail square.

3. Drag CO2 Per Capita to Color.

4. Click on Color, then Edit Colors.

5. Click on the Palette dropdown and change it from Automatic to Red-Green diverging.

6. Check the boxes for Stepped Color and Reversed. (Because green is generally viewed as positive for CO2 emissions, you want the colors to move towards red as emissions go up.)

7. Click the Show Advanced dropdown.

8. Check the Start and End boxes.

You might have noticed that the legend on the right-hand side of the screen shows Sum(CO2 per capita). You need to change the start and end values in order to notice color contrasts showing red shades. 

The lowest CO2 Per Capita emission for any year is 0.0396 and the largest is 61.9898. 

9. Enter 0 into the Start field, and 62 into the End field. Click OK. Click the X button.

10. Drag Year from under CO2 Data Cleaned into the Filters area. 

11. Click on Years, Next, All, OK.

12. In the Filters box, right-click on YEAR(Year)

13. Select Show Filter. The filter will appear on the right side of the screen.

14. 14. Click on the arrow to the right of YEAR(Year) on the far-right side of the screen.

15. Select Single Value (dropdown). Now the areas are colored only for the values of each year. Use the checkboxes in the list to choose which years you want to include in the visualization. You can select only the years between 2000-2011 to view the emissions relevant to the scenario.

![viz1](https://github.com/PoojaParab-DA/Tableau/assets/172165136/c054fa94-ee32-494c-a7b3-c44769849751)

![viz2](https://github.com/PoojaParab-DA/Tableau/assets/172165136/6f10fc7f-0971-4677-92bd-2a3c91de48f6)

Hence, the visualization using Tableau was created.

