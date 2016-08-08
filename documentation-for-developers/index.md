# Livingdocs quick start

## In a nutshell

Livingdocs is a SaaS offering users of the publishing industry a seamless WYSIWYG editor to create and publish articles. Livingdocs core feature is a single access gate where to write content once and publish it everywhere.

The Livingdocs software stack spans over 4 repositories:

### The editor
The user creates an article in the **editor**. The **editor** is rendering the article live, as the end reader would see it, while the user makes changes to it.

The **editor**, under the wood, manipulates an object called a *Livingdoc* which holds the content and the form of the article.

The **editor** is an Angular web application.

### The framework
The **framework** is a *Livingdoc* rendering engine which renders a *Livingdoc* to HTML.

In the **editor**, the live rendering of the article is done by the **framework**.

It is written as a Javascript library dependency.

### The server
Each time a modification is made to the article, in the **editor**, the *Livingdoc* object is saved to the **server**.

Once done with the creation of the article, the user can make it available to the readers, a process named publishing. From now, when asked for a published article, the **server** retrieves the corresponding *Livingdoc* object from the database and render it with the **framework** as an HTML web page.

The **framework** is used both in the editor and in the **server**.

The **server** is a node.js application.

### The design
A *Livingdoc* is made of components: titles, paragraphs, videos, images... the list of the available components and their styles (as in CSS) is defined in an object called a **design**.

The **design** is used by the **framework** to style the HTML rendition of a *Livingdoc*, once again, both in the **editor** and the **server**.

The **editor** shows a set of available components, defined in the **design**, for the user to compose articles with.

A **design** is a set of fully customizable components that the user can generate, through dedicated tooling, as a JSON object.

## Guides for

### a developer working on
- [x] [the editor only](./guides/developer/editor-only.md)
- [ ] [the editor and the server](./guides/developer/editor-and-server.md)
- [ ] [the editor, the server and the framework](./guides/developer/editor-server-and-framework.md)

### a designer
- [ ] [design only](./guides/designer/design-only.md)




