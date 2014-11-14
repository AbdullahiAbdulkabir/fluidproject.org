# Fluid Project Website

This repository contains the files needed to build a copy of the Fluid Project website.

This is not an immediately deployable version of the website - [docpad](http://docpad.org/) is used to build the site from source files.

## Requirements

Download and install the following packages before building the Fluid website:

* docpad installed - https://docpad.org/
* docpad handlebars plugin - https://github.com/docpad/docpad-plugin-handlebars/
* moment plugin - https://www.npmjs.org/package/docpad-plugin-moment
* markdown plugin - https://github.com/docpad/docpad-plugin-marked
* stylus plugin - https://www.npmjs.org/package/docpad-plugin-stylus
* eco plugin - https://github.com/docpad/docpad-plugin-eco


## How to Build for Local Development

1. Clone the fluid website repository
```
> git clone <fluid-website-git-repo>
```

2. Run docpad from the fluid-website directory
```
> cd fluidproject.org
> docpad run
```
   There should be output similar to this:
```
info: Generated 377/379 files in 13.422 seconds
info: Watching setup starting...
info: Watching setup
info: The action completed successfully
```

3. Open http://localhost:9778/ to see the website.

**Note:** docpad runs its own webserver for development. To create a deployable version of the website, see "Building a Deployable Version" below.

## Building a Deployable Version for Github Pages

1. To build a deployable version of the website for github pages, first install the gh-pages plugin:
```
> docpad install ghpages
```
2. Then run the github pages deploy command:
```
> docpad deploy-ghpages --env static
```

This will:
- create the website locally under the ./output/ directory
- create a new branch in your remote github repository under http://github.com/username/project/gh-pages
- and push the output files to that branch.

For more information on the gh-pages plugin, see: https://github.com/docpad/docpad-plugin-ghpages.

## Other Notes for Developers

* It is strongly recommended to work from source files located within the ``fluidproject.org/src/`` directory. Do not work from the ``fluidproject.org/out/`` directory as these files get overwritten by docpad.
* There is no need to version the ``/fluidproject.org/out/`` directory. This removes ambiguity as to which files to work from.

## License

The Fluid Project website is available under [Creative Commons Attribution License](http://creativecommons.org/licenses/by/3.0/).
