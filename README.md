# Book to Static Site

This script will export all chapters and pages within a given book to a folder
of basic HTML and image files which could act as a static site.

Once ran, you should be able to open `index.html` within the output folder to start browsing.

**This is a very simplistic single-script-file example of using the book, chapter and pages
API together**, the output lacks a lot of detail including styling and inter-content link transforming. 

This script is a slight modification of [this script](https://github.com/BookStackApp/api-scripts/tree/main/php-book-to-static-site) by [ssddanbrown](https://github.com/ssddanbrown)

## Requirements

- php ```~7.2+```
- curl
- BookStack API ```TOKEN_ID```
- BookStack API ```TOKEN_SECRET```
- Markdown CSS file. One can be found here [http://markdowncss.github.io/](http://markdowncss.github.io/)
- A URL Slug of the desierd book you wish to export. e.g. https://bookstack.example.com/books/**example-book**
- A directory where you wish the book to be saved

## Running

Download the script
```bash
curl https://raw.githubusercontent.com/bsncubed/bookstack-static-site/main/book-to-static.php > book-to-static.php
```

Export Variables
```bash
export BS_URL=https://bookstack.example.com # Set to be your BookStack base URL
export BS_TOKEN_ID=abc123 # Set to be your API token_id
export BS_TOKEN_SECRET=123abc # Set to be your API token_secret
export BS_CSS_FILE=style.css # Set to be the name of your CSS markdown file
```
Or, alternatively, you can modify the variables in the script manualy

Run the script
```bash
php book-to-static.php <book_url_slug> <output_dir>
```

#### An Example

```bash
# Export a book with URL slug of my_book to an "out" directory
php book-to-static.php example-book ./out
```
#### CSS
Move the CSS file to the Output Directory
