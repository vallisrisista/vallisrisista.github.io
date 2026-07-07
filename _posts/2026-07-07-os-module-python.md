---
layout: post
title: "OS Module in Python"
date: 2026-07-02
categories: [Python]
tags: [python,os]
---


If you have worked with unix, you might be aware of commands like mkdir,chmod,pwd, etc to perform operations on files and directories.
We can perform those operations in python using “os” module.
Below are few functions that can be performed using os.

|method| functionality|
| :--- | :----: | 
|os.getcwd()| returns current working directory|
|os.mkdir(path)|creates a directory
|os.chdir(path)|to change to a different path|
|os.listdir(path)| lists file and directories in the file path|
|os.remove(file)|deletes the file. Does NOT delete a directory. If given a dir, it will return OSError|
|os.rmdir(path)|removes an empty directory.
|os.chmod(file,permissions)|changes the file permissions as specified|
|os.chown(file,user_id,group_id)|changes the ownership of the file as specified|

OS has a submodule ‘path’ which offers few functions to verify or modify path.
These as useful while loading the required files from our directory.

|os.path.exisits(file_path)|checks is a file exists, return true/false|
|os.path.getsize(filename)| returns size of the file|
|os.path.join(*paths)|joins the given paths to form a single string, generally used when we have to append a filename to a path
|os.path.getmtime(file)|returns last modification time stamp|

Os has open(),close(),read(),write(). These methods return file descriptors instead of file objects.
It is generally recommended to use built in open(), etc, for file operations annd only go for os.open , etc when we need low level operations to be performed.

