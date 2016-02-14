# refactoringkatatemplate

Step 1. Find a refactoring kata

Reasonable - https://github.com/adi-bolb/trivia/tree/master/java
Pretty Good - https://github.com/emilybache/Racing-Car-Katas
 
Step 2. Refactoring and Cleaning

I suggest that you probably:

* Clean it up based on best practices from Clean Code (safe refactorings guided by a tool)
* Try and write a test around it and use code coverage (run mvn cobertura:cobertura)
* Run Intellij > Analyse to tell you what's wrong with it - https://www.jetbrains.com/idea/help/code-analysis.html
* Run PMD - mvn pmd:pmd and look in target/site/pmd.html
* Run Findbugs - mvn findbugs:check

You could use this as a template and copy other refactorings in I guess.  There's a number of other things:

* You can glance at a small codebase and provide guidance on how it should be just based on single responsibility principle, number of classes, how easy it is change, good naming principles, comments, formatting and JDK best practices (e.g. use Guava Lists instead of creating ArrayLists).  Sometimes that's good enough and you don't need anything else.

* If you're going further then design should be guided by tools - e.g. run Intellij inspections to identify common bugs.  Alternatively, PMD and findbugs can be run against your code (complex conditionals - bad).  This is generally referred to as static analysis.  Going further look at software metrics (large classes - bad, classes with lots of dependencies - bad).