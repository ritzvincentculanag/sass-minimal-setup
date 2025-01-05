# Minimal SASS setup for static websites

> This is my personal guide that I have written so I don't have to look for
> resources in the web. This is inteded only for static websites.

## Setting up the project

1. Install `node` [here](https://nodejs.org/en). It should also install `npm`.
2. Create a folder to store your source code.

```bash
# go to the home directory
cd ~

# create a folder called web and go change directory to it
mkdir web && cd web

# create a folder using mkdir
mkdir sass-minimal-setup

# go to the folder using cd
cd sass-minimal-setup
```

3. Once you are done creating your root folder. Go ahead and create the folder
   to store your assets such as `assets`, `scripts`, etc.

```bash
# create an assets folder
mkdir assets

# go into the assets folder and create folders named sass and css
cd assets && mkdir sass css
```

4. Create the necessary files for you to get started.

```bash
# go back to root directory of the project
cd ..

# create index.html
touch index.html

# create styles.scss
touch assets/sass/styles.scss
```
