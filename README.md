Documentation for Creating KPI Indicator Arrows in PowerBI
This guide describes how to create and visualize KPI indicator arrows in PowerBI. We will use the measures "Arrow-Up" and "Arrow-Down" and visualize the result using the "Image Pro by Cloud Scope" visual.

1. Creating the "Arrow-UP" Measure
Create a new measure named "Arrow-UP". This measure should contain the path or URL to an image of the upward-pointing arrow.

dax
Code kopieren
Arrow-UP = "URL_TO_YOUR_UPWARD_ARROW_IMAGE"
2. Creating the "Arrow-Down" Measure
Create a new measure named "Arrow-Down". This measure should contain the path or URL to an image of the downward-pointing arrow.

dax
Code kopieren
Arrow-Down = "URL_TO_YOUR_DOWNWARD_ARROW_IMAGE"
3. Creating the "KPI" Measure
Create a new measure named "KPI". This measure compares the values of Value1 and Value2 and uses the appropriate arrow.

dax
Code kopieren
KPI = IF(
    CALCULATE(SUM(Value1)) > SUM(Value2), 
    [Arrow-UP], 
    [Arrow-Down]
)
// Note: SUM is only needed if the values are given as sums.
4. Visualizing the KPI
Use the "Image Pro by Cloud Scope" visual to visualize the KPI indicators.

Add the "Image Pro by Cloud Scope" visual to your report.
Drag the "KPI" measure into the "Image URL" field of the visual.
Customize the design of the visual to achieve the desired appearance. Use the "GitHub Basic ReadMe" template for the design.
Example of Customizing the Design
You can customize the colors, fonts, and other design elements according to your needs. Here is an example of a basic customization in the GitHub Basic ReadMe style:

Background color: White
Border color: Black
Font: Consolas, 12pt
Arrow size: 32x32px
Done!
Your KPI indicator arrow visual should now be correctly displayed and visualize the KPI measurement based on the comparison values Value1 and Value2.

Summary
With this guide, you can create visual indicators for KPIs in PowerBI that display the performance of your metrics using upward or downward pointing arrows. Use the "Image Pro by Cloud Scope" visual and customize the design according to your requirements to create meaningful and appealing dashboards.
