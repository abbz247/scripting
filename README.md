# scripting
Ho to Write Script
Good coding practices - Writing our scripts the “right” way
The script example for functions we have seen so far works, but one of the big advantages of using scripts is including features that make the code easier to read and understand. These include comments in the code, which explain what the code does, but are not executed when the code is run. As your scripts get longer and more complicated, features such as comments will become essential. Below are some suggestions to make sure your code is formatted nicely and easy to understand.

Inline comments
Inline comments are comments within the code that explain what certain lines of the code do. To you, it may seem obvious how the code works, but if you share it with another person perhaps they will not feel the same way. This is particularly true when you start using scripts instead of Jupyter notebooks, where you might not feel you can include as much text describing your code. Because we want to teach you to code in an effective way, it is a very good idea to make your scripts as easy to read as possible for people. Consider the example below.

# Finnish Meterological Institute observation station name and location data
# Station name for the station in Kaivopuisto, Helsinki, Finland
stationName = 'Helsinki Kaivopuisto'
# Station latitude and longitude - Latitude is north, longitude is east
stationLat = 60.15
stationLong = 24.96
# Print station name and location to the screen
print("The", stationName, "station is located at", stationLat, "N,", stationLong, "E")
Here, we have provided a a bit more information about the data in this script by adding inline comments. Inline comments begin with a # (number sign or hash), and all characters that follow on that line will be ignored by Python. Adding comments to scripts is essential for scientists like ourselves to both help us remember how a script works and to make it easier to share with colleagues. It is best to get into the habit of adding comments as you write, especially if you’re not using a Jupyter notebook.

Use line breaks wisely
Line breaks, or blank lines, in your scripts can greatly improve readability, and help divide different sections of the script. Perhaps it is obvious, but Python will ignore blank lines in a script.

# Finnish Meterological Institute observation station name and location data

# Station name for the station in Kaivopuisto, Helsinki, Finland
stationName = 'Helsinki Kaivopuisto'

# Station latitude and longitude - Latitude is north, longitude is east
stationLat = 60.15
stationLong = 24.96

# Print station name and location to the screen
print("The", stationName, "station is located at", stationLat, "N,", stationLong, "E")
Use a docstring
A documentation string, or a docstring a block of text that describes what a spesific method or module does and how to use it. Surprise surprise, PEP 8 contains more guidance about documentation strings, and docstrings even have their own guide page: PEP 257.

A docstring is always the first statement in a module or a function. Docstrings are written using """triple double quotation marks""". We already discussed docstrings when defining functions earlier in lesson 4, and here is an example of using a multi-line docstring at the start of a script file.

When adding docstrings at the start of a script file, you can also include your name, and also licensing information.

"""Prints information about an FMI observation station to the screen.

Usage:
    ./stationinfo.py

Author:
    David Whipp - 26.9.2018
"""

# Finnish Meterological Institute observation station name and location data

# Station name for the station in Kaivopuisto, Helsinki, Finland
stationName = 'Helsinki Kaivopuisto'

# Station latitude and longitude - Latitude is north, longitude is east
stationLat = 60.15
stationLong = 24.96

# Print station name and location to the screen
print("The", stationName, "station is located at", stationLat, "N,", stationLong, "E")
In this example the script is simple, but many Python programs have optional values that can be used by the code when it is run, making the usage statement crucial.

Note that the closing quotes are on a line by themselves. It is also possible to write one-line docstrings, for example with very simple functions, in which case the starting and closing quotation marks are on the same line.

Advanced topics
Adding a license
Depending on what you aim to do with your script, you may want to include a formal software license in the docstring to state the conditions under which the code can be used or modified. There are many helpful web resources to teach you about software licenses and how to choose a license. In most cases my preference is the MIT License, which is simple and allows software use by anyone. An example is below.

"""Prints information about an FMI observation station to the screen.

Usage:
    ./stationinfo.py

License:
    MIT License

    Copyright (c) 2017 David Whipp

    Permission is hereby granted, free of charge, to any person obtaining a copy
    of this software and associated documentation files (the "Software"), to deal
    in the Software without restriction, including without limitation the rights
    to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
    copies of the Software, and to permit persons to whom the Software is
    furnished to do so, subject to the following conditions:

    The above copyright notice and this permission notice shall be included in all
    copies or substantial portions of the Software.

    THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
    IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
    FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
    AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
    LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
    OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
    SOFTWARE.
"""

# Finnish Meterological Institute observation station name and location data

# Station name for the station in Kaivopuisto, Helsinki, Finland
stationName = 'Helsinki Kaivopuisto'

# Station latitude and longitude - Latitude is north, longitude is east
stationLat = 60.15
stationLong = 24.96

# Print station name and location to the screen
print("The", stationName, "station is located at", stationLat, "N,", stationLong, "E")
In this case I have taken the license information directly from an online software license template. Software licensing is an important consideration when posting your software in online repositories such as GitHub. It is one way to protect your intellectual property from being used in ways you do not wish.

Starting with a shebang
Starting with a shebang is another thing to consider doing with your scripts. Why? Well, without going into too much detail, it makes it easier for users to run your script directly from a terminal, rather than needing to use a Jupyter notebook or open an Python console first. If this doesn’t make a great deal of sense, you can get a bit more information on Wikipedia.

Starting with a shebang means that the first line of your program starts with the characters #! followed by the location of a program that will run the Python software installed on the computer. An example is below.

#!/usr/bin/env python3
'''Prints information about an FMI observation station to the screen.

Usage:
    ./stationinfo.py

Author:
    David Whipp - 10.9.2017
'''

# Finnish Meterological Institute observation station name and location data

# Station name for the station in Kaivopuisto, Helsinki, Finland
stationName = 'Helsinki Kaivopuisto'

# Station latitude and longitude - Latitude is north, longitude is east
stationLat = 60.15
stationLong = 24.96

# Print station name and location to the screen
print("The", stationName, "station is located at", stationLat, "N,", stationLong, "E")
We’ll leave it at that for now, but if you have questions let us know.

Page summary
As we continue in the course we will be creating more advanced Python scripts that include more complex code logic and other features we’ve not yet learned. With these, we’ll also learn a few tips for incorporating them in our scripts. However, an expectation in this course is that you stick to the general template described above when writing your script files, which means including appropriate use of inline comments, blank lines, and a docstring.
