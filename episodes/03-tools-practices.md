---
title: "Tools and good practices for research software"
teaching: 60
exercises: 30
---

:::::::::::::::::::::::::::::::::::::: questions

- What tools are available to help us develop good quality and FAIR research software?
- How do the tools fit together to enable open and reproducible research?

::::::::::::::::::::::::::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::: objectives
After completing this episode, participants should be able to:

- Identify some key tools to aid the development of research software
- Explain how can these tools help us work in a FAIR way
- Install and run these key tools on learner's machines

::::::::::::::::::::::::::::::::::::::::::::::::

## Good practices for developing research software

Along with the FAIR principles covered in the previous episode, other good practices exist for developing research 
software that foster open and reproducible research:

### Software version control 

Use version control systems like Git to track changes, collaborate, and manage the software’s history.

### Reproducible software environments 

Use virtual development environments (e.g. Conda, venv) or containerisation (e.g. Docker) to ensure software can be run and developed consistently across different systems.

### Compliance with coding standards 

Apply relevant coding style guidelines (e.g. PEP8 for Python) to maintain consistency and improve code readability and the reproducibility of results.

### Software project and code structure 

Organise your software project according to community practices and write clean, modular, and reusable code to make it easier to understand, test, extend and reuse.

### Software testing 

Implement tests to verify code functionality and ensure result accuracy as well as consistency over time when making updates to the code.

### Software documentation 

Provide comprehensive documentation, including code comments, setup guides and usage instructions to ensure that others can understand and use the software.

### Software licensing 

Apply open-source licenses (e.g., MIT, BSD) to your code to ensure that it is freely available and can be modified or redistributed.

### Software sharing 

Publish your research software openly, making sure it is well-documented and formatted, and stored in accessible repositories. 

### Collaborative software platforms
Store your code on platforms like GitHub or GitLab to encourage collaboration, transparency, and code review.

### Code review
Encourage peer reviews of code to identify bugs, improve quality, and promote knowledge sharing.

### Software citation
Ensure that software is properly cited in publications and research outputs, and provide citation information in documentation.

## Tools for open and reproducible research software

There are various tools and practices for the development of research software that support open and reproducible 
research and support the FAIR and other quality software principles.
These tools and practices work together - no single one will fully address one principle, and each one can contribute to multiple principles simultaneously.
It is important to note that simply using these tools, without following good practice and guidance on how best to align
their usage with the FAIR principles, is not enough to produce FAIR software.

