botqueue-engines
================

This is a test to separate botqueue from the possible engines (like slicers) available.

How to use:

The master branch should remain empty of engines. All engines should go in a unique name under a unique branch. Say you want to upload slic3r version 1.0.0RC1. The current accepted name for this is "slic3r-1.0.0RC1".  Then, depending on what version you want, you choose a name. Currently supported versions are linux, osx, and raspberrypi. Now that we know what version we want, we simply have to create a branch, edit our data, and commit it. Here are the steps to do that for our example:

1. git checkout --orphan raspberrypi-slic3r-1.0.0RC1
2. git rm -rf .
3. (Add all code here. This is what goes into the raspberrypi directory on the client. The same thing happens with the linux and osx.app directory. The branch contains what goes inside the folder)
4. Add the manifest.json file (See other branches for examples)
5. Add whatever default configuration there is
6. git add -A .
7. git commit -m 'Adding slic3r 1.0.0RC1 for raspberry pi'
8. git push origin raspberrypi-slic3r-1.0.0RC1

And you're done!
