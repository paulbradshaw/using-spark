# using-spark
Tutorial for using the Spark font for creating sparklines in text

Spark [is](https://github.com/paulbradshaw/spark) "a typeface for creating sparklines in text". The [GitHub repo](https://github.com/aftertheflood/spark) is useful, but assumes some prior knowledge. This tutorial is designed to explain how to use it if you're not already familiar with web fonts and other technicalities of web design.

## Breaking down the elements

To create a webpage with a Spark chart you need the following ingredients:

1. A HTML page. Specifically, we need to make sure that part of the HTML includes some numbers that the font can work with.
2. A CSS file. The CSS file is what 'styles' part of the HTML into the Spark font.
3. The Spark font. This needs to be downloaded from the Spark GitHub repo's ['Output/fonts' folder](https://github.com/paulbradshaw/spark/tree/master/Output/Webfonts) and stored in the same place as the CSS file.

## Creating the HTML page

Let's make the HTML page first. I've created mine using the text editor Atom, and saved it as 'index.html'.

```html
<!DOCTYPE html>
<html >
<head>
  <meta charset="UTF-8">
  <title>Sparklines font</title>
      <link rel="stylesheet" href="css/style.css">
</head>
<body>
  <p>There were 70 Airprox reports involving drones coming close to aircraft over the UK in 2016 - compared to 29 in 2015 and just 6 in 2014. There were no incidents at all between 2011 and 2013: <span class="barchart">2010 {4,0,0,0,6,29,70} 2016</span>. There have been 33 incidents up to May 2017. </p>
  <p>That chart above is created using the font Spark: each bar of the chart is actually a number.</p>
  <p> The font to turn it into a chart needs to be stored in the same place as the CSS file.</p>
</body>
</html>
```

## How to use fonts in a webpage

To use this font in the webpage we need to add a line at the top of the CSS file: 

```css
@font-face {
  font-family: spark;
  src: url(spark-bar-medium.woff);
}
```

## The quick version

The quickest way of achieving the results above is to: 

1. Export [my Codepen pen on Spark](https://codepen.io/paulbradshaw/pen/zEBzmE) as a zip file (the button to export should be in the bottom right corner). 
2. Unzip the export. You should now have a folder with an `index.html` file and a `css` folder containing a `style.css` file.
3. Download the [font file from the Spark GitHub repo](https://github.com/paulbradshaw/spark/blob/master/Output/Webfonts/Bar%20-%20medium/spark-bar-medium.woff). That link takes you to the 'spark bar medium' font, but you can also find fonts for other widths of bar chart and for line charts in [the 'Output/fonts' folder](https://github.com/paulbradshaw/spark/tree/master/Output/Webfonts)
4. Put that file in the `css` folder
5. The chart should now be working based on the numbers in curly brackets on the HTML page. Just change those numbers to change the text - or copy and paste it (including the `<span>` ) to create new charts. 

*Note: At the moment it is "compatible with Microsoft Word (2011 and later), Adobe Creative Cloud applications, Chrome 33+, Safari 6+, Firefox 4+, and Internet Explorer 10+. (See: http://stateofwebtype.com/ for a fuller listing of browser compatibility.)"*
