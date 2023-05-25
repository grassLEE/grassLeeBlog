# Lesser Known HTML Elements and Attributes  
Let's turn our attention to the language of the web, Hypertext Markup Language (HTML). But rather than bore you with the basics, let's look at some of the lesser known attributes... well, at least they were to me. 

## The Third List type
Despite popular belief, HTML has more than two types of lists: **&lt;ol&gt;** and **&lt;ul&gt;**. However, there is a third type reserved for **description lists** **&lt;dl&gt;&lt;/dl&gt;**.  

This element provides an excellent way of formatting longer content elements of similar type. 

A &lt;dl&gt;&lt;/dl&gt; functions in conjunction with two other elements: the &lt;dt&gt;&lt;/dt&gt;, which provides our **Description Topic**, and the &lt;dd&gt;&lt;/dd&gt;, which serves as our longer **Description Definition**. 

## Description List in Practice  
``` 
<dl class="discworld">
    <dt></dt>
    <dd>
    Here is our description text for example one.
    </dd>
    <dt>Example Two</dt>
    <dd>
    And here is some description text for example two.
    </dd>
</dl>
```
[The &lt;dl&gt;&lt;/dl&gt; Element in actiona]("file:///Users/grasslee/Desktop/my_projects/learn_html/index.html")  

## Application Examples:
- A glossery of similar terms, such as a recipe/cookbook.
- Metadata tags/descriptions
- Appendix content
- Embedded material to support longer content like articles

## Putting the Element in Pactice  
Of course, there are a range of important elements to use and consider when drafting longer text content, such as &lt;article&gt;, &lt;main&gt;, and our ever faithful &lt;p&gt; element. However, the &lt;dl&gt; elements are an excellent alternative for reference content that directly supports a main content entry like a blog post.

And remember, we can wrap the &lt;dl&gt; in a class name, allowing us to easily target the element (and associated content) with Cascading Style Sheets (CSS).

More on that later  
[Top](#lesser-known-html-elements-and-attributes) 