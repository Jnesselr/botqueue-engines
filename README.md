botqueue-engines
================

This is a test to separate botqueue from the possible engines (like slicers) available.

How to use:

The master branch should remain empty of engines. All engines should go in a unique name under a unique branch off of master. Say you want to upload slic3r version 1.0.0. The current accepted name for this is "slic3r-1.0.0".  Then, depending on what operating system you want, you choose a name. Currently supported operating systems are linux, osx, win, and raspberrypi. Each branch is named based off of it's os and engine name. For example, if we were adding this for Raspberry Pi, we would name the branch raspberrypi-slic3r. If it already exists, then you are simply adding another version to the branch. Make sure the order of the commits is in the order of the versions, even if you have to force a change when editing it. This system is not designed to stay on a computer, but be re-downloaded every time. This is to make it cleaner for the users at the expense of the developers.

Now that we know what version and operating system we want, we simply have to create a branch, edit our data, and commit it. Here are the steps to do that for our example:

1. git checkout raspberrypi-slic3r
2. git rm -rf .
3. (Add all code here. This is what goes into the raspberry directory on the client. The same thing happens with the linux and osx.app directory. The branch contains what goes inside the folder)
4. Add the manifest.json file (See other branches for examples)
5. Add whatever default configuration there is
6. git add -A .
7. git commit -m 'Added slic3r 1.0.0 for raspberry pi'
8. git tag -a raspberrypi-slic3r-1.0.0 -m "Raspberry Pi Slic3r 1.0.0"
9. git push origin raspberrypi-slic3r
10. git push --tags

And you're done!
