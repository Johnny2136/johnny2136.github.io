---
layout: post
title: Day 62 of 100 Days Of Code
---

![Monday](https://raw.githubusercontent.com/Johnny2136/johnny2136.github.io/master/images/D3_Day62.png)

## Day 62: September 24, Monday

**Today 's Progress**: Continued lessons on [Introduction to the Data Visualization with D3 Challenges](https://learn.freecodecamp.org/data-visualization/data-visualization-with-d3).

**Thoughts**: Continued the D3.js lessons and Challenges, confirmed there is some content missing from `#freeCodeCamp` The examples that are there are pretty good some are not needed.

### Resources used:
  * [JSFiddle](https://jsfiddle.net/johnny2136/1pLubnqc/)
  * [REPL.IT](https://repl.it/@JohnJohnson2/FCCD3)
  * [GitHub_FCC_Repo](https://github.com/Johnny2136/FCC-Projects/blob/master/FCC_Challenges/DataVisualizationWithD3.md)
  * [D3: setting style conditionally with immediately invoked arrow function and ternary](https://stackoverflow.com/questions/45593251/d3-setting-style-conditionally-with-immediately-invoked-arrow-function-and-tern/45654334)
  * [D3 Tutorial](https://www.dashingd3js.com/table-of-contents)
  * [D3 in Depth](https://d3indepth.com/)

**Change the Presentation of a Bar Chart** (Last challenge I did)
**Example:** none

**Challenge Instructions:** First, add a margin of `2px` to the bar class in the style tag. Next, change the callback function in the `style()` method so it returns a value 10 times the original data value (plus the "px").

*Note: Multiplying each data point by the same constant only alters the scale. It's like zooming in, and it doesn't change the meaning of the underlying data.*

**My solution**
```html
<style>
  .bar {
    width: 25px;
    height: 100px;
    /* Add your code below this line */
    margin: 2px;
    /* Add your code above this line */
    display: inline-block;
    background-color: blue;
  }
</style>
<body>
  <script>
    const dataset = [12, 31, 22, 17, 25, 18, 29, 14, 9];    
    d3.select("body").selectAll("div")
      .data(dataset)
      .enter()
      .append("div")
      .attr("class", "bar")
      // Add your code below this line
      .style("height", (d) => (d * 10 + "px"));      
      // Add your code above this line
  </script>
</body>
```
**Link(s) to work**

1. Started work on [Introduction to the Data Visualization with D3 Challenges](https://learn.freecodecamp.org/data-visualization/data-visualization-with-d3).

**Introduction to the Data Visualization with D3 Challenges**

 - [x] Add Document Elements with D3
 - [x] Select a Group of Elements with D3
 - [x] Work with Data in D3
 - [x] Work with Dynamic Data in D3
 - [x] Add Inline Styling to Elements
 - [x] Change Styles Based on Data
 - [x] Add Classes with D3
 - [x] Update the Height of an Element Dynamically
 - [x] Change the Presentation of a Bar Chart
All code is in GitHub [FCC_Challenges/DataVisualizationWithD3.md](https://github.com/Johnny2136/FCC-Projects/edit/master/FCC_Challenges/DataVisualizationWithD3.md).
