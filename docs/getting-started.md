# Getting Started

## Installation

Before doing anything we need to install AutoHotkey v2. Head over to https://www.autohotkey.com/, download and install the setup.

## Code Editor Configuration

For this tutorial we will be using VS Code as our code editor. Download it from https://code.visualstudio.com/. Once downloaded, open VS Code and install the extension [AutoHotkey v2 Language Support](https://marketplace.visualstudio.com/items?itemName=thqby.vscode-autohotkey2-lsp). This extension will add code completions, syntax highlighting, code format functionality and much more.

## Hello, World!

### Creating a Project Directory

Now that we have installed AutoHotkey, it's time to write our first script. First we will need to create a project directory where we will be placing all our scripts. In Windows Terminal, enter this:

```
> mkdir $HOME\Projects
> cd $HOME\Projects
> mkdir AutoHotkey
> cd .\AutoHotkey
```

### Writing our First AHK Script

Once in our project directory, in Windows Terminal, enter the following to open our project folder in VS Code and create a `HelloWorld.ahk` file.

```
> code ./; code HelloWorld.ahk
```

Once our script is open in VS Code, enter the following lines of code and save it.

Filename HelloWorld.ahk:

```ahk
^h:: {
    MsgBox "Hello, World!"
}
```

### Running our AHK Script

Running ahk scripts is as simple as double clicking them in File Explorer. Assuming you are still in VS Code, click on the Run button in the top right corner or press `Ctrl + F5` instead to run our `HelloWorld.ahk` script.

Once the script is running, it's icon will show under System tray in your Task bar.

If a small window with "Hello, World!" pops up, then congratulations on writing your very first ahk script!

### Reloading and Exiting

For now to reload a script after you make changes to it, right click on the script's tray icon and select `Reload Script`. Or simply run the script again from File Explorer or via VS Code's code runner.

Once you run a script it will keep on running until you stop it, or well your PC shuts down. To exit a script, right click on the script's tray icon and select `Exit`.

### Anatomy of an AHK Script

Lets take a closer look at our `HelloWorld.ahk` script. This is the first part: 

```ahk
^h::
```

It represents a `Hotkey` or just a custom key combination that does something. Now let's take a look at the "something" part:

```ahk
{
    MsgBox "Hello, World!"
}
```

`{` and `}` marks the start and end of a code block. When you press a Hotkey, the code block associated to it gets executed. In our `HelloWorld.ahk` script, on pressing the Hotkey `Ctrl + h`, the code inside the code block gets executed and you see a message box pop up.

```ahk
MsgBox "Hello, World!"
```

`MsgBox` is a function which creates that pop up box. We will talk about functions in-depth later in the tutorial.
