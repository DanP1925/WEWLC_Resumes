# The Seam Model

One thing that nearly everyone notices when try to write tests for existing code is just how poorly suited code is to testing.

## A huge sheet of text (This is what people usually think)

A program can seem like a large sheet of text. Changing a little text can cause the meaning of the whole document to change, so people make those changes carefully to avoid mistakes.

## Seams (This is how it really is)

### Seam

> A seam is a place where you can alter behavior in your program without editing in that place.

For example, if we are calling a global funcion on another package. We can call a function that is on the same package and it will override its behaviour.
Or we can inject the class that uses that method with a test class based on that object.

## Seam Types

### Enabling Point

> Every seam has an enabling point, a place where you can make the decision to use one behavior or another

### Link Seam

When the compiler is building the code, it links multiple files together through imports.

### Object Seam

When the object calls a method, you can modify its behaviour by calling one son of the object that should be called.
