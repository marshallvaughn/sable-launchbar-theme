A LaunchBar theme for the dark at heart.

## Methodology
I based this on the "Default" LaunchBar theme, which is shipped with the app. That's marked as the "parent" in the [Properties.plist](Properties.plist) file, but it's very heavily modified, so that's just a jumping off point. I'm far from fluent with .plist files, so I just attacked this as simply as possible, alphabetizing the keys as best I could.

It's meant to be a friendly looking, clear, concise theme. Built for people like me, who want it to be visually appealing, but also just get out of the way and do the job. If it looks nice at first, and is never noticed again, that's mission accomplished.

Feel free to use the theme however you like! Modify, fork, or steal as you wish.

## Construction
The base directory for the repo is the package dir for the theme, so you should be able to clone this straight into `~/Library/Application Support/LaunchBar/Themes/Sable.lbtheme` and be ready to rock and roll. For convenience, you can use the following to do this from the command line: `git clone 'https://github.com/marshallvaughn/Sable-LaunchBar-Theme.git' ~/Library/Application Support/LaunchBar/Themes/Sable.lbtheme`.

The fonts used are all Apple system fonts. I like to keep it in the family, because it jives with the rest of the system UI, and because I find the whole San Francisco font family to be beautiful and generally agreeable. Specifically, the two major font families this uses are **SF Mono** and **SF Compact Rounded**.

Apple has kindly provided access to the **SF Compact Rounded** family (and others) [here](https://developer.apple.com/fonts/). The **SF Mono** family likely already exists on your machine (*the files are **in** the computer*)! Head on over to `/Applications/Utilities/Terminal.app/Contents/Resources/Fonts` and install using the standard double-click.

## Known Properties
I don't know of any place that lists out the possible properties for LaunchBar themes, so I've included the ones I found in the [Keys.md](Keys.md) file. I've included the shell commands I used to query them below, both of which are run from within the app package, at `/Applications/LaunchBar.app/Resources/Themes`.

```bash
# Query keys for a specific term 
term='ENTER-SEARCH-TERM-HERE'; ag "[A-z]*${term}[A-z]*" --only-matching --nonumbers --nofilename | sort -u
```

```bash
# Query the entire list of keys
ag "<key>[A-z]*" --only-matching --nonumbers --nofilename | sort -u | sed 's/<key>//g' | copy
```