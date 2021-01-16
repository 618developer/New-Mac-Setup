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

View available versions of JDK to install

```brew search jdk```

Install Java 8 and 11

```
brew install --cask AdoptOpenJDK/openjdk/adoptopenjdk8
brew install --cask AdoptOpenJDK/openjdk/adoptopenjdk11
```

Add each version of Java installed to 'jenv'

```
jenv add <your_jdk_path>
#Example: jenv add /Library/Java/JavaVirtualMachines/adoptopenjdk-8.jdk/Contents/Home
```
**The last version you add will be set as current**

Verify all versions are in 'jenv'

```jenv versions```

Set Java 8 as current(after installing a different after it)

```jenv global 1.8```

Verify

```java -version```


#Install Maven
via Homebrew(recommended)

```brew install maven```

or dowload from Apache Maven and move to your ```~/development``` dir
