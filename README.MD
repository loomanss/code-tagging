---
title: "readme.md"
author: "sloomans"
date: "2021-02-14"
status : "development"
---


# code Tagging

## the need for code-tagging

- highlighting in code -editors
- automating code/conf-handling files.
- automatted documenting?
- information how to open the file for other devs/ops



## sources and existing tag-framworks

### vim tags 

```bash
#!/usr/bin/env python3
# encoding: utf-8
# Author: sloomans
# vim: fileencoding=utf-8 tabstop=4 expandtab shiftwidth=4
# pylint: disable=C0103,C0301,W1202,W0212
# escape=`
# version = '1.0.0'
```
### Rscript

```
#!/usr/bin/env Rscript
---
title: "Untitled"
author: "ekoam"
date: "`r Sys.Date()`"
output: html_document
---
```


## code tagging in python : pep-0350
https://www.python.org/dev/peps/pep-0350/
https://canadiancoding.ca/posts/post/python/codetags/
```bash
# NOTE: A general note/mild warning
# HACK: Temporary solution to a problem, to be properly solved later
# PORT: An OS/Platform specific workaround
# IDEA: An idea to solve an issue (Not that useful unless solution will take time to implement)
# REQ: Requirement for a file/function/class
# FAQ: A frequently asked question
# SEE: Point to a reference such as a documentation link, or other function
# TODO: As the name implies, tells people/you something that needs to be done (very useful for multi-day/multi-developer projects)
# FIXME: Addresses a problem that should be fixed in the code
# BUG: Identifies a known bug
# WONTFIX: Put next to something you know has an unintended/unexpected outcome, but have no intention to fix
# CAVEAT: A caveat to the implementation; something that is not so obvious to layman's, or first time users necessarily
# DOCUMENT:Need to write documentation
```

### idea's

###

```bash
/**
* ? this is a question
* ! this is deprecated
* * this is important
* TODO: refactor this document
* @param dbconnection   Ad this parameter 
**/
```

[](https://raw.githubusercontent.com/jbgutierrez/vim-better-comments/master/images/screenshoot.gif)

###  markdown - yml

```
#
#```yml
#  - DOCUMENT: this files 
#  - TODO: Come up with full list of class attributes
#  - REQ: Store user information such as name, birthday, city etc.
#  - Arguments:
#  - name(str): The name of the user. NOTE: Name implies first name, not necessarily full name
#```
```



###   ansible tags in document
#```ýml
#- name: Copy file with owner and permissions
#  ansible.builtin.copy:
#    src: /srv/myfiles/foo.conf
#    dest: /etc/foo.conf
#    owner: foo
#    group: foo
#    mode: '0644'
# ```
