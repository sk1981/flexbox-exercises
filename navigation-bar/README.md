##Exercise - Navigation Bar

##Description
Flex box allows us to easily have multiple elements in a row with required spacing and alignment.
This helps us in easily creating a navigation bar with a search field.

Problem structure is present at : [Navigation Bar Problem](http://jsbin.com/pujafe/1/edit?html,css,output)
Here we have the navigation bar indicated by the ***nav*** element and the navigation elements are present as unordered list.
The last navigation element is a search box with ***search*** text and icons.

Aim of this exercise is to create the navigation bar using css so that:-
* All navigation elements including the search box elements are vertically centered.
* Horizontal white space is distributed equally inside the navigation bar.
* Icons after the search element should appended to the search text.

##Solution
The solution can be found at [Navigation Bar Solution](https://jsbin.com/qedohil/2/edit?html,css,output).

#### Details

Make the list items center aligned and set the justify-content property to space-between to distribute space between the navigation elements. 
```css
nav > ul {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
```

The icons and text inside the search box are still not aligned so we need to make the search box also a flex container.
```css
nav .search {
  display:flex;
}
```

The ***search text*** is still misaligned as the we are using default align-items which is ***stretch***, to ensure that the search elements are stretched to take the full height. 
To ensure that the search text is aligned in the center we can user align-self property.
```css
nav .search-title {
  align-self: center;
  padding-right: 5px;
}
```
The cancel icon 'x' box is stretched full but the icon itself is not aligned within that box, hence we need to align it also centrally.
```css
nav .fa-times.search-icon {
  display:flex;
  align-items: center;
}
```

#### Notes
* We used space-between for the navigation element instead of space-around as we wanted the space to be distributed inside the navigation elements.
Space between would have distributed it on the edges of the navigation elements, which we didn't wanted.
* We had to add a padding between text and the input box as the segment-break collapsing rules are not relevant for "flex" display. [[1](https://www.w3.org/TR/css-text-3/#white-space-rules)] 
* We had to create a new flex container to centrally align the cancel icon 'x' because the actual content in font-awesome is displayed via a psuedo element. 
Also, this shows that we can apply flex properties on pseudo elements also.   
