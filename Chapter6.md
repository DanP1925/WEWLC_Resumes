# I don't have much time and I have to change it

Adding tests and refactoring code is extra time that maybe we don't have. On the best case scenario, the code is organized enough to get easier and faster changes next time. On the worst case scenario, the code is easier to read even if we won't need to use it.

## Sprout Method

When you add new code to a specific part as a call to a method and without changing the code as much as possible.

1. Identify where you need to make your code change
2. If the change can be formulated as a single sequence of statements in one method, write down a call for a new method that will do the work involved and then comment it out.
3. Determine what local variables you need from the source method, and make them arguments to the call.
4. Determine whether the sprouted method will need to return values to source method. If so, change the call so that is return value is assigned to a variable.
5. Develop the sprout method using TDD.
6. Remove the comment in the source method to enable the call.

### Sprout Method Advantages

You are clearly separating the new code with the old code as the new code will always have tests.

### Sprout Method Disadvantages

You give on the class that contains the sprout method and it continues smelling bad.

## Sprout Class

When some class is such a mess that we add a new class that complements it and is completely testable.

1. Identify where you need to make your code change
2. If the change can be formulated as a single sequence of statements in one place in a method, think of a good name for a class that could do that work. Afterward, write code that would create an object of that class in that place, and call a method in that will do the work that you need to do; then comment those lines out.
3. Determine what local variables you need from the source method, and make them arguments to the class constructor.
4. Determine wheter the sprouted class will need to return values to the source method. If so, provide a method in the class that will supply those values, and add a call in the source method to receive those values.
5. Develop the sprout class with TDD.
6. Remove the comment in the source method to enable the object creation and calls.

### Sprout Class Advantages

The advantage is that when creating a new class you can be completely sure that the class would be fully tested.

### Sprout Class Disadvantages

The disadvantage is that complexity gets worse because you start creating multiple disconnected classes.

## Wrap Method

When a method has to be added so it works at the same time than another method.

1. Identify a method you need to change
2. If the change can mbe formulated as a single sequence of statements in one place, rename the method and then create a new method with the same name and signature as the old method.
3. Place a call to the old method in the new method.
4. Develop a method for the new feature. Test first and call it from the new method.

### Wrap Method Advantages

Helps when is difficult to test the calling of a method. Also it lefts the method exactly the same as how it was before.

### Wrap Method Disadavantages

It leads to poor method naming.

## Wrap Class

Uses decorator pattern to extend the functionality of a current method.

1. Identify a method you need to change
2. If the change can be formulated as a single sequence of statements in one place, create a class that accepts the class you are going to wrap as a constructor argument.
3. Create a method on that class, using TDD, that does the new work. Write a new method that calls the new method and the old method on the wrappet class.
4. Instantiate the wrapper class in your code in the place where you need to enable the new behaviour.

### When to use Wrap Class

* The behaviour I want to add is completely independent, and I don't want to pollute the existing class with unrelated behaviour.
* The class has grown so large that I really can't stand to make it worse.
