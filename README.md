# Video-Game-Sales-Data-Analytics
First Solo Data Analytics Project

-- Top Selling Genre (excluding no genre listed) by Total Global Sales and broken down by region/misc

SELECT Genre, 
  ROUND(SUM(Global_Sales), 2) AS Total_Global_Sales, 
  ROUND(SUM(NA_Sales), 2) AS North_America_Sales, 
  ROUND(SUM(EU_Sales), 2) AS Europe_Sales, 
  ROUND(SUM(JP_Sales), 2) AS Japan_Sales, 
  ROUND(SUM(Other_Sales), 2) AS Misc_Sales
 FROM Video_Game_Sales
 WHERE Genre <> ''
 GROUP BY Genre
 ORDER BY Total_Global_Sales DESC;
 
 
 
 
