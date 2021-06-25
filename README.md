# TapeClassroom (WIP)

A simple script to auto fetch all active google classroom assignments into [Aeriform Tape](https://www.aeriform.io/docs/tape). 
The repo contains the main snippet of the js needed to make this work. At the moment a script is not available, but will be once
I get the program working.
---
## Instructions:
* Note that this is not a flushed out script, and cause problems with the application. Always to make a backup of everything that is being replaced in
the instructions. 
If you understand the risks, the continue on to the instructions
### Prerequisites:
1. Install node.js and npm (you will need them for all the stuff in general)
2. Install the `asar` package globally with `npm install -g asar` 
3. Install the googleclient api for node.js, and generate valid certificates
### Install:
1. `cd` into the apps directory, in case of MacOS you want to `cd /Applications/Tape.app/Contents/Resources`
2. Run `asar extract app.asar $(Wherever you want the source code files to be located`
3. `cd` into the folder you extracted the contents into, and there should be the source code for the program
4. Use an editor of choice to edit the app.js file, and paste the above app.js into the `function main() {`
5. At this point, you will need to change some variables, such as the google authorize function, just hardcoding the credentials in (Will attempt to find a fix)
6. Add:
```dict[newCollectionName] = newCollectionID``` to the `addNewCollection()` function right before the return statement
7. Save all the files and run `asar pack $(Whatever directory that holds the source code files) app.asar`
8. Replace the app.asar in the apps directory in step 1 with the new one generated
