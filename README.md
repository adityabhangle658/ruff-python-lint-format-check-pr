# Github Action : 
adityabhangle658/ruff-python-lint-format-check@main

# What it does 
Now you can easily check the formatting and do a lint check on the python files in your repository. Not only that, to avoid changing multiple files at a time, this action only does a formating and lint check on the changed files in a PR 

This action makes use of 2 important things 

1) Ruff: An extremely fast Python linter and code formatter, written in Rust.
   More Info here: https://github.com/astral-sh/ruff
   
3) A github action called "tj-actions/changed-files@v41", that gives changed files in a PR. Going forward, this will be changed to something native to this action
   More info here: **https://github.com/tj-actions/changed-files**

# How to use:
```
Example: 
    - name: Python Ruff Lint and Format 
      uses: adityabhangle658/ruff-python-lint-format-check@main
```

# What the error may look like: 
If your python files have lint errors, it may look like this 

<img width="1262" alt="image" src="https://github.com/adityabhangle658/ruff-python-lint-format-check/assets/124627213/0fba214c-2578-4159-8537-e5d7d552089f">

If your python files have format errors, it may look like this 

<img width="689" alt="image" src="https://github.com/adityabhangle658/ruff-python-lint-format-check/assets/124627213/00f7a11c-ece8-4cb6-9732-01cf00207d9f">

If your python files have both lint and format errors, it may look like this 

<img width="1262" alt="image" src="https://github.com/adityabhangle658/ruff-python-lint-format-check/assets/124627213/c2341d61-af21-4d78-9e03-60e5ac906ef2">

And finally, if your code is clean, it will look like this 

<img width="663" alt="image" src="https://github.com/adityabhangle658/ruff-python-lint-format-check/assets/124627213/8bc7734e-a1fc-45b3-8e9e-d1c6bdb86ea5">

You can auto resolve any formatting issues using
```
ruff format <foldername/or/space_separated_filenames>
```
Pls make sure you check/test the code after auto-format

You can auto resolve any lint issues using 
```
ruff check <foldername/or/space_separated_filenames> --fix
```
Pls make sure you check/test/format the code after auto-lint fix

-------

More information on how to make use of Ruff, can be checked in the link given above 

-------

[Click here to check the README about this action] (https://github.com/adityabhangle658/ruff-python-lint-format-check/blob/main/README.md)
