# Serenity-BDD-with-Cucumber

Project Summary

This is a Spring-based test automation project that uses Serenity BDD and Cucumber to write acceptance tests for a Joke API service. The goal of the project is to ensure that the Joke API service behaves as expected when interacting with different joke providers.

**Key Components**

1. **Serenity BDD**: A BDD framework that provides a simple way to write feature files (tests) and step definitions (implementation code).
2. **Cucumber**: A testing framework that allows you to write tests in a natural language style.
3. **Spring Boot**: The underlying framework for the project, providing a robust and flexible foundation for building web applications.
4. **WireMock**: A library used to stub out dependencies and simulate API responses.


## Serenity BDD

[https://serenity-bdd.info/](https://serenity-bdd.info/)

Serenity BDD has been implemented in this project using the following approach:

1. **Step Definitions**: The `JokeStepDefinitions` class is created to define the step implementations for the feature files.
2. **Actions**: A separate package (`actions`) is created to contain classes that implement the actions described in the feature files, such as `JokeApiActions`.
3. **Steps Annotations**: The `@Steps` annotation is used to inject an instance of the `JokeApiActions` class into the `JokeStepDefinitions` class.
4. **Given-When-Then Syntax**: The feature file uses a Given-When-Then syntax to describe the scenario, and the corresponding step implementations are defined in the `JokeStepDefinitions` class.
5. Runner: The `SpringRunnerTests` class is a JUnit test suite that serves as the entry point for running Serenity BDD tests with Cucumber. This class is responsible for configuring and executing the tests.


## WireMock

WireMock is used in this project to simulate API responses for the Joke API service. Here's how it's used:

1. **Stubbing**: WireMock stubs are created to mimic the behavior of external APIs, such as joke providers. JokeApiStubs holds the stubs.
2. **Mocked Responses**: Mocked API responses are defined using WireMock's DSL (Domain Specific Language) to return specific data or error scenarios.
3. **Request Matching**: WireMock is used to match incoming requests against predefined mock responses.

Overall, WireMock is used to simulate the behavior of external APIs, allowing for faster and more reliable testing of the Joke API service
