# CSS Floats:
- Floats are **used to float things left and right on any element** you want to and you **can wrap any text around it** and can also use **floats inside of container** but remember to apply **display:float-root;** to the container so the container can contain the full floated element and doesn't shrink based on the text content alone.


- **float:left;**
![float:left](image.png)
![when margin applied on p](image-1.png)
![when margin applied on p](image-2.png)


- **float:right;**
![float:right](image-3.png)

- **clear:both;**
![clear:both](image-4.png)


- .section {
<br>    background-color: bisque;
<br>    border: 1px solid #333;
<br>    padding: 1rem;
<br>}![wrap in section element](image-5.png)

    And, when shorten paragraph and remove div below it
        
Problem:
    ![problem: box come out from container contained](image-6.png)

Solution:
- Approach 01: **overflow: auto;**. It will get the container element all the way down and increase the container with respect to box. It is kind of old approach.

- Approach 02: **display:float-root;** recommended by MDN. It is considered current modern way to fix the problem


- In the past, floats were also used to create columns on the page. But, it is oldest approach and now we have different modern way to create columns like css grid, flexbox etc.

