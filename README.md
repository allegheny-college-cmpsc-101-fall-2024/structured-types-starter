
# Structured Types - Specification Lab

[![build](../../actions/workflows/build.yml/badge.svg)](../../actions/)
![Platforms: Linux, MacOS, Windows](https://img.shields.io/badge/Platform-Linux%20%7C%20MacOS%20%7C%20Windows-blue.svg)
[![Language: Python](https://img.shields.io/badge/Language-Python-blue.svg)](https://www.python.org/)
[![Code Style: Black](https://img.shields.io/badge/Code%20Style-Black-blue.svg)](https://github.com/psf/black)
[![Commits: Conventional](https://img.shields.io/badge/Commits-Conventional-blue.svg)](https://www.conventionalcommits.org/en/v1.0.0/)
[![Discord](https://img.shields.io/discord/872320492936257537?logo=discord)](https://discord.gg/kjah8MFYbR)

## Introduction

In this assignment you will implement python code that works with structred
types. Specifically, you will make complete two scripts. One will find the
intersection of two tuples, and the other will create a higer-order function
that can apply any function to items within a list container.

## Learning Objectives

This assignment is about exploring structured types.
The learning objectives of this assignment are to:

1. Use Git and GitHub to manage source code file changes.
2. Practice using and writing code involving tuples, lists, and higher-order
  functions.
3. Write clearly about the programming concepts in this assignment.

## Quick Links

- Due date: Check Discord or the
  [Course Materials Schedule](https://github.com/allegheny-college-cmpsc-101-fall-2024/course-materials/blob/main/Schedule.md)
- Policy on
  [Tokens](https://github.com/allegheny-college-cmpsc-101-fall-2024/course-materials#tokens)
- [Token Form for Automatic Extension](https://forms.gle/y9Mz55hQKr84wzvXA)
- Policy for
  [Assignment Evaluation](https://github.com/allegheny-college-cmpsc-101-fall-2024/course-materials#assignment-evaluation)
- Policy for [Assignment Submission](https://github.com/allegheny-college-cmpsc-101-fall-2024/course-materials#assignment-submission).
- [#data-structures Discord channel](https://discord.com/channels/877320365825749002/1274744318124359732)
- [Starter repo](https://github.com/allegheny-college-cmpsc-101-fall-2024/structured-types-starter)

## Policy Reminders

Students are reminded to uphold the Honor Code. Cloning this assignment
repository is a commitment to the latter.

For this assignment, you may use class materials, the textbook, notes,
and the internet, including AI, for reference and learning. AI may **not** be
used to generate answers that you submit. All code and writing that are turned
in **must be your own work and your own words**. Copying or otherwise
representing ChatGTP or other AI outputs as your own work or your own words is
not permitted.

Please ask questions freely in Lab, on the #data-structures Discord channel,
TL office hours, instructor office hours, or by opening a GitHub Issue with
@emgraber tagged at least 24 hours before the deadline.

Modifications to the gatorgrade.yml file are not permitted without explicit
instruction.

## Project Goals

This assignment invites you to run and observe two Python programs called
`compute-tuple-intersection` and `perform-apply-to-each`. Instead of using the
[Poetry](https://python-poetry.org/) tool for managing dependencies and
packaging these programs, these programs are scripts, without any dependencies
on other Python
packages, that you can run through the Python 3 interpreter. As you continue to
practice a different way to run a Python program, this project offers you the
opportunity to improve your understanding of how to compute the intersection (or
elements in common) between two tuples that can contain an arbitrary number of
values each of an arbitrary type. You will also learn more about high-order
functions as you implement a program that can apply an arbitrary function to the
contents of an arbitrary length list of `int` values.

## Project Access

After accepting you individual repository with the GitHub Classroom link,
use the `git clone` command to download the project from GitHub to
your computer. Now you are ready to add source code and documentation to the
project!

## Expected Output & Adding Functionality

If you change into the `source/` directory of your GitHub repository, you will
see two Python files called `compute-tuple-intersection.py` and
`perform-apply-to-each.py`. You can run the `compute-tuple-intersection.py`
program by typing `python compute-tuple-intersection.py` in your terminal
window. This program currently has several `TODO` markers asking you to add
source code from the text book to provide an implementation of a function with
the following signature: `def compute_intersection(tuple_one: Tuple[Any, ...],
tuple_two: Tuple[Any, ...]) -> Tuple[Any, ...]`. Once you have added the
required source code your program should produce the following output. Can you
explain why different calls to `compute_intersection` yield output with the
same elements but in a different order?

```shell
The first tuple: (1, 'a', 2)
The second tuple: ('b', 2, 'a')

The first intersection tuple: ('a', 2)
The second intersection tuple: (2, 'a')
```

The second program in the `source/` directory is called `perform-apply-to-each`.
Again, this program has several `TODO` markers that invite you to add source
code from the text book to finish the implementation of the function with the
signature `def apply_to_each(values: List[int], function: Callable) -> None`.
After you have added the required source code your program should produce the
following output. One interesting aspect of the `apply_to_each` function is that
it does not return any values, as indicated by the return type annotation of
`None`. If the function does not return a value, then how can it modify the
`values` input parameter of type `List[int]` as shown in the output? Finally,
you will note that `apply_to_each` accepts a `function` parameter of type
`Callable`, making it a higher-order function. What are the benefits of using
high-order functions in Python programs? How does `apply_to_each` use the
`function` parameter?

```shell
Values before transformations: [1, -2, 3.33]
Values after applying abs: [1, 2, 3.33]
Values after applying int: [1, 2, 3]
Values after applying squaring: [1, 4, 9]
```

## Running Checks

Since this project does not use [Poetry](https://python-poetry.org/) to manage
project dependencies and virtual environments, it does not support the use of
commands like `poetry run task ruff`.

### Gatorgrade

After you have added functionality and checked that your code produces the
expected output, the command `gatorgrade --config config/gatorgrade.yml`
will check your work with the automatic grader. If
your work meets the baseline requirements and adheres to the best practices that
proactive programmers adopt you will see that all the checks pass when you run
`gatorgrade`. All checks must pass in order to get 100% on this lab. All other
gatorgrade score are graded as 0%. Note, modifications to the gatorgrade.yml file
are not permitted without explicit instruction.

## Project Reflection

Once you have finished all of the previous technical tasks, you can use a text
editor to answer all of the questions in the `writing/reflection.md` file. Since
this is a source code survey, you should provide output from running each of the
provided Python programs on your own laptop and then explain how the program's
source code produced that output. A specific goal for this project is to ensure
that you can explain each component of a function's type signature, including
details about its inputs and outputs.

### Project Assessment

You may make an unlimited number of reattempts at submitting
source code and technical writing that meet all aspects of the project's
specification. This spec lab is graded pass/fail. Gatorgrade reports of 100%
meeting all the specs receive a grade of 100%. All other gatorgrade reports
result in a grade of 0%.

## Project Overview

After cloning this repository to your computer, please take the following
steps:

- Use the `cd` command to change into the directory for this repository.
- Change into the program source code directory by typing `cd source`.
- Add the requested code as described
  [above](#expected-output--adding-functionality)
- Run both of the provided Python scripts by typing the following:
  - `python compute-tuple-intersection.py`: demonstrate computation of tuple
    intersection
  - `python perform-apply-to-each.py`: demonstrate the use of a higher-order
    function
- Confirm that the programs are producing the expected output.
- Make sure that you can explain why the programs produce the output that they
  do.
- Run the automated grading checks by typing
  `gatorgrade --config config/gatorgrade.yml`.
- You may also review the output from running GatorGrader in GitHub Actions.
- Don't forget to provide all of the required responses to the technical writing
  prompts in the `writing/reflection.md` file.
- Please make sure that you completely delete the `TODO` markers from the provided
  source code and `writing/reflection.md`.
- Submit work to GitHub using git in the terminal
  - Open a terminal
  - `cd` to the project directory on your computer
  - type `git status` to see a list of files you have updated
  - type `git add .` to "stage" your files
  - type `git commit -m "PUT YOUR OWN SHORT MESSAGE"`
  - type `git push origin main`
  - type your ssh passphrase if requested
