# Config

* This static website is built with Hugo using the LoveIt theme. It is hosted on AWS Amplify.

* Some config and sections can be added by amending `config.toml`. See the [theme documentation](https://hugoloveit.com/theme-documentation-basics/#33-style-customization).

* For custom styling, edit the relevant CSS files in `themes/LoveIt/assets/css`. E.g. the homepage font size can be increased by changing the rem in `themes/LoveIt/assets/css/_page/_home.scss`

* New posts are made by creating a `.md` file in `content/posts`. Use `hugo new posts/new-post-name.md` in command line for shortcut. 

* Once any changes have been made, check locally with `hugo server`. Then build the pages into html by typing `hugo -D` in command line.

* `git add .` -> `git commit -m "message"` -> `git push origin master` 

* The new website will build and deploy in AWS Amplify. 