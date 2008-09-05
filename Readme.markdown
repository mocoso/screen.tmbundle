The Screen Textmate Bundle

## Installation

Run this:

    cd ~/Library/Application\ Support/TextMate/Bundles
    git clone git://github.com/mocoso/screen.tmbundle.git Screen.tmbundle
    
## Set up your screen configuration for a project

Create a .screenrc file *in your project directory* if you want to specify a particular configuration for your project.

For example for a Ruby on Rails project you might create a .screenrc file in your project directory like this

    # Have the server running in screen 1
    #
    # Stuff is used so that when you exit the stuff-ed program, you drop back
    # to the bash shell for that screen instead of immediately exiting that
    # screen. This is useful for "^c, up-arrow, enter" restarting of programs.
    screen -t server 1
    stuff "script/server\012"
    
    # Have autotest running in screen 2
    screen -t autotest 2
    stuff "autotest\012"
    
    # Have the console running in screen 3 
    screen -t console 3
    stuff "script/console\012"
    
    # Finally have a command line prompt at the project root in screen 4
    screen -t project_root 4


## Usage

Use this bundle's 'Start Session' command (ctrl-shift-s) to start (or reconnect to) your project's screen session.

If you have created a .screenrc file in your project directory then this will be used to initialize the new session.

