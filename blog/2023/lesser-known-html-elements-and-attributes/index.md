# Lesser Known HTML Elements and Attributes  
Let's turn our attention to the language of the web, Hypertext Markup Language (HTML). But rather than bore you with the basics, let's look at some of the lesser known attributes... well, at least they were to me. 

## The Third List type
Despite popular belief, HTML has more than two types of lists: **&lt;ol&gt;** and **&lt;ul&gt;**. However, there is a third type reserved for **description lists** **&lt;dl&gt;&lt;/dl&gt;**.  

This element provides an excellent way of formatting longer content elements of similar type. 

A &lt;dl&gt;&lt;/dl&gt; functions in conjunction with two other elements: the &lt;dt&gt;&lt;/dt&gt;, which provides our **Description Topic**, and the &lt;dd&gt;&lt;/dd&gt;, which serves as our longer **Description Definition**. 

## Description List in Practice  
``` 
<dl>
    <dt>Example One</dt>
    <dd>
    Here is our description text for example one.
    </dd>
    <dt>Example Two</dt>
    <dd>
    And here is some description text for example two.
    </dd>
</dl>
```
[image]()



### Application Examples:
- A glossery of similar terms.
- 