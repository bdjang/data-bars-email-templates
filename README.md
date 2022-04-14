# Accessible Data in Email Templates

## Background
One way to display data within email templates is to code data visuals, such as horizontal and vertical bar charts, completely in HTML/CSS. This method will allow screen readers to detect any live text, numbers, and labels within these bar charts.

**Some advantages to this method**:
* Charts can be mobile responsive through media queries.
* Load times are faster compared to downloading images.
* Can be dynamic - since data bar widths, chart numbers, label text, and hex colors are coded in HTML/CSS, these fields can be set up as variables within ESPs.
* Dark mode compatible.

**Disadvantages of this method**:
* Requires time to code and test these bar charts.
* For very complex and detailed bar charts and graphs, HTML/CSS is not an option. Simpler is better.
* Can take up email file weight.

## Basics

## Customizing Bar Charts

## CSS Animations

<!-- Is there another method to display data tables, bar graphs, and other visuals in email templates without using images? Is there a way to display data in email templates that is accessible?

Start Simple

Create a column for the databar name, the actual databar, and the data end label.
Define the width for each <td> cell within the style tag.
Since all three columns are sharing the width percentage, make sure all <td> cells add up to 100%. I usually set the databar name column and the data end label to specific widths. The databar width in the middle will change.
Define the height of each <td> cell within the style tag.



In order to make this mobile responsive, add some media queries that sets the width of the table wrapper to 100%. Also, reduce the font-size for the databar name and data end label to fit in smaller screen sizes.

Now you have a basic horizontal data chart that is accessible to screen readers since live text is used.


If you want to add top labels, simply add an additional <tr> above and add the relevant text to give more context to the chart.

 -->