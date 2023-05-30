# 0x06. Star Wars API
AlgorithmAPIJavaScript

    By: Alexa Orrico, Software Engineer at Holberton School
    Weight: 1
    Project will start May 29, 2023 6:00 AM, must end by Jun 2, 2023 6:00 AM
    Checker was released at May 30, 2023 6:00 AM
    An auto review will be launched at the deadline

## Requirements
General

    Allowed editors: vi, vim, emacs
    All your files will be interpreted on Ubuntu 14.04 LTS using node (version 10.14.x)
    All your files should end with a new line
    The first line of all your files should be exactly #!/usr/bin/node
    A README.md file, at the root of the folder of the project, is mandatory
    Your code should be semistandard compliant. Rules of Standard + semicolons on top. Also as reference: AirBnB style
    All your files must be executable
    The length of your files will be tested using wc
    You are not allowed to use var

More Info
Install Node 10

$ curl -sL https://deb.nodesource.com/setup_10.x | sudo -E bash -
$ sudo apt-get install -y nodejs

Install semi-standard

Documentation

$ sudo npm install semistandard --global

Install request module and use it

Documentation

$ sudo npm install request --global
$ export NODE_PATH=/usr/lib/node_modules

Tasks
0. Star Wars Characters
mandatory

Write a script that prints all characters of a Star Wars movie:

    The first positional argument passed is the Movie ID - example: 3 = “Return of the Jedi”
    Display one character name per line in the same order as the “characters” list in the /films/ endpoint
    You must use the Star wars API
    You must use the request module

alexa@ubuntu:~/0x06$ ./0-starwars_characters.js 3
Luke Skywalker
C-3PO
R2-D2
Darth Vader
Leia Organa
Obi-Wan Kenobi
Chewbacca
Han Solo
Jabba Desilijic Tiure
Wedge Antilles
Yoda
Palpatine
Boba Fett
Lando Calrissian
Ackbar
Mon Mothma
Arvel Crynyd
Wicket Systri Warrick
Nien Nunb
Bib Fortuna
alexa@ubuntu:~/0x06$ 

Repo:

    GitHub repository: alx-interview
    Directory: 0x06-starwars_api
    File: 0-starwars_characters.js


# JavaScript Semi-Standard Style

tests npm downloads
One Semicolon for the Dark Lord on his dark throne

All the goodness of standard/standard with semicolons sprinkled on top.
Install

npm install semistandard

## Rules

Importantly:

    semicolons
    Check standard/standard for the rest of the rules.

Badge

Use this in one of your projects? Include one of these badges in your readme to let people know that your code is using the standard style.

js-semistandard-style

[![js-semistandard-style](https://raw.githubusercontent.com/standard/semistandard/master/badge.svg)](https://github.com/standard/semistandard)

js-semistandard-style

[![js-semistandard-style](https://img.shields.io/badge/code%20style-semistandard-brightgreen.svg)](https://github.com/standard/semistandard)

## Usage

The easiest way to use JavaScript Semi-Standard Style to check your code is to install it globally as a Node command line program. To do so, simply run the following command in your terminal (flag -g installs semistandard globally on your system, omit it if you want to install in the current working directory):

npm install semistandard -g

After you've done that you should be able to use the semistandard program. The simplest use case would be checking the style of all JavaScript files in the current working directory:

$ semistandard
Error: Use JavaScript Semi-Standard Style
  lib/torrent.js:950:11: Expected '===' and instead saw '=='.

Editor plugins

    Sublime users: Try SublimeLinter-contrib-semistandard for linting in your editor!
    Atom users - Install linter-js-standard
    VSCode users - Install vscode-standardjs

What you might do if you're clever

    Add it to package.json

{
  "name": "my-cool-package",
  "devDependencies": {
    "semistandard": "*"
  },
  "scripts": {
    "test": "semistandard && node my-normal-tests-littered-with-semicolons.js"
  }
}

    Check style automatically when you run npm test

$ npm test
Error: Code style check failed:
  lib/torrent.js:950:11: Expected '===' and instead saw '=='.

    Never give style feedback on a pull request again! (unless it's about semicolons)

Custom Parser

To use a custom parser, install it from npm (example: npm install babel-eslint) and add this to your package.json:

{
  "semistandard": {
    "parser": "babel-eslint"
  }
}

Vim

Install Syntastic and add these lines to .vimrc:

let g:syntastic_javascript_checkers=['standard']
let g:syntastic_javascript_standard_exec = 'semistandard'

For automatic formatting on save, add these two lines to .vimrc:

autocmd bufwritepost *.js silent !semistandard % --fix
set autoread

Ignoring files

Just like in standard, The paths node_modules/**, *.min.js, bundle.js, coverage/**, hidden files/folders (beginning with .), and all patterns in a project's root .gitignore file are automatically excluded when looking for .js files to check.

Sometimes you need to ignore additional folders or specific minfied files. To do that, add a semistandard.ignore property to package.json:

"semistandard": {
  "ignore": [
    "**/out/",
    "/lib/select2/",
    "/lib/ckeditor/",
    "tmp.js"
  ]
}

Make it look snazzy

If you want prettier output, just install the snazzy package and pipe semistandard to it:

$ semistandard --verbose | snazzy

See standard/standard for more information.
