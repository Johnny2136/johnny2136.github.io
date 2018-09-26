---
layout: post
title: Day 63 of 100 Days Of Code
---

## Day 63: September 25, Tuesday

**Today 's Progress**: Continued lessons on [Introduction to the Data Visualization with D3 Challenges](https://learn.freecodecamp.org/data-visualization/data-visualization-with-d3).

**Thoughts**: Continued the D3.js lessons and Challenges, aside from content missing from `#freeCodeCamp` The examples disappeared. So two days of hellish commutes lasing 4 hours on Monday and 3.5 hours round trip today. I'm tired.

### Resources used:
  * [JSFiddle](https://jsfiddle.net/johnny2136/1pLubnqc/)
  * [REPL.IT](https://repl.it/@JohnJohnson2/FCCD3)
  * [GitHub_FCC_Repo](https://github.com/Johnny2136/FCC-Projects/blob/master/FCC_Challenges/DataVisualizationWithD3.md)
  * [D3: setting style conditionally with immediately invoked arrow function and ternary](https://stackoverflow.com/questions/45593251/d3-setting-style-conditionally-with-immediately-invoked-arrow-function-and-tern/45654334)
  * [D3 Tutorial](https://www.dashingd3js.com/table-of-contents)
  * [D3 in Depth](https://d3indepth.com/)

  **Display Shapes with SVG**
  **Example:**
  none, a freaking example would have been awesome!
  ```html
  <svg width="400" height="180">
   <rect x="50" y="20" width="150" height="150" style="fill:blue;stroke:pink;stroke-width:5;fill-opacity:0.1;stroke-opacity:0.9" />
  </svg>
  ```

  **Challange Instructions:**
  Add a rect shape to the svg using append(), and give it a width attribute of 25 and height attribute of 100. Also, give the rect x and y attributes each set to 0.

  *Resources:*

  **My solution**
  ```html
  <body>
    <script>
      const dataset = [12, 31, 22, 17, 25, 18, 29, 14, 9];

      const w = 500;
      const h = 100;

      const svg = d3.select("body")
                    .append("svg")
                    .attr("width", w)
                    .attr("height", h)
                    // Add your code below this line
                    .append("rect")
                    .attr("x", 0)
                    .attr("y", 0)
                    .attr("width", 25)
                    .attr("height", 100);           
                    // Add your code above this line
    </script>
  </body>
  ```
**Link(s) to work**

1. Started work on [Introduction to the Data Visualization with D3 Challenges](https://learn.freecodecamp.org/data-visualization/data-visualization-with-d3).

**Introduction to the Data Visualization with D3 Challenges**

 - [x] Learn About SVG in D3
 - [x] Display Shapes with SVG

All code is in GitHub [FCC_Challenges/DataVisualizationWithD3.md](https://github.com/Johnny2136/FCC-Projects/edit/master/FCC_Challenges/DataVisualizationWithD3.md).
