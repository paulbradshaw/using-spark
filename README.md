# using-spark
Tutorial for using the Spark font for creating sparklines in text

Spark [is](https://github.com/paulbradshaw/spark) "a typeface for creating sparklines in text". The GitHub repo is useful, but assumes some prior knowledge. This tutorial is designed to explain how to use it if you're not already familiar with web fonts and other technicalities of web design.

## The quick version

The quickest way of achieving the results above is to: 

1. Export [my Codepen pen on Spark](https://codepen.io/paulbradshaw/pen/zEBzmE) as a zip file (the button to export should be in the bottom right corner). 
2. Unzip the export. You should now have a folder with an `index.html` file and a `css` folder containing a `style.css` file.
3. Download the [font file from the Spark GitHub repo](https://github.com/paulbradshaw/spark/blob/master/Output/Webfonts/Bar%20-%20medium/spark-bar-medium.woff). That link takes you to the 'spark bar medium' font, but you can also find fonts for other widths of bar chart and for line charts in [the 'Output/fonts' folder](https://github.com/paulbradshaw/spark/tree/master/Output/Webfonts)
4. Put that file in the `css` folder
5. The chart should now be working based on the numbers in curly brackets on the HTML page. Just change those numbers to change the text - or copy and paste it (including the `<span>` ) to create new charts. 

*Note: At the moment it is "compatible with Microsoft Word (2011 and later), Adobe Creative Cloud applications, Chrome 33+, Safari 6+, Firefox 4+, and Internet Explorer 10+. (See: http://stateofwebtype.com/ for a fuller listing of browser compatibility.)"*
