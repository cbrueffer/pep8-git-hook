PEP8 Git Commit Hook
====================

This is a pre-commit hook for Git that checks the code to be committed
for Python PEP8 style compliance.  The hook will prevent the commit in
case style violations are detected.

Installation:

1. Install the pycodestyle (formally called pep8) program: ```$ pip install pycodestyle```
2. Save pre-commit as your_project/.git/hooks/pre-commit
3. Mark pre-commit executable: ```$ chmod +x your_project/.git/hooks/pre-commit```

The hook can be overridden: ```$ git commit --no-verify```

Currently, the following PEP8 codes are checked for:

E111 indentation is not a multiple of four   
E125 continuation line does not distinguish itself from next logical line   
E203 whitespace before ':'   
E261 at least two spaces before inline comment   
E262 inline comment should start with '# '   
E301 expected 1 blank line, found 0   
E302 expected 2 blank lines, found 1   
E303 too many blank lines (2)   
E502 the backslash is redundant between brackets   
E701 multiple statements on one line (colon)   
E711 comparison to None should be 'if cond is None:'   
W291 trailing whitespace   
W293 blank line contains whitespace   

In case you want to modify the list of codes to ignore, edit the
```ignore_codes``` list in the pre-commit file.   
If you want to select only specific codes to scan for, use the
```select_codes``` list.
Additional arguments to the pycodestyle program (e.g., ```--max-line-length=120```) can be added to the ```overrides``` list.

This code was forked from [https://gist.github.com/810399](https://gist.github.com/810399).
