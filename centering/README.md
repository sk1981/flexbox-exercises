#Exercise - Centering

##Description
Centering especially vertically centering has been difficult and previously different approaches have been used for centering of content. 
The list of such techniques can be found at [CSS Tricks](https://css-tricks.com/centering-css-complete-guide/). 
FlexBox solves this issue by providing easy options to center any element. 

The problem structure is present at [Centering Problem](http://jsbin.com/citulux/1/edit?html,css,output)
Here we have two containers - a parent (with class ***content***) and the child container (with class ***data***).

The aim of this exercise is to center to the child container inside the parent container and then center the text inside the child container.

The final page should resemble :-
![Centering Solution](CenteringImage.png)

##Solution
The solution can be found at [Centering Solution](http://jsbin.com/vaduli/1/edit?html,css,output).

#### Details
To center the child container first, change the display for parent container to flex and then add the centering properties.
```css
.content {
    display: flex;
    align-items: center;
    justify-content: center;
}
```

Similarly, to center text inside child container we should set the display as flex and add the centering properties to the child css class. 
Also, ensure that text inside the container wraps so that it does not overflows. 
```css
.data {
    flex-wrap:wrap;
    display: flex;
    align-items: center;
    justify-content: center;
}
``` 

***Hello*** and ***user*** still appear to be misaligned due to different sizes. Let's align them by their baseline.
```css
.data {
    align-items: baseline;  
} 
``` 

####Notes
* As seen above, child items of a flex box do not get the "display:flex" property automatically and it should be added if the items inside the child also need to be layed out using flexbox.
* Text directly contained in a flex container like "***user***" in the above example, is wrapped in an anonymous flex item.
Hence the adding flex properties on the child container impact the text inside.
* From above example difference between ***align-items*** and ***align-content*** should be clear.
***align-content*** aligns the flex lines, while align-items aligns the items inside each flex-line.
