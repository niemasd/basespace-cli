# BaseSpace Sequence Hub Command Line Interface
The existing installation instructions for the [BaseSpace CLI](https://help.basespace.illumina.com/articles/descriptive/basespace-cli/#Installation) require the user to have superuser access on their machine, which is not often the case in shared compute servers. After extracting the `deb` file to try to get it running without root, I noticed that it's basically just a series of Python modules/scripts. I extracted it, changed the hardcoded full paths to local paths, and created a symbolic link in the root of this repository for convenience.

I am in no way affiliated with Illumina, the BaseSpace team, or the BaseSpace CLI code. I do not claim to have written the code myself. Further, the code I modified is publicly available [here](https://basespace.bintray.com/BaseSpaceCLI-DEB/), meaning this falls under fair use. Full rights and credits to Illumina and the BaseSpace team.

# INSTALLATION
Simply clone this repository and add it to your `PATH`. To run, simply run the `bs` symbolic link in the root of the repository, which links to `usr/local/bin/bs`.
