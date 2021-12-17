# Personal Blog Public

## Overview & Initial Setup

The following is to keep a record of how I setup the site. The site is built on the [Hugo](https://gohugo.io/) and uses the Congo theme from [Congo](https://github.com/jpanther/congo) by JPanther. There are 2 repositories. One is a main working repository. One is a deployment repository i.e. this repository which is a submodule of the working repository. This deployment repository is where the site is deployed off of and only contains the static build content. 

Assuming you have this deployment repository with a `main` branch, you now want to add this repository as a submodule of the working repository. So CD into the root directoy of your Hugo site i.e. the working repository. 
```
git submodule add -b main INSERT_LINK_TO_THIS_GIT public
```

## Build

Now when you build the site the static files are stored in `site_name/public`. To build the site, CD into the root directory of your Hugo site.
```
hugo -t congo
```

Then CD into the `site_name/public` and push to origin main. This pushes the static files in public to this submodule deployment repository.

## Further Clarification

For further information or clarification see this:
https://www.youtube.com/watch?v=LIFvgrRxdt4&t=519s
