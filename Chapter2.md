# Working with Feedback

Edit and pray

`Testing to attempt to show correctiness`

Cover and modify

`Testing to detect change`

Unit testing ftw, feedback asap.
Helps to refactor.

## What is unit test

Unit tests: Tests in isolation of individual components of software.

Test Harness: The code written to excersice and the (tool) usually a framework needed to use it.

Issues with large tests:

* It gets harder to localize the specific issue there.
* Tests tend to take larger to execute.
* If you want to get full coverage, it is harder to get to some conditional branches with large tests.

Advantages of unit tests:

* They run fast
* They help us localize problems.

## Higher-Level Testing

It helps to pin behaviour to a specific class. After that then you can test for specific behaviour inside a class.

## Test Coverings

Is always better to have tests around the changes to make.

> Dependency is one of the most critical problems in software development. Much legacy code work involves breaking dependencies so that changes can be easier

### THE LEGACY CODE DILEMA

>When we change code, we should have tests in place
>To put tests in place, we often have to change code.

¯\\_(ツ)_/¯

When you break dependencies in legacy code, you often have to suspend your sense of aesthetics a bit.

## The Legacy Code change algorithm

1. Identify Change points
2. Find test points.
3. Break dependencies.
4. Write tests.
5. Make changes and refactor.
