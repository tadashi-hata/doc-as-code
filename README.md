# Markdoc Demo

This project was created based on [markdoc-starter](https://github.com/markdoc/markdoc-starter)

Markdoc is a Mardown based document format and a framework for content publishing. It was designed internally at Stripe to meet the needs of user-facing product documentation. Markdoc extends Mardown with a custom syntax for tags and annotations, providing a way to tailer content to individual users and introduce interactive elements.

[Getting Started](https://markdoc.io/docs/getting-started)

Key takeways:
- Under MIT License
- Must be attached as a dependency to a project (Read, NextJS and other js-based framewoks)
- Dynamic content on markdown files
- Can be extended and customized.
- Supports variable definitions and conditional statements
- Standard markdown has poor visual experience
- Its required to learn about how Markdoc works to improve the documentation layout.
- Users will need to set up an NextJS application environment to test how markdown files will be rendered.

## How Markdocs works
By design, Markdoc is not a full-blown templating language and does not allow mixing arbitrary code and content. It is, however, a fully declarative format that is machine-readable from top to bottom: it parses to a data structure that can be traversed to support powerful static analysis, validation, and programmatic content transformation.

The Markdoc renderer interprets custom tag and node definitions, transforming the document data structure into a tree of renderable nodes, which is finally converted into the desired output format. The Markdoc framework currently includes three renderers: an HTML string renderer, a static React renderer that transpiles a document to JavaScript code, and a dynamic React renderer that converts renderable tree nodes directly into a React elements.

Markdoc's React renderer makes it possible to use React components within Markdown content, supporting interactive features like tab switchers and collapsible sections. It is possible to implement custom renderers that introduce support for additional output formats and client frameworks.

---

# Run this project:
To run this project locally you just need to clone this repo and execute the following commands:

    npm install
    npm run dev