##Exercise - Sticky Footer

##Description
Creating a sticky footer has always been a tricky task. 
Flexbox provides an elegant solution to this problem.

Problem structure is present at : [Sticky Footer Problem](http://jsbin.com/gesaqo/1/edit?html,css,output)
Here we have the structure of a simple site with a header element, some site content indicated by ***site-content*** class and a footer indicated by ***footer*** element.
The ***body*** element which represent the full site is given a class ***site***.

Aim of this exercise is to create a sticky footer which :-
* Sticks to bottom of the page when the site content is less than height of the page. 
* Comes immediately after the site content if it's height is more than the height of the page.

The page also contains a checkbox to expand the site content so that it's easy to reproduce the scenario where site content is more than the page height.

##Solution
The solution can be found at [Sticky Footer Solution](http://jsbin.com/memokit/1/edit?html,css,output).

#### Details

Fix the minimum height of the site to be full viewport height so that footer can appear at the bottom of page. 
Change display of the site to ***flex*** and the direction to ***column*** so that we can align content along the height of the page. 
```css
.site {
    display: flex;
    min-height: 100vh;
    flex-direction: column;
}
```

Add flex-grow to site content so that it fills up to take the available space. 
```css
.site-content {
    flex: 1;
}
```

#### Notes
* We have used the flex shortcut ***flex: 1*** which means flex-grow is 1 (a single unitless value corresponds to flex-grow) 
