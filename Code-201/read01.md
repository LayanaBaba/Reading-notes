HTML describes the structure of pages, the HTML code is made up of characters that live inside angled brackets, tags come in pairs, the opening tag and closing tag.
# Examples:
* < p > opening tag
* </ p > closing tag.

* < head >
This contains information about the page.
</ head > 

* < title >
The contents of the < title > element are either shown in the top of the browser.
</ title >

* < body > 
Anything written between the < body > tags will appear in the main browser window.
</ body >

To tell the browser which version of HTML the page is using, each web page should begin with a DOCTYPE declaration.
- <! DOCTYPE html> HTML5
- <! DOCTYPE html PUBLIC
   "-//W3C//DTD HTML 4.01 Transitional//EN"
   "http://www.w3.org/TR/html4/loose.dtd">   HTML4


<! --  -- > this characters used to add a comment to a code that will not be visible in the user's browser.
ID attribute is a global attribute, and allows you to style an element differently.
Class attribute can be used by multiple HTML elements.
Block elements: < h1 >,< p >,< ul >, and < li >.
Inline elements: < a >, < b >, and < img >.

## Grouping text and elements in a block:
* < div >: The < div > element allows you to group a set of elements together in one block-level box.
* < span >: The < span > contain a section of text where there is no other suitable element to differentiate it from its surrounding text and contain a number of inline elements.
* < inframe >: There are few attributes that you will need to know to use it: 
  - src : The src attribute specifies the URL of the page.
  - height :  The height attribute specifies the height of the iframe in pixels.
  - width : The width attribute specifies the width of the iframe in pixels.
* Escape characters are used to include special characters in your pages such as <,>,&,',and ".

### HTML5 introduces a new set of elements that allow you to divide up the parts of a page.
* < header > and < footer >: The main header or footer that appears at the top or bottom of every page on the site.
* Navigation: The < nav > element is used to contain the major navigational blocks on the site such as the primary site navigation.
* Article: The < article > element acts as a container for any section of a page.
* Asides: When the < aside > element is used inside an < article > element, it should contain information that is related to the article but not essential to its overall meaning, and when the < aside > element is used outside of an < article > element, it acts as a container for content that is related to the entire page.
* Sections: The < section > element groups related content together, and typically each section would have its own heading.

It's important to know who is the site for, why people visit your website, what your visitors are trying to achieve, what information your visitors need, and how often people will visit your site. Also, site maps allow you to plan the structure of a site.

#### JavaScript makes web pages more interactive. To write a Script you need to:
- Define the goal.
- Design the script.
- Code each step.

##### How a browser sees a web page:
- Receive a page as HTML code.
- Create a model of the page and store it in memory.
- Use a rendering engine to show the page on screen.

How HTML, CSS, and JavaScript fit together: The HTML gives the page structure and adds semantics (.html files). The CSS enhances the HTML page with rules that state how the HTML content is presented. JavaScript makes the web more interactive.