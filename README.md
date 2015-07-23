# ABOUT

This site is managed through [Statocles](https://metacpan.org/pod/Statocles). Direct editing of components of the site outside of this README are not encouraged. Information on Github markdown can be found an the [Github Flavored Markdown Page](https://help.github.com/articles/github-flavored-markdown/).

## USAGE

These are basic steps for performing particular tasks with Statocles. If you wish to know more then consult the Statocles documentation pages or run: ```statocles -h```

### Install statocles using cpanm
```
cpanm statocles
```

### Create the site

```
statocles create ias3perl.github.io
statocles build
```

### Create the blog and create a new blog post

```
statocles generate blog
statocles blog post 
```

### Add a new page
There are several approaches to adding content but for now we'll use the [plain page approach]().
```
mkdir page/usecases
vim page/usecases/index.markdown
statocles build
git add page/usecases/index.markdown
git commit -m "Add use cases index."
vi index.html [ add page to index ]
git add index.html
git commit -m "Adjust home page."
```

### Rebuild the site (generate HTML)
Statocles generates markup for you based on the markdown files you create. As a consequence of this approach you need to regenerate the markup with a build process. All of the changes can be previewed using your favorite editor and looking at the resulting "staged" items located under the hidden directory .statocles located in the project directory. 
```
statocles build
   view .statocles/build/page/usecases/index.html [ review the changes before publishing ]
```
  

### Preview your changes locally
```
statocles daemon
```

### Deploy new site
```
statocles deploy
```
