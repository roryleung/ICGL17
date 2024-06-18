#ICGL17 conference website

This is the code for the conference website for the [17th International Conference on Greek Linguistics](https://http://icgl17.mmll.cam.ac.uk) (ICGL17) -- based on the code for [IVACS 2024](https://github.com/cainesap/ivacs2024).

It's currently using the [Minimal Mistakes Jekyll Theme](https://mmistakes.github.io/minimal-mistakes/).

# Table of contents

* [Forking for a New Conference](#forking-for-a-new-conference)
   * [Important Files](#important-files)
   * [Domain Setup](#domain-setup)
* [License](#license)


# Forking for a New Conference

For a new conferences, you may either set up a repository from scratch by forking the original [Minimal Mistakes repository](https://mmistakes.github.io/minimal-mistakes/) or you may fork this repository directly. The latter may be easiest since all of the changes that are required for more complex things like the web-based schedule to work are already there. However, the disadvantage of forking this repository is that the version of the Minimal Mistakes theme will be out of date and you might miss out on bugfixes and new features. 

**IMPORTANT**: Note also that if you fork this repository, you will get all of the existing conference's pages and blog posts and schedule and other content. Therefore, it is up to you to modify/temporarily remove that content before you make your website public so that your new domain is not indexed by search engines with old content. It might be best to rename the `gh-pages` branch so that the website for the new conference does not get built with content from the old conference. You can rename the branch back to `gh-pages` once you have made sufficient changes locally to remove/modify the old conference content.


## Important Files

If you fork this repository, the following files are the ones to pay attention to in order to create content for the website:

- `_pages/xxx.md` : The markdown files contain the main contents of the different web pages of the website. Please note that
  once you fork, you would need to move the already existing .md files out into a different folder so that old pages do not
  get rendered into the new website.

- `downloads/` : Contains files that can be downloaded from the website.

- `_sass/minimal-mistakes/*.scss` : SASS files that control the look and the feel of the website. The file `_program.scss` is not part of the them and controls the look and feel of the web schedule page.

- `_data/navigation.xml` : YAML file that contains the links in the masthead at the top of the website and also links in the various sidebars. 

- `_data/authors.yml` : YAML file that contains the information about the various blog post authors, e.g., Program Chairs, Diversity Chairs, General Chair. This file _must_ be updated with the right names and links.

- `_config.yml` : YAML file that contains meta-information about the website that should be set properly for a new conference. Details are given in the comments in the file. You must edit this file properly before making the website public.

- `_posts/*.md` : If you are going to have a blog, this where the blog posts live and are named `YYYY-MM-DD-title.md`. Same as the
  files under `_pages`, you should move out already existing files from this folder to prevent them from getting rendered.

- `_includes/masthead.html`: A block of Javascript code is appended at the end of the file such that the navigation menu can be changed according to users' langauge choice (Greek/English). You should remove it if you are not planning for your site to be multilingual. 

- `CNAME` : You should delete this file since this contains the old external domain from the older conference. This file will be
  automatically re-generated when you add the new external domain for the new conference. If you do not remove this file, you will
  get a page build warning from GitHub.

## Domain Setup

In my case the underlying GitHub Pages URL is https://roryleung.github.io/ICGL17/

I have a university-based domain (https://icgl17.mmll.cam.ac.uk/) set up and changed the repository settings to point the CNAME to 'roryleung.github.io', and those for the domain as described here: https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site


## License

The MIT License (MIT)

Copyright (c) 2018 Association for Computational Linguistics.

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
