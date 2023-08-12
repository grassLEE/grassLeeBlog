# Getting Started with Technical Writing

I'm sure you are well aware of the amazing opportunities available through technical writing, so I won't spend a lot of time going over this ever-expanding field. However, if you would like to learn a bit more about potential roles, the purpose of technical documents, and other helpful tips, check out [id rather be writing](https://idratherbewriting.com/) for a rich repository of information.  

Instead, I would like to talk about the tools technical writers use to draft new content, edit/revise, and produce final deliverables.

## Tools:

Every organization will utilize a range of tools to effectively document their content. These tools can span from common what you see is what you get (WYSIWYG) programs, like Microsoft Word or Google Docs, to more robust platforms, such as [iA Writer](https://ia.net/writer) or [OxygenXML](https://www.oxygenxml.com/).  

These are but a few examples from dozens, if not hundreds, of widely used options. Of course, it's impossible to become a power-user in all of them, but a working knowledge of their basic functions is often expected.  

It's a fair assumption that most people are familiar with the common WYSIWYG platforms, but if this is not the case, log into Google (or create an account, they are FREE!), and follow this quick-start [tutorial](https://support.google.com/docs/answer/7068618?hl=en&co=GENIE.Platform%3DDesktop&oco=0). Make sure to familiarize yourself with the basic commands to properly format, save, and share your content. 

The last two entries (iA Writer and OxygenXML) demonstrate some of the more advanced principles of technical writing, i.e., **structured writing**. These tools leverage a lightweight markup language, as in the case with iA Writer, and modular, component-based writing, found with OxygenXML.  

We'll spend a bit more time with that concept and its far-reaching potential in a later article, but for now let's focus on something more tangible and easier to pick up.

## Learning Markdown:

There are several great resources available for learning everything you need to know to start writing with Markdown. A couple of my favorites include this [**free tutorial**](https://www.markdowntutorial.com/lesson/1/), and the textbook, *The Markdown Guide* available on [**Amazon**](https://www.amazon.com/Markdown-Guide-Matt-Cone-ebook/dp/B07G7JB641/ref=sr_1_1?crid=V3PPDG97Z61J&keywords=markdown+guide&qid=1678321060&sprefix=markdown+guid%2Caps%2C183&sr=8-1). 

But I'd like to spend a little bit of time demonstrating some lesser-known syntax and functional capabilities available through Markdown.

### Linking to sections within a document: 
Of course, both above resources will go into great detail concerning hyperlinks, including inline and reference options. 

However, what about navigation links for text sections within a Markdown file?

Markdown has us covered. Take a look at this quick code snippet:

~~~ 
[Top](#getting-started-with-technical-writing)
~~~

This output leverages the normal *linking* syntax, but with a few key differences. To start, the parens ( ) begin with a single hash symbol (#). The hash symbol allows us to directly link back with a previous heading section. Our example above matches the first heading value, i.e. the title of this post. Next, we follow the hash symbol with the value of the heading (in our case, once again, the title of this blog post).

However, there is a notable exception to keep in mind. The value inside the parenthesis must be lowercase, separated by a dash (-).

Remember, these embedded links aren't exclusive to the introduction of our files. They can be utilized for any section of your Markdown file that's notated with a heading tag

~~~
* h1
** h2
*** h3 
~~~

Depending on the text editor you select, the built-in function will likely suggest valid endpoints based on the current headings. The single ( # ) will be used at the beginning of each heading, regardless of size... At least for Github flavored Markdown.

[Linking Section](#linking-to-sections-within-a-document)

### Future Posts: The Flavors of Markdown
In our next post we will look into some of the more popular Markdown flavors, which offer novel functionality, such as improved list/table creation. 

### Wrap-Up: 
There are seemingly a limitless number of tools, platforms, text editors, and resources out there to help you. Don't get bogged down with the number of choices, experiment with a range of solutions, and find what works best for you.

And consider starting your technical writer journey out with Markdown, you'll find it is much easier to get started than you might think... and there is seemingly no limits to this tool's potential. 

<img src="https://raw.githubusercontent.com/grassLEE/grassleeblog/main/images/markdown.jpg" width="25%" height="25%">

[Top](#getting-started-with-technical-writing)
