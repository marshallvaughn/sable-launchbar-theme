A LaunchBar theme for the dark at heart.

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