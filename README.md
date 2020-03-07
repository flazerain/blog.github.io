pytorch 不同版本安装

pip3 install torch==1.3.1+cu100 torchvision==0.4.2+cu100 -f https://download.pytorch.org/whl/torch_stable.html

Cmake

###----------------add pytorch c++ header

execute_process (COMMAND python -c "import torch;print(torch.__file__[:torch.__file__.find('torch')]+'torch')"
        OUTPUT_VARIABLE PYTHON_SITE_PACKAGES OUTPUT_STRIP_TRAILING_WHITESPACE)
MESSAGE( STATUS "output = ${PYTHON_SITE_PACKAGES},${OUTPUT_STRIP_TRAILING_WHITESPACE}")

#find_package(Python 3 REQUIRED COMPONENTS Interpreter Development NumPy)
##

include_directories("${PYTHON_SITE_PACKAGES}/include")
include_directories("${PYTHON_SITE_PACKAGES}/include/torch/csrc/api/include")
include_directories("${PYTHON_SITE_PACKAGES}/include/TH")
include_directories("${PYTHON_SITE_PACKAGES}/include/THC")




## Welcome to GitHub Pages

You can use the [editor on GitHub](https://github.com/flazerain/blog.github.io/edit/master/README.md) to maintain and preview the content for your website in Markdown files.

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

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/flazerain/blog.github.io/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
