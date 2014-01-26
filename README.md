YARGS: Yet Another Responsive Grid System
=========================================

*YARGS is a custom responsive grid system I developed for myself.*

  - YARGS has been calculated using the [CSSWizardry fluid grids] repo
  - Instead of using margin-right on every grid, I used left and right padding on each grid element.
  - The base type size has been set using [Type Scale], which was inspired from Tim Brown's [Modular Scale] calculator.

Version
----

0.1

Crunching Numbers
-----------
* **Base font-size** - 16px
* **Scale** - 1.618
* **Gutter width** - 20px
* **Number of columns (n)** - 12
* **Column width** - 80px
* **Total width** - 1200px
      Total width = Total columns * (Column width + Gutter width)
* **Fluid gutter width** - 0.8335%
      Fluid gutter width = ((Gutter width / Total Width) * 100 ) / 2
* **Actual column width** - 12%
      Actual column width = [ { (n * Column width)+(n * Gutter width) - Gutter width} / 2 ] * 100
    
Installation
--------------
Download and include the [grid.css] file into your project folder silly! ;)

##### Some useful info

* The mobile <code>.small</code> grids start from 600px
* The tablet <code>.medium</code> grids start from 940px

How to use it
--------------
The grid can be added in any sequence as long as it adds up to 12.

For example: In the following case, 4 + 4 + 4 = 12

     <div class="grid-wrapper">
        <div class="grid grid-4">Content</div>
        <div class="grid grid-4">Content</div>
        <div class="grid grid-4">Content</div>
     </div>

In order to make it realign for tablet screens.

     <div class="grid-wrapper">
        <div class="grid medium grid-4">Content</div>
        <div class="grid medium grid-4">Content</div>
        <div class="grid medium grid-4">Content</div>
     </div>

In order to make it realign for mobile and tablet screens.

     <div class="grid-wrapper">
        <div class="grid medium small grid-4">Content</div>
        <div class="grid medium small grid-4">Content</div>
        <div class="grid medium small grid-4">Content</div>
     </div>

License
----

[MIT]


**P.S.**
* This code was written at one go after a little bit of tinkering around with typography and grid systems. So, it might not be as robust as other grid frameworks.
* It still might have bugs/flaws I may not have addressed yet. If you sir, have the time, please consider helping to tidy it up and making it a little bit more robust and lightweight than other grid frameworks.
* I think there are more use cases that can be addressed with the <code>.medium</code> grids and the documentation can be improved a little bit too.

[Modular Scale]:http://modularscale.com/
[Type Scale]:http://type-scale.com/
[CSSWizardry fluid grids]:https://github.com/csswizardry/fluid-grids/
[grid.css]:http://github.com/maxxon15/yargs/
[MIT]:http://opensource.org/licenses/MIT