# How do I add a feature?

Once we have tests in place, we are in a better position to add new features.

## Test-Driven Development

1. Write a failing test case.
2. Get it to compile.
3. Make it pass.
4. Remove duplications.
5. Repeat

One of the most valuable things about TDD is that it lets us concentrate on one thing at a time. We are either writing code or refactoring; we are never doing both at once.

## Programming by Difference

1. Add new behavior (add new method to derived class)
2. Replace behavior (override base class method)
3. Re-use behavior (do nothing, default to inherited behavior)
4. Only changes in behavior require changes in program code
5. is_a relationship

It lets you add new functionality by abstracting a previous functionality and only modifying the new class. This is done by overriding the unnafected part of the old class that becames an abstract class now with the changed method becoming an abstract method that gets overrided by the old method abstracted or the new method that gets created for that.
