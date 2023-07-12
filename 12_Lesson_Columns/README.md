# CSS Columns:
- to create columns, need to use declaration:
**column-count: 4;**, it will create 4 columns and always will be 4 columns even though we increase or decrease screen size
![keep same columns even screen size change](image.png)

- But, if we want to manage columns numbers according to screen size, we need to set the width of column like **column-width:250px**
![manage no of columns according to screen size](image-1.png)

- create column divider/separator **column-rule: 3px solid #333**. Divider will not be shown when device size changes to one column.
![column divider](image-2.png)

- spacing between columnn: **column-gap: 3rem**
![spacing between columns](image-3.png)

## Problem:
- Spacing issue between columns like first column has top and bottom margin but second column has only bottom margin etc.

## Solution: 
- use **margin-top: 0;** to **.columns p {}** and now the margin top of each column is removed but spacing between columns is still there. So, that is **Margin Collapsing**

- **Margin Collapsing**: So, it is not going to double up the margin between the second and the third paragraph by just having **bottom margin on 1st column** and and the **top margin on the 2nd one**
![margin collapsing](image-4.png)

## Problem when add h1 between paragraphs:
- add new topic **h1**
![initially](image-5.png)
when resize the screen
![after resizing screen](image-6.png)


## Solution:
- when add **break-inside:avoid;** to h1
![after adding break-inside:avoid](image-7.png)


## Problem:
- when add property **break-before: column;**, forces to column break, to keep h1 on the top of column instead of bottom of the column when screen size changes. But, it will hightlight a problem: it will go down to three columns when screen size change to smaller **of one column** as shown below
![before one column](image-9.png)
![after resizing to one column](image-8.png)

## Solution:
- so, try to avoid **break-inside:column; property** if you know to shrink screen size. But, **break-inside: avoid;** will avoid h1 from splitting into more than one column


## Resources:
![unicode character table site](image-10.png)

1. Unicode Character Table (unicode.table.com/)
- It let us look other character like html entities, unicode characters and there are different ways to provide those different characters in our project by pasting those codes and in response we get those characters.

- creating quote: use html code and apply css
![quote character html code](image-11.png)
![quote after applying css](image-12.png)

## Problem:
- we have top margin is 0. so let's add top margin to quote **marign-top:2rem;**, but no change in output due to specificity problem
![specificity problem](image-13.png)

## Solution:
**.columns .quote** and then apply **margin-top:2rem**
![solution](image-14.png)
![output](image-15.png)

## Problem:
- when we resize the screen size, author name breaks to different lines
![problem with author name](image-16.png)

## Solution:
- wrap author name into **<span>**, add class **nowrap** and then apply css **white-space:nowrap**. And, now author name will always be on new line rather than breaking-up name words.
![author name on new line](image-17.png)