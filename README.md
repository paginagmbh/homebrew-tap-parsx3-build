Homebrew Tap for parsX 3 Build Tools
====================================

This is a custom [Homebrew](https://brew.sh/) Tap to maintain older version of software needed for the parsX 3 build process.

More on Taps: https://docs.brew.sh/How-to-Create-and-Maintain-a-Tap


Installation
------------

1. Make sure you have your GitHub credentials / SSH keys set up
1. Make sure you have Homebrew (for Mac) or Linuxbrew (for Windows Bash / WSL) installed
1. Install this tap with `brew tap paginagmbh/homebrew-tap-parsx3-build`
1. Install software from this tap with regular `brew` command like `brew install gradle@4.10.2`


Archive (deprecated) formulae in this Tap
--------------------------------------

This Tap is needed because Homebrew only supports up to 5 most recent versions of a package.
For a fast-moving software like Gradle, this is just a few month and too fast for us to adapt.
Therefore we need this tap to archive mission critical software on a specific version.

This can be done with the following command:

```
brew update
brew extract gradle paginagmbh/homebrew-tap-parsx3-build --version=4.10.2
```

Homebrew is searching its repository history for this specific version and extracts it to this repository.

Make sure to commit the archived formula after the extraction. The tap repo is a bit hidden, but Homebrew is showing the location after the extraction:

```
$ brew extract gradle paginagmbh/homebrew-tap-parsx3-build --version=4.10.2
==> Tapping paginagmbh/tap-parsx3-build
Cloning into '/usr/local/Homebrew/Library/Taps/paginagmbh/homebrew-tap-parsx3-build'...
warning: You appear to have cloned an empty repository.
Tapped (15 files, 20.5KB).
==> Searching repository history
==> Writing formula for gradle from revision 01e0511 to /usr/local/Homebrew/Library/Taps/paginagmbh/homebrew-tap-parsx3-build/Formula/gradle@4.10.2.rb
```

You can then open this repo with `fork` from the commandline:

```
fork /usr/local/Homebrew/Library/Taps/paginagmbh/homebrew-tap-parsx3-build/
```

Or commit the changes from the commandline:

```
cd /usr/local/Homebrew/Library/Taps/paginagmbh/homebrew-tap-parsx3-build/
git add -A
git commit -m "Added Formula XYZ@VERSION"
git push
```
