---
title: Pre-Workshop Software Test
date: January 24, 2020
---

## Table of Contents

- [1. Text Editor Available?](#text-editor-available)

- [2. RStudio and Package Installation](#rstudio-and-package-installation)

- [3. Git and GitHub](#git-and-github)


<br>
<br>
<br>
<br>
<br>
<br>

## 1. Text Editor Available?

We need to use a proper text editor throughout the workshop.  Check if any of these are available.

- ``Vim``

- ``Notepad++``

If neither are available, we will need to install one or the other.

<br>
<br>
<br>
<br>
<br>
<br>


## 2. RStudio and Package Installation

- Make sure you can launch R studio successfully.

- Try installing some packages

```r

install.packages("tidyverse")

```

- If this generates an error such as ``Tidyverse is not available for this R version``, try it with another method:

```r

library(devtools)

```

- If devtools is not available, first install it.


```r

install.packages("devtools")

```

- Then load it:

```r

library(devtools)


```

Then retry installing ``tidyverse`` as follows:

```r

devtools::install_github("hadley/tidyverse")

```

- If this fails, copy paste the entire installation log and please email it to me.

- If it succeeds, try loading ``tidyverse``


```r

library(tidyverse)

```

<br>
<br>
<br>
<br>
<br>
<br>



## 3. Git and GitHub

### 3.1 Create Remote Git Repository

1. Login to your github account using a web browser.  If you don't have an account yet, make one first.

2. Click the ``+`` button in TOP RIGHT corner and choose ``New Repository``.

3. Give it a name: ``testgit``.

4. **Do not** initialize it with a README.

5. Click ``Create repository``.


<br>
<br>
<br>

### 3.2 Create Local Git Repository

- The program we will use is called [Git for Windows](https://gitforwindows.org).  You can right click anywhere on the desktop and choose ``Git Bash`` from the resulting dialogue box.  This will open up a terminal session.  


1. First check where you are on the system

```bash

pwd

```

2. Create a new folder

```bash

mkdir testgit

chdir testgit

pwd

```

3. Initiate a new git repository in this location


```bash

git init

```


4. Create some content

```bash


vim README.md

```

5. This will open up a new file ``README.md`` in the ``vim`` text editor.  Press the ``i`` key to start adding content to this file.

```bash

This is a test git repository.

```

6. Press ``ESC`` key to exit the edit mode in the text editor.  You are still inside the editor.  Next, you will save and close the file.

```bash

:wq

```

7. This will return  you to your terminal session.  Now let's work with git again.

```bash
 
git status

```

- This should tell you that there is a new file in the repo (the file you just created)

8. Add file to git

```bash

git add .

git status

```

9. Commit the changes to your repository

```bash

git commit -m "My first commit"

```

10. Tell git about your GitHub account


```bash

git config user.name luisalza ## This is just an example, use your own.

git config user.email luis@alza.com ## Again, just an example, use your own.

git remote add origin https://github.com/luisalza/testgit.git

```

11. Make sure all these settings were correctly saved.

```bash

git config --list

```

12. Push your work to GitHub

```bash

git push -u origin master

```

- If everything goes right, you will get a ``username`` and then a ``password`` prompt from Github.  Once you enter the password, your new file should be uploaded to your github account.  Check it by going to the repo's page e.g. **https://github.com/luisalza/testgit**.

**Note**: If the step#12 above fails, copy paste the entire log from the terminal and please email it to me.


#### This concludes the software checkup.



 

