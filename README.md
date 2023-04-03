# SoftLabs
This repository is for the development of SoftLabs project from the Applied Science Department at Guru Nanak Dev Engineering College, Ludhiana.

# Rules for contributing to this repository:
1. Create a Fork for this repository by clicking on 'fork'. 
1. On your fork create two branches: main and <your_name>, by clicking on: branches > create new branch.
1. Clone the forked repository on your machine (navigate to the desired folder and execute the following in cmd).
    ```
    git clone https://github.com/<user-name>/SoftLabs
    ```
1. Only edit code present in <your_name> branch, and make a commit
    ```
    git checkout <your_name>
    git status
    git add .
    git commit -m "a meaningful and detailed commit message"
    ```
1. Once you are done making changes merge your changes into <your_name> branch of your fork, and contribute in the following way:
    - Click 'Sync Fork' option on GitHub, this will bring all the changes from CasumicClub/SoftLabs to <user_name>/SoftLabs.
    - Go to main branch of your fork on your machine and pull the changes from GitHub (these changes are made by other users).
    ```
    git checkout main
    git fetch 
    git pull
    ```
    - Now either using GitHub Desktop of GitCLI merge main into <your_name>, this will bring your changes from main to <your_name> branch.
    ```
    git checkout <your_name>
    git merge main
    ```
    - Bring your changes to main.
    ```
    git checkout main
    git merge <your_name>
    ```
    - Push the changes, this will push the changes from your local machine to GitHub.
    ```
    git checkout main
    git push
    ```
    - Lastly, go back to <user_name>/Softlab (your fork) and 'Contribute'. There are will be a branch named after you in the main repository, example: CausmicClub/SoftLabs:RaghavJit_Complete. When contributing your work you have to make sure that you only contribute change in your respective branch. So when you contribute make sure to select your branch as target:
        ```
        CausmicClub/SoftLabs:RaghavJit_Complete <-- RaghavJit/SoftLabs:main
        ``` 
    ![alt text](./Images_for_readme/contribute.png?raw=true)
    
    <marquee><span style="color: red">!!! Please don't push your contributions to CausmicClub/SoftLabs:main, even if someone forces you to do so at a gun point (we will remember you and your contributions forever \*wiping a teardrop\*)</span>
    </marquee>

## Important things to remember.
1. Only edit code present in <your_name> branch of your fork.
1. Don't create new folders without permission.
1. Don't upload files that are not directly related to the project.
1. Small changes (typos/non-functional bugs) don't need to be immediately sent to CausmicClub/SoftLabs. Instead, you can keep these changes in your main and push them along only when there are more important changes to be sent.
1. You might face "conflicts" when merging main and <your_name> or vise versa, in this case, either try to resolve the conflicts (only if you know what you are doing), of contact someone higher in the project management hirarchy. 
1. Get comfortable with gitbash/GithubCLI.
1. Keep in contact of the team and make sure that not more than 1 person is not working on a file.

# Devolopment Rules

## Naming variables
### Use meaningful names for variables and functions, try to avoid abbreviations/short forms

1. Global variables have to be in uppercase in snake_case.
```
let NEEDLE_ANLGE = 12
```
1. Local variables have to be in PascalCase 
```
let SampleVariable = 33
```
1. Functions have to be in camelCase
```
const setMeters()
```

## Documentation and commenting
### Each experiment will have a README.md file where you need to enter a description for each variable, function, class etc. created by you.
1. Write variables and functions under the variable and function section respectively.
2. Refer to the variables used in a function in the beginning of the description.
```
<pre>
Function name
  Var list
    1. VariableOne: description
    2. VariableTwo: description
    3. SampleGlobalVariable: Ref. line:54, optional description
  
  Description
    description-description-description
</pre>
```
3. Classes have to be documented in the following way
```
<pre>
Class name
  Var list
    1. VariableOne: description
    2. VariableTwo: description
    3. SampleGlobalVariable: Ref. line:54, optional description
  
  Functions
      Function name
        Var list
          1. VariableOne: description
          2. VariableTwo: description
          3. SampleGlobalVariable: Ref. line:54, optional description

        Description
          description-description-description
</pre>
```
4. When an update is made to a function/class it has to be added in the documentation by the modifier in the following way:
```
<pre>
Update-<update-number>
  Reason: why the update was made
  Change: what has been changed
  Issues: <issue-number> which issue was solved (optional, only to be written when there was an issue for the bug) 
</pre>
```

## Code Clarity
1. Provide proper indentation in your code.
1. User meaningful names for identifiers.
1. Keep all the global variables on the top.
1. Keep all the Functions below the global variables.
1. You might skip writing documentation if the function/class is insignificant to other users, but writing comments is mandatory. 

# Directory Structure
<pre>
TEMPLATE 
|
+---README.md: Documentation for the BasicStyle.css and BasicFunction.js
    BasicStyle.css: Contains all the classes which are common to a number of experiments.
    BasicFuntion.js: Contains all the basic JavaScript code common to experiments.

ASSETS
|
+----Contains all the assets (.jpg .png etc)

FILES
|
+---Contains libraries/modules etc. being used

experiment-name
|
+---README.md: Documentation for the experiment
    testing.md: Report for testing team
    index.html
    style.css
    function.js

experiment-name
|
+---README.md: Documentation for the experiment
    testing.md: Report for testing team
    index.html
    style.css
    function.js
</pre>

# Testing and Issue resolution
Testing and bug reporting will be done by the testing team. The procedure for the same is mentioned below.

## Testing 
1. Development team will develop an experiment and provide the testing team with a prototype along with testing document (testing.md). The contents of testing.md will be as following:
    - Feature list: List of all the features in the program
    - Procedure: procedure that user has to follow
    - Flag list: All the features that are potentially buggy
1. Testing team will go through the document and perform the experiment according to the given procedure.
1. Team will test each feature mentioned in Flag List.
1. If a bug is found it has to be reported by creating 'ISSUE' on GitHub.
1. When writing a description for the issue follow this format:
    - Feature Name: Name/Number of the feature according to testing.md
    - When it occurs: How was the bug encountered
    - Suggestion (optional): Suggestion for solving/enhancing the feature. If other features are being affected due to this bug, they can also be reported in this section.
    - Code snippet (optional): Code snippet that might be causing the bug.
1. Appropriate labels must also be added to the issues.

## Issue Resolution
1. When an issue is reported the development team will try to resolve it.
1. Issue will be assigned to a member. Everyone is allowed to assign issues to each other.
1. When the issue is fixed, update the README.md according to the above instructions. (See Documentation and commenting pt. 4) 
