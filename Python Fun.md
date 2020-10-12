# Python Fun Stuff #

## Files and the File System ##
file paths:
Windows - c:\Users\David\Documents\hello.txt
macOS   - /Users/David/Documents/hello.txt 
Linux   - /home/David/Documents/hello.txt

On macOS and Linux, the operating system uses a virtual file system that organizes all files and directories for all devices on the system under a single root directory, usually represented by a forward slash symbol. Files and folders from external storage devices are usually located in a subdirectory called *media/*.

On Windows, there is no universal root directory. Each device has a separate file system with a unique root directory that is named with a **drive letter** followed by a colon and a backslash symbol. Typically, the drive on which the operating system is installed is assigned the letter C, so the root directory of the file system for that drive is C:

The other major difference between Windows, macOS, and Linux file paths is that directories in Windows file paths are separated by backslashes (\), whereas directories in macOS and Linux file paths are separates by forward slashes (/).

### pathlib ###
When you write programs that need to run on multiple operating systems, it's critical that you handle the differences in file paths appropriately. In versions of Python greater than 3.4, the standard library contains a module called *pathlib* that helps take the pain out of handling file paths across operating systems.

The following creates a Path object representing the macOS file path "/Users/David/Documents/hello.txt".

import pathlib

path = pathlib.Path ("/Users/David/Documents/hello.txt")

There's a problem, though, with Windows paths. On Windows, directories are separated by backslashes. Python interprets backslashes as the start of an escape sequence that represent a special character in the string, such as the newline character (\n).
Attempting to create a Path object with the Windows file path "C:\Users\David\Documents\hello.txt" raises an exception.

There are two ways to get around this problem:
a) use a forward slash instead of a backslash in your Windows file paths
    path = pathlib.Path("C:/Users/David/Documents/hello.txt")
   Python can interpret this just fine and will translate the path appropriately and automatically when interfacing with the Windows operating system.
b) Second, you can turn the string into a *raw string* by prefixing it with an *r*:
    path = pathlib.Path(r"C:\Users\David\Documents\hello.txt")
   This tells Python to ignore any escape sequences and just read the string as is.

Besides creating a Path object from a string, the Path class has methods that return the Path objects of special directories. Two of the most useful class methods are Path.home() and Path.cwd().
The Path.home() method creates a Path object representing the home directory regardless of which operating system the code runs on.
    home = pathlib.Path.home()

The Path.cwd() method returns a Path object representing the current working directory.

### Using the / Operator ###
If you have an existing Path object, then you can use the / operator to extend the path with subdirectories or filenames.

    >>> home / "Desktop" / "hello.txt"
    WindowsPath("C:/Users/David/Desktop.hello.txt")

The / operator must always have a Path object on the left-hand side. The right-hand side can have a string representing a single file or directory, or it can have a string representing a path or other Path object.    

### Absolute and relative file paths ###
You can determine if a file path is absolute using .is_absolute():
    path = pathlib.Path("Photos/image.jpg")
    print(path.is_absolute())

    False

Relative paths only make sense when considered with the context of some other directory. They are perhaps most commonly used to describe the path to a file relative to the current working directory or the user's home directory.

### Accessing File Path components ###
All file paths contain a list of directories. The .parents attribute of a Path object returns an iterable containing a list of directories in the file path:

    >>> path = pathlib.Path.home() / "hello.txt"
    >>> path
    WindowsPath("C:/Users/David")
    >>> list(path.parents)
    [WindowsPath("C:/Users/David"), WindowsPath("C:/Users"), WindowsPath("C:/")]

Notice that the directories are returned in reverse order of how they appear in the file path. That is, the last directory in the path is the first directory in the list of parent directories.
You can iterate over the parent directories in a for loop:

    >>> for directory in path.parents:
    ...     print(directory)
    ...
    C:\Users\David
    C:\Users
    C:\

The .parent attribute returns the name of the first parent directory in the file path as a string. .parent is a shortcut for .parents[0]
If the file path is absolute, then you can access the root directory of the file path with the .anchor attribute. Note that .anchor returns a string, not another Path object. For relative paths, .anchor returns an empty string.

The .name attribute returns the name of the file or directory that the path points to

    >>> home = pathlib.Path.home()      # C:\Users\David
    >>> home.name
    'David'
    >>> path = home / "hello.txt"
    >>> path.name
    'hello.txt'

File names are broken down into two parts. The part to the left of the dot (.) is called the **stem**, and the part to the right is called the **suffix** or **file extension**. The .stem and .suffix attributes return strings containing each of these parts of the filename.

### Checking whether a file path exists ###
You can create a Path object for a file path even if that path doesn't actually exist. Of course, file paths that don't represent actual files or directories aren't very useful unless you plan on creating them at some point.
Path objects have an .exists() method that returns True or False depending on whether or not the file path exists on the machine executing the program.

You can check whether a file path refers to a file or a directory. To check if the path is a file, use the .is_file() method:
    >>> path = pathlib.Path.home() / "hello.txt"
    >>> path.is_file()
    True

Note that .is_file() returns False if the file doesn't exist.

Use the .is_dir() method to check if the file path refers to a directory.

## Creating and Modifying PDF files ##


## Beautiful Soup ##


## Data Science Basics (Scientific Computing and Plotting) ##


## Databases ##


## CSVs and Excel ##
 

