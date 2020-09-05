# E.nav Dev

Welcome to the dev section.

## Directory structure

 - **Development/**
    - **CORE/**
        - **Additional Notes/**
        - **Isolated/**
            - **dev/**
            - **Releases/**
        - **Modular/**
            - **`<Module Name>`/**
                - **dev/**
                - **Releases/**
                - **README.MD**
    - **Addon Modules/**
        - **`<Module Name>`/**
            - **dev/**
            - **Releases/**
            - **README.MD**

The **dev/** folder can contain whatever notes you have pertaining to the problem, in whatever folder structure you like. Use the .yodev & .yolol formats to explain yolol code, and note formats for extra explanation.

The **Releases/** folder should contain only .yorel files, with a name that starts with a copy of the `<Module Name>`, followed by whatever you like, ending with a version identifier `V#.#.#.#[a|b|t]`. And an optional README.MD detailing the updates in each version, especially if there are multiple "current versions". 

Also, check out documentation/README.md for info on E.nav related terms you may wish to use to create more descriptive names for your files.

# File Types:
Extension | description
-|-
none, .txt| Notes
.md | Markdown, more complete explanations
.yolol | Yolol code exactly as it would appear in a single chip
.yodev | Multiple chips worth of code, potentially violating the line and/or character limits.
.yorel| A yolol release file.
other | should only be used for additional material like images, or helper scripts in other languages

# Versoning

We'll be using an extended version of SemVer. All yolol & yorel files *must* contain this version string in their name.

```
Format: V#.#.#.#[a|b|t]
```
Given a version number Enav.MAJOR.MINOR.PATCH, increment the:

- E.NAV version, never. (it should match the parent E.NAV Major version)
- MAJOR version when you make incompatible API changes,
- MINOR version when you add functionality in a backwards compatible manner, and
- PATCH version when you make backwards compatible bug fixes.

[a|b|t] refers to the requirement of a single character (a, b or t) at the end of the version string. 
 - a: Alpha version (not tested in game)
 - b: Beta version  (minor in-game testing)
 - t: tested, known to work in game

### yorel-template

```c
//Name: 
//Current Version: 
//Credit: 

//Globals:
//  :Y - description
----+----|----+----|----+----|----+----|----+----|----+----|----+----|
//Code for chip 1
//You can have chip specific comments after their code, that are ofc not mandatory to copy
//It'd be nice if you included descriptive names for local vars, but that's not nessesary
//Please include a relative path to related .yolol/.yodev file(s) if they exist
----+----|----+----|----+----|----+----|----+----|----+----|----+----|
//Code for chip 2
----+----|----+----|----+----|----+----|----+----|----+----|----+----|
//Code for chip 3...
```

### yodev-template

```c
//Name: 
//Credit: 
----+----|----+----|----+----|----+----|----+----|----+----|----+----|
```