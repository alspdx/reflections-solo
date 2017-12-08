# 

####  _2017_

#### by **Adam Smith**

## Two-Day Project Thoughts & Feedback:

My partner and I spent more time than we needed to building out two separate HTML layouts, as our previous experience with the term "wire-framing" in the lessons had us building layouts as opposed to sketching out the designs. We did end up sketching a third design

When we got to planning and building the final layout we were originally working with Hugo Giraudel's "7-1" architecture. We found another [article with a "5-1" architecture](http://matthewelsom.com/blog/simple-scss-playbook.html) that seemed more intuitive given the smaller size of our webpage.

Either architecture we were working in, it was tricky to know which file we should be putting certain pieces in. Some of that was intuitive, like putting _mixins_ in the _mixins_ file and _variables_ in the _variables_ file. Other styles were harder to place. Should we write everything about the _hero_ under the _hero_ file? What about a _component_ used only in the _hero_ section? Should I make a new individual _variable_ for the background-color of the _component_ in the _variables_ file who's value is _$accent-color_? Or should I just write the property _background-color: $accent-color_ in the component's file? Does it make sense to write a _variable_ for every little thing?

What I took away from the project was that there are a lot of different approaches. Each project is different and I'll have to be flexible in how I work when I'm on a team with other developers and designers.

## Sass Elements:

| Term | Description | Implementation |
| -- |:--:| --|
| Variables | Variables are names used to store and recall data in a program. Any Sass data type can be stored in a variable and used wherever that variable name is called throughout the program. | We used variables whenever possible to manage colors, margins, and other style values throughout the page. All of the variables are declared in one location which makes it easier to make global style changes. |
| Extend | Extend is used to share the properties of one selector with another selector. The selector where @extend is called can have it's own unique styles in addition to the styles of the extended selector. | We used extends where we wanted to apply the same set of properties to one element that another element already has. Instead of calling both selectors together on one set of brackets, we call @extend in the selectors own set of brackets so we can apply unique properties in addition to the extended properties. |
| Mixins | Mixins are a way to write a block of code to be reused throughout the page. A mixin can use parameters to pass data to the properties in each instance the mixin is called. | We used mixins when we were adjusting the same properties across multiple selectors with different data values. Data was passed through the parameter of the mixin, much like passing an argument in a JavaScript function, to set unique styles each time the mixin was called. |
| Functions | Sass functions are a way to repeat a block of code that accepts arguments and returns a specific value. | Although we didn't end up using functions, we found that the use of functions in Sass are similar to mixins and are sometimes confused with one another. We _would_ use functions where data needs to be processed and one specific value is expected to be returned, as in a math function or concatenation of a string. |
| Nesting | Nesting is the practice of calling selectors inside the brackets another selector. This is used to affect descendants of the original parent element selected. | We used nesting to write rules that affect specific elements or groups of elements inside a specific container. |
| Partials | Partials are Sass files with blocks of code for a specific element, function, category, or role that will be compiled with other partials to make a complete stylesheet. | We use partials to create and organize separate files for variables, colors, layout, mixins, functions, reset/normalize, third-party libraries, and any other unique categories. Those files were then imported into a central file that was being watched and processed as a complete CSS output by the Sass program to be used as the main stylesheet. |
| Import | Import is a way to compile partials together. One file is specifically dedicated to call partials to be imported and compiled by Sass. This can be done in a few different ways, but common practice is to have one import file in each sub-directory in the Sass file structure, then call each of those import files into a single file in the Sass root directory. | We used an import file in each directory to compile all of the partials from that location, then imported each of those files into the main Sass directory to be compiled into a complete CSS stylesheet for the browser to read and apply to the page. |
| Interpolation | Interpolation (_#{$variable}_) is used to replace a part of an expression or a string where use of _$variable_ is not applicable. | We used interpolation whenever we used a Sass variable in the CSS calc() function and when we wrote a loop to build a grid system with unique selector names for each column width and breakpoint size. |

## Moving Forward:

I think today will go a lot quicker since I have a sketch of the layout I'll be working on. I'll continue to not use a framework, I'm really enjoying building my own grid with a loop and setting my own styles. It's harder for me to style a page working in a pair, I like to move quickly with ideas and it can be tough to stop and talk out those ideas. I'm also much more likely to make regular commits on my own than I am working in a pair. I still haven't nailed down a topic for the page today so I'm going to start with getting a basic layout and go from there. After the layout I'll work on styling components and working on solidifying a topic.

## Setup

Visit the webpage [here]().

Alternately you may [Clone this repository]().
  1. Click on the link above.
  2. Click the green button marked **Clone or download**.
  3. Click **Download ZIP**.
  4. Unzip file.
  5. Open index.html in Chrome or another web browser.

## License

Copyright (c) 2017, Adam Smith

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
