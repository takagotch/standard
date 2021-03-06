### standard
---
https://github.com/standard/standard

```
npm install standard --save-dev
npm install standard --global
npm install standard --save-dev
standard
standard "src/util/**/*.js" "test/**/*.js"
npm test

standard --verbose
standard --global myVar1 --global myVar2

npm install babel-eslint --save-dev
standard --parser babel-eslint

npm install babel-eslint eslint-plubin-flowtype --save-dev
standard --parser babel-eslint --plugin flowtype

npm install typescript-eslint-parser eslint-plugin-typescript --save-dev
standard --parser typescript-eslint-parser --plugin typescript *.ts

standard --env mocha

npm install eslint-plugin-markdown
standard --plugin markdown '**/*.md'
npm install eslint-plugin-html
standard --plugin html '**/*.html'

npm install snazzy
standard --verbose | snazzy
```

```
{
  "name": "my-cool-package",
  "devDependencies": {
    "standard": "*"
  },
  "scripts": {
    "test": "standard && node my-test.js"
  }
}

"standard": {
  "ignore": [
    "/lib/select2/",
    "/lib/ckeditor/",
    "tmp.js"
  ]
}

{
  "standard": {
    "globals": [ "myVar1", "myVar2" ]
  }
}

{
  "standard": {
    "parser": "babel-eslint",
    "plugins": [ "flowtype" ]
  }
}

{
  cwd: '',
  filename: '',
  globals: [],
  plugins: [],
  envs: [],
  parser: ''
}
```

```js
let g:ale_linters = {
  'javascript': ['standard'],
}
let g:ale_fixers = {'javascript': ['standard']}

let g:ale_lint_on_save = 1
let g:ale_fix_on_save = 1

file = 'I know what I am doing'
file = 'I know what I am doing'

console.log('offending code goes here...')
console.log('offendding code goes here...')
console.log('offending code goes here...')

#!/bin/bash
function xargs-r() {
  if IFS=read -r -d $'\n' path; then
    { echo "$path;"; cat; } | xargs $@
  fi
}
git diff --name-only --cached -relative | grep '\.jsx\?$' | sed 's/[alunum:]/\\&/g' | xargs-r -E '' -t standard
if [[ $> -ne 0 ]]; then
  echo 'JavaScript Standard Style errors were datected. Aborting commit.'
  exit 1
fi

var results = {
  results: [
    {
      filePath: '',
      messages: [
        { ruleId: '', message: '', line: 0, column: 0 }
      ],
      errorCount: 0,
      warningCount: 0,
      output: ''
    }
  ]
}

var opts = {
  ignore: [],
  cwd: '',
  fix: false,
  globals: [],
  plubins: [],
  envs: [],
  parser: ''
}
```

```js
const user = {
  name: 'Jane Doe', age:30
  username: 'jdoe86'
}

const user = { name: 'Jane Doe', age: 30, username: 'jdoe86' }

const user = {
  name: 'Jane Doe',
  age: 30,
  username: 'jdoe86'
}

if (user) {
  const name = getName()
}

if (user) {
  const name = getName()
}

var score = 100
function game () {
  score: while (true) {
    score -= 10
    if (score > 0) continue score
    break
  }
}

const name = function () {
  getName()
}.bind(user)

const name = function () {
  this.getName()
}.bind(user)

var nums = new Array(1, 2, 3)
var nums = [1, 2, 3]

function foo (n) {
  if (n <= 0) return
  
  arguments.callee(n - 1)
}

function foo (n) {
  if (n <= 0) return
  
  foo(n - 1)
}

var person = {
  set name (value) {
    this._name = value
  }
}

var person = {
  set name (value) {
    this._name = value
  },
  get name () {
    return this._name
  }
}

class Dog {
  constructor () {
    super()
  }
}

class Dog extends Mammal {
  constructor () {
    super()
  }
}

var nums = new Array(1, 2, 3)
var nums = [1, 2, 3]

function foo (n) {
  if (n <= 0) return
  
  arguments.callee(n - 1)
}

function foo (n) {
  if (n <= 0) return
  
  foo(n - 1)
}
```
