# css简介

+ ##  css

  + 实质是层叠样式表
  + 网页实际上时一个多层的结构，通过css可以分别给网页的每一层设置样式，最终我们能看到的只是网页的最上层。

+ ## 使用css来改变网页的样式的方式

  + 第一种方式

    + 内联样式：

      1. 在标签内部通过style属性来设置元素的样式

      2. 局限性

         + 使用内联样式的时候，只能对一个标签生效

         + 当需要修改网页样式的时候，要全部改一遍

         + 注意：开发的时候绝对不要使用内联样式

           ```html
           <p style="color:aquamarine">我是你爹</p>
           ```

           

  + 第二种方式（内部样式表）

    + 将样式编写到head标签中的style标签里，然后通过css的选择器来选中元素并为其设置各种样式，以至于修改样式时只需要修改一处即可全部应用

    + 局限：我们的内部样式只能对一个网页起作用，它里面的样式不能跨页面进行复用

      ```html
      <head>
          <meta charset="UTF-8">
          
          <style>
              p{
                  color:blueviolet;
                  font-size:xx-small;
                  /* 设置字体大小 */
              }
          </style>
      </head>
      ```

      

  + 第三种方式（外部样式表）

    + 可以将css样式编写到一个css的外部文件中，然后通过link标签来引入外部的css文件中

    + 使用此方法只需要使用的时候在想要使用此样式的网页的head标签中添加link标签，以此实现多网页复用

    + 此方法在实际开发中最频繁使用

      ```html
      <link rel="stylesheet" href="yangshi.css">
      <!--这是在HTML的head标签里需要写的-->
      ```

      ```css
      p{
          color :aquamarine;
          font-size: bisque;
      }
      /*这是在css文件中需要写的*/
      ```

      