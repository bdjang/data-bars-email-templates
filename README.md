# Accessible Data in Email Templates

## Background
A simple and straightforward way to display horizontal and vertical bar charts coded in pure HTML/CSS.

Some advantages of this method:
* Bar charts coded in HTML/CSS are more accessible compared to bar charts displayed through images. Live text is used for numbers and labels which allow screen readers to pick up that information.
* They can be dynamic since data bar widths, chart numbers, label text, and hex colors are coded in HTML/CSS. These fields can be set up as variables within an ESP that can then populate and render when the user opens up the email.
* The load times are much faster compared to downloading images.
* Can be coded to be mobile responsive.
* Bar charts coded in HTML/CSS look great in dark mode.

Some disadvantages of this method:
* It takes time and effort to code and test these bar charts compared to displaying them as an image within email templates.
* For very complex and detailed bar charts and graphs, HTML/CSS is not a viable option.
* Bar charts coded in HTML/CSS can take up a good amount of email file weight.

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