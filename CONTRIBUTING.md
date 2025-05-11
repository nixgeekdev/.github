# Contributing to NixGeek.Dev Projects

First off, thanks for taking the time to contribute! ❤️ 
All types of contributions are encouraged and valued.

## Quick Reference

This is a quick reference for how to set up the development environment and
contribute with a PR. It assumes you're familiar with contributing to projects,
and with [Git][git], [GitHub][github], [Gradle][gradle], and a JVM language 
such as [Kotlin][kotlin], [Clojure][clojure], or [Java][java]. 

These instructions will work with at least [Bash][bash] and 
[PowerShell][powershell], and should work on other shells. On Windows, use 
PowerShell, not CMD. 

### Toolchain

These tools are known to work. You can use others if you wish, but YMMV.

- [Azul (zulu) JDK 21][zulu]
- [Kotlin][kotlin] 2.1.20 or newer
- [Gradle][gradle] 8.14 or newer
- [IntelliJ][intellij] 2025.1.1 or newer
- [Git][git]

If you don't want to use a community version of IntelliJ or don't want to 
spend the money on a license for IntelliJ Ultimate, then a good alternative 
is [Visual Studio Code][vscode]. To manage multiple versions of JVM related tools, we 
highly recommend the use of [sdkman][sdkman]. The code and command examples below 
also use [Github CLI][githubcli], but those could be easily translated to plain `git` 
commands.

### Setup Development Environment

To quickly setup a developmen environment for the NixGeek.Dev projects, simply 
run the following commands:

```bash
$ curl -s "https://get.sdkman.io" | bash
```

Then restart your shell or reload your shell `rc` file and run the following commands:

```bash
$ sdk install java 21.0.7.crac-zulu
$ sdk install kotlin 2.1.20
$ sdk install gradle 8.14
```

Next, fork and clone one of the projects:

```bash
$ gh repo fork --clone nixgeekdev/passphraser4k
$ cd passphraser4k
```

Then sync gradle, create a new branch, and start coding:

```bash
$ ./gradlew build --refresh-dependencies
$ git checkout -b my-new-branch-name
```

### Development Standards

We stick to a few simple rules to keep our codebase in good shape.

1. Formatting and linting is handled by [detekt](https://github.com/detekt/detekt). Builds will 
   fail if your code does not pass these checks.
    1. To lint your code: `./gradlew check`
2. Test your code.
    1. All code should almost always have unit tests.
    2. We use the [kotest](https://kotest.io/) framework to implement our tests.
    3. Make sure all tests are passing before submitting a PR for review.
3. Document your code.
    1. Try to imagine what a new developer with no context will need to know about your code. If 
       it's not obvious, document it.
    2. Include links to reference materials you use.
    3. Use [KDoc](https://kotlinlang.org/docs/kotlin-doc.html#kdoc-syntax) syntax.
  
### Create a Pull Request

Make your changes and commit them. Add tests that demonstrate that your code works, and ensure 
all tests pass. Change documentation if needed to reflect your change. Adding a changelog entry 
is optional, a maintainer will write one if you're not sure how to. Most of our projects use 
[Github Releases][ghrelease] to track changes and most of our projects will generate a release 
via a Github Action.

Use the GitHub CLI to start your pull request creation. Specify the target branch with `-B`. 
The `main` branch is most likely the target for your PR, unless otherwise noted in the 
project's `readme` file.

```bash
$ gh pr create --web --base main
```

[Github Actions][ghactions] CI will run after you create the PR. If CI fails, you can click to see 
the logs and address those failures, pushing new commits. Once you feel your PR is ready, click the 
"Ready for review" button. A maintainer will review and merge the PR when they are available.

_**Additional project-specific details are available in each projects `readme` file.**_

## Code of Conduct

The NixGeek.Dev organization has a [Code of Conduct](CODE_OF_CONDUCT.md) to which all contributors 
must adhere. Read it and abide it!

## Developer's Certificate of Origin 

As part of your contributions to NixGeek.Dev, you will be asked to accept the
Developer's Certificate of Origin. The below text will automatically be included in 
every pull request.

```text
By making a contribution to this project, I certify that:

 (a) The contribution was created in whole or in part by me and I
     have the right to submit it under the open source license
     indicated in the file; or

 (b) The contribution is based upon previous work that, to the best
     of my knowledge, is covered under an appropriate open source
     license and I have the right under that license to submit that
     work with modifications, whether created in whole or in part
     by me, under the same open source license (unless I am
     permitted to submit under a different license), as indicated
     in the file; or

 (c) The contribution was provided directly to me by some other
     person who certified (a), (b) or (c) and I have not modified
     it.

 (d) I understand and agree that this project and the contribution
     are public and that a record of the contribution (including all
     personal information I submit with it, including my sign-off) is
     maintained indefinitely and may be redistributed consistent with
     this project or the open source license(s) involved.
```

[git]:https://git-scm.com/
[github]:https://github.com/
[githubcli]:https://cli.github.com/
[ghrelease]:https://docs.github.com/en/repositories/releasing-projects-on-github/managing-releases-in-a-repository
[ghactions]:https://docs.github.com/en/actions
[gradle]:https://gradle.org/
[kotlin]:https://kotlinlang.org/
[java]:https://www.java.com/en/
[clojure]:https://clojure.org/
[bash]:https://www.gnu.org/software/bash/
[powershell]:https://learn.microsoft.com/en-us/powershell/?view=powershell-7.5
[zulu]:https://www.azul.com/downloads/?package=jdk#zulu
[intellij]:https://www.jetbrains.com/idea/
[vscode]:https://code.visualstudio.com/
[sdkman]:https://sdkman.io/
