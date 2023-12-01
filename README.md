# Development Guidelines

## Naming Conventions 
- ReactJS: https://airbnb.io/javascript/react/

## Version Control
Below are some rules to follow when working with a version control system such as Git:

### 1. MAKE SURE THE BUILD SUCCEEDS BEFORE COMMITTING CODE.
Broken code should not be committed.

### 2. CREATE FEATURE BRANCHES. ISOLATE CODE THAT WILL CREATE OR CHANGE A FEATURE.    
Creating a branch does not affect other team members working on a different branch. This is desireable because a feature under development can create instability in the codebase.

### 3. ALWAYS PULL DOWN THE LATEST CHANGES BEFORE BEGINNING TO CODE. 
This means that even before you start coding, you must perform a `pull`. In the CLI this command is `git pull origin [branch-name]`.   
This also means that you must keep you local version of the repository up to date. This is crucial if you’re working on a feature branch that may take more than a few hours to close, don’t let your branch diverge too far from the master branch.   
To elaborate if you create a feature branch called `feature-1` from the `develop` branch, make sure the perform a `pull` on the `develop` branch daily or as needed. Below we highlight this flow through commands.  

```
# Create a new feature branch called "feature-1" from the "develop" branch"
git checkout -b feature-1 develop
# Begin coding for sometime

# Perform a pull on develop
git pull develop

# Continue coding. Review any conflicts or merges
```

### 4. USE MEANINGFUL AND SUCCINCT GIT MESSAGES.
You are writing the commits not for yourself, rather for the rest of the team.   
“A commit message shows whether a developer is a good collaborator”. **A project’s long-term success rests (among other things) on its maintainability** and being able to review others’ commits and pull requests with ease.  
This drives efficiency.

Here's an example of adequate commit messages:
```
5ba3db6 Fix failing CompositePropertySourceTests
84564a0 Rework @PropertySource early parsing logic
e142fd1 Add tests for ImportSelector meta-data
887815f Update docbook dependency and generate epub
ac8326d Polish mockito usage
```

- [A Successful Git Branching Model](http://nvie.com/posts/a-successful-git-branching-model/)

**Git Messages**

When [committing](http://dont-be-afraid-to-commit.readthedocs.io/en/latest/git/commandlinegit.html) code into a Git repository, you will have to write a message describing your code changes.  
It is crucial that we make these messages concise and consistent. A well-crafted commit message can tell other developers right away why your code changes matter or why they took place.  
  
Chris Beams has a great [post](https://chris.beams.io/posts/git-commit/) that summarizes the importance of a well-crafted commit message, along with the rationale behind it. Below are the seven rules he writes in his post, check out his post for more information.
    
**The seven rules of a great Git commit message**  
1. Separate subject from body with a blank line
2. Limit the subject line to 50 characters
3. Capitalize the subject line
4. Do not end the subject line with a period
5. Use the imperative mood in the subject line
6. Wrap the body at 72 characters
7. Use the body to explain what and why vs. how

- [How to Write a Git Commit Message](http://chris.beams.io/posts/git-commit/)
