# Setting the HTML Table  

Tables are an excellent way to store tabular data, allowing for quick information retrieval.  HTML offers robust options for generating, and styling, tables. 

The **&lt;table&gt;&lt;/table&gt;** element constructs the basic architecture of our table. All our data content will need to be wrapped within those tags.

Additionally, there are two more required elements: **&lt;tr&gt;&lt;/tr&gt;**, which stands for our **table row** and **&lt;td&gt;&lt;/td&gt;**, which will serve as our **table data**. 

Our &lt;tr&gt; element will wrap each of our &lt;td&gt;(s), but let's see what it looks like in action.

### Example Syntax

```
<table>
    <tr>
        <td>First cell</td>
        <td>Second cell</td>
    </tr>
    <tr>
        <td>First cell of SECOND row</td>
        <td>Second cell... of SECOND row</td>
    </tr>
</table>
```

## Each Piece of the Table:
It can be a little tricky at first, but keep in mind that the &lt;td&gt; elements will extend the width of the row... not the length of the column. 

This basic markup will generate the architecture for our table. However, we can introduce a bit of styling (without the need for CSS) to make the data more readable with the **&lt;th&gt;&lt;/th&gt;**, which serves as our **table header** element. 

The &lt;th&gt; element will mark our top level cells, making them simpler to identify and read. This improved readability is achieved through the element's prepackaged styling, including bold/centered text.

### Example Syntax for &lt;th&gt; Element
```
<table>
    <tr>
        <th>Park Name</th>
        <td>Heartwell</td>
        <td>El Dorado</td>
    </tr>
    <tr>
        <th>Location</th>
        <td>Long Beach, CA</td>
        <td>Long Beach, CA</td>
    </tr>
    <tr>
        <th>Distance</th>
        <td>3.4 miles</td>
        <td>7.1 miles</td>
    </tr>
</table>
```
Now we have clear header indicators for each of our rows, providing a clean, well formatted-- excellent for those utilizing Screan Readers and other such devices. 
  
[Top](#each-piece-of-the-table)