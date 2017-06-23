# BaseSpace Sequence Hub Command Line Interface
The existing installation instructions for the [BaseSpace CLI](https://help.basespace.illumina.com/articles/descriptive/basespace-cli/#Installation) require the user to have superuser access on their machine, which is not often the case in shared compute servers. After extracting the `deb` file to try to get it running without root, I noticed that it's basically just a series of Python modules/scripts. I extracted it, changed the hardcoded full paths to local paths, and created a symbolic link in the root of this repository for convenience.

I am in no way affiliated with Illumina, the BaseSpace team, or the BaseSpace CLI code. I do not claim to have written the code myself. Further, the code I modified is publicly available [here](https://basespace.bintray.com/BaseSpaceCLI-DEB/), meaning this falls under fair use. Full rights and credits to Illumina and the BaseSpace team.

Currently, this repository contains `basespace-cli_0.8.12-590_amd64` and `bscp_0.5.3-327_i386` (I chose the 32-bit version of `bscp` for compatibility).

# INSTALLATION
Simply clone this repository and add it to your `PATH`. To run, simply run the `bs` symbolic link in the root of the repository, which links to `usr/local/bin/bs`.

I was able to run BaseSpace CLI out-of-the-box after cloning on an Ubuntu 16.04 and a CentOS 5.7 version, so it seems to work fine cross-platform. Mac OS X is missing the `realpath` command, which was needed for portability, but you can get it with Homebrew (`brew install coreutils`) or you can get it from [this repository](https://github.com/harto/realpath-osx) if Homebrew is not an option on your Mac. After installing `coreutils` via Homebrew, it was able to run out-of-the-box on my Mac OS X Sierra machine as well.
