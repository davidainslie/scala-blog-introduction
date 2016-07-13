# Scala Blog Introduction

We introduce Scala with some simple example code. See the [blog](https://davidainslie.github.io/scala-blog-introduction).

If you don't have Scala set up on your machine, see the footnote below.

To run test code (from a command prompt at the root of this project):
```
$ sbt test
```

There is also a Scala **worksheet**.

Scala has a REPL (Read, Evaluate, Print, Loop) that allows you *interact* with Scala by providing an environment, where your code is immediately interpreted and executed.
This shows to users, Scala's dynamic side - even though Scala is a statically typed language and applications must be first compiled before run, we can develop (try things out) as if the language was dynamic.

A **worksheet** represents a saved session of your dynamic interaction.

Typing **scala** at a command prompt, brings up the Scala REPL. Within your project, such as this one, you can instead type **sbt** followed by **console** to bring up a REPL session that has access to all your project code.

The easiest was to work with a Scala worksheet, is within an IDE such as Intellij or Eclipse. E.g. in Intellij, open the file **introduction-worksheet.sc** which is under the **test** directory and there you can run the worksheet in interactive mode to see results immediately.
Note that the file in question ends with **.sc** which is essentially stating that the contents is a **script** and not full blown Scala, where the file would end in **.scala**.
As pointed out in the introduction blog, Scala grows with the needs of developers/systems, and Scala can start as small as a shell script e.g. replacing your bash scripts with Scala.

From the command prompt (within the root of this project) you can do the following:
```scala
$ scala

scala> :load src/test/scala/introduction-worksheet.sc
// WHERE YOU WILL SEE THE OUTPUT
x: Int = 2
res0: Int = 3
res1: scala.collection.immutable.IndexedSeq[Int] = Vector(2, 4, 6, 8, 10, 12, 14, 16, 18, 20)
res2: Int = 55
warning: there was one feature warning; re-run with -feature for details
res3: Int = 55
passed: List[Int] = List(76, 82, 88, 90)
failed: List[Int] = List(49, 58)
```

and within the above REPL, you can continue to play around e.g. just type **x** followed by <enter>

## Footnote

Scala runs on the JVM. You need Java installed, and then install Scala.

The following notes are for Mac users. Regarding other platforms, please see the links provided.

#### Installing Homebrew for Mac
The following installations use [Homebrew](http://brew.sh/). Paste the the following at a command/terminal prompt:
```
$ /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

#### Installing Java on your computer

To install Java, either go to the [Java website](http://www.oracle.com/technetwork/java/javase/downloads/index.html) or, if you are lucky to have a Mac with Homebrew installed, then the following (from a command console) will install the latest [Open JDK](http://openjdk.java.net/):
```
$ brew update
$ brew tap caskroom/cask
$ brew install brew-cask
$ brew cask install java
```

#### Installing Scala on your computer

To install Scala, either go to the [Scala website](http://www.scala-lang.org/download/) or, if you are lucky to have a Mac with Homebrew installed, then the following (from a command console) will install the latest version of Scala:
```
$ brew install scala
$ brew install sbt
```

From these the above commands: Scala is... well, you can guess.

SBT is Scala's interactive build tool.