# New-Mac-Setup

Steps taken to setup a new mac as a development machine

Assumes macOS Big Sur(11.1) and M1 chip(may not matter)

# Basic Apps
1. Xcode and Command line tools
2. Visual Studio Code

# Development Home
Make a *development* directory
```mkdir ~/development```
> This will be our home directory for all our code and extra tools

# Homebrew
Follow initial steps at [Homebrew](https://brew.sh) 

```/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"```

# Java Install
Will utilize *jenv* to easily switch between different jdk versions
Reference -> [How to Manage Multiple Java Versions in macOs](https://medium.com/@chamikakasun/how-to-manage-multiple-java-version-in-macos-e5421345f6d0)
