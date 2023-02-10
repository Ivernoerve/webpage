---
title: "Workflow tools"
date: 2023-01-21T10:55:17+01:00
draft: true
---

Having good workflow tools is really important when working on several projects at the same time. This became more prominent in my later years at university where I had to balance several assignments at the same time as well as my personal programming projects. This led me to create som basic shell-scripts to help organize projects, as well as automate tedious tasks. 


The first and most used workflow is by far my project manager to keep track of current projects, as well as switching between projects easily. The idea is quite simple, as i wanted to create a json file with projectnames and the corresponding paths to the project directory as key-value pairs, and creating a shell script with flags for adding, deleting, and open the projects listed in the json file. When opening a project a terminal, finder, and a vscode window is opened in the project directory making starting a project far easier. 

Later afrer being introduced to [Alfredapp]({{<ref "https://www.alfredapp.com">}}) as a powerful replacement for the spotlight search engine I wanted to integrate my workflow as alfred workflow allowing me to open and archive projects from the alfred search bar rather than opening the terminal to open a project. 

