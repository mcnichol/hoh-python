# Google IT Automation with Python

## Course 2: Using Python to Interact with the Operating System

* Will be using the linux OS to follow this course.
* I'm trying this with [WSL](https://docs.microsoft.com/en-us/windows/wsl/about) Ubuntu on Win10x64
* Ensure using Python 3

### Resources
* [RealPython.com Installation Steps](https://realpython.com/installing-python/) - Steps and tips/best practices for installing python on various OS's 
* [Qwiklabs](https://www.qwiklabs.com/) - Lab based exercise to support learning in Cloud environments. GCP
* [The Hitchhiker's Guide to Python!](https://docs.python-guide.org/) - Online Python book sharing opinionated best practices
* [Python Language Reference](https://docs.python.org/3/reference/index.html) - Syntax and Core Semantics
* [Automate the Boring Stuff with Python](https://automatetheboringstuff.com/) - No Starch Press implementing automation tasks using python.

### IDE Editors

* [Intellij PyCharm](https://www.jetbrains.com/pycharm/?_ga=2.72593687.545792099.1646404242-367428489.1646207259) - Built on Java, used in a majority of professional work environments. Leans heavy on shortcuts and productivity. Has a little bit of a learning curve to use all of it's functionality. The Vim/Emacs of GUI IDE's although maybe not as deep a learning curve. Great for Pair Programming. High pricing compared to other options.
* [Atom](https://atom.io/) - Built on Electron framework. Intended to have a low learning curve, high customization, and OSS
* [Sublime Text](https://www.sublimetext.com/) - Simple to use, fairly easy to customize, while free to evaluate you will receive a pop-up to buy at certain intervals.
* [VS Code](https://code.visualstudio.com/) - Microsoft editor that parallels to Atom functionality in addition to being built on Electron Framework and OSS.

### Tips
#### Using WSL
* You will need to modify file permissions when ssh'ing to other machines (pem files need 0600). In order to do this using Windows Subsystem Linux, you will need to modify (or create) /etc/wsl.conf in order to modify the metadata of files. 

```bash
$> sudo vim /etc/wsl.conf

# /etc/wsl.conf
[automount]
options = "metadata"
```
* There are a few Quality of Life improvements over Powershell / CMD. 
  * Highly recommend using [Windows Terminal](https://docs.microsoft.com/en-us/windows/terminal/) or something similar. Visibility, Font Support, and overall usability is dramatically better. It's not quite Linux but it's much closer to what you'd be expecting. 
  * I swap shells to zsh and style it with [oh-my-zsh](https://github.com/ohmyzsh/ohmyzsh) (Agnoster Theme), and [Powerline Fonts](https://github.com/powerline/fonts) (DejaVu Mono has the best character support for my gitflow)
  * adjusting the file/directory highlighting as I have this hideous Green+Blue that is painful to decipher. 
    ```
    $> dircolors --print-database > ~/.dircolors	# Modify OTHER_WRITABLE variable (~Line 60). First code is font color, second is background color i.e. 37;42  is white text on green
    $> echo 'test -r ~/.dircolors && eval "$(dircolors -b ~/.dircolors)" || eval "$(dircolors -b)"' >> ~/.zshrc 	# It already exists in .bashrc if you haven't switched shells
    ```
