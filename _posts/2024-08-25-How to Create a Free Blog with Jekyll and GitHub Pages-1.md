layout:
post title: "Your Step-by-Step Guide to Creating a Free Blog with Jekyll and GitHub Pages"
date: 2025-08-25 14:45:00 +0530
categories: jekyll github tutorial guide


Have you ever wanted to start your own blog without the cost and complexity of traditional hosting platforms? You're in the right place. This guide will walk you through the entire process of creating a fast, secure, and completely free blog using Jekyll, a powerful static site generator, and GitHub Pages for hosting.

This post will cover everything from initial setup on macOS, Windows, and Linux to deploying your site and troubleshooting common issues.

Step 1: Getting Your System Ready
Before we can start building, we need to install a few essential tools. Jekyll is built with a programming language called Ruby, so the first step is to get a modern version of Ruby running on your computer.

For macOS Users
Setting up on a Mac is smooth with the help of Homebrew, a package manager for macOS.

Install Homebrew:

{% highlight bash %}
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
{% endhighlight %}

Install Ruby:

{% highlight bash %}
brew install ruby
{% endhighlight %}

Configure Your Terminal's PATH:

{% highlight bash %}
echo 'export PATH="$(brew --prefix ruby)/bin:$PATH"' >> ~/.zshrc
echo 'export PATH="/usr/local/lib/ruby/gems/3.4.0/bin:$PATH"' | sudo tee -a ~/.zshrc
{% endhighlight %}

Reload Your Terminal:

{% highlight bash %}
source ~/.zshrc
{% endhighlight %}

Install Jekyll and Bundler:

{% highlight bash %}
gem install bundler jekyll
{% endhighlight %}

For Windows Users
The easiest way to get started on Windows is with the RubyInstaller.

Install Ruby+Devkit:
Download and run the RubyInstaller. Choose a Ruby+Devkit version and ensure the “Add Ruby executables to your PATH” box is checked.

Install Jekyll and Bundler:

{% highlight cmd %}
gem install jekyll bundler
{% endhighlight %}

Step 2: Creating Your First Jekyll Blog
With the tools installed, it's time for the fun part.

Create a New Site:

{% highlight bash %}
jekyll new my-awesome-blog
{% endhighlight %}

Preview Your Blog Locally:

{% highlight bash %}
cd my-awesome-blog
bundle exec jekyll serve
{% endhighlight %}

Now, open a web browser and go to http://localhost:4000.

Step 3: Pushing Your Blog to GitHub
Let's connect your local blog to your new GitHub repository.

Initialize Git:

{% highlight bash %}
git init
git remote add origin https://github.com/your-username/your-username.github.io.git
{% endhighlight %}

Add, Commit, and Push Your Files:

{% highlight bash %}
git add .
git commit -m "Initial commit"
git push -u origin main
{% endhighlight %}

After a few minutes, your blog will be live at https://your-username.github.io!

GitHub Push Troubleshooting
Even with the correct setup, you may face some issues while pushing code to GitHub. Here are common errors and fixes.

Error: src refspec main does not match any
This means you haven't made any commits yet. Run the following commands:

{% highlight bash %}
git add .
git commit -m "Initial commit"
git push -u origin main
{% endhighlight %}

Error: Password authentication is not supported
GitHub no longer accepts passwords for command-line operations. You must use a Personal Access Token (PAT).

Generate a Token:
On GitHub, go to Settings > Developer settings > Personal access tokens > Tokens (classic).

Configure Token:
Click Generate new token, give it a name, set an expiration, and check the repo scope.

Use the Token:
Copy the token and use it when the terminal asks for your password.