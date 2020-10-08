# Class 04

## Navigation ##
 - [class 01](class-01.md)
 - [class 02](class-02.md)
 - [class 03](class-03.md) 
 - [class 04](class-04.md)
 - [class 05](class-05.md)
 - [class 06](class-06.md)
 - [class 07](class-07.md)
 - [class 08](class-08.md)
 - [class 09](class-09.md) 
 - [class 10](class-10.md)
 - [class 11](class-11.md)
 - [class 12](class-12.md)
 - [class 13](class-13.md)
 - [class 14a](class-14a.md)
 - [class 14b](class-14b.md)


# Read: 04 - Responsive Web Design and Regular Expressions #

# Bookmark/Skim
[RegExr](https://regexr.com/) - Pay particular attention to the cheatsheet
[Regex](https://medium.com/factory-mind/regex-tutorial-a-simple-cheatsheet-by-examples-649dc1c3f285) Tutorial
[Regex 101](https://regex101.com/)
[CSS Grid Reference](https://css-tricks.com/snippets/css/complete-guide-grid/)
[Responsive design with CSS Grid](https://medium.com/samsung-internet-dev/common-responsive-layouts-with-css-grid-and-some-without-245a862f48df)

Grid Garden

typing out both grid-column and grid-row is too much for you, there's yet another shorthand for that. grid-area accepts four values separated by slashes: grid-row-start, grid-column-start, grid-row-end, followed by grid-column-end.

One example of this would be grid-area: 1 / 1 / 3 / 6;.

#garden {
  display: grid;
  grid-template-columns: 20% 20% 20% 20% 20%;
  grid-template-rows: 20% 20% 20% 20% 20%;
}

#water-1 {
  grid-area: 1 / 4 / 6 / 5;
}

#water-2 {
grid-area: 2/3/5/6;
}


NPM = Node Package Manager

![GridGarden](images/Screenshot (880).png)

