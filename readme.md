## Table of Content
- [Git](#git)
  - [1.1 Uploding_File_On_Git:)](#1.1)
  - [1.2 CREATE NEW BRANCH](#u1.2)
  - [1.3 Merge master branch to main](#1.3)
- [JavaScript](#javascript)
- [jQuery](#jquery)
## git
### 1.1 Uploding_File_On_Git:)
### *…or create a new repository on the command line*
```bash
 echo "# javascript-core" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/sanjivpaul/javascript-core.git
git push -u origin main

```
### *…or push an existing repository from the command line*
```bash
git remote add origin https://github.com/sanjivpaul/javascript-core.git
git branch -M main
git push -u origin main
```
- 1. Creating Folder
        - On local host
        - On git repository

- 2. Initialize local host
        - ```$git status```
        - ```$git init```

- 3. Add files:-
        - ```$git status```
        - ```$git add .```

- 4. Add origin:-
        - ```$git remote add origin {SSH copy from git repositore file}```

- 5. Commit:-
        - ```$git status```
        - ```$git commit -m "file name" (like version1)```

- 6. Push:-
        - ```$git status```
        - ```$git push -u origin master/main```

### 1.2 CREATE NEW BRANCH
- ```$git checkout -b <branch-name>```

### 1.3 Merge master branch to main
- 1 Git fetching
  - The initial command to run is git fetch for getting the latest updates of your repository.
  - ```$git fetch```

- 2 Git rebasing
  - The git rebase command will bring the latest commits of the master to your branch.
  - ```$git rebase origin/main```

- 3 Switching to main
  - Switch to the master branch by running git checkout
  - ```$git checkout main```

- 4 Pulling changes
  - Get the latest changes from the main by using git pull:
  - ```$git pull origin main```

- 5 Merging changes
  - Then merge the changes with the git merge command
  - ```$git merge master```

- 6 Pushing changes
  - The final step is pushing local changes to the remote repository
  - ```$git push origin main```

## Javascript
### Variables
Variables are the containers used to store data, we can declare variables in JavaScript by using the keywords `var`, `let`, and `const`.
``` js
var varName = "hello world";
```
- The `var` keyword has no block scope.
- The `var` keyword is either function-scoped or global-scoped.
- In `var`  we can redeclare variables again and again.

``` js 
let userId = 29
```
- In `let` we can not redeclare it we can only update the value of the variable.

``` js 
const COLOR_RED = "#F00";
const COLOR_GREEN = "#0F0";
const COLOR_BLUE = "#00F";
const COLOR_ORANGE = "#FF7F00";

// ...when we need to pick a color
let color = COLOR_ORANGE;
alert(color); // #FF7F00
```

- `const` are nor update nor redeclare they are constants.

## jQuery
### 1 jQuery Installation
- By downloading the compressed jQuery file
- Using the jQuery CDN
``` html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>jQuery tutorial</title>
  </head>
  <body>
    hello world
    <p>click on p</p>
  </body>
  <!-- <script src="./js/code.jquery.com_jquery-3.7.0.min.js"></script> -->
  <script
    src="https://code.jquery.com/jquery-3.7.0.min.js"
    integrity="sha256-2Pmvv0kuTBOenSvLm6bvfBSSHrUJ+3A7x6P5Ebd07/g="
    crossorigin="anonymous"
  ></script>
  <script>
  
    console.log($); // $ means jquery
    console.log("we are using jQuery")
    // $('selector').action()
  
  </script>
</html>

```

### 2. jQuery Syntax
General syntax of jQuery
``` js
$('selector').action();
```

### 3. jQuery Functions
- 3.1. `click()`:
On click paragraph tag 'p' the simple message is print on the console.
``` js
 $('p').click(function(){
        console.log("you click on p");
});
```

- 3.2. `hide()`: hide() function simply hide the content on click. We can select any tag, id, or class.
``` js
 $('p').hide(); //it will hide all the p tags
```
note: if there exist multiple p tags then we can use `this` keyword to target specific p tags.

``` js
 $(this).hide(); // by using this keyword we can hide specific p tag 
```
**for selecting #id or .class**
``` js
 $('#id').hide(); //for selecting id
 $('.class').hide(); // for select class
```

### 4. **`document.ready()`** event:
When our page is big, it takes time to load the document, but if we run JavaScript before the page is loaded, then there may be a create problem. So, to confirm that our document is ready, we will write it here in the `document.ready()` function, and **all jquery code will be inside that function**.
``` js
// document.ready() event for confirm that document is ready.
$(document).ready(function () {
        console.log("we are using jQuery");

        $("p").click(function () {
                console.log("you click on p");
                //$('p').hide(); //it will hide all the p tags
                $(this).hide(); // by using this keyword we can hide specific p tag
                $("#id").hide(); //for selecting id
                $(".class").hide(); // for select class
      }); // do this when click on p
    });
```

### 5. jQuery Selectors
There are three main types of selectors in jQuery
- Element Selector
- Id selector
- Class Selector

#### 5.1. Element Selector:
Element selector selects all the elements with the specified element name. e.g. if we select p tag then it will target all the p elements of the document.
``` js
$('p').click();
```

