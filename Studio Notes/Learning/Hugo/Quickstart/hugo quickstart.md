These steps are summarised from https://gohugo.io/getting-started/quick-start/

1. Check hugo is installed with `hugo version`
2. Make a new site with `hugo new site {name}` where {name} is the name of the folder for your new site.
3. Open the new site in your IDE of choice, e.g: `cd {name} && code .`
4. Run `git init` and if you don't want `master` as a branch, `git checkout -b main`
5. Next add the theme with `git submodule add`. Check https://themes.gohugo.io/ for some good themes. For this quickstart, I used [PaperMod](https://themes.gohugo.io/themes/hugo-papermod/): 
	1. `git submodule add --depth=1 https://github.com/adityatelange/hugo-PaperMod.git themes/PaperMod`
	2. `git submodule update --init --recursive`
6. Set the theme in the config.yml file. I did this with `echo "theme = 'PaperMod'" >> hugo.toml`
7. Check everything is setup correctly with `hugo server`
8. Add some content to the new website with `hugo new content posts/{new-post-title}.md`
9. Edit the markdown file with some content
	1. Note this will by default be set to draft, check the top of the md file to determine this.
10. Run `hugo server -D` to run a development view
11. Once happy with the markdown file, make sure to change the draft status.
12. Build the website with `hugo`

From here, consider pushing to GitHub