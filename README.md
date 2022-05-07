# Data Bar Charts in Email Templates

## Background
An alternative way to display data without using images is to code horizontal bar charts in HTML/CSS.

**Some advantages to this method**:
* Charts can be mobile responsive through media queries.
* Load times are faster compared to downloading images.
* Screen readers can detect live text, numbers, and labels in these charts.
* Can be dynamic - since data bar widths, chart numbers, label text, and colors are coded in HTML/CSS, these fields can be set up as variables within ESPs.
* Additional code is not required to make these charts compatible in dark mode.

**Disadvantages of this method**:
* Requires time to code and test these bar charts.
* For very complex and detailed bar charts and graphs, this method is not an option.
* Can take up email file weight.

## Basics

Start with a `<table>` element and `<td>` cells for the **data bar name**, **data bar**, and **end label**. In this chart example, the name and end label will be place outside the data bar.

```html
<table width="600">
  <tr>
    <td>Data bar #1</td> <!-- Data bar name -->
    <td></td> <!-- Data bar -->
    <td>Label #1</td> <!-- End label -->
  </tr>
</table>
```

Define the `height` and `width` for each `<td>` cell *within* the `<style>` tag.

```html
<table width="600">
  <tr>
    <td style="background-color: #ffffff; height: 24px; width: 20%;">Data bar #1</td>
    <td style="background-color: #0dbd67; height: 24px; width: 65%;"></td>
    <td style="background-color: #ffffff; height: 24px; width: 15%;">Label #1</td>
  </tr>
</table>
```

![accessible-data1](https://user-images.githubusercontent.com/6575035/163897218-beb5f43c-50f9-4d1e-92b8-82ffa5e10beb.png)

Adjust the `width` values to change the size of the data bar. Since all three columns are sharing the width percentage, make sure all `<td>` cells add up to 100%.

```html
<table width="600">
  <tr>
    <td style="background-color: #ffffff; height: 24px; width: 20%;">Data bar #1</td>
    <td style="background-color: #0dbd67; height: 24px; width: 35%;"></td> <!-- The data bar width was reduced from 65% to 35%. The difference is added to the `<td>` cell below. -->
    <td style="background-color: #ffffff; height: 24px; width: 45%;">Label #1</td>
  </tr>
</table>
```

To create a second data bar, nest the code within new `<table>`, `<tr>`, and `<td>` elements. This will allow you to have more control over the spacing between each horizontal data bar. Adjust the spacing using `padding` within the outer `<td>` cell.

```html
<table>
  <tr>
    <td style="padding: 0 0 2px 0;">
      <table width="600">
        <tr>
          <td style="background-color: #ffffff; height: 24px; width: 20%;">Data bar #1</td>
          <td style="background-color: #0dbd67; height: 24px; width: 35%;"></td>
          <td style="background-color: #ffffff; height: 24px; width: 45%;">Label #1</td>
        </tr>
      </table>
    </td>
  </tr>
  <tr>
    <td style="padding: 0 0 2px 0;">
      <table width="600">
        <tr>
          <td style="background-color: #ffffff; height: 24px; width: 20%;">Data bar #2</td>
          <td style="background-color: #0d5fbd; height: 24px; width: 65%;"></td>
          <td style="background-color: #ffffff; height: 24px; width: 15%;">Label #2</td>
        </tr>
      </table>
    </td>
  </tr>
</table>
```

![accessible-data2](https://user-images.githubusercontent.com/6575035/163897313-4fa95403-3ad9-4c1a-982e-e11b32fc472c.png)

## Mobile Responsiveness

To make this chart mobile responsive, make sure all the `<td>` cell widths are set as percentages. Then change the `<table>` wrapper width value to 100% through media queries and reduce the `font-size` for the any chart text. Large text will skew the size of the data bars in mobile view.

## Dark Mode

These data bar charts are compatible in dark mode just as is - they do not require any additional custom code.

## CSS Animations

For specific email clients (Apple Mail, iOS, etc.) that support CSS animations, you can progressively enhance these bar charts and create an animation effect.

<!-- ## Dynamic Rendering -->