# Continuous Integration

**Continuous Integration (CI)** is another key practice in many Agile methods (perhaps most notably [Extreme Programming](https://en.wikipedia.org/wiki/Extreme_programming)).

Team working is all about process, which is the key to happier developers and better quality software.

As a developer, you should be using [Test Driven Development](../05a%20Verification%20%26%20Validation%20and%20Test%20Driven%20Development/README.md), where you write tests, check your code passes and can tell it works.

HOWEVER....! Sometimes you will face a problem where everything seems fine, then you merge it into production, and suddenly it doesn't, leading to the super-common refrain of:

![It works on my machine](CI%20resources/IWOMM.png)

It could be that you're working in different OSs to your team mates, for example - you could be working on Windows, a team mate is working on a Mac, and the production system is Linux. One way to avoid problems like this is to automate as much of the testing as possible - unit testing, the different modules, the integration systems on our own machines and on the production systems.  Having an **automated Quality Assurance system** can solve our problems - and part of this is Continuous Integration (CI), followed by Continuous Deployment (CD).

![Automated QA system](CI%20resources/CICD.png)

**Continuous Integration** automates merging code from different developers, running it through the test suites and integrating it into the main branch of the development environment.  It is important for Agile, because it allows us to merge small amounts of code often, without having to spend a lot of time manually running tests.

**Continuous Deployment** is a process where once CI is completed, the changes to the code are automatically released to the client/users.

We will talk more about CD later in the Teaching Block, but you should be planning to build CI into your system so it's in place around the time of the MVP.

## Why CI?

Continuous Integration is a driver for efficiency and to increase [code coverage](../05a%20Verification%20%26%20Validation%20and%20Test%20Driven%20Development/README.md#code-coverage) - if your test coverage is high and it's automated, you're able to spot a lot more mistakes than if you are testing manually.

## CI is not just automation!

There are lots of tools to help you, and we have listed some below - but remember, **automation is the easy part of CI**! You'll need a strong bedrock of a robust test suite, which in turn relies on a thorough understanding of the requirements of the system.  When we say we expect to see your projects having CI in place, we are talking about the whole process, not just the automation!

## You're not expected to have CI in place now - but we'd like you to understand it!

CI is something we expect in SEP projects.  Most teams will not be ready for this now, but read the workbook to get a general idea of the principles, and come back to it later, when you're ready to implement. The minimum we want you to do now is to add a GitHub Action to your project.

---

## Continuous Integration in Practice

Below, we'll explore some tools that allow us to implement CI in practice. These may not cover the tech stack you are using - if they don't, **search for tools yourself** and practice some simple tests. We've included some examples from previous projects.

### Introduction to GitHub Actions

**[GitHub Actions](https://docs.github.com/en/actions)** are tasks that you can set up within GitHub which automatically run a *workflow* of testing, building and deploying within a virtual machine hosted on GitHub. These are typically used for Continuous Integration (CI) and Continuous Deployment (CD).

Each workflow is defined by a `.yml` config file stored in the `.github/workflows` directory in your repository. We do not recommend creating one from scratch, as there are templates available for almost every task. These files define:

- What the workflow will do
- When the workflow will run
- Which OS will run the workflow (e.g. Ubuntu, Windows or MacOS)
- Which third-party applications it will interact with

**Take a look at the Actions tab of your repository** and look through the descriptions of the templates. No need to set them up now, but can you get an idea of which look useful? Look at one of the `.yml` config files: can you get a high-level idea of what it is trying to define?

### Examples from previous projects

**Flutter:** [Harry Greentree](https://github.com/lm22433), one of our previous lead TAs, has written a [comprehensive guide to CI, CD and linting in Flutter](https://github.com/spe-uob/knowledge-hub/blob/main/Flutter%20-%20CI%20and%20Linting.md) that we strongly recommend if you are building in Flutter. It uses examples from his 2023-4 team, [2023-MarineConservationApp](https://github.com/spe-uob/2023-MarineConservationApp), which is also worth a look.

**Unity:** Unity and GitHub have some quirks, but [Game.ci](https://game.ci/) has everything you need for CI. Previous mentor [Phillip Daniel](https://github.com/phil-daniel) has written [a guide to CI for Unity with game.ci](https://github.com/spe-uob/knowledge-hub/blob/main/Unity%20-%20CI%20with%20game.ci.md), which we really recommend reading. His team's repo, [2023-SkillsLearningGame](https://github.com/spe-uob/2023-SkillsLearningGame), used Game.ci (they were a 2-person team for most of the project, so bear that in mind!).

> [!TIP]
> We always recommend former student James Millan's [guide to using Unity with Git](https://github.com/spe-uob/knowledge-hub/blob/main/Using%20Unity%20with%20Github.md) for any Unity project. If you haven't already read it, read it now!

**iOS (including Flutter):** building and testing iOS apps requires macOS runners (`macos-latest`) because of Xcode dependencies. These consume 10 times the compute minutes of Linux runners, so they can quickly deplete your allocated minutes and, in previous years, have used up the entire SEP organisation budget.

> [!WARNING]
> **Use macOS runners only when necessary (e.g., for iOS builds)** and keep an eye on how many minutes they are consuming. Overspending can mean we have to temporarily close the organisation!
>
> If you want technical help to avoid macOS runner problems, come to the drop-ins!

---

## Task 1: Add a GitHub Action to your group's repository

With this understanding of Continuous Integration, **as a team**, add a GitHub Action to your team's repository.  We'd recommend you also individually try CI on a project in your personal repo, so you can understand how CI works.

1. **Set up the mechanisms now**, even if your project isn't particularly substantial. It will be there ready and waiting for when you need it - there are benefits to having Continuous Integration from an early stage of your project.

2. **Check that your CI pipeline is operating correctly** by pushing changes to your repo and ensure that your test cases are being rerun each time.

3. **Introduce a bug into the code** - just to check that failed tests are indeed reported by GitHub.

> [!TIP]
> Don't forget to add GitHub Actions to the [User Instructions and Developer Instructions](../../README%20requirements/README.md#what-to-include-in-your-readme) on your README \
>   \
> You will need to frame your information differently for both, and might want to direct readers to a document, but every time you add something like CI, add a task to the Kanban board to update the README, so you don't forget.

---

## Linters

**Linters** or **lint tools** are static code analysing tools that check the quality of your code and can be used in CI.  Linters do not check if the code is *correct*, as in if the code will do what you want it to do, but if it is *well-written*. They can check for bugs, style, code complexity and more, and they can generate warnings or error messages for bad practice.

You can build linting into your CI through GitHub Actions, with thresholds so that code cannot be merged at all if it has a certain percentage of errors.

Some software development companies are very pedantic about using linters, and will set a 100% error-free threshold; others won't care at all!

Linters can also be controversial, with some people seeing them as a distraction - [there's a pro-linting blog on Stack Overflow that touches on why](https://stackoverflow.blog/2020/07/20/linters-arent-in-your-way-theyre-on-your-side/). There can also be an overhead in working out how to respond to them (there are tools to auto-fix errors caught by linters, but if you're using them, you probably want the reminder on how to improve your code). You might want to try them out and then decide not to use them, but it's important you know they're an option.

**We are not enforcing linters in SEP**, but if you choose to use one, tell us in the viva!

Linters are **language specific**, so while previous students generally recommend [Pylint](https://pypi.org/project/pylint/) for Python, what you will use depends on what you're using to code. Google to see what's available for your project.

**If you're using C#**, previous mentor [Phillip Daniel](https://github.com/phil-daniel) has written a [guide to Linters for Unity, using Super-Linter](https://github.com/spe-uob/knowledge-hub/blob/main/Unity%20-%20linting.md), which we recommend!

**If you're using Dart (for example, with Flutter)**, previous mentor [Harry Greentree](https://github.com/lm22433) has written a [comprehensive guide to Continuous Integration, Continuous Deployment and linting in Flutter](https://github.com/spe-uob/knowledge-hub/blob/main/Flutter%20-%20CI%20and%20Linting.md), which we also recommend!

> [!TIP]
> **How to pick tools like linters**
>
> When you're picking tools like linters, things to take into account include:
>
> - will it integrate with GitHub Actions?
> - is it based on actual [language standards](https://en.wikipedia.org/wiki/Programming_language_specification)?
> - how easy is it to configure?
> - how much does it cost? For SEP it should be free!

---

## Dependency checking

One of the risks of using third-party libraries or components in your software is if they have security vulnerabilities that impact your product.  It is also time-consuming to keep track of upgrades you'll need to make for security purposes.  There are reports produced that will identify issues, but it is much easier to automate this process.

Some software companies may use paid-for systems like [SonarQube](https://www.sonarsource.com/products/sonarqube/) to identify issues, but we recommend you use GitHub's [Dependabot](https://docs.github.com/en/code-security/getting-started/dependabot-quickstart-guide), as it is free to use, obviously integrated into GitHub's ecosystem and good enough for [the British Government Digital Service](https://docs.publishing.service.gov.uk/manual/manage-dependencies.html)!
