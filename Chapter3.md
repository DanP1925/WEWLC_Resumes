# Sensing and Separation

Dependencies among classes can make it very difficult to get particular clusters of objects under test.

When we want to get tests in place, there are two reasons to break dependencies:

* **Sensing** : To sense when we can't access a value our code computes. Like when trying to access a value from a web service.
* **Separation** : To separate when we can't even get a piece of code into a test harness to run. If you need to create the whole system to do a test, is going to be too hard to test new stuff.

## Faking Collaborators (Best Technique for Sensing)

If we can put some test code instead of real code just for testing, this can help us sense the values when interacting with that code.

### Fake Object

A fake object is an object that impersonates some collaborator of your class when being tested. Usually this is done via interfaces and a fake implementation of an object.

> When we write tests for individual units, we end up with small, well-understood pieces. This can make it easier to reason about our code.

### The two sides of a fake object

Usually the fake object should have two kinds of methods: The ones that respond like the real object should do and the ones used for testing the fake object.

On a test this is represented by instanciating a fakeObject for having the extra methods and assigning it to another object as the interface of the real object.

## Mock Objects

Mock objects are fakes that perform assertions internally. They are usually helpful to let you test without writing a full fake object.