You should already have these tools installed on your machine by following the [setup instructions](./index.html#astronaut-data-and-analysis-code).
Here we will give an overview of the tools and good practices and how, when used in combination, they can help you 
achieve the aims of FAIR research software.
In later episodes we will describe these tools and practices in more detail.

### Development environments

Virtual and integrated development environments (IDEs), such as VS Code or PyCharm, help with reading, running, testing, and debugging code.
Virtual environments further enable us to share our working environments with others, making it easier to reuse and extend our code.
IDEs often provide integrations with other tools, e.g. version control and command line terminals, enabling you to do many tasks from a single environment,
saving time in switching between different tools.

### Command line terminals

Command line terminals (e.g. Bash, GitBash) enable us to run and test our code without graphical user interfaces (GUI) afforded to us by IDEs -
this is sometimes needed for running our code remotely on servers and high-performance systems without a GUI provision, where time,
memory and processing power are expensive or in high demand.

Version control systems are typically provided as command line tools, making them often only accessible from command line terminals to enter commands and access
remote version control servers to backing up and sharing our work.

Finally, command line tools are interoperable software that use standard protocols for passing parameters, inputs and outputs via the command line terminal.
This makes it easier to integrate with other tools, allowing us to chain command line tools and build up complex and reproducible workflows and analysis pipelines
using several programs in different steps.
If we write our software in a way which provides such an interoperable command line interface - we will be able to integrate it with other command line tools to
automate and speed up our work.

### Standard input/output formats and communication protocols

Using standard data exchange, input and output formats and communication protocols helps create interoperable software that can more readily integrate
with other tools into more complex pipelines - increasing its interoperability and reusability.

### Version control tools

Version control means knowing what changes were made to your code, when and by whom - promoting code ownership, responsibility and credit.
When combined with software sharing and collaborative platforms such as GitHub or GitLab, it facilitates code publication, sharing and findability,
teamwork and discussions about software and design decisions, provides backup facilities for your code and speeds up
collaboration on shared code by allowing edits by more than one person at a time.

### Code testing

Testing ensures that your code is correct and does what it is set out to do.
When you write code you often feel very confident that it is perfect, but when writing bigger codes or code that is meant to do complex operations
it is very hard to consider all possible edge cases or notice every single typing mistake.
Testing also gives other people confidence in your code as they can see an example of how it is meant to run and be assured that it does work
correctly on their machine - helping with code understanding and reusability.

### Coding conventions

Following coding conventions and guides for your programming language that is agreed upon by the community and other programmers
are important practices to ensure that others find it easy to read your code, reuse or extend it in their own examples and applications.

### Code licensing

A licence is a legal document which sets down the terms under which the creator of work (such as written text,
photographs, films, music, software code) is releasing what they have created for others to use, modify, extend or exploit.
It is important to state the terms under which software can be reused - the lack of a licence for your software
implies that no one can reuse the software at all.

A common way to declare your copyright of a piece of software and the license you are distributing it under is to
include a file called **LICENSE** in the root directory of your code repository.

### Code citation

We should add a **CITATION** file to our repository to provide instructions on how and when to cite our code.
A citation file can be a plain text (CITATION.txt) or a Markdown file (CITATION.md), but there are certain benefits
to using use a special file format called the [Citation File Format (CFF)][cff], which provides a way to include richer
metadata about code (or datasets) we want to cite, making it easy for both humans and machines to use this information.

### Code documentation

Software documentation comes in many forms - from **code-level documentation** including descriptive names of variables and functions and
additional comments that explain lines of your code, to **project-level documentation** (including README, LICENCE, CITATION, CONTRIBUTING, etc. files)
that help to discover it, explain the legal terms of reusing it, describe its functionality and how to install, run and contribute to it,
to whole websites full of documentation with function definitions, usage examples, tutorials and guides.
You many not need as much documentation as a large commercial software product, but making your code reusable relies on other people being able to understand
what your code does and how to use it.

### Software repositories and registries

Having somewhere to share your code is fundamental to making it findable and accessible.
Your institution might have a code repository, your research field may have a practice of sharing code via a specific website, archive or journal,
or your version control system might include an online component that makes sharing different versions of your code easy.
You should check the rules or guidelines of your institution, grant or domain on publishing code, as well as any licenses of the code your software depends on or reuses.

Some examples of commonly used software repositories and registries include:

- general-purpose software repositories - [GitHub][github] and [GitLab][gitlab]
- programming language-specific software repositories - [PyPi][pypi] (for Python) and [CRAN][cran] (for R)
- software registries - [BioTools][biotools] (for biosciences) and [Awesome Research Software Registries][awesome-rs-registries], providing a list of research software registries (by country, organisation, domain and programming language) where research software can be registered to help promote its discovery

### Persistent identifiers

Unique persistent identifiers, such as **Digital Object Identifiers** (DOIs) provided by [Zenodo][zenodo],
[FigShare][figshare], etc., or **SoftWare Heritage persistent IDentifiers** ([SWHID](swhid)) provided by [Software Heritage][software-heritage],
and similar digital archiving services, and commits/tags/releases used by GitHub and similar code sharing platforms,
help with findability and accessibility of your software, and can help you get credit for your work by providing citable references.


## Tools and practices summary

The table below provides a summary of how different tools and practices help with the FAIR software principles.

| Tools and practices                                                                                  | Findable | Accessible | Interoperable | Reusable |
|------------------------------------------------------------------------------------------------------|----------|------------|---------------| -------- |
| Virtual development environments                                                                     |          |            |               | x        |
| Integrated development environments (IDEs)                                                           |          |            |               | x        |
| Command line terminals - automated and reproducible pipelines                                        |          |            | x             | x        |
| Standard data exchange formats - e.g. for data exchange (CSV, YAML)                                  |          |            | x             | x        |
| Communication protocols - Command Line Interface (CLI) or Application Programming Interface (API)    |          |            | x             | x        |
| Version control tools                                                                                | x        |            |               |          |
| Code testing & correctness                                                                           |          |            |               | x        |
| Coding conventions                                                                                   |          |            |               | x        |
| Code-level documentation (comments and docstrings, explaining functionality)                         |          |            |               | x        |
| Project-level documentation & metadata (README, explaining functionality/installation/running, etc.) |          |            | x             | x        |
| License - code sharing & reuse                                                                       |          |            |               | x        |
| Citation - code reuse & credit                                                                       |          |            |               | x        |
| Software repositories & registries                                                                   | x        | x          |               |          |
| Unique persistent identifiers                                                                        | x        | x          |               |          |

Let's explore some of these practices and tools in detail.

## Further reading

We recommend the following resources for some additional reading on the topic of this episode:

- [CodeRefinery: Reproducible research - preparing code to be usable by you and others in the future][coderefinery-tools]
- [Python IDEs and Code Editors (Guide) - Real Python][real-python-ides]
- [The Zenodo data repository][zenodo-org]
- [The Fair Cookbook - Depositing to generic repositories - Zenodo use case][fair-cookbook-zenodo]

Also check the [full reference set](learners/reference.md#litref) for the course.

:::::::::::::::::::::::::::::::::::::::: keypoints

- Automating your analysis with shell scripts allows you to save and reproduce your methods.
- Version control helps you back up your work, see how data and code change over time and identify which analysis used which data and code.
- Programming languages each have advantages and disadvantages in different situations. Use the correct tools for your own work.
- Integrated development environments (IDEs) automate many coding tasks, provide easy access to documentation, and can identify common errors.
- Testing helps you check that your code is behaving as expected and will continue to do so in the future or when used by someone else.

::::::::::::::::::::::::::::::::::::::::::::::::::
