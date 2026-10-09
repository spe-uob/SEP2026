# Architecture - Technology Stacks

## Introduction

This week we'll introduce you to software architecture and how to make decisions about and describe your tech stack.  

The workshop should give you an understanding of some of the factors that play into choosing an appropriate technology stack for a software project, and you should have already started to **choose a tech stack for your project**. You should also start thinking about which **Software License** you will use for your project. 

> [!IMPORTANT]
>  Your tech stack can and will change over time - this might feel scary, but you can evolve it, change parts of it and even burn everything to the ground and start again - as the [highest marked team in 2023-4](https://github.com/spe-uob/2023-MarineConservationApp) did!


> [!TIP]
> Every time you see a task in the workbooks, add it as an issue in your [Kanban board](https://github.com/spe-uob/SEP2025/tree/main/Weekly%20Workbooks/02%20Software%20Processes#task-5-set-up-your-kanban-board-and-add-your-first-issues)!
> You can decide how to action it in the next team meeting, but this way you won't lose it.   

## Introduction to Software Architecture and Architecture Diagrams

<a href='https://github.com/spe-uob/SEP2025/blob/main/Weekly%20Workbooks/03%20Architecture%20-%20Technology%20Stacks/TechStack.pdf' target='_blank'> ![](../../resources/icons/slides.png) </a> 

Click the icon to bring up the slides from the lecture - you'll need to download them to see them all!

Read the slides from the lecture and make sure you understand them.  You'll need to draw your architecture diagrams and add them to the README and `DOCS` folder - some tools you might want to use are [draw.io](https://app.diagrams.net/), [LucidChart](https://www.lucidchart.com/pages/) or [Miro](https://miro.com/diagramming/what-is-software-architecture-diagramming/).


## Tech Stacks

In this workbook, you are tasked with evaluating a variety of tech stacks against the requirements of your project. One of the workshop tasks is to **complete the table at the end** to guide your analysis and decision-making. Below we have provided a brief overview of some common tech stacks used in past projects and signposts to resources. 

The examples are just a selection of popular tech stacks and this is not an exhaustive list - you can choose an unlisted tech stack if you believe it is appropriate. However, do your own research and analysis and speak to your mentor and/or visit the drop-in if you are unsure.

Note that the intention of this week is **not** to *teach* you a tech stack directly but to allow you to gain the independent skills required to grasp a new technology. Many frameworks and libraries have their own tutorials and 'get started' documentation, which, frankly, would not add value to recreate within these workbooks. Finding useful and informative tutorials and documentation is a skill in of itself. These skills are vital in industry where changing trends in technology require developers to pick up unfamiliar tools and integrate them into systems.

In this workbook, we give you examples of previous student projects - these examples should not be taken as the gold standard or as perfect work. While looking at their work, you should still maintain a critical eye to good and bad practices and to the relevance to *your* project. All projects are unique, so a method a past team has used may not necessarily be relevant to you.

When making the choice, you must consider the languages **all** your team can use - if some members already have skills in a language, please work together to make sure everyone understands, so you can all work on the code.

#
### Example Stack 1: Web App

Before choosing a web app, it is important to understand how this is different from a website. 

* **Websites** are typically static or informational in nature, providing content like text, images, and links that users can view but not interact with beyond simple navigation. 

* **A web app** is an interactive, dynamic website that offers more complex functionality, allowing users to perform specific tasks online. Unlike static websites, web apps are built to handle user inputs, process data, and provide real-time responses, often resembling the behaviour of desktop or mobile applications. Web apps often require back-end services for data processing and are distinguished by their interactive elements, such as forms, dashboards, and user accounts, which go beyond simple content display.

To achieve the scope and complexity of a project for SEP, browser-hosted projects should function as web apps and not just as websites. However, in some projects, a website might be appropriate to accompany other components - the key thing to note is that generally *just* making a website is not enough for SEP.

- **Languages:** JavaScript/TypeScript, HTML, CSS
- **Back End:** [Node.js](https://nodejs.org/en) 
- **Databases:** MySQL, PostgreSQL, MongoDB, and others
- **Targeted Platform:** Browser
- **Example Project:** [2023-RoboSim](https://github.com/spe-uob/2023-RoboSim)

or 

- **Languages:** Java, JavaScript, HTML, CSS
- **Framework:** [Spring Boot](https://spring.io/) with [Thymeleaf](https://www.thymeleaf.org/)
- **Databases:** [Works with SQL or NoSQL databases](https://docs.spring.io/spring-boot/reference/data/index.html)
- **Targeted Platform:** Browser
- **Example Project:** [2023-CityFarm](https://github.com/spe-uob/2023-CityFarm) - their architecture diagram is below:

![Branches diagram](https://github.com/spe-uob/SEP2024/blob/main/resources/CityFarm.png)


Choosing which tech stack to use is very subjective.  Springboot is really good at interacting with databases and serving up data - to do the same tasks in Node.js, you'd need to find a good library; however, *if* you find a good library, which could be through the package manager [npm](https://www.npmjs.com/) you might find the tasks easier.  

[Spring Initializer](https://start.spring.io/) is a project creation wizard you might want to use to get started.  

#
### Example Stack 2: Cross-Platform / Mobile Applications

**Cross-platform applications** are designed to run on multiple operating systems or platforms, such as Windows, macOS, Linux, or mobile systems like iOS and Android, without requiring significant modification. These applications are typically developed using frameworks or tools that enable compatibility across different environments, by abstracting the platform-specific details. This allows developers to write code once and deploy it across different platforms, reducing development time and ensuring consistency in functionality and user experience across devices.

This could be a good option if your client requires the application to run on multiple platforms.

- **Languages:** [Dart](https://dart.dev/)
- **Framework:** [Flutter](https://flutter.dev/)
- **Databases:** [PostgreSQL](https://www.postgresql.org/)
- **Example Project:** [2023-MarineConservationApp](https://github.com/spe-uob/2023-MarineConservationApp) - their Architecture diagram is below:

![Branches diagram](https://github.com/spe-uob/SEP2024/blob/main/resources/MarineConservationDiag.jpg)


Another notable mention, which is likely more popular than Flutter, is [React](https://react.dev/) which is a framework written in JSX or TypeScript. 

> [!CAUTION]
> If you are using Flutter/React, be very careful when you started on Continuous Integration and Continuous Deployment, as it can get very expensive and crash our Organisation!  There are articles on [CI for Flutter](https://github.com/spe-uob/knowledge-hub/blob/main/Flutter%20-%20CI%20and%20Linting.md) and [CD for Flutter](https://github.com/spe-uob/knowledge-hub/blob/main/Flutter%20-%20CD.md) on the Knowledge Hub.

#
### Example Stack 3: Apple Native Applications

**Apple native applications** are designed specifically for iOS and macOS platforms. This can be advantageous when seamless integration with Apple’s ecosystem and hardware are desired. These applications are typically written in Swift which is a language developed by Apple.

- **Languages:** [Swift](https://developer.apple.com/swift/)
- **Front End:** [SwiftUI](https://developer.apple.com/xcode/swiftui/) or [UIKit](https://developer.apple.com/documentation/uikit/)
- **Databases:** MySQL, PostgreSQL, MongoDB, and others
- **Targeted Platforms:** iOS & macOS 
- **Example Projects:** [2023-AIAREnhancedTech](https://github.com/spe-uob/2023-AIAREnhancedTech) & [2023-FriendlyCognitiveTask](https://github.com/spe-uob/2023-FriendlyCognitiveTask)

**Warning:** Collaborating on Xcode requires an [Apple Developer account](https://developer.apple.com/) which the Tech Hub can buy for you - email [engf-tech-hub@bristol.ac.uk](mailto:engf-tech-hub@bristol.ac.uk), however, this has historically taken some time to arrange. 
> [!CAUTION]
> **DO NOT PAY FOR ANYTHING YOURSELF!!**

#
### Example Stack 4: Games & 3D Environments

**Games and 3D environments** are highly interactive applications that often involve real-time rendering, physics simulations, and user-driven experiences. These applications are typically built with powerful game engines that provide the tools and libraries necessary for developing immersive, graphically-rich experiences. Unity is a popular framework for developing games and 3D applications due to its wide platform support and extensive asset library.

- **Languages:** C#
- **Framework:** [Unity](https://unity.com/)
- **Databases:** C# libraries can connect to a variety of SQL or no-SQL databases.
- **Targeted Platforms:** Windows, Linux, macOS, iOS, Andriod and others.
- **Example Projects:** [2023-Edutopia](https://github.com/spe-uob/2023-Edutopia) & [2023-SkillsLearningGame](https://github.com/spe-uob/2023-SkillsLearningGame) (This has some interesting design documents in their 'docs' folders that you might want to take inspiration from.)

Unity has a steeper learning curve than other tech stacks and is harder to integrate with GitHub. It will require using [GitLFS](https://docs.github.com/en/repositories/working-with-files/managing-large-files/installing-git-large-file-storage). 

A previous mentor wrote a useful article on [using Unity with Github](https://github.com/spe-uob/knowledge-hub/blob/main/Using%20Unity%20with%20Github.md) which we recommend you read if you're thinking about using Unity. There are also Knowledge Hub items on [Continuous Integrations and Deployment in Unity](https://github.com/spe-uob/knowledge-hub/blob/main/Flutter%20-%20CD.md) and [linting for Unity](https://github.com/spe-uob/knowledge-hub/blob/main/Unity%20-%20linting.md).

#
## Task 1: Tech Stack Analysis

Read the examples above and do further research into any tech stacks you believe will be relevant to your project. 

Once you have a good high-level understanding of each, **work as a team to fill out the table below** for three or more tech stacks. Completing this analysis should open up a discussion within your team as to which tech stack to use within the project - and hopefully reach a decision on which to go forward with. 

**If you are still unsure of which tech stack to use**, speak to your mentor or come to the drop-in sessions, where we can help you. 

For ease of use, we have also provided this table in a [Word Document](https://github.com/spe-uob/SEP2025/blob/main/Weekly%20Workbooks/03%20Architecture%20-%20Technology%20Stacks/tech-stack-analysis.docx) and [PDF](https://github.com/spe-uob/SEP2025/blob/main/Weekly%20Workbooks/03%20Architecture%20-%20Technology%20Stacks/tech-stack-analysis.pdf).

| Tech Stack | Description | Fit to Project | Experience in Team | Maintenance | Risks |
| :--------: | ----------- | -------------- | ------------------ | ----------- | ----- | 
| A          |             |                |                    |             |       |
| B          |             |                |                    |             |       |
| C          |             |                |                    |             |       |

## Open Source Software and Software Licences

### Open Source Software

You will probably already know a few specific examples of Open Source software projects. You will undoubtably have benefitted from Open Software (even if you didn't realise it at the time). Two high-impact examples of Open Source initiatives that you will probably encounter on a daily basis are Linux operating systems and Android OS. Some of you might even have contributed to the development of Open Source software yourselves.

In SEP, most teams will build Open Source software as part of their project and the majority of teams will certainly link to existing Open Source libraries. However, it is important to appreciate that the use and provision of Open Source is governed by various rules and regulations. It is essential that we understand these in order to stay out of legal trouble!  

### Software Licences

For most of you, SEP will be your first foray into professional software development. As professionals, we need to think not only about the technical components of a system but about the legal aspects as well. An important topic within this area is that of software licensing. 

**Licences** are legal instruments governing the use or redistribution of software.  They are not [Patents](https://www.gov.uk/patent-your-invention), which in the UK are 5-year protections for inventions, and prevent other people from implementing an idea *any* patented software.  Instead, licences protect a *specific piece* of software.  

You need a licence because, without it, the default [copyright laws](https://www.gov.uk/copyright) apply. This means you retain all the rights and no one may reproduce, distribute or create derivative works.  Everybody who contributes to your project also becomes an exclusive copyright holder and to use the code, people must contact the author directly and ask permission.  

Licenses also make it clear what happens if something goes wrong with the software and who is responsible and legally liable. 

**If your client needs something different**, please email [Sarah Connolly](mailto:sarah.connolly@bristol.ac.uk) and [Dan Schien](mailto:daniel.schien@bristol.ac.uk) to ask for advice on which license to use.  


## Task 2: Choose an open licence

GitHub has an excellent guide to [Licensing a repository](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/licensing-a-repository) - as a team, **read this and make sure you understand what you need to do and why.

GitHub created [Choose-a-license](https://choosealicense.com), a website designed to help you choose what kind of licence you could use for your project.  **Your task** is to look through the website and choose what license you will use for your project. 

All licences include a generic disclaimer of liability, and some you might choose are:

* **[MIT License](https://choosealicense.com/licenses/mit/)** - enables people to do anything with the software, preserving the copyright
* **[Apache](https://choosealicense.com/licenses/apache-2.0/)** - like MIT but with more boilerplate language (explicit patent licence - good for business use)
* **[Copyleft licences](https://www.gnu.org/licenses/copyleft.en.html)** like the **[GNU General Public License](https://choosealicense.com/licenses/gpl-3.0/)** - releases a modified open source programme, and must also release the source code for that programme alongside it.  

**After your team has selected the most relevant license for your project**, push a `LICENSE` document to the top level of your group's GitHub repository. 

**If your project is intended to be Open Source**, spend some time exploring the **[FOSSA tool](https://fossa.com/)**. Once you start adding dependencies to your project you are going to need to ensure that they don't break the terms and conditions of your chosen licence. FOSSA will automatically scan your project to check that the licenses of any dependencies are consistent with your overall project license.  


#
## How to work with Tech Stacks
It can sometimes be tempting to decide to divide the team into a separate Front End and Back End team.  However, in SEP, this can cause problems, especially when the 2 teams split off and don't work together.  Specific reasons we don't recommend this: 

* **You will all need to review each others' code**, so having separation makes the job much harder.

* **You will be completing work at a different pace**, so you would have times when one sub-team is waiting for the other - and this will **not** be an excuse for not doing work!  Having one sub-team working frantically to hit a deadline, while the other is sitting around with nothing to do is wildly inefficient. 

* **You will need to be integrating them at some point**, and the more separation you have, the harder this will be.  

* **Sometimes team members get sick, or have to leave** and if they are the only person on the team who understands an aspect, it can break a project.

* **It's not great for job interviews** - imagine the difference between one candidate saying they only worked on the front end, and another saying that while they mainly worked on X feature, they made sure they knew what everyone else was working on, so they could jump in and help out when things were going wrong, and were able to code review everything.  

So while you might start off working on one aspect or another, you are expected to understand all aspects of the system, and be creating documentation and walking team-mates through it as you go.  You are definitely expected to review code from parts you are not working on directly.  

Please also **do not split into sub-teams by language**!  It might be tempting, but you are all students in an international University, and you are expected to be able to work with students from all over the world.  

**Rotating roles and working with different team-mates** is a marks magnet, if you tell us about it in the vivas!

**TL;DR**:
![Front End Back End](https://github.com/spe-uob/SEP2025/blob/main/Weekly%20Workbooks/03%20Architecture%20-%20Technology%20Stacks/meme1.png)
[Meme stolen from r/ProgrammerHumor](https://www.reddit.com/r/ProgrammerHumor/comments/1nwbam4/neveragoodplan/)
