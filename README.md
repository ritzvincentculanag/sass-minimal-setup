# Minimal SASS setup for static websites

> [!INFO]
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

5. After following the steps this is what your folder structure should look like.

![tree structure](/assets/img/file-structure.png)

## Installing SASS and setting up `sass watch`

1. Go back to the root directory of your project and initialize it
   as an npm project. It will create a `package.json` file containing meta
   data about your project such as the auhtor, version, dependencies, etc.

```bash
npm init

# Optional
# You can run this command to skip answering the questions
npm init -y
```

2. After initializing it as an npm project, go ahead and install sass.

```bash
npm install sass --save-dev
```

3. Open your `package.json` file and add the follwing lines of code
   under the scripts section.

```json
"scripts": {
    "test": "echo \"Error: no test specified\" && exit 1",

    // Add these
    "sass-watch": "sass --watch --update --style=expanded sass:css",
    "sass-build": "sass --no-source-map --style=compressed sass:css"
},
```

This is what your `package.json` should look like.
![package json](/assets/img/package-json.png)

5. To automatically start watching for changes in the sass folder, run
   the command `npm run sass-watch`.
