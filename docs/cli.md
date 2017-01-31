#### Find big files on the server

`find / -type f -size +1000M`

#### Kill all on port 80

`fuser -k -n tcp 80`


### Find text by RegEx recursive and save to file all muches 

`grep "'[[:digit:]]+[[:alpha:]][[:digit:]]*_.[^[:space:]\"]*'" ./ -R -o -E | cut -d: -f2 | sort -u > tooltips.txt`

### Clean all log files
 `find /var/log -type f -exec /bin/cp /dev/null {} \;`

### Generate ssh key

`ssh-keygen -t rsa`

#### Grab site:

- `wget -r -p -e robots=off http://www.example.com`
- `wget -r -k -l 7 -p -E -nc http://site.com/`



### CLI hotkeys

- Ctrl-A Move cursor to start of line
- Ctrl-E Move cursor to end of line
- Ctrl-B Move back one character
- Alt-B  Move back one word
- Ctrl-F Move forward one character
- Alt-F Move forward one word
- Ctrl-D Delete current character
- Ctrl-W Cut the last word
- Ctrl-K Cut everything after the cursor
- Alt-D Cut word after the cursor
- Alt-<- cut word before the cursor
- Ctrl-y Paste the last deleted command
- Ctrl-_ Undo
- Ctrl-u Cut everything before the cursor
- Ctrl-XX Toggle between first and current position
- Ctrl-L Clear the terminal
- Ctrl-C Cancel the command
- Ctrl-R Search command in history - type the search term
- Ctrl-J End the search at current history entry
- Ctrl-G Cancel the search and restore original line
- Ctrl-N Next command from the History
- Ctrl-P previous command from the History


