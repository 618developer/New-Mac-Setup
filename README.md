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

```brew install jenv```

Update shell configuration file

```
echo 'export PATH="$HOME/.jenv/bin:$PATH"' >> ~/.zshrc
echo 'eval "$(jenv init -)"' >> ~/.zshrc
```

source ~/.zshrc to resource your conifg(or restart terminal)

I'm using maven so these two commands are needed to make sure maven sees JAVA_HOME and uses the current JDK we select

```
jenv enable-plugin export
jenv enable-plugin maven
```

Install Java 8

```brew install --cask AdoptOpenJDK/openjdk/adoptopenjdk8```

Install Java 11 (or any other available version you would like)

```brew install --cask AdoptOpenJDK/openjdk/adoptopenjdk11```
