# Book

Are you working on a new book? Do you want to share it with the world while you create it, allowing everyone to read the latest version? When you're done, do you want to publish it via a markdown-to-ebook service like [LeanPub.com](https://leanpub.com/) and/or send the same output to a drop-ship print service for hardcover or paperback books like [Lulu.com](https://www.lulu.com/)?

If so, you've come to the right place!


> When it comes to books, don't use JekyllFaces widgets in your markdown. For example, favor the typical markdown way of inserting images into your text over the JekyllFaces image widget.
> 
> If your markdown is clean and standardized, it will be easier to reuse content (such as images and gists) both on the site and in your book.
> 
> Use: _!&lsqb;Alt text&rsqb;(/image/path/photo.png)_
> 
> Not: _{% include image.widget file="foo.png" %}_


## Usage

Adding a book is as simple as adding a new folder with your markdown files, and a `book.txt` file that contains the order in which you wish them to appear. This module favors convention over configuration.

```text
docs/
 ├─ books/
 │   ├─ my-novel/
 │   │   ├─ images/
 │   │   │   ├─ photo1.jpg
 │   │   │   └─ photo2.jpg
 │   │   ├─ book.txt
 │   │   ├─ sample.txt
 │   │   ├─ chapter01.md
 │   │   ├─ chapter02.md
 │   │   └─ chapter03.md
 │   ├─ my-tech-book/
 │   │   ├─ images/
 │   │   │   ├─ diagram1.png
 │   │   │   └─ diagram2.png
 │   │   ├─ book.txt
 │   │   ├─ sample.txt
 │   │   ├─ chapter01.md
 │   │   ├─ chapter02.md
 │   │   └─ chapter03.md
```

This structure is based heavily on the [LeanPub](https://leanpub.com/) folder structure. The content you create here should be a drop-in, copy-and-paste for LeanPub's source files.

The `book.txt` and `sample.txt` files define which chapters will be included, as well as the order in which they will appear.

>  **NOTE:** The `book.txt` and `sample.txt` files can be crafted by hand, or automatically generated.
> 
> If automatic generation is configured, `books.txt` and `sample.txt` will include all markdown files (sorted by filename), and `sample.txt` will contain only those files that have `.sample.` in their name.
> 
> For example:
> 
> ```
>    010-a-new-day.sample.md
>    020-the-brevity-of-life.md
>    030-hellish-maelstrom.md
>    040-thats-what-she-said.sample.md
> ```

### Configuration Options

Blah, blah, blah ...