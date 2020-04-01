# Review Guide

## Easy way to pass review
+ Good code style
+ No Wlidcards imports (with asterisk *)
+ `Ctrl+Alt+O` & `Ctrl+Alt+L` in IDEA IDE before any commit
+ Right branch and label in PR

## Short checklist
1. Branch
2. Label
3. Codacy
4. *Other checks
5. Changed files

## Detailed list
1. Branch should NOT be ***master***
2. For it shold be ***bootstrap***
3. Codacy check should be OK. If not then you need to see what's wrong
4. *When Travis would be fixed
5. Also reviewing files you can mark them with checkboxes. Should be checked:
   + Code style
   + Understandable naming
   + JDI asserts instead of others
   + Unnecessary empty lines and spaces
   + Unnecessary or forgotten comments
   + Chaining should be separated by lines

## Recommended tools
1. Intellij IDEA
2. Git

## Using libraries
1. As log library: slf4j + logback-classic (TO_VERIFY)
2. As tests runner: TestNG (TO_VERIFY)
3. As reporter: Allure Framework (TO_VERIFY)
4. As test framework: JDI (TO_VERIFY)

## Intellij IDEA Preferences
1. Preferences -> Version Control -> Commit Dialog > Before commit block, setup checkboxes: Reformat Code, Rearrange code, Optimize imports
2. In app press hotkeys: `Ctrl+Shift+Alt+L`, choose checkboxes: Optimize imports, Rearrange Code
3. When you work to apply autoreformatting please use (on file, on directory or inside file) `Ctrl-Alt-L` hotkey
4. To fast open any class by its name use `Ctrl+N`/`Cmd+O`
5. Be sure that NOT checked: Settings->Editor-> Code Style -> Java -> Tabs and Indents -> Use tab character
6. Be sure that equals to 4: Settings->Editor-> Code Style -> Java -> Tabs and Indents -> Tab size field and Indent field
7. Turn off wildcard imports: set to 999 for Settings -> Editor -> Code style -> Java -> Imports -> Class count to use imports with `*` field and Names count to use static imports with `*`

## CVS section
1. Use Git
   + Name branches with useful names 
2. Merge code into any branch only through GitHub pull request (PR)
   + Name PR with useful name
3. Before add reviewers to your PR be ensure: 
   + no codacy issues
   + code is ready to review
   + you push the last changes
   + you have last changes from target branch
   + there is no merge conflicts
   + you take into account all review comments (if such were)
4. Add ReviewTeam as reviewers or re-request review (if there is already reviewers in PR)
5. When you get review changes request you should resolve all issues and re-request code review from the same reviewers
6. Repeat until branch will be merged by reviewers
7. Keep actual **.gitignore** file

## Code style
1. Use spaces, 1 tab size equals to 4
2. Don't use wildcard imports
3. Use Intellij's autoreformatting, imports optimization and rearrange option
4. Fix all codacy issues
5. If codacy issue shouldn't be resolved use warnings supressions
6. Use semantic-value names for classes , variables, methods and so on. Use full version of words (human instead of h and so on). Common abbreviations (as id, uid and so on are applied). Use valuable names, for example instead of accountList use accounts and so on
7. Remove double empty lines, use empty lines only when it make sense (additionally to autoreformatting)
8. Use correct line breaks: (PROVIDE_SAMPLES)
9. Try to use lines with no more 100-120 symbols (including indents) 
10. Use chaining style, recommended sample:
    ```java
    object
        .method(1)
        .otherMethod();
    ```
11. Always use `{}` braces for even empty if, for, etc.
12. Follow to the sequence of keywords: public protected private abstract default static final transient volatile synchronized native strictfp
13. Don't use such convinences as: `mValue`, `_value`, and so on. Acceptable `__` as unused argument of dataprovider in test methods
14. Feel free to smart refactoring
15. Feel free to use smart ?:
16. Use `UpperCamelCase` naming style for classes, `lowerCamelCase` for fields and methods, `UPPERCASE` for enums, `lowercase` for packages
17. Always use `@Override` annotation
18. Don't leave empty `catch{}`, use relevant exceptions with messages
19. Try to not use global variables
20. Use variables for integer, string and other values (for instance, `int piNumber=3.14; println(piNumber)`)
21. Write comments in English
22. It's better to write code than create task to write code
23. It's better to create task and `TODO` with this task number than to write simple `TODO` in code
24. It's better to write simple understandable `TODO` in code than to tell about problem to someone
25. It's better to tell about a problem to someone than to not take actions at all
26. Always leave newline symbol as a last symbol of file
