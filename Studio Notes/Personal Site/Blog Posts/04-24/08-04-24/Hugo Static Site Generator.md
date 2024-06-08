---
tags:
  - Personal-Blog
---
Hugo is a command line (CLI) tool which allows you to generate your own static website in a matter of minutes. Today I'm going to talk to you about what a static website is, why you might want one for yourself and how to use Hugo to generate your own website. This article will run through the [Hugo quick start](https://gohugo.io/getting-started/quick-start/) guide, as well as talking about why you might want to consider this for your own personal site. This is a beginner friendly guide which will attempt to explain some of the work we undertake today.

![hugo](https://gohugo.io/images/hugo-logo-wide.svg)
# Installation
## Binary Files
Installation is different depending on your operating system. For all operating systems though, you can visit the Hugo repositories [releases page](https://github.com/gohugoio/hugo/releases), where every operating system's compressed file sits (`.zip`, `.deb` or `.tar.gz`).
## Command Line
If you'd prefer to install this via command line, choose from the below commands for your Operating System:
### Windows
**Choco:** `choco install hugo-extended`
### Linux/MacOS
Due to the variety of flavours of Linux, I'm not going to list all of them here. However here are a few popular choices:
- **Debian/Ubuntu** - Apt: 
  `sudo apt install hugo`
- **Arch Linux** - Pacman: 
  `sudo pacman -S hugo`
- **Various Linux variants** - Snap: 
  `sudo snap install hugo`
- **MacOS (and Linux)** - Homebrew: 
  `brew install hugo`

Once you've gotten yourself setup, you're going to also need to have git setup. I won't walk through the steps of getting git setup, however you can find a pretty comprehensive guide [here](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git). Git is needed because this is how you'll be setting up the theme of your website. I'd also recommend getting set up on GitHub, so you can deploy your static website *for free*.
## Creating Your First Hugo Website
First, just make sure hugo is correctly installed. In your terminal, just type `hugo version` and you should see some information about the version number of hugo you've installed.

These steps will now take you through to making your very first website with hugo:

1. Make a new site with `hugo new site {name}` where {name} is the name of the folder for your new site.
	1. For example, `hugo new site my-blog` will create all the files necessary in a directory (folder) called `my-blog`. For example, if your terminal says you're in your Documents folder, it might be made under `C:\Users\{your-username}\Documents\my-blog` for windows, or `~/Documents/my-blog` for Linux and MacOS.
2. Open the new site in your IDE of choice, e.g: `cd {name} && code .` if you have VS Code installed. 
	1. If you don't have anything like this, on Windows you can use notepad, on Linux you can use nano, vim, gedit or any other text editor.
3. Run `git init` and git will setup your folder so it can use git's features.
4. Next add the theme of your choice with `git submodule add`. Check https://themes.gohugo.io/ for some good themes. For this quickstart, I used [PaperMod](https://themes.gohugo.io/themes/hugo-papermod/): 
	1. `git submodule add --depth=1 https://github.com/adityatelange/hugo-PaperMod.git themes/PaperMod`
		1. If you've already added a submodule and just want to re-download all the files for your theme: `git submodule update --init --recursive`
		2. A submodule is basically another git repository that you want to include in this git repository you've made.
5. Set the theme in the `config.yml` file. I did this with `echo "theme = 'PaperMod'" >> hugo.toml` on Linux. Open the hugo.toml file if you can't use echo,  then just add a new line for `theme = 'PaperMod'`
6. Check everything is setup correctly with `hugo server` - You'll see a link in your terminal, which would look something like http://localhost:1313/.
	1. If you're not sure what this is, when you develop something locally and run a server, then it will always go to localhost (which is basically just your machine). The 1313 denotes the port this sits on. Normally, on your web browser, you'd go to port `80` for HTTP connections, or `443` for HTTPS connections.
7. Add some content to the new website with `hugo new content posts/{new-post-title}.md`
8. Edit the new markdown file with some content
	1. Note this will by default be set to draft, we'll update this later.
	2. Don't know what to put? Why not just type "Hello World" under the second `+++` line.
9. Run `hugo server -D` to run a development view and view your new website. Isn't it great?
10. Once happy with the content you've made, make sure to change the draft status.
11. Build the website with the command `hugo`
12. Here I'd recommend you get your changes 'committed' to git, by running the following commands:
	1. `git add .` - This adds all files in the current directory (and subdirectories) to a state
	2. `git commit -m "Initial commit"` - This commits all files in the state to a commit, which is like a point in time for your code. The "Initial commit" is the message associated with the commit. You could replace this with "Hi mum" if you'd prefer, or anything else.
	3. We won't be pushing this yet, because we have some more work to do first.


Congratulations, you've just made your first static website.
## What's A Static Website Exactly?
The internet is made up of a multitude of technologies. If you're new to development, you may have heard of HTML and CSS. HTML is often called the bones, or structure of a website. CSS is therefore the flesh, the skin, what makes it pretty. Then you have JavaScript, which is like the nervous system - You use JavaScript if you want interactivity with a website. Have a pair of eyes that follow your cursor? That's probably JavaScript.

Those three technologies make up most websites. However, some websites require more than this. Some websites might, for example, have a sign up page. Once you sign up, you can log in, you can make changes to your account, etc. This is done with a backend. Communicating to another service like this is what's not covered by a static website. 

So if you can't have accounts and the likes, what's the point of a static website? Well, it's great for if you want to point people to something of yours, perhaps an email address, another website, your favourite game. Game developers often create static pages for their latest games, so then people can be linked to all the places they can buy their game. Also, blogs can be static websites, which is what this article covers.

## How To Host My Website?
Okay, so if you've gotten this far, you might want your friends and family to see what you've done. Earlier I said you should get a GitHub account. If you now navigate to [GitHub.com](https://github.com), you'll see a `+` icon at the top right hand of the page (At the time of writing, this may change if you read this article years in the future). Click this and click `New repository`.

Give your repository a name and a description if you'd like (the description is completely optional). Ensure you've got Public selected as this is important for free hosting of your website. Don't worry about anything else, just hit `Create repository`.

![Create a new repository page on GitHub](https://i.ibb.co/wdQQdKL/image.png)

Then it'll give you instructions on how to get your git repository going. If you were to copy the instructions presented in the "...or push an existing repository from the command line" section, so long as you followed the earlier instructions, this will work for you. The instructions GitHub gives you sets a remote origin (I.E a server you're sending your git files to), then get you to push your changes, which means all of your files will be sent to that server for storing.

![The command line commands you need](https://i.ibb.co/dGVq0ss/Git-Hub-Command-Line-Options.png)

Next, head to Settings > Pages, set the Build and Deployment to GitHub Actions and then head back to your local development.

You'll need to create a new file in your repository. You'll need to make the following folders: `.github` then inside the `.github` directory you'll need to make `workflows`. Then inside of there, make a `hugo.yaml` file. Hugo have kindly made a template for what needs to go inside of this, which you can find [here](https://gohugo.io/hosting-and-deployment/hosting-on-github/).

Run your git commands again:
`git add .`
`git commit -m "Add GitHub Workflow"`
`git push -u origin master` (or main if you're like me and have changed the name of the default branch)

This will push all of your changes direct to your main branch. Note, if you were to work in a team, or if you wanted to be safer, it's better practice to make a new branch and then raise a Pull Request (PR) to merge your code in... However as this is a simple example, I'm not going to go into how to handle PRs and the likes in this article.

Finally, with all of this done, if you head back to your GitHub repository, you should see a "workflow" has started. You'll see an orange dot, red cross or green check mark which denotes the status of the workflow. It doesn't take long for this to do its job. Once done however, if you click on it, if it was a green check mark, you'll be able to see where the website has been deployed to. With any luck, you'll have [your website working](https://timothyfothergill.github.io/timlah-webroll/). If you can't see where your website has been deployed to, it'll be at `https://{your-github-username}.github.io/{the-name-of-your-github-repo}/`.

### I don't get this but want a simple website built for me

I'm sure I can help with that for a small fee. Reach out to me on the Contact page and we'll discuss this. However, hopefully the instructions above are enough for you to get going. Hopefully this inspires you enough to make your very own website and host it for free. Get blogging, get creating and practice your web development skills.

Remember if you're stuck to check out the [Hugo documentation](https://gohugo.io/documentation/), or any specific documentation for the theme you chose.

Until next time, much love and happy tinkering and get out there and make something cool. If you follow this and want to share what you create with me, add a comment below with a link to your new website. I'd love to see it! - 
Timlah