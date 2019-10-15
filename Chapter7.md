# It takes forever to make a change

## Understanding

In a well-maintained system, it might take a while to figure out how to make a change, but once you do, the change is usually easy and you feel much more comfortable with the system.

In a legacy system, it can take a long time to figure out what to do, and the change is difficult also.

## Lag Time

You should be able to compile every class or module in your system separately from the others and in its own test harness.

When you have that, you can get very rapid feedback, and that just helps development go faster.

## Breaking Dependencies

In object-oriented code, often the first step is to attempt to instantiate the classes that we need in a test harness.

When you are able to create an object of a class in a test harness, you might have other dependencies to break if you want to test individual methods.

### Build Dependencies

To figure out which dependencies will get in the way just attempt to use the class in a test harness.

When we have these clusters of classes under test, we have the option of changing the physical structure of our project to make builds easier.

#### The Dependency Inversion Principle

>When your code depends on interface, that depends is usually very minor and unobtrusive. Your code doesn't have to change unless the interface changes, and interfaces change far less often than code behind them.
