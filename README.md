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

1) Example: How to use action in existing flow
```
    - name: Python Ruff Lint and Format 
      uses: adityabhangle658/ruff-python-lint-format-check-pr@main
```

2) Sample Workflow
```
name: Adi - Ruff Test My Action

on: 
  pull_request:

jobs:
  code-quality-check:
    runs-on: ubuntu-latest

    steps:
    - name: Checkout repository
      uses: actions/checkout@v4.1.1

    - name: Set Python Version
      uses: actions/setup-python@v4
      with:
        python-version: ${{ inputs.python_version }}

    - name: adi658-python-ruff-lint-format-check
      uses: adityabhangle658/ruff-python-lint-format-check-pr@main
 
    - name: Testing 
      run: echo "Done"
```

# What the error may look like: 
If your python files have lint errors, it may look like this 

<img width="1262" alt="image" src="https://github.com/adityabhangle658/ruff-python-lint-format-check-pr/assets/124627213/9e54d80d-41e3-4788-a098-d086f0dcc561">

If your python files have format errors, it may look like this 

<img width="1262" alt="image" src="https://github.com/adityabhangle658/ruff-python-lint-format-check-pr/assets/124627213/ffde048c-00b1-4640-a100-5bcc79c94d37">

If your python files have both lint and format errors, it may look like this 

<img width="1262" alt="image" src="https://github.com/adityabhangle658/ruff-python-lint-format-check-pr/assets/124627213/bcf60f09-2ec9-42d5-b21b-72cc9c12a785">

And finally, if your code is clean, it will look like this 

<img width="1262" alt="image" src="https://github.com/adityabhangle658/ruff-python-lint-format-check-pr/assets/124627213/55743e1e-d9fa-4793-90ec-2980084d69dd">

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
