---
title: "Workflow tools"
date: 2023-01-21T10:55:17+01:00
draft: false
imgpath: shell_script.png
git: https://github.com/Ivernoerve/workflow_tools
---

Having good workflow tools is really important when working on several projects at the same time. This became more prominent in my later years at university where I had to balance several assignments at the same time as well as my personal programming projects. This led me to create som basic shell-scripts to help organize projects, as well as automate tedious tasks. 

<!--more-->

Put the shellscripts in PATH folder such that they are accesible from all locations on the computer. 

### work

The first and most used workflow is by far my project manager to keep track of current projects, as well as switching between projects easily. The idea is quite simple, as i wanted to create a json file in the work directories containing the project-name, the path, and which tools to opep i.e; sublime, terminal, safari... This allowed me to keep track of, and switch between active projects, such as this webpage, assignments and work. 

Future updates for this will create a the needed dependencies when initiating a given type of project. Given that a C project is initiated, a src, and header folder should be created as well as a template makefile. For a python project it should create a venv, and a source folder. 

#### alfredapp extention

To simplify opening the projects even further I created a workflow for the alfredapp (spotlight replacement for mac) extending some interactions with the work-configs created by the work shell scipt from the searchbar. The extended functionalities are opening and deleting projects.  

### University workflows (Latmint)

Tedious tasks such as creating latex files for the src is a tedious task which I found out is quite easy to automate with the latmint script, making for a smoother experience when writing reports.


### watch 

The watch script and watch_python script uses entr to run the code on saves, making it easier to debug and run smaller projects efficiently without tabing to the terminal for running small changes. The watch script is for compiling a single C file and running it, whereas watch_python runs a python script. It should be noted that scripts like these should only be run on smaller projects as one doesn´t always want code to run on saves (such as bigger ML/DL projects.).

