# Github Action : 
adityabhangle658/ruff-python-lint-format-check-pr@main

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
      uses: adityabhangle658/ruff-python-lint-format-check-pr@main
```

# What the error may look like: 
If your python files have lint errors, it may look like this 


If your python files have format errors, it may look like this 


If your python files have both lint and format errors, it may look like this 


And finally, if your code is clean, it will look like this 


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

[Click here to check the README about this action] (https://github.com/adityabhangle658/ruff-python-lint-format-check-pr/blob/main/README.md)
