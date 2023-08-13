# Web resume template

Template to publish a professional resume on the web, built on [Jekyll](https://jekyllrb.com), a static website generator.

The generated website can be hosted free of charge on [GitHub Pages](https://pages.github.com).

You can see an example here:  
[xmzio.github.io/resume](https://xmzio.github.io/resume)

The resume template is custom made, but it was originally based on the `Page` layout of the [Minima theme](https://jekyll-themes.com/jekyll/minima).

It uses basic features of the [Bootstrap](https://getbootstrap.com) frontend toolkit.

The stylesheet has a `@media print` section and the content has intentional page-breaks, so the same page can generate the PDF version of the resume.

The content is written in plain text files and formatted using [Markdown](https://daringfireball.net/projects/markdown/), a lightweight markup language.


## How to use this template

### Pre-requisites

1. The latest version of Ruby (it's highly likely you already have it on your system). For instructions visit: [ruby-lang.org/en/documentation/installation](https://www.ruby-lang.org/en/documentation/installation/)
2. Jekyll: [jekyllrb.com](https://jekyllrb.com)
3. A GitHub account: [github.com](https://github.com)
4. A public GitHub repository to host your resume, ideally named `resume`.

### Create the site

1. Fork this repository into a public repository named `resume`, in your GitHub account, and clone that new repository
2. Modify the [_config.yml](_config.yml) file. You will want to update the following properties with your own information:
	* title
	* footnote
	* contact_methods (email, LinkedIn profile, location)
	* website - This should point to the rendered version on GitHub Pages; it is used by the footer to present links to the online version of the resume if someone decides to print it or generates a PDF
	* github_repository - This should point to your repository; it is used in the footer to present a link to the source of your resume
	* google_analytics - Add here your own Analytics code. If you don't want to use Google Analytics, just remove this line
3. Create the content of your resume. There's one main content file and 5 sections:
	* The main content file is [index.md](index.md); check the example and replace the text accordingly.
	* The sections are:
		* [content/_skillsSoft](content/_skillsSoft) - Soft skills
		* [content/_skillsTechnical](content/_skillsTechnical) - Technical skills
		* [content/_experience](content/_experience) - Experience
		* [content/_experiencePrevious](content/_experiencePrevious) - Older experience
		* [content/_education](content/_education) - College and other education
4. You can preview your site locally by running Jekyll: ```bundle exec jekyll serve```
5. When you're happy with your site, push the changes to the remote GitHub repository
6. Go to your repository settings, find the **Pages** feature in the sidebar, at the bottom of the **Code and automation** menu, and enable GitHub Pages. Select **Deploy from a branch**, and specify the main branch as its source (or any other branch, depending on your workflow).
7. Wait for the GitHub Actions workflow to build your site (around 5 minutes) and visit your site in the address **<your_github_id>.github.io/resume**



## Known issues

* **Print layout** - It is currently necessary to manually mark page-breaks either in the layout or the content, by using `<div class="page-break"></div>`. This is because most browsers can't automatically break Bootstrap divs, used for the layout of the main sections.  
The `page-break` class will force a page break when printing from most browsers; it is defined in the `@media print` stylesheet.

## TODO:

* Convert this project into a real Jekyll theme (i.e. bundle it into a Ruby gem).


---
&#169; 2023 Xavier Muñiz - Released under the [MIT License](LICENSE)  

Find me on Mastodon: [@xmz@mastodon.social](https://mastodon.social/@xmz)  
And LinkedIn: [linkedin.com/in/xaviermuniz](https://www.linkedin.com/in/xaviermuniz/)  


