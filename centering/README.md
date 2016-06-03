##Exercise 1 - Centering

##Description
The problem structure is present at [Centering Problem](https://jsbin.com/puvuma/1/edit?html,css,output)

Here we have two containers - a parent (with class content) and the child container (with class data). The aim of this exercise is to center to the child container inside the parent container and then center the text inside the child container.

Centering especially vertically centering has been difficult and previously different approaches have been used for centering of content. 
The list of such techniques can be found at [CSS Tricks](https://css-tricks.com/centering-css-complete-guide/). 
FlexBox solves this issue by providing easy options to center any element. 

 
##Solution
The solution can be found at [Centering Solution](https://jsbin.com/fiqipu/1/edit?html,css,output).

### Details
To center the child container first change the display for parent container to flex and then add the centering properties.
```css
.content {
    display: flex;
    align-items: center;
    justify-content: center;
}
```

Similarly, to center text inside child container we should set the display as flex add the centering properties to the child css class
```css
.data {
    display: flex;
    align-items: center;
    justify-content: center;
}
``` 

###Notes
* As seen above, child items of a flex box do not get the "display:flex" property automatically and it should be added if the items inside the child also need to be layed out using flexbox.
* Text directly contained in a flex container is wrapped in an anonymous flex item, hence the flex properties on the child container are able to impact the text inside.
