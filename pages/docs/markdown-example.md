# Testing markdocs
Random text here

> Info
> Whatever works for you, works for me too

| Testing | Table | 
|---------|-------|
| item    | tic tac |
| item    | foo |

--- 

## Testing markdoc features

`Inline code example `

--- 

```
    Code block
    example
```
            

## Testing markdoc Tags

This is using conditional features

{% if true %}

{% callout type="note" %}
Tags are composable!
{% /callout %}

{% else /%}

{% callout type="warning" %}
Tags aren't composable!
{% /callout %}

{% /if %}


Table using tags:
{% table %}
* Heading 1
* Heading 2
---
* Row 1 Cell 1
* Row 1 Cell 2
---
* Row 2 Cell 1
* Row 2 cell 2
{% /table %}

Table with rich content

{% table %}
* Foo
* Bar
* Baz
---
*
  ```
  puts "Some code here."
  ```
*
  {% list type="checkmark" %}
  * Bulleted list in table
  * Second item in bulleted list
  {% /list %}
* Text in a table
---
*
  A "loose" list with

  multiple line items
* Test 2
* Test 3
---
* Test 1
* A cell that spans two columns {% colspan=2 %}
{% /table %}


### Partial

Markdoc uses partials to reuse content across docs. The content is stored in a separate markdown file, and it's referenced from the file attribute in the partial tag, which includes the corresponding piece of content.

Here is an example of including the header.md file as a partial.


{% partial file="partial.md" /%}

---
