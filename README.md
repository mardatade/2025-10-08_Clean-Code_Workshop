# Clean Code Workshop

Example research project: There's a small [example research project](example_project/README.md) which can serve as a playground for our activities in the workshop.

## Possible tasks

During the workshop, we can use the example project to explore different aspects.

### "Metrics" for scientific code

Let's find and define metrics describing about which properties of scientific code or scientific software a user / developer may care.

Suggestions:
- readability
- flexibility
- ...

### Analysis

Before even changing any code, we can take a look at the internal structure and identify potential problems (or strenths) of the existing implementation.
Questions to be asked could be:

1. What assumptions are made in the implementation which may not be known to a new users? Is there anything that can go wrong without the user noticing?

1. Which aspects of the compute environment may be different for different users?

1. Are there parts of the logic which could be indirected (encapsulated in, e.g., a function) or which are currently indirect and which could be used explicitly?

1. If you're familiar with UML or other ways to graphically represent software (consider [mermaid](https://mermaid.js.org/)), you could visualize the existing software using these approaches.

1. How would you rate the existing implementation using the metrics _flexibility_, _readability_, _testability_, _time for changes_?

### Refactoring

The existing example project consists of two Jupyter Notebooks one of which is used like a module and the other is used like a scripted application.
From here, we can take very different routes.

We can either tackle issues found in the analysis part above.
Possible projects include:

1. Adding tests and aiming for high test coverage.

1. Writing a package for the library parts.

1. Catch and either fix or report possible wrong user input.

1. Work towards elegant (to be defined) code especially in the user-facing parts.

Or we go for a few extreme (and maybe fun) approaches:

1. Refactoring into maximally imperative code (no loops, no functions, no objects).

1. Refactoring into maximally object-oriented code.

1. Complete obfuscation: How to rewrite the code into maximally un-intelligible form without changing its results.

## Links

- While there's dozens of approaches of defining and maintaining Python packages, a good basic intro is provided by the offical [Python Packaging Guide](https://packaging.python.org/).

- [Mermaid.js](https://mermaid.js.org) for building quick graphical representations of software.

- A prior [MarDATA course on Software Testing](https://github.com/mardatade/Course-Software-Testing) including a set of slides.

- [The Turing Way](https://book.the-turing-way.org/) online book which, among other topics, covers code quality for reproducible research.

-  Talk by David Beazley: [The problem with the problem](https://youtu.be/t-IUY6QrJyU)

- Talk by Rich Hickey: [Simple made easy](https://youtu.be/SxdOUGdseq4) about (hidden) complexity