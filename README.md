# Tips on modifying the website

I use *pelican* branch to edit the content and *master* branch to store the generated output files.

For convenience you can have two separate copies of the repo:

```
git clone https://github.com/GrayTophatclan-GTC/GrayTophatclan-GTC.github.io.git gtc-deploy
cp -r gtc-deploy gtc-develop
cd gtc-develop
git checkout pelican
```

To work with the website you need installing *pelican* and *python-markdown* packages from your system repository.

The content (articles) are written in markdown and are stored in the *content* directory. The theme (css and templates) defines the website structure and look and is stored in the *theme* directory. The one used here is based on the [lightweight](https://github.com/getpelican/pelican-themes/tree/master/lightweight) theme.

To render the website type `make html` in the *gtc-develop* folder. The output files will be generated and saved into *gtc-develop/output/* directory. Then you just copy them into the *gtc-deploy* directory and make a commit there. If some articles were deleted or files renamed you should clean the *gtc-deploy* first (but please don't wipe out this readme xD).

You may want to learn about pelican from its [documentation](http://docs.getpelican.com/en/stable/). The idea of pelican is simple so it's to get started with it if you are familiar with HTML/CSS and python.