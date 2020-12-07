# EE290C Spring 2021 Course Site 

## Editing 

Editing the course site is performed through git. 
Each git-push is published by GitHub Pages after a short HTML build process. (Usually one to a few minutes.)

Most content is written in [Markdown](https://guides.github.com/features/mastering-markdown/) 
and compiled into HTML on GitHub's servers. Examples of most common elements are included 
in the existing home page, as well as the help-excerpt below. 

The course home page is (index.md)[index.md]. Thus far essentially all content is in the home-page, 
save for attached files such as PDFs and images. 

## Attachments, Files & Assets 

The GitHub-stack seems to prefer any such files be kept in the (assets/)[./assets] directory. 
Example PDF attachment: [demo.pdf](assets/demo.pdf). 

## Styling 

Our general intent is to perform as little custom style-izing as we can. 
The site template is courtesty the [Pages Cayman theme](https://github.com/pages-themes/cayman). 
A few tweaks are applied, particularly to drop a few tropical colors 
and replace them with some more Berkeley-ish ones. 

If you do really want to much with the site style, 
it's largely done with the SASS in [assets/css](./assets/css). 

## Running Locally 

GitHub provides [a terrific guide](https://docs.github.com/en/free-pro-team@latest/github/working-with-github-pages/testing-your-github-pages-site-locally-with-jekyll) 
on how to run local preview-versions of our site before publishing them. 
This will generally require installing some Ruby packages, and if necessary Ruby itself. 


---

## (A GitHub Pages Help Excerpt)

You can use the editor on GitHub to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/dan-fritchman/Sp21/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.

