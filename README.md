# This is the site for The Sungods. 

To edit anything you see here without having to 
run anything locally, just visit our GitHub 
repo at: [https://github.com/thesungods/thesungods.github.io](https://github.com/thesungods/thesungods.github.io).

To see what your changes look like before sending
us the pull request that contains your changes,
change your fork of our repo to be named:

    YOUR_USERNAME.github.io

Then, visit: [http://YOUR_USERNAME.github.io](http://YOUR_USERNAME.github.io).

You should see a special-to-you version of the site.

## Working locally

If that's too easy, or you have files to upload, or you have more
extensive changes in mind, run the below commands.

First install rvm

	\curl -sSL https://get.rvm.io | bash -s stable

Then load it into your environment

	source /Users/(USERNAME)/.rvm/scripts/rvm (or whatever is prompted by the installer)

Then install Ruby 2.2 or higher

	rvm install 2.2
	rvm use 2.2 --default
	
Verify that this new version is running (optional)

	which ruby
	ruby -v
	
Install the GitHub Pages package, which includes Jekyll

	gem install github-pages

Clone our site

	git clone https://github.com/thesungods/thesungods.github.io.git

Then, see it run locally:

	cd thesungods.github.io
	jekyll serve .

Your copy of the site will then be viewable at: [http://0.0.0.0:4000](http://0.0.0.0:4000)
(or wherever Ruby tells you).

If you're a bit rusty with git/GitHub, you might wanna read
[this](http://readwrite.com/2013/10/02/github-for-beginners-part-2) for a refresher.

## Thank you!

Thank you for anything you can do to help us out. The Sungods is an
[open-source music project](http://thesungods.co/opensource/) and we love you. 
