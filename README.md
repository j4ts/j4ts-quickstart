# j4ts-quickstart
A quickstart project to get started with Java library support for TypeScript/JavaScript

DISCLAIMER: this project is under construction and is open for contributions.

## Expected content
- A basic support for a simple Java API (for instance the BigDecimal class) so that users can clone the project and get started from there
- A HOWTO (in this README), that explains all the steps for creating a new Java API support.

# HOWTO

(Still under construction)

In this section, we explain how to create a new support for an existing Java API and the required steps to create/compile/publish the project.

- Step 1: Create the J4TS project
Just clone this repo to start from an existing minimalistic project.

- Step 2a: Import the source code of the Java API
If you have the source code of the Java API you need to support, one way to start is to import the Java source code as is and try to compile it with JSweet (``mvn generate-sources``). It is likely that it will not compile as is because it will miss dependencies to other Java API. In that case, go to step 3.

- Step 2b: Write a minimalistic version of the Java API in Java
This is the preferred choice if you don't have/own the source code, or if the source code is too Java-platform-dependent to be transpiled easily.  

- Step 3: Solve external dependencies
If you imported existing source code, it is most likely that it depends on a Java library. If this Java library is already supported, you can just add it as a Maven dependency. Otherwise, you also need to provide support for this library. This is where it can become complicated...
It is likely that an existing JavaScript library will make the implementation much simpler (for instance, for implementing Java ``BigDecimal``, using the JavaScript library ``big.js`` will save you a lot of time - eventhough the behavor might not be fully similar to Java).

- Step 4: Compile and share
TBD
