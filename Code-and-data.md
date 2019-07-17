[The Zen of Python, by Tim Peters](https://www.python.org/dev/peps/pep-0020/): "Long time Pythoneer Tim Peters succinctly channels the BDFL's guiding principles for Python's design into 20 aphorisms, only 19 of which have been written down."

* Beautiful is better than ugly.
* Explicit is better than implicit.
* Simple is better than complex.
* Complex is better than complicated.
* Flat is better than nested.
* Sparse is better than dense.
* Readability counts.
* Special cases aren't special enough to break the rules.
* Although practicality beats purity.
* Errors should never pass silently.
* Unless explicitly silenced.
* In the face of ambiguity, refuse the temptation to guess.
* There should be one-- and preferably only one --obvious way to do it.
* Although that way may not be obvious at first unless you're Dutch.
* Now is better than never.
* Although never is often better than *right* now.
* If the implementation is hard to explain, it's a bad idea.
* If the implementation is easy to explain, it may be a good idea.
* Namespaces are one honking great idea -- let's do more of those!

Some more rules copied from https://web.stanford.edu/~gentzkow/research/CodeAndData.pdf

* Automation
  - Automate everything that can be automated
  - Write a single script that executes all code from beginning to end

* Directories
  - Separate directories by function
  - Separate files into inputs and outputs
  - Make directories portable

* Keys
  - Store cleaned data in tables with unique, non-missing keys
  - Keep data normalized as far into your code pipeline as you can

* Abstraction
  - Abstract to eliminate redundancy
  - Abstract to improve clarity
  - Otherwise, don’t abstract

* Documentation 
  - Don’t write documentation you will not maintain
  - Code should be self-documenting

* Management
  - Manage tasks with a task management system
  - E-mail is not a task management system

* Code Style
  - Make your functions shy
  - Order your functions for linear reading
  - Use descriptive names
  - Pay special attention to coding algebra
  - Make logical switches intuitive
  - Be consistent
  - Check for errors

Source: [Code and Data for the Social Sciences: A Practitioner's Guide](https://web.stanford.edu/~gentzkow/research/CodeAndData.pdf)

* Computing practices from https://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1005510

  * Data management
    - Save the raw data.
    - Ensure that raw data are backed up in more than one location.
    - Create the data you wish to see in the world.
    - Create analysis-friendly data.
    - Record all the steps used to process data.
    - Anticipate the need to use multiple tables, and use a unique identifier for every record.
    - Submit data to a reputable DOI-issuing repository so that others can access and cite it.
  * Software
    - Place a brief explanatory comment at the start of every program.
    - Decompose programs into functions.
    - Be ruthless about eliminating duplication.
    - Always search for well-maintained software libraries that do what you need.
    - Test libraries before relying on them.
    - Give functions and variables meaningful names.
    - Make dependencies and requirements explicit.
    - Do not comment and uncomment sections of code to control a program's behavior.
    - Provide a simple example or test data set.
    - Submit code to a reputable DOI-issuing repository.
  * Collaboration
    - Create an overview of your project.
    - Create a shared "to-do" list for the project.
    - Decide on communication strategies.
    - Make the license explicit.
    - Make the project citable.
  * Project organization
    - Put each project in its own directory, which is named after the project.
    - Put text documents associated with the project in the doc directory.
    - Put raw data and metadata in a data directory and files generated during cleanup and analysis in a results directory.
    - Put project source code in the src directory.
    - Put external scripts or compiled programs in the bin directory.
    - Name all files to reflect their content or function.
  * Keeping track of changes
    - Back up (almost) everything created by a human being as soon as it is created.
    - Keep changes small.
    - Share changes frequently.
    - Create, maintain, and use a checklist for saving and sharing changes to the project.
    - Store each project in a folder that is mirrored off the researcher's working machine.
    - Add a file called CHANGELOG.txt to the project's docs subfolder.
    - Copy the entire project whenever a significant change has been made.
    - Use a version control system.
  * Manuscripts
    - Write manuscripts using online tools with rich formatting, change tracking, and reference management.
    - Write the manuscript in a plain text format that permits version control.
